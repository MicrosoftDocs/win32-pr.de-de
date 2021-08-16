---
description: Windows WIA-Hardwaregeräte (Image Acquisition) werden als hierarchische Strukturen von Item-Objekten dargestellt. Das Stammelement in dieser Struktur stellt das Gerät selbst dar, während untergeordnete Elemente Bilder, Ordner oder Scanvorgänge darstellen.
ms.assetid: 240557d6-665e-4879-8c6e-f564ca61e031
title: Elementobjekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 2b5b32603f334148fede3bc2866367817fd3dcd5ab33aaa40bab84fe3cf49624
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208933"
---
# <a name="item-object"></a>Elementobjekt

Windows WIA-Hardwaregeräte (Image Acquisition) werden als hierarchische Strukturen von **Item-Objekten** dargestellt. Das Stammelement in dieser Struktur stellt das Gerät selbst dar, während untergeordnete Elemente Bilder, Ordner oder Scanvorgänge darstellen.

Verwenden Sie das **Item-Objekt,** um Daten in eine Datei zu übertragen, in der Elementstruktur für ein bestimmtes Gerät zu navigieren oder Informationen zu einem Bild oder Gerät abzurufen.

## <a name="members"></a>Member

Das **Item-Objekt** verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **Item-Objekt** verfügt über diese Methoden.



| Methode                                                         | Beschreibung                                                                                                                                                                                                                                                                    |
|:---------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetItemsFromUI**](-wia-iwiadispatchitem-getitemsfromui.md) | Die [**GetItemsFromUI-Methode**](-wia-iwiadispatchitem-getitemsfromui.md) des **Item-Objekts** zeigt ein Dialogfeld an, in dem ein Benutzer Bilder und Audiodaten auswählen kann, die von einem Gerät übertragen werden sollen.<br/>                                                                     |
| [**GetPropById**](-wia-iwiadispatchitem-getpropbyid.md)       | Die [**GetPropById-Methode**](-wia-iwiadispatchitem-getpropbyid.md) des **Item-Objekts** verwendet die ID einer Elementeigenschaft, um ihren Wert zurückzugeben.<br/>                                                                                                                     |
| [**TakePicture**](-wia-iwiadispatchitem-takepicture.md)       | Die [**TakePicture-Methode**](-wia-iwiadispatchitem-takepicture.md) des **Item-Objekts** bewirkt, dass ein Digitalkameragerät ein Bild macht und ein **Item-Objekt** zurückgibt, das das resultierende Bild darstellt. Diese Methode gilt nur für Digitalkamerageräte.<br/> |
| [**Übertragen**](-wia-iwiadispatchitem-transfer.md)             | Die [**Transfer-Methode**](-wia-iwiadispatchitem-transfer.md) des **Item-Objekts** überträgt Daten von einem Gerät in eine Datei. Diese Methode gilt nur für Gerätetypelemente.<br/>                                                                                         |



 

### <a name="properties"></a>Eigenschaften

