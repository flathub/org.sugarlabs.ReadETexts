# ReadETexts Flatpak

ReadETexts is an activity for the Sugar desktop.
Read ETexts lets you read all the free e-texts from Project Gutenberg on your XO, or use Text to Speech to have them read to you. The built in offline catalog search lets you browse through and download over 30,000 great titles!

To know more refer: https://github.com/sugarlabs/readetexts

## How To Build

```
git clone https://github.com/flathub/org.sugarlabs.ReadETexts.git
cd org.sugarlabs.ReadETexts
flatpak -y --user install flathub org.gnome.{Platform,Sdk}//46
flatpak -y --user install org.sugarlabs.BaseApp//24.04
flatpak-builder --user --force-clean --install build org.sugarlabs.ReadETexts.json
```

## Check For Updates

Install the flatpak external data checker
```
flatpak --user install org.flathub.flatpak-external-data-checker
```

Now to update every single module to the latest stable version use
```
cd org.sugarlabs.ReadETexts
flatpak run --filesystem=$PWD org.flathub.flatpak-external-data-checker org.sugarlabs.ReadETexts.json
```