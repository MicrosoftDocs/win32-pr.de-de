---
title: Neuerungen in Windows Media Player 12
description: In diesem Thema sind die neuen Features von Windows Media Player 12 aufgeführt.
ms.assetid: 17f76963-c96d-46c9-82c0-3ed2d8a4e892
keywords:
- Windows Media Player, Neuerungen
- Windows Media Player, neue Features
- Software Development Kit (SDK), Windows Media Player 12
- SDK (Software Development Kit), Windows Media Player 12
- Dokumentation, Windows Media Player 12 SDK
- Neuerungen, Windows Media Player 12
- neue Features, Windows Media Player 12
- Schnittstellen, neue Features in Windows Media Player 12
- Attribute, neue Features in Windows Media Player 12
- Metadaten, neue Features in Windows Media Player 12
- Enumerationen, neue Features in Windows Media Player 12
- Flags, neue Features in Windows Media Player 12
- Schnittstellen, veraltet in Windows Media Player 12
- Methoden, veraltet in Windows Media Player 11 und nicht 12
- Versionen von Windows Media Player, neue Features in Version 12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d16b21077df1f4a9c11edbfa20032ed473f872a0
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2020
ms.locfileid: "104101371"
---
# <a name="whats-new-in-windows-media-player-12"></a>Neuerungen in Windows Media Player 12

In diesem Thema sind die neuen Features von Windows Media Player 12 aufgeführt.

## <a name="new-interfaces"></a>Neue Schnittstellen

-   [**Iwmpaudiorenderconfig**](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpaudiorenderconfig)
-   [**IWMPEvents4**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents4)
-   [**IWMPLibrary2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary2)
-   [**IWMPSyncDevice3**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice3)

## <a name="new-attributes"></a>Neue Attribute

Die folgenden neuen Attribute für Medienelemente sind über die [**iwmpmedia**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia) -und [**IWMPMedia3**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia3) -Schnittstellen verfügbar.

-   [**Albumcoverurl**](wm-albumcoverurl-attribute.md)
-   [**Alternative ceurl**](alternatesourceurl-attribute.md)
-   [**Dlnasourceuri**](dlnasourceuri-attribute.md)
-   [**Dlnaserverudn**](dlnaserverudn-attribute.md)
-   [**Dtcpiphost**](dtcpiphost-attribute.md)
-   [**Dtcpipport**](dtcpipport-attribute.md)
-   [**LIBRARYID**](libraryid-attribute.md)
-   [**LibraryName**](libraryname-attribute.md)

## <a name="new-device-metadata"></a>Neue Geräte Metadaten

Die folgenden neuen gerätemetadatenelemente können durch Aufrufen von [**iwmpsyncdevice:: getiteminfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-getiteminfo)abgerufen werden.

-   **Backgroundsyncstate**
-   **Skippedfiles**
-   **SyncFilter**

Die folgenden neuen gerätemetadatenelemente können durch Aufrufen von [**IWMPSyncDevice2:: setiteminfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice2-setiteminfo)festgelegt werden.

-   **Autosyncdefaultrules**
-   **Backgroundsyncstate**
-   **Includeskippedfiles**
-   **SyncFilter**
-   **Synchronisierungs Verbindung**

## <a name="new-enumeration-member"></a>Neuer Enumerationsmember

Die [**wmpsyncstate**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpsyncstate) -Enumeration weist den folgenden neuen Member auf.

-   **wmpssestimating**

## <a name="new-flag"></a>Neues Flag

Die [**iwmpgraphcreation:: getgraphkreationflags**](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpgraphcreation-getgraphcreationflags) -Methode unterstützt das folgende neue Flag.

-   **wmpgc- \_ Flags \_ verwenden \_ benutzerdefiniertes \_ Diagramm**

## <a name="deprecated-interface"></a>Veraltete Schnittstelle

Die folgende Schnittstelle ist veraltet.

-   [**Iwmpfoldermonitorservices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)

## <a name="methods-that-are-no-longer-deprecated"></a>Methoden, die nicht mehr als veraltet eingestuft werden

Die folgenden Methoden wurden im Windows Media Player 11 SDK als veraltet markiert, sind jedoch nicht mehr als veraltet markiert.

-   [**Iwmpgraphcreation:: graphkreationprerender**](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpgraphcreation-graphcreationprerender)
-   [**Iwmpgraphcreation:: graphkreationpostranender**](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpgraphcreation-graphcreationpostrender)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zum Windows Media Player SDK](about-the-windows-media-player-sdk.md)
</dt> </dl>

 

 