Das **Item-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                                    | Zugriffstyp          | Beschreibung                                                                                                                                                                                                                                                 |
|:----------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Children**](-wia-iwiadispatchitem-children.md)<br/>               | Schreibgeschützt<br/> | Die [**Children-Eigenschaft**](-wia-iwiadispatchitem-children.md) des **Item-Objekts** ruft eine Auflistung von **Item-Objekten** ab. Die Elemente in dieser Auflistung stellen Elemente dar, die direkte untergeordnete Elemente dieses Elements in der hierarchischen Struktur sind. <br/> |
| [**ConnectStatus**](-wia-iwiadispatchitem-connectstatus.md)<br/>     | Schreibgeschützt<br/> | Ruft den Verbindungsstatus des Geräts ab. Diese Eigenschaft gilt nur für Elemente vom Typ Gerät (Stammelemente). Mögliche Werte sind "connected", "disconnected" oder **NULL** (wenn diese Eigenschaft nicht für das Element gilt). <br/>                     |
| [**FirmwareVersion**](-wia-iwiadispatchitem-firmwareversion.md)<br/> | Schreibgeschützt<br/> | Ruft die Firmwareversion des Geräts ab. Diese Eigenschaft gilt nur für Elemente vom Typ Gerät (Stammelemente). <br/>                                                                                                                                  |
| [**FullName**](-wia-iwiadispatchitem-fullname.md)<br/>               | Schreibgeschützt<br/> | Ruft den vollständigen Namen des Elements ab, wie es auf der Benutzeroberfläche angezeigt wird. <br/>                                                                                                                                                                                    |
| [**Höhe**](-wia-iwiadispatchitem-height.md)<br/>                   | Schreibgeschützt<br/> | Die Höhe des Elements in Pixel. <br/>                                                                                                                                                                                                             |
| [**Itemtype**](-wia-iwiadispatchitem-itemtype.md)<br/>               | Schreibgeschützt<br/> | Der Typ dieses Elements. <br/>                                                                                                                                                                                                                          |
| [**Name**](-wia-iwiadispatchitem-name.md)<br/>                       | Schreibgeschützt<br/> | Der Name des Elements, wie er auf der Benutzeroberfläche angezeigt wird. <br/>                                                                                                                                                                                                   |
| [**PictureHeight**](-wia-iwiadispatchitem-pictureheight.md)<br/>     | Schreibgeschützt<br/> | Die Höhe der von dieser Digitalkamera erzeugten Bilder in Pixel. Gilt nur für Digitalkameras. <br/>                                                                                                                                              |
| [**PictureWidth**](-wia-iwiadispatchitem-picturewidth.md)<br/>       | Schreibgeschützt<br/> | Die Breite der von dieser Digitalkamera erzeugten Bilder in Pixel. Gilt nur für Digitalkameras. <br/>                                                                                                                                               |
| [**ThumbHeight**](-wia-iwiadispatchitem-thumbheight.md)<br/>         | Schreibgeschützt<br/> | Die Höhe des Miniaturbilds in Pixel. Diese Eigenschaft gibt -1 zurück, wenn dieses Element keine Miniaturansichten unterstützt. <br/>                                                                                                                               |
| [**Miniaturansicht**](-wia-iwiadispatchitem-thumbnail.md)<br/>             | Schreibgeschützt<br/> | Der Pfad und der Dateiname des Miniaturbilds. Diese Eigenschaft ist **NULL,** wenn das Element keine Miniaturansichten unterstützt, oder wenn kein Pfad erstellt werden kann. <br/>                                                                                                  |
| [**ThumbWidth**](-wia-iwiadispatchitem-thumbwidth.md)<br/>           | Schreibgeschützt<br/> | Die Breite des Miniaturbilds in Pixel. Diese Eigenschaft gibt -1 zurück, wenn dieses Element keine Miniaturansichten unterstützt. <br/>                                                                                                                                |
| [**Zeit**](-wia-iwiadispatchitem-time.md)<br/>                       | Schreibgeschützt<br/> | Die aktuelle Zeit. Gilt nur für Geräte. <br/>                                                                                                                                                                                                      |
| [**Breite**](-wia-iwiadispatchitem-width.md)<br/>                     | Schreibgeschützt<br/> | Die Breite des Elements in Pixel. <br/>                                                                                                                                                                                                              |



 

## <a name="remarks"></a>Hinweise

### <a name="creationaccess-functions"></a>\\Erstellungszugriffsfunktionen

Verwenden Sie einen der folgenden Angaben, um einen Verweis auf das -Objekt abzurufen:



[**TakePicture**](-wia-iwiadispatchitem-takepicture.md)

[**Erstellen**](-wia-iwiadeviceinfo-create.md)

[**Erstellen**](-wia-iwia-create.md)



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (Version 4.90 oder höher)</dt> </dl> |



 

 




