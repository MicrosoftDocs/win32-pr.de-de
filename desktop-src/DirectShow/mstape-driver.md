---
description: MSTape-Treiber
ms.assetid: aa59f322-09b1-4b0a-be6f-d865c20f76e5
title: MSTape-Treiber
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23eaf6dd7f0d6713b0db5ba5ed21ba4f7640c1373f23cb0066b0b31f366809cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952209"
---
# <a name="mstape-driver"></a>MSTape-Treiber

Dieses Thema gilt für Windows XP oder höher.

Der MSTape-Treiber unterstützt D-VHS- und MPEG-Mpeg-Geräte. Sie wird für Anwendungen als [WDM Video Capture-Filter](wdm-video-capture-filter.md) verfügbar gemacht. Seine Funktionalität ähnelt der von [MSDV](msdv-driver.md), dem DV-Treiber:

-   Sie wird in den Filterkategorien "Video Capture Sources" (CLSID \_ VideoInputDeviceCategory) und "WDM Streaming Rendering Devices" (AM \_ KSCATEGORY \_ RENDER) angezeigt.
-   Eine Anwendung kann mithilfe der [**ICreateDevEnum-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) eine Instanz des Filters erstellen.
-   Sie verfügt über einen Ausgabestecker für die Erfassung und den Transport vom Gerät und einen Eingabepin für den Transport zum Gerät. Es kann jeweils nur eine Stecknadel verbunden werden.

**Medientypen**

Der Eingabepin unterstützt einen Medientyp.



| Bezeichnung | Wert |
|--------------|------------------------------------------------------------|
| Haupttyp   | \_MEDIATYPE-Stream                                          |
| Subtype      | MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT \_ STRIDE                     |
| Stichprobengröße  | 192 x 256                                                  |
| Block formatieren | [**MPEG2 \_ TRANSPORT \_ STRIDE**](mpeg2-transport-stride.md) |



 

Der Ausgabepin unterstützt zwei Medientypen.



| Bezeichnung | Wert |
|--------------|----------------------------------------|
| Haupttyp   | \_MEDIATYPE-Stream                      |
| Subtype      | MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT \_ STRIDE |
| Stichprobengröße  | 192 x 256                              |
| Block formatieren | MPEG2 \_ TRANSPORT \_ STRIDE               |



 



| Bezeichnung | Wert |
|--------------|----------------------------------------|
| Haupttyp   | \_MEDIATYPE-Stream                      |
| Subtype      | MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT \_ STRIDE |
| Stichprobengröße  | 188 x 256                              |
| Block formatieren | **NULL**                               |



 

**Geräteinformationen**

Der Treiber liest dynamisch Informationen aus dem Gerätekonfigurations-ROM. Die Anwendung kann diese Informationen abrufen, indem sie den Gerätemoniker an einen Eigenschaftenbehälter bindet und die **IPropertyBag::Read-Methode** aufruft.



| Eigenschaft            | Beschreibung                                                                                                                                                                         | Datentyp           |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| UniqueID \_ Low       | Eindeutige ID des Geräts (niedriger **DWORD-Wert).**                                                                                                                                            | **long** (VT \_ I4)   |
| UniqueID \_ High      | Eindeutige ID des Geräts (hohes **DWORD)**                                                                                                                                            | **long**            |
| VendorID            | Anbieter-ID.                                                                                                                                                                          | **long**            |
| ModelID             | Modell-ID                                                                                                                                                                           | **long**            |
| VendorText          | Name des Anbieters.                                                                                                                                                                        | **BSTR** (VT \_ BSTR) |
| ModelText           | Name des Gerätemodells.                                                                                                                                                                  | **Bstr**            |
| UnitModelText       | Name des Einheitenmodells; kann mit ModelText identisch sein.                                                                                                                                      | **Bstr**            |
| DeviceOPcr0Payload  | oPCR(Output Plug Control)-Nutzlast. Beispiel: 146 Quadlets.                                                                                                                          | **long**            |
| DeviceOPcr0DataRate | oPCR-Datenrate. Beispiele: 0 (S100), 1 (S200) oder 2 (S400).                                                                                                                          | **long**            |
| DeviceClassGUID     | GUID, die den Gerätetreiber identifiziert. Für MSTape ist dieser Wert `{8C0F6AF2-0EDB-44C1-8AEB-59040BD830ED}` . Diese GUID ist in der Headerdatei Xprtdefs.h als MSTapeDeviceGUID definiert. | **Bstr**            |
| Beschreibung         | Eine Beschreibung des Geräts aus der INF-Datei. Diese Zeichenfolge enthält in der Regel den Markennamen des Geräts.                                                                    | **Bstr**            |



 

Die Geräte-ID ist eine 64-Bit-Ganzzahl. Das niedrige **DWORD** wird in der UniqueID \_ Low-Eigenschaft und das hohe **DWORD** in der UniqueID \_ High-Eigenschaft gespeichert.

Weitere Informationen zu Gerätemonikern finden Sie unter [Verwenden des Systemgeräte-Enumerators.](using-the-system-device-enumerator.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> <dt>

[Steuern eines DV-Dvds](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



