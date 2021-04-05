---
description: Windows-Abbild Beschaffung-Hardware Geräte (WIA) werden als hierarchische Struktur von Element Objekten dargestellt. Das Stamm Element in dieser Struktur stellt das eigentliche Gerät dar, während untergeordnete Elemente Bilder, Ordner oder das Scannen von Betten darstellen.
ms.assetid: 240557d6-665e-4879-8c6e-f564ca61e031
title: Item-Objekt
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
ms.openlocfilehash: 6af0642a47db9d3a7a1c30aea76be22ea5ce1d07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752848"
---
# <a name="item-object"></a>Item-Objekt

Windows-Abbild Beschaffung-Hardware Geräte (WIA) werden als hierarchische Struktur von **Element** Objekten dargestellt. Das Stamm Element in dieser Struktur stellt das eigentliche Gerät dar, während untergeordnete Elemente Bilder, Ordner oder das Scannen von Betten darstellen.

Verwenden Sie das **Item** -Objekt, um Daten in eine Datei zu übertragen, um in der Elementstruktur nach einem bestimmten Gerät zu navigieren oder um Informationen zu einem Bild oder einem Gerät abzurufen.

## <a name="members"></a>Member

Das **Item** -Objekt verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **Item** -Objekt verfügt über diese Methoden.



| Methode                                                         | BESCHREIBUNG                                                                                                                                                                                                                                                                    |
|:---------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Getitemsfromui**](-wia-iwiadispatchitem-getitemsfromui.md) | Die [**getitemsfromui**](-wia-iwiadispatchitem-getitemsfromui.md) -Methode des **Item** -Objekts zeigt ein Dialogfeld an, in dem ein Benutzer Bilder und Audiodaten auswählen kann, die von einem Gerät übertragen werden sollen.<br/>                                                                     |
| [**Getpropbyid**](-wia-iwiadispatchitem-getpropbyid.md)       | Die [**getpropbyid**](-wia-iwiadispatchitem-getpropbyid.md) -Methode des **Item** -Objekts verwendet die ID einer Item-Eigenschaft, um ihren Wert zurückzugeben.<br/>                                                                                                                     |
| [**Takebild**](-wia-iwiadispatchitem-takepicture.md)       | Die [**takepicture**](-wia-iwiadispatchitem-takepicture.md) -Methode des **Item** -Objekts bewirkt, dass ein digitales Kamera Gerät ein Bild annimmt und ein **Element** Objekt zurückgibt, das das resultierende Bild darstellt. Diese Methode gilt nur für digitale Kamerageräte.<br/> |
| [**Übertragen**](-wia-iwiadispatchitem-transfer.md)             | Die [**Übertragungs**](-wia-iwiadispatchitem-transfer.md) Methode des **Item** -Objekts überträgt Daten von einem Gerät in eine Datei. Diese Methode gilt nur für Gerätetyp Elemente.<br/>                                                                                         |



 

### <a name="properties"></a>Eigenschaften

