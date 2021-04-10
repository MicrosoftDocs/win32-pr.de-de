---
description: Mstape-Treiber
ms.assetid: aa59f322-09b1-4b0a-be6f-d865c20f76e5
title: Mstape-Treiber
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14f37e22c26866fca9519219d358e9733fb56151
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103859985"
---
# <a name="mstape-driver"></a>Mstape-Treiber

Dieses Thema gilt für Windows XP oder höher.

Der mstape-Treiber unterstützt D-VHS-und MPEG-Camcorder-Geräte. Sie wird für Anwendungen als [WDM-Video Erfassungs](wdm-video-capture-filter.md) Filter verfügbar gemacht. Seine Funktionalität ähnelt der von [msdv](msdv-driver.md), dem DV-Camcorder-Treiber:

-   Sie wird in den Filter Kategorien "Video Erfassungs Quellen" (CLSID \_ videoinputdebug) und "WDM Streaming Rendering Devices" (am \_ kscategory Rendering \_ ) angezeigt.
-   Eine Anwendung kann eine Instanz des Filters mithilfe der [**ikreatedevenum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) -Schnittstelle erstellen.
-   Es verfügt über eine Ausgabe-PIN zum Erfassen und transportieren vom Gerät und eine Eingabe-PIN für den Transport zum Gerät. Es kann jeweils nur eine PIN verbunden werden.

**Medientypen**

Die eingabepin unterstützt einen Medientyp.



|              |                                                            |
|--------------|------------------------------------------------------------|
| Haupttyp   | MediaType- \_ Stream                                          |
| Subtype      | Mediasubtype \_ MPEG2- \_ Transport \_ Stride                     |
| Stichprobengröße  | 192 x 256                                                  |
| Format Block | [**MPEG2- \_ Transport \_ Stride**](mpeg2-transport-stride.md) |



 

Die Ausgabepin unterstützt zwei Medientypen.



|              |                                        |
|--------------|----------------------------------------|
| Haupttyp   | MediaType- \_ Stream                      |
| Subtype      | Mediasubtype \_ MPEG2- \_ Transport \_ Stride |
| Stichprobengröße  | 192 x 256                              |
| Format Block | MPEG2- \_ Transport \_ Stride               |



 



|              |                                        |
|--------------|----------------------------------------|
| Haupttyp   | MediaType- \_ Stream                      |
| Subtype      | Mediasubtype \_ MPEG2- \_ Transport \_ Stride |
| Stichprobengröße  | 188 x 256                              |
| Format Block | **NULL**                               |



 

**Geräteinformationen**

Der Treiber liest dynamisch Informationen aus dem Geräte Konfigurations-Rom. Diese Informationen können von der Anwendung abgerufen werden, indem der gerätermoniker an einen Eigenschaften Behälter gebunden und die **IPropertyBag:: Read** -Methode aufgerufen wird.



| Eigenschaft            | BESCHREIBUNG                                                                                                                                                                         | Datentyp           |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| UniqueId \_ niedrig       | Eindeutige ID des Geräts (niedriges **DWORD**).                                                                                                                                            | **Long** (VT \_ I4)   |
| UniqueId \_ hoch      | Eindeutige ID des Geräts (High **DWORD**)                                                                                                                                            | **long**            |
| VendorID            | Anbieter-ID.                                                                                                                                                                          | **long**            |
| ModelID             | Modell-ID                                                                                                                                                                           | **long**            |
| Vendortext          | Der Name des Anbieters.                                                                                                                                                                        | **BSTR** (VT \_ BSTR) |
| Modeltext           | Gerätemodell Name.                                                                                                                                                                  | **BSTR**            |
| Unitmodeltext       | Name des Einheitsmodells; kann mit modeltext identisch sein.                                                                                                                                      | **BSTR**            |
| DeviceOPcr0Payload  | opcr-Nutzlast (Ausgabe-Plug-in). Beispiel: 146 quadlets.                                                                                                                          | **long**            |
| DeviceOPcr0DataRate | opcr-Datenrate. Beispiele: 0 (S100), 1 (S200) oder 2 (S400).                                                                                                                          | **long**            |
| Geräte-ID     | GUID, die den Gerätetreiber identifiziert. Für mstape ist dieser Wert `{8C0F6AF2-0EDB-44C1-8AEB-59040BD830ED}` . Diese GUID wird in der Header Datei xprtdefs. h als mstapedeviceguid definiert. | **BSTR**            |
| BESCHREIBUNG         | Eine Beschreibung des Geräts aus der INF-Datei. Diese Zeichenfolge enthält normalerweise den Markennamen des Geräts.                                                                    | **BSTR**            |



 

Die Geräte-ID ist eine 64-Bit-Ganzzahl. Das niedrige **DWORD** wird in der UniqueId \_ Low-Eigenschaft gespeichert, und das High **DWORD** wird in der UniqueId \_ High-Eigenschaft gespeichert.

Weitere Informationen zu gerätermonikern finden [Sie unter Verwenden des System Geräte Enumerators](using-the-system-device-enumerator.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectShow-Filter](directshow-filters.md)
</dt> <dt>

[Steuern eines DV-Camcorder](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



