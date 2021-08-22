---
title: Informationen zu Objektmodellversionen
description: Informationen zu Objektmodellversionen
ms.assetid: 20bb1681-9079-4f8c-bb5e-5c98e3bdc76a
keywords:
- Windows Media Player,Versionen
- Windows Media Player-Objektmodell, Versionen
- Objektmodell, Versionen
- Windows Media Player ActiveX-Steuerelement, Versionen für das Objektmodell
- ActiveX-Steuerelement, Versionen für das Objektmodell
- Windows Media Player Mobiles ActiveX-Steuerelement,Versionen für Objektmodell
- Windows Media Player Mobil, Versionen für Objektmodell
- Versionen von Windows Media Player,Objektmodell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce90455d93d71f6fde62b97d3b4d38e34963307e60b831c8110a914cc535cffd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119510060"
---
# <a name="about-the-object-model-versions"></a>Informationen zu Objektmodellversionen

Windows Media Player 7.0 wurde ein neues Objektmodell eingeführt. Dieses Objektmodell wurde mit Windows Media Player 7.1, Windows Media Player für Windows XP, Windows Media Player 9 Serie, Windows Media Player 10, Windows Media Player 11 und Windows Media Player 12 erweitert. Jedes Thema in der Objektmodellreferenz enthält einen Abschnitt Anforderungen, in dem die Mindestanforderungen für die einzelnen Eigenschaften, Methoden oder Ereignisse beschrieben werden. In der folgenden Liste sind die neuen Objekte, Methoden, Eigenschaften und Ereignisse aufgeführt, die seit Version 7.0 für jede Version hinzugefügt wurden. Diese Listen enthalten auch neue C++-Schnittstellen, -Methoden und -Ereignisse.

Wenn eine neue oder aktualisierte Schnittstelle auch als Objekt verfügbar gemacht wird, wird nur das -Objekt aufgeführt. Informationen zum Suchen der Schnittstelle finden Sie in der [Objektmodellreferenz für C++.](object-model-reference-for-c.md) In der Regel müssen Sie dem Objektnamen einfach das IWMP-Präfix hinzufügen. Wenn eine neue Schnittstelle eine vorhandene erweitert, müssen Sie möglicherweise nach der neuesten Versionsnummer suchen. Beispielsweise wurden Windows Media Player 9-Serie neue Eigenschaften und Methoden eingeführt, die über das [**Einstellungen-Objekt**](settings-object.md) verfügbar sind. In C++ sind diese über die [**IWMPSettings2-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings2) verfügbar, die [**IWMPSettings**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings)erweitert.

## <a name="added-for-windows-media-player-71"></a>Für Windows Media Player 7.1 hinzugefügt

-   [**Player.stretchToFit-Eigenschaft**](player-stretchtofit.md)

## <a name="added-for-windows-media-player-for-windows-xp"></a>Für Windows Media Player für Windows XP hinzugefügt

-   [**Controls.step-Methode**](controls-step.md)
-   [**DVD-Objekt**](dvd-object.md)
-   [**Media.error-Eigenschaft**](media-error.md)
-   [**Player.DomainChange-Ereignis**](player-player-domainchange.md)
-   [**Player.MediaError-Ereignis**](player-player-mediaerror.md)
-   [**Player.OpenPlaylistSwitch-Ereignis**](player-player-openplaylistswitch.md)
-   [**Player.windowlessVideo-Eigenschaft**](player-windowlessvideo.md)

## <a name="added-for-windows-media-player-9-series"></a>Für Windows Media Player 9-Serie hinzugefügt