Das **Item** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                                    | Zugriffstyp          | BESCHREIBUNG                                                                                                                                                                                                                                                 |
|:----------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Children**](-wia-iwiadispatchitem-children.md)<br/>               | Schreibgeschützt<br/> | Die [**Children**](-wia-iwiadispatchitem-children.md) -Eigenschaft des **Item** -Objekts Ruft eine Auflistung von **Element** Objekten ab. Die Elemente in dieser Auflistung stellen Elemente dar, die direkt untergeordnete Elemente dieses Elements in der hierarchischen Struktur sind. <br/> |
| [**Connectstatus**](-wia-iwiadispatchitem-connectstatus.md)<br/>     | Schreibgeschützt<br/> | Ruft den Verbindungsstatus des Geräts ab. Diese Eigenschaft gilt nur für Elemente vom Typ Device (root Items). Mögliche Werte sind "verbunden", "getrennt" oder **null** (wenn diese Eigenschaft nicht für das Element gilt). <br/>                     |
| [**Firmwareversion**](-wia-iwiadispatchitem-firmwareversion.md)<br/> | Schreibgeschützt<br/> | Ruft die Firmwareversion des Geräts ab. Diese Eigenschaft gilt nur für Elemente vom Typ Device (root Items). <br/>                                                                                                                                  |
| [**FullName**](-wia-iwiadispatchitem-fullname.md)<br/>               | Schreibgeschützt<br/> | Ruft den vollständigen Namen des Elements ab, das in der Benutzeroberfläche angezeigt wird. <br/>                                                                                                                                                                                    |
| [**Höhe**](-wia-iwiadispatchitem-height.md)<br/>                   | Schreibgeschützt<br/> | Die Höhe des Elements in Pixel. <br/>                                                                                                                                                                                                             |
| [**ItemType**](-wia-iwiadispatchitem-itemtype.md)<br/>               | Schreibgeschützt<br/> | Der Typ dieses Elements. <br/>                                                                                                                                                                                                                          |
| [**Name**](-wia-iwiadispatchitem-name.md)<br/>                       | Schreibgeschützt<br/> | Der Name des Elements, wie er in der Benutzeroberfläche angezeigt wird. <br/>                                                                                                                                                                                                   |
| [**Pictureheight**](-wia-iwiadispatchitem-pictureheight.md)<br/>     | Schreibgeschützt<br/> | Die Höhe von Bildern, die von dieser digitalen Kamera erzeugt werden, in Pixel. Gilt nur für digitale Kameras. <br/>                                                                                                                                              |
| [**Picturewidth**](-wia-iwiadispatchitem-picturewidth.md)<br/>       | Schreibgeschützt<br/> | Die Breite von Bildern, die von dieser digitalen Kamera erzeugt werden, in Pixel. Gilt nur für digitale Kameras. <br/>                                                                                                                                               |
| [**Thumbheight**](-wia-iwiadispatchitem-thumbheight.md)<br/>         | Schreibgeschützt<br/> | Die Höhe des Miniatur Bilds in Pixel. Diese Eigenschaft gibt-1 zurück, wenn dieses Element keine Miniaturansichten unterstützt. <br/>                                                                                                                               |
| [**Miniaturansicht**](-wia-iwiadispatchitem-thumbnail.md)<br/>             | Schreibgeschützt<br/> | Der Pfad und der Dateiname des Miniatur Bilds. Diese Eigenschaft ist **null** , wenn das Element keine Miniaturansichten unterstützt, oder wenn kein Pfad erstellt werden kann. <br/>                                                                                                  |
| [**Thumbwidth**](-wia-iwiadispatchitem-thumbwidth.md)<br/>           | Schreibgeschützt<br/> | Die Breite des Miniatur Bilds in Pixel. Diese Eigenschaft gibt-1 zurück, wenn dieses Element keine Miniaturansichten unterstützt. <br/>                                                                                                                                |
| [**Time**](-wia-iwiadispatchitem-time.md)<br/>                       | Schreibgeschützt<br/> | Die aktuelle Zeit. Gilt nur für Geräte. <br/>                                                                                                                                                                                                      |
| [**Breite**](-wia-iwiadispatchitem-width.md)<br/>                     | Schreibgeschützt<br/> | Die Breite des Elements in Pixel. <br/>                                                                                                                                                                                                              |



 

## <a name="remarks"></a>Bemerkungen

### <a name="creationaccess-functions"></a>Zugriffs Funktionen für die Erstellung \\

Verwenden Sie eine der folgenden Informationen, um einen Verweis auf das-Objekt abzurufen:



[**Takebild**](-wia-iwiadispatchitem-takepicture.md)

[**Stelle**](-wia-iwiadeviceinfo-create.md)

[**Erstellen**](-wia-iwia-create.md)



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (Version 4,90 oder höher)</dt> </dl> |



 

 




