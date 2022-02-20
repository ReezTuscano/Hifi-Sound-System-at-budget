# Hifi-Sound-System-at-budget
Build a complete 5.1 surround sound system for home audio having studio grade quality

Motivation:
Love for HIFI music experience at low cost.
Breaking the monopoly of pre existing HIFI audiophiles system.

// ==UserScript==
// @name        github add youtube
// @namespace   damien@pobel.fr
// @include     https://github.com/*
// @version     1
// @grant       none
// ==/UserScript==
//
(function () {

    function addButton (group) {
        var button = group.querySelector('.toolbar-item:last-of-type').cloneNode(true);

        button.setAttribute('aria-label', "Add a Youtube video");
        button.setAttribute('data-ga-click', "");
        // https://simpleicons.org/icons/youtube.svg
        // + class="octicon"
        // + width="20"
        // + height="16"
        // -viewBox
        button.innerHTML = '<svg class="octicon" width="20" height="16" xmlns="http://www.w3.org/2000/svg" fill-rule="evenodd" clip-rule="evenodd" stroke-linejoin="round" stroke-miterlimit="1.414"><path d="M0 7.345c0-1.294.16-2.59.16-2.59s.156-1.1.636-1.587c.608-.637 1.408-.617 1.764-.684C3.84 2.36 8 2.324 8 2.324s3.362.004 5.6.166c.314.038.996.04 1.604.678.48.486.636 1.588.636 1.588S16 6.05 16 7.346v1.258c0 1.296-.16 2.59-.16 2.59s-.156 1.102-.636 1.588c-.608.638-1.29.64-1.604.678-2.238.162-5.6.166-5.6.166s-4.16-.037-5.44-.16c-.356-.067-1.156-.047-1.764-.684-.48-.487-.636-1.587-.636-1.587S0 9.9 0 8.605v-1.26zm6.348 2.73V5.58l4.323 2.255-4.32 2.24h-.002z"/></svg>';
        group.appendChild(button);

        return button;
    }

    function addMarkdown (textarea) {
        var vid,
            value = textarea.value;

        if ( textarea.selectionStart !== textarea.selectionEnd ) {
            vid = textarea.value.substring(textarea.selectionStart, textarea.selectionEnd).trim();
        } else {
            vid = window.prompt('Youtube video URL?');
        }
        vid = vid.replace(/.*v=([a-z0-9_-]+).*/gi, '$1');
        textarea.value = `${value.substring(0, textarea.selectionStart)}
[![](https://img.youtube.com/vi/${vid}/0.jpg)](http://www.youtube.com/watch?v=${vid} "Click to play on Youtube.com")
${value.substring(textarea.selectionEnd)}`;
    }

    function enhanceToolbar(commentForm) {
        var textarea = commentForm.querySelector('.comment-form-textarea'),
            toolbarGroup = commentForm.querySelector('.toolbar-group:last-of-type'),
            button;

        if ( !textarea || !toolbarGroup ) {
            return;
        }

        button = addButton(toolbarGroup);
        button.onclick = function (e) {
            e.stopPropagation();
            addMarkdown(textarea);
        };
    }

    Array.prototype.forEach.call(document.querySelectorAll('.previewable-comment-form'), enhanceToolbar);
})();

//
https://user-images.githubusercontent.com/100014146/154802864-e8267968-62f6-4594-85e7-2ec494578576.mp4 


