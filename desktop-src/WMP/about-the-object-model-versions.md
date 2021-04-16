---
title: Informationen zu Objektmodellversionen
description: Informationen zu Objektmodellversionen
ms.assetid: 20bb1681-9079-4f8c-bb5e-5c98e3bdc76a
keywords:
- Windows Media Player, Versionen
- Windows Media Player-Objektmodell, Versionen
- Objektmodell, Versionen
- Windows Media Player ActiveX-Steuerelement, Versionen für das Objektmodell
- ActiveX-Steuerelement, Versionen für das Objektmodell
- Windows Media Player Mobile ActiveX-Steuerelement, Versionen für das Objektmodell
- Windows Media Player Mobile, Versionen für das Objektmodell
- Versionen von Windows Media Player, Objektmodell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59886f5750b6fc42112f73d6bb6e05e8d013ffdc
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/21/2020
ms.locfileid: "104390045"
---
# <a name="about-the-object-model-versions"></a>Informationen zu Objektmodellversionen

In Windows Media Player 7,0 wurde ein neues Objektmodell eingeführt. Dieses Objektmodell wurde mit Windows Media Player 7,1, Windows Media Player für Windows XP, Windows Media Player 9-Serie, Windows Media Player 10, Windows Media Player 11 und Windows Media Player 12 erweitert. Jedes Thema in der Objektmodell Referenz enthält einen Anforderungs Abschnitt, der die Mindestanforderungen für die jeweilige Eigenschaft, Methode oder das jeweilige Ereignis beschreibt. In der folgenden Liste werden die neuen Objekte, Methoden, Eigenschaften und Ereignisse erläutert, die seit Version 7,0 für jede Version hinzugefügt wurden. Diese Listen enthalten auch neue C++-Schnittstellen, Methoden und Ereignisse.

Wenn eine neue oder aktualisierte Schnittstelle auch als Objekt verfügbar gemacht wird, wird nur das Objekt aufgelistet. Informationen zum Auffinden der-Schnittstelle finden Sie in der [Objektmodell Referenz für C++](object-model-reference-for-c.md). Normalerweise müssen Sie dem Objektnamen lediglich das iwmp-Präfix hinzufügen. Wenn eine neue Schnittstelle eine vorhandene erweitert, müssen Sie möglicherweise nach der aktuellen Versionsnummer suchen. Beispielsweise wurden in der Windows Media Player 9-Reihe neue Eigenschaften und Methoden eingeführt, die im [**Settings**](settings-object.md) -Objekt verfügbar sind. In C++ sind diese über die [**IWMPSettings2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings2) -Schnittstelle verfügbar, die [**iwmpsettings**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings)erweitert.

## <a name="added-for-windows-media-player-71"></a>Für Windows Media Player 7,1 hinzugefügt

-   [**Player. stretchdefit (Eigenschaft)**](player-stretchtofit.md)

## <a name="added-for-windows-media-player-for-windows-xp"></a>Für Windows-Media Player für Windows XP hinzugefügt

-   [**Controls. Step-Methode**](controls-step.md)
-   [**DVD-Objekt**](dvd-object.md)
-   [**Media. Error (Eigenschaft)**](media-error.md)
-   [**Player. domainchange-Ereignis**](player-player-domainchange.md)
-   [**Player. MediaError-Ereignis**](player-player-mediaerror.md)
-   [**Player. openplaylistswitch-Ereignis**](player-player-openplaylistswitch.md)
-   [**Player. windowlessvideo (Eigenschaft)**](player-windowlessvideo.md)

## <a name="added-for-windows-media-player-9-series"></a>Für Windows Media Player 9-Reihe hinzugefügt