-   [**ClosedCaption.getSAMILangID-Methode**](closedcaption-getsamilangid.md)
-   [**ClosedCaption.getSAMILangName-Methode**](closedcaption-getsamilangname.md)
-   [**ClosedCaption.getSAMIStyleName-Methode**](closedcaption-getsamistylename.md)
-   [**ClosedCaption.SAMILangCount-Eigenschaft**](closedcaption-samilangcount.md)
-   [**ClosedCaption.SAMIStyleCount-Eigenschaft**](closedcaption-samistylecount.md)
-   [**Controls.audioLanguageCount-Eigenschaft**](controls-audiolanguagecount.md)
-   [**Controls.currentAudioLanguage-Eigenschaft**](controls-currentaudiolanguage.md)
-   [**Controls.currentAudioLanguageIndex-Eigenschaft**](controls-currentaudiolanguageindex.md)
-   [**Controls.currentPositionTimecode-Eigenschaft**](controls-currentpositiontimecode.md)
-   [**Controls.getAudioLanguageDescription-Methode**](controls-getaudiolanguagedescription.md)
-   [**Controls.getAudioLanguageID-Methode**](controls-getaudiolanguageid.md)
-   [**Controls.getLanguageName-Methode**](controls-getlanguagename.md)
-   [**ErrorItem.condition-Eigenschaft**](erroritem-condition.md)
-   [**External.appColorLight-Eigenschaft**](external-appcolorlight.md)
-   [**External.OnColorChange-Ereignis**](external-oncolorchange-event.md)
-   [**External.version-Eigenschaft**](external-version.md)
-   [**IWMPEvents::P layerDockedStateChange-Ereignis**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-playerdockedstatechange)
-   [**IWMPEvents::P layerReconnect-Ereignis**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-playerreconnect)
-   [**IWMPEvents::SwitchedToControl-Ereignis**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-switchedtocontrol)
-   [**IWMPEvents::SwitchedToPlayerApplication-Ereignis**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-switchedtoplayerapplication)
-   [**IWMPPlayerServices-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices)
-   [**IWMPRemoteMediaServices-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices)
-   [**IWMPSkinManager-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpskinmanager)
-   [**Media.getAttributeCountByType-Methode**](media-getattributecountbytype.md)
-   [**Media.getItemInfoByType-Methode**](media-getiteminfobytype.md)
-   [**MetadataPicture-Objekt**](metadatapicture-object.md)
-   [**MetadataText-Objekt**](metadatatext-object.md)
-   [**Player.AudioLanguageChange-Ereignis**](player-player-audiolanguagechange.md)
-   [**Player.isRemote-Eigenschaft**](player-isremote.md)
-   [**Player.MediaCollectionAttributeStringChanged-Ereignis**](player-player-mediacollectionattributestringchanged.md)
-   [**Player.newMedia-Methode**](player-newmedia.md)
-   [**Player.newPlaylist-Methode**](player-newplaylist.md)
-   [**Player.openPlayer-Methode**](player-openplayer.md)
-   [**Player.playerApplication-Eigenschaft**](player-playerapplication.md)
-   [**Player.StatusChange-Ereignis**](player-player-statuschange.md)
-   [**PlayerApplication-Objekt**](playerapplication-object.md)
-   [**Einstellungen.defaultAudioLanguage-Eigenschaft**](settings-defaultaudiolanguage.md)
-   [**Einstellungen.mediaAccessRights-Eigenschaft**](settings-mediaaccessrights.md)
-   [**Einstellungen.requestMediaAccessRights-Methode**](settings-requestmediaaccessrights.md)

## <a name="added-for-windows-media-player-10"></a>Für Windows Media Player 10 hinzugefügt

-   [**IWMPGraphCreation-Schnittstelle**](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpgraphcreation)
-   [**IWMPPlayerServices2-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices2)
-   [**IWMPSyncDevice-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
-   [**IWMPSyncServices-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncservices)
-   [**WMPDeviceStatus-Enumeration**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus)
-   [**WMPSyncState-Enumeration**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpsyncstate)

## <a name="added-for-windows-media-player-11"></a>Für Windows Media Player 11 hinzugefügt

-   [**IWMPC über die Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn)
-   [**IWMPCorpora Überl-Schnittstelle (VB und C#)**](iwmpcdromburn--vb-and-c.md)
-   [**IWMPCpinRip-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip)
-   [**IWMPCorporaRip-Schnittstelle (VB und C#)**](iwmpcdromrip--vb-and-c.md)
-   [**IWMPEvents3-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents3)
-   [**IWMPFolderMonitorServices-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)
-   [**IWMPLibrary-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary)
-   [**IWMPLibrary-Schnittstelle (VB und C#)**](iwmplibrary--vb-and-c.md)
-   [**IWMPLibraryServices-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibraryservices)
-   [**IWMPLibraryServices-Schnittstelle (VB und C#)**](iwmplibraryservices--vb-and-c.md)
-   [**IWMPLibrarySharingServices-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrarysharingservices)
-   [**IWMPMediaCollection2-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection2)
-   [**IWMPMediaCollection2-Schnittstelle (VB und C#)**](iwmpmediacollection2--vb-and-c.md)
-   [**IWMPQuery-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpquery)
-   [**IWMPQuery-Schnittstelle (VB und C#)**](iwmpquery--vb-and-c.md)
-   [**IWMPRenderConfig-Schnittstelle**](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmprenderconfig)
-   [**IWMPStringCollection2-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection2)
-   [**IWMPStringCollection2-Schnittstelle (VB und C#)**](iwmpstringcollection2--vb-and-c.md)
-   [**IWMPSyncDevice2-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice2)
-   [**IWMPVideoRenderConfig-Schnittstelle**](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpvideorenderconfig)
-   [**Abfrageobjekt**](query-object.md)
-   [**WMPHäufingFormat-Enumeration**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnformat)
-   [**WMPState-Enumeration**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate)
-   [**WMPLibraryType-Enumeration**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype)
-   [**WMPRipState-Enumeration**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate)

## <a name="added-for-windows-media-player-12"></a>Für Windows Media Player 12 hinzugefügt

-   [**IWMPAudioRenderConfig-Schnittstelle**](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpaudiorenderconfig)
-   [**IWMPEvents4-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents4)
-   [**IWMPLibrary2-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary2)
-   [**IWMPSyncDevice3-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice3)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zum Playerobjektmodell**](about-the-player-object-model.md)
</dt> <dt>

[**Objektmodellreferenz für Skripterstellung**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




