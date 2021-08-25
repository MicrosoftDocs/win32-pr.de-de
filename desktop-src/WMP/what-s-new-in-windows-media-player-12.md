---
title: Neuerungen in Windows Media Player 12
description: In diesem Thema werden features aufgeführt, die in Windows Media Player 12 neu sind.
ms.assetid: 17f76963-c96d-46c9-82c0-3ed2d8a4e892
keywords:
- Windows Media Player,What es new (Neues)
- Windows Media Player,neue Features
- Software Development Kit (SDK), Windows Media Player 12
- SDK (Software Development Kit), Windows Media Player 12
- Dokumentation,Windows Media Player 12 SDK
- What es new,Windows Media Player 12
- neue Features,Windows Media Player 12
- Schnittstellen,neue Features in Windows Media Player 12
- Attribute,neue Features in Windows Media Player 12
- Metadaten,neue Features in Windows Media Player 12
- Enumerationen,neue Features in Windows Media Player 12
- Flags,neue Features in Windows Media Player 12
- Schnittstellen,veraltet in Windows Media Player 12
- -Methoden, veraltet in Windows Media Player 11 und nicht 12
- Versionen von Windows Media Player,neue Features in Version 12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 976c9b0995188f9d6c6db6e7394ec0019047ff18b51940ada202c8c7ea713f39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862280"
---
# <a name="whats-new-in-windows-media-player-12"></a>Neuerungen in Windows Media Player 12

In diesem Thema werden features aufgeführt, die in Windows Media Player 12 neu sind.

## <a name="new-interfaces"></a>Neue Schnittstellen

-   [**IWMPAudioRenderConfig**](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpaudiorenderconfig)
-   [**IWMPEvents4**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents4)
-   [**IWMPLibrary2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary2)
-   [**IWMPSyncDevice3**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice3)

## <a name="new-attributes"></a>Neue Attribute

Die folgenden neuen Attribute für Medienelemente sind über die [**SCHNITTSTELLEN IWMPMedia**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia) und [**IWMPMedia3**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia3) verfügbar.

-   [**AlbumCoverURL**](wm-albumcoverurl-attribute.md)
-   [**AlternateSourceURL**](alternatesourceurl-attribute.md)
-   [**DLNASourceURI**](dlnasourceuri-attribute.md)
-   [**DLNAServerUDN**](dlnaserverudn-attribute.md)
-   [**DTCPIPHost**](dtcpiphost-attribute.md)
-   [**DTCPIPPort**](dtcpipport-attribute.md)
-   [**LibraryID**](libraryid-attribute.md)
-   [**LibraryName**](libraryname-attribute.md)

## <a name="new-device-metadata"></a>Neue Gerätemetadaten

Die folgenden neuen Gerätemetadatenelemente können durch Aufrufen von [**IWMPSyncDevice::getItemInfo abgerufen werden.**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-getiteminfo)

-   **BackgroundSyncState**
-   **SkippedFiles**
-   **SyncFilter**

Die folgenden neuen Gerätemetadatenelemente können durch Aufrufen von [**IWMPSyncDevice2::setItemInfo festgelegt werden.**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice2-setiteminfo)

-   **AutoSyncDefaultRules**
-   **BackgroundSyncState**
-   **IncludeSkippedFiles**
-   **SyncFilter**
-   **SyncOnConnect**

## <a name="new-enumeration-member"></a>Neuer Enumerationsmember

Die [**WMPSyncState-Enumeration**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpsyncstate) verfügt über den folgenden neuen Member.

-   **wmpssEstimating**

## <a name="new-flag"></a>Neues Flag

Die [**IWMPGraphCreation::GetGraphCreationFlags-Methode**](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpgraphcreation-getgraphcreationflags) unterstützt das folgende neue Flag.

-   **WMPGC-FLAGS \_ \_ VERWENDEN \_ BENUTZERDEFINIERTES \_ DIAGRAMM**

## <a name="deprecated-interface"></a>Veraltete Schnittstelle

Die folgende Schnittstelle ist veraltet.

-   [**IWMPFolderMonitorServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)

## <a name="methods-that-are-no-longer-deprecated"></a>Methoden, die nicht mehr veraltet sind

Die folgenden Methoden sind im 11 SDK Windows Media Player veraltet, aber nicht mehr veraltet.

-   [**IWMPGraphCreation::GraphCreationPreRender**](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpgraphcreation-graphcreationprerender)
-   [**IWMPGraphCreation::GraphCreationPostRender**](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpgraphcreation-graphcreationpostrender)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zum Windows Media Player SDK](about-the-windows-media-player-sdk.md)
</dt> </dl>

 

 