-   [**Closedcaption. getsamilangid-Methode**](closedcaption-getsamilangid.md)
-   [**Closedcaption. getsamilangname-Methode**](closedcaption-getsamilangname.md)
-   [**Closedcaption. getsamistylename-Methode**](closedcaption-getsamistylename.md)
-   [**Closedcaption. samilangcount (Eigenschaft)**](closedcaption-samilangcount.md)
-   [**Closedcaption. samistylecount (Eigenschaft)**](closedcaption-samistylecount.md)
-   [**Controls. audiolanguagecount (Eigenschaft)**](controls-audiolanguagecount.md)
-   [**Controls. currentaudiolanguage (Eigenschaft)**](controls-currentaudiolanguage.md)
-   [**Controls. currentaudiolanguageindex (Eigenschaft)**](controls-currentaudiolanguageindex.md)
-   [**Controls. currentPositionTimecode-Eigenschaft**](controls-currentpositiontimecode.md)
-   [**Controls. getaudiolanguagedescription-Methode**](controls-getaudiolanguagedescription.md)
-   [**Controls. getaudiolanguageid-Methode**](controls-getaudiolanguageid.md)
-   [**Controls. getlanguagename-Methode**](controls-getlanguagename.md)
-   [**ErrorItem. Condition (Eigenschaft)**](erroritem-condition.md)
-   [**Extern. appcolorlight (Eigenschaft)**](external-appcolorlight.md)
-   [**Externes. oncolorchange-Ereignis**](external-oncolorchange-event.md)
-   [**Extern. Version (Eigenschaft)**](external-version.md)
-   [**Iwmpevents::P layerdockedstatechange-Ereignis**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-playerdockedstatechange)
-   [**Iwmpevents::P layerreconnect-Ereignis**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-playerreconnect)
-   [**Iwmpevents:: switchedto Control-Ereignis**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-switchedtocontrol)
-   [**Iwmpevents:: switchedtoplayerapplication-Ereignis**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-switchedtoplayerapplication)
-   [**Iwmpplayerservices-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices)
-   [**Iwmpremotemediaservices-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices)
-   [**Iwmpskinmanager-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpskinmanager)
-   [**Media. getattributezähltbytype-Methode**](media-getattributecountbytype.md)
-   [**Media. getItemInfoByType-Methode**](media-getiteminfobytype.md)
-   [**MetadataPicture-Objekt**](metadatapicture-object.md)
-   [**MetadataText-Objekt**](metadatatext-object.md)
-   [**Player. audiolanguagechange-Ereignis**](player-player-audiolanguagechange.md)
-   [**Player. IsRemote-Eigenschaft**](player-isremote.md)
-   [**Player. mediacollectionattributestringchanged-Ereignis**](player-player-mediacollectionattributestringchanged.md)
-   [**Player. newmedia-Methode**](player-newmedia.md)
-   [**Player. newwiedergabe-Methode**](player-newplaylist.md)
-   [**Player. openplayer-Methode**](player-openplayer.md)
-   [**Player. playerapplication (Eigenschaft)**](player-playerapplication.md)
-   [**Player. statusChange-Ereignis**](player-player-statuschange.md)
-   [**Playerapplication-Objekt**](playerapplication-object.md)
-   [**Settings. defaultaudiolanguage (Eigenschaft)**](settings-defaultaudiolanguage.md)
-   [**Settings. mediaaccessrights (Eigenschaft)**](settings-mediaaccessrights.md)
-   [**Settings. requestmediaaccessrights-Methode**](settings-requestmediaaccessrights.md)

## <a name="added-for-windows-media-player-10"></a>Für Windows Media Player 10 hinzugefügt

-   [**Iwmpgraphcreation-Schnittstelle**](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpgraphcreation)
-   [**IWMPPlayerServices2-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices2)
-   [**Iwmpsyncdevice-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
-   [**Iwmpsyncservices-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncservices)
-   [**Wmpdevicestatus-Enumeration**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus)
-   [**Wmpsyncstate-Enumeration**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpsyncstate)

## <a name="added-for-windows-media-player-11"></a>Für Windows Media Player 11 hinzugefügt

-   [**Iwmpcdromburn-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn)
-   [**Iwmpcdromburn-Schnittstelle (VB und c#)**](iwmpcdromburn--vb-and-c.md)
-   [**Iwmpcdromrip-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip)
-   [**Iwmpcdromrip-Schnittstelle (VB und c#)**](iwmpcdromrip--vb-and-c.md)
-   [**IWMPEvents3-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents3)
-   [**Iwmpfoldermonitorservices-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)
-   [**Iwmplibrary-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary)
-   [**Iwmplibrary-Schnittstelle (VB und c#)**](iwmplibrary--vb-and-c.md)
-   [**Iwmplibraryservices-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibraryservices)
-   [**Iwmplibraryservices-Schnittstelle (VB und c#)**](iwmplibraryservices--vb-and-c.md)
-   [**Iwmplibrarysharingservices-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrarysharingservices)
-   [**IWMPMediaCollection2-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection2)
-   [**IWMPMediaCollection2-Schnittstelle (VB und c#)**](iwmpmediacollection2--vb-and-c.md)
-   [**Iwmpquery-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpquery)
-   [**Iwmpquery-Schnittstelle (VB und c#)**](iwmpquery--vb-and-c.md)
-   [**Iwmprenderconfig-Schnittstelle**](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmprenderconfig)
-   [**IWMPStringCollection2-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection2)
-   [**IWMPStringCollection2-Schnittstelle (VB und c#)**](iwmpstringcollection2--vb-and-c.md)
-   [**IWMPSyncDevice2-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice2)
-   [**Iwmpvideorenderconfig-Schnittstelle**](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpvideorenderconfig)
-   [**Query-Objekt**](query-object.md)
-   [**Wmpburnformat-Enumeration**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnformat)
-   [**Wmpburnstate-Enumeration**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate)
-   [**Wmplibrarytype-Enumeration**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype)
-   [**Wmpripstate-Enumeration**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate)

## <a name="added-for-windows-media-player-12"></a>Für Windows Media Player 12 hinzugefügt

-   [**Iwmpaudiorenderconfig-Schnittstelle**](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpaudiorenderconfig)
-   [**IWMPEvents4-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents4)
-   [**IWMPLibrary2-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary2)
-   [**IWMPSyncDevice3-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice3)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zum Player-Objektmodell**](about-the-player-object-model.md)
</dt> <dt>

[**Objektmodell Referenz für die Skripterstellung**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