![Screen Shot 061](https://user-images.githubusercontent.com/100014146/154802769-05f5d539-df0d-4cf3-9e48-a5ca6c1e88c9.PNG)



![Screen Shot 062](https://user-images.githubusercontent.com/100014146/154802774-b45fa031-3ee2-4cd5-a172-e2620c30344a.PNG)



https://user-images.githubusercontent.com/100014146/154803498-02eccdb6-1806-4ace-a5cd-e9d42913ac58.mp4

Why does our product costs less?
● The products produced by the companies cost way more
than the cost of discrete components is because of R&D.
● These Giants invest loads of money in R&D and come up
with new and noticeable improvements .So somehow they
have to manage the cost to run the company.
● That’s why Iphone(1.5Lac) costs way more than
Xiaomi(12k).
● The cost increases by 10 folds when you decrease the THD
by 10.thus out product cost less as less efforts are taken to
reduce the THD to atomic level.


![WhatsApp Image 2022-02-19 at 1 20 40 PM](https://user-images.githubusercontent.com/100014146/154802311-63925973-05fa-412f-b3fe-deca313d6d4c.jpeg)



![WhatsApp Image 2022-02-19 at 1 21 26 PM](https://user-images.githubusercontent.com/100014146/154802314-c3e51065-aedd-4b73-a6ac-19a0ce2b2b29.jpeg)


Problem Statement:
• To create a audiophile music system at cost effective solution.
• It should include wired as well as wireless communication
interfaces.
• Amplifier for 5.1 dolby surround sound for cost as low as 3500.
• Active subwoofer to cover the bass frequencies
• To produce quality off about 80-90% of what the big audio
companies offer to their user ,but still maintain the budget and
pocket friendly features


![WhatsApp Image 2022-02-19 at 1 21 27 PM (1)](https://user-images.githubusercontent.com/100014146/154802316-ace153f9-6597-4dc6-8b51-6e5814f784e7.jpeg)
![WhatsApp Image 2022-02-19 at 1 21 27 PM](https://user-images.githubusercontent.com/100014146/154802318-37d451ea-3992-4b16-9668-2c9bb265860f.jpeg)

Survey of Existing System:
Audiophiles have worked diligently to alert the rest of the world to products
with superior sound quality, and to warn us away from expensive gimmicks
that have middling features at best.
Unfortunately, the downside of most high quality audio equipment is the
sticker price. But with some soldering skills and a bit of hardware.
Existing systems like sony ,jbl ,etc do offer great sounding systems but the
cost that they sell them is not affordable to the customer… so what we did
is ,we created a audio music system which cost way less but matches the
quality of the top audio companies upto 90%


![WhatsApp Image 2022-02-19 at 1 21 28 PM (1)](https://user-images.githubusercontent.com/100014146/154802319-ef39babf-664b-4e56-864e-4a8842b0d5df.jpeg)


![WhatsApp Image 2022-02-19 at 1 21 28 PM](https://user-images.githubusercontent.com/100014146/154802321-f393c57e-1aa9-4254-ae40-947f460d96a1.jpeg)



Proposed System
• Everyone wants a better experience while listening to music, so
people tend to buy music systems which are extremely cheap or
expensive . Buying cheap system just gets things done but does not
provide important features that are the sole of good music system.
And buying an expensive set just doesn’t justify the cost to
experience ratio.
• So what we try to build is a music system that provides features
with cost as low as possible without degradation of sound quality
• HIFI 5.1 music system have 6 channels for front left and right
speakers, rear left right speakers ,and one channel for subwoofer
and other for center.
• Left and right speakers Lm3886 60watt max HIFI Amplifier each
• Active Subwoofer c5200 and a1943 4 pair 400watt amplifier
• Surround left and right pam8610 class d 15+15 watts (for now
but later, we will use 100 watt each using ttc5200 and 1943)
• Bass blaster circuit for front left and right and subwoofer


![IMG_20210321_073022767](https://user-images.githubusercontent.com/100014146/154802328-42d5ecfd-cf6b-48bc-a197-5de56f10fe3c.jpg)

Preamplifier Features –Modes of connectivity
• Aux ,Bluetooth , usb to computer as sound card , coaxial and
optical communication for dolby/dts decoding **USB pendrive,
sdcard and fm.
Amplifier Features
• Class Ab configuration thus has sound quality of class A with high
output configuration of class B.
• Dc offset at output is less than 50mv.
• Max wattage is 68watts each for speakers and 400watt or more
as per need. But currently Rms wattage for subwoofer is 45watts
due to transformer power limitation
• 20hz-192khz for dolby
• 20hz – 48khz for Bluetooth aux.
• Bass blaster circuit for front and subwoofers.
• Lowpass and subsonic filters for subwoofer.



![IMG_20210321_073028811](https://user-images.githubusercontent.com/100014146/154802332-c48f13da-ed74-49b0-a0be-7778297ef5f8.jpg)

Some features of the Amplifier
• Designed 1
st order low and high pass filter for the analog input
from the phone.
• Zoble network and Thiele’s network.
(They are used to prevent oscillations caused by inductive and capacitive
loads. they also prevents radio frequencies picked up by the speaker
wires from getting back into the amplifier’s inverting input via the
feedback loop.)
• Low power supply ripple by using multiple capacitors both high
and low values.(planning to use capacitance multiplier for reduce
the ripple even further)


![IMG_20210321_073033873](https://user-images.githubusercontent.com/100014146/154802339-b5516fa6-0a38-4b03-b32f-911a02110abb.jpg)



Active subwoofer features
About the amplifier
• 400 watt rms class ab amplifier using ttc5200 and tta1943
transistors
• bass blaster circuitry
• 600 watt transformer (30 – 0 – 30 10 amp)
About the box
• Tunning frequency 26hz
• Total Box volume 4300 cubic inches
• Ported enclosure for more spl


![IMG_20210321_073036240](https://user-images.githubusercontent.com/100014146/154802345-f5745331-3141-44b3-8026-c5d758690df4.jpg)


Details of Hardware & Software
1.Amplification stage of input analog signal
• Current we have used AUX input for analog input signal for
amplifier which is generated by phone. Thus avoiding the other
two sections for now….
• Here we have used an LM3886 which is a HIFI Audiophile class IC
which can produce maximum output of 50watts which is enough
to power an 60watt 8ohm speaker.
•



![IMG_20210321_073055515](https://user-images.githubusercontent.com/100014146/154802352-5c292660-3e94-448e-b9d5-82b83b6864f8.jpg)


Why Lm3886 IC ?
• LM3886 is one of the most highly regarded audio chip amplifiers.
• We have chosen it because
• Very low distortion(0.001% THD + N),
• Minimal external components (mostly stability Components),
• and low cost ( ₹180).


![IMG_20210321_073019605](https://user-images.githubusercontent.com/100014146/154802323-4242f5de-e96b-43af-bffc-980b14d1d764.jpg)

Experiment and Results:
The sound quality of the Audio system is Awesome comparing to the
price segment of the analog circuit(lm3886)….
Lm3886 works as expected to fulfill the first step of audio signal
Amplification satisfactorily.
Conclusion:
At the end of this project, An5.1 dolby audiophile music system will
be ready for use with, Bluetooth ,USB and aux Input.
Future Scope of this project
• Open source DSP like Viper4Android can be used to take the audio
signature Next Level.
• Number of connection interfaces can be increased for better user
experience

![Screen Shot 080](https://user-images.githubusercontent.com/100014146/154803800-31659bba-cf6e-46c4-ad54-e341d460f3c7.PNG)
![Screen Shot 081](https://user-images.githubusercontent.com/100014146/154803801-ed9cec64-2449-417e-b73a-533b0ddf923b.PNG)
![Screen Shot 082](https://user-images.githubusercontent.com/100014146/154803803-a5484be5-6f2a-42af-a5bb-d631cc152d68.PNG)




![Screen Shot 061](https://user-images.githubusercontent.com/100014146/154802769-05f5d539-df0d-4cf3-9e48-a5ca6c1e88c9.PNG)
![Screen Shot 062](https://user-images.githubusercontent.com/100014146/154802774-b45fa031-3ee2-4cd5-a172-e2620c30344a.PNG)
![Screen Shot 063](https://user-images.githubusercontent.com/100014146/154802778-d4b2744d-6a39-4d36-9635-5354fdd29b05.PNG)
![Screen Shot 064](https://user-images.githubusercontent.com/100014146/154802781-39b632cf-bf13-4c24-bdd0-c941ae93f9a7.PNG)
![Screen Shot 065](https://user-images.githubusercontent.com/100014146/154802783-dfabcc67-5c76-4c51-9562-fadd0ac51cdd.PNG)
![Screen Shot 066](https://user-images.githubusercontent.com/100014146/154802787-1b663b93-bfb6-4ee5-afc9-243e002ac614.PNG)
![Screen Shot 067](https://user-images.githubusercontent.com/100014146/154802791-945e15f8-0781-46a9-bc37-34439c0bba4d.PNG)
![Screen Shot 068](https://user-images.githubusercontent.com/100014146/154802793-4631e96b-0865-443e-b62c-d5101097d9c7.PNG)
![Screen Shot 069](https://user-images.githubusercontent.com/100014146/154802796-6c716fd1-872f-4d02-84c5-3b670ee86d91.PNG)
![Screen Shot 070](https://user-images.githubusercontent.com/100014146/154802799-ae282ab1-3519-4d47-9cda-a109b927b0a9.PNG)
![Screen Shot 071](https://user-images.githubusercontent.com/100014146/154802802-b20e7cb5-83cc-41ac-a20f-8a1a3c3a6425.PNG)
![Screen Shot 072](https://user-images.githubusercontent.com/100014146/154802810-65e9096a-0aa7-49a9-a510-6f6692ce635b.PNG)
![Screen Shot 073](https://user-images.githubusercontent.com/100014146/154802811-bbea5378-81c6-48fd-8cfc-535fad255ff3.PNG)
![Screen Shot 074](https://user-images.githubusercontent.com/100014146/154802812-e513a9d4-c220-4ff9-9227-7ecff787655d.PNG)
![Screen Shot 075](https://user-images.githubusercontent.com/100014146/154802814-c93b774e-8e21-4902-8056-301585e34928.PNG)
![Screen Shot 076](https://user-images.githubusercontent.com/100014146/154802816-17fc7f71-fb23-415d-a622-2fe43e832751.PNG)
![Screen Shot 077](https://user-images.githubusercontent.com/100014146/154802818-e3e67bd1-3773-49cd-87f7-f4191c603628.PNG)
![Screen Shot 078](https://user-images.githubusercontent.com/100014146/154802822-03950199-e192-4fef-8d00-a0dd3edd4546.PNG)
![Screen Shot](https://user-images.githubusercontent.com/100014146/154802825-4fb29b0a-a8fd-445c-8d96-5d777dc2b6dd.JPG)



Refrences:
References:
• https://www.circuitbasics.com/wp-content/uploads/2016/10/LM3
886-Datasheet.pdf
• https://en.wikipedia.org/wiki/Zobel_network
• https://neurochrome.com/pages/stability
• Youtube and lots of audio blogs and podcasts
