---
description: Diese Programmierreferenz für das Core Audio SDK enthält die folgenden Eigenschaften.
ms.assetid: db7d68c3-5642-4238-a212-88d3479ce73d
title: Kernaudioeigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad2d6513798a03cbcd9092e24b37900b5eb686d5fd0c434480a933af50c02fd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120059000"
---
# <a name="core-audio-properties"></a>Kernaudioeigenschaften

Diese Programmierreferenz für das Core Audio SDK enthält die folgenden Eigenschaften.

## <a name="audio-endpoint-properties"></a>Audioendpunkteigenschaften

Das Core Audio SDK enthält mehrere Eigenschaften von [Audioendpunktgeräten.](audio-endpoint-devices.md) Weitere Informationen finden Sie unter [AudioEndpunkteigenschaften.](audio-endpoint-properties.md)

Die folgenden Eigenschaften werden in Mmdeviceapi.h in Windows Vista und höher definiert.



| Eigenschaft                                                                                                            | BESCHREIBUNG                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PKEY \_ AudioEndpoint \_ Association**](pkey-audioendpoint-association.md)                                          | Ordnet einem Audioendpunktgerät eine Kernelstreaming-Pinkategorie (KS) zu.                                                                                |
| [**PKEY \_ AudioEndpoint \_ ControlPanelPageProvider**](pkey-audioendpoint-controlpanelpageprovider.md)                | Gibt die CLSID des registrierten Anbieters der Geräteeigenschaftenerweiterung für das Audioendpunktgerät an.                                              |
| [**PKEY \_ AudioEndpoint \_ Disable \_ SysFx**](pkey-audioendpoint-disable-sysfx.md)                                     | Gibt an, ob Systemeffekte in dem Datenstrom im freigegebenen Modus aktiviert sind, der zum oder vom Audioendpunktgerät fließt.                                       |
| [**PKEY \_ AudioEndpoint \_ FormFactor**](pkey-audioendpoint-formfactor.md)                                            | Gibt die physischen Attribute des Audioendpunktgeräts an.                                                                                               |
| [**PKEY \_ AudioEndpoint \_ FullRangeSpeakers**](pkey-audioendpoint-fullrangespeakers.md)                              | Gibt die Kanalkonfigurationsmaske für die Lautsprecher im voll verfügbaren Bereich an, die mit dem Audioendpunktgerät verbunden sind.                                         |
| [**\_PKEY-AudioEndpoint-GUID \_**](pkey-audioendpoint-guid.md)                                                        | Gibt den DirectSound-Gerätebezeichner an, der dem Audioendpunktgerät entspricht.                                                                     |
| [**PKEY \_ AudioEndpoint \_ PhysicalSpeakers**](pkey-audioendpoint-physicalspeakers.md)                                | Definiert die Konfiguration des physischen Lautsprechers für das Audioendpunktgerät.                                                                                     |
| [**PKEY \_ AudioEngine \_ DeviceFormat**](pkey-audioengine-deviceformat.md)                                            | Gibt das Geräteformat an. Dabei handelt es sich um das Format, das die Audio-Engine für den Datenstrom im freigegebenen Modus verwendet, der zum oder vom Audioendpunktgerät fließt.       |
| [**PKEY \_ AudioEngine \_ OEMFormat**](pkey-audioengine-oemformat.md)<br/>                                       | Gibt das Standardformat des Geräts an, das zum Rendern oder Erfassen eines Streams verwendet wird. Die Werte werden vom OEM in einer INF-Datei aufgefüllt. <br/> |
| [**PKEY \_ AudioEndpoint \_ unterstützt den \_ EventDriven-Modus. \_**](pkey-audioendpoint-supports-eventdriven-mode.md)<br/> | Gibt an, ob der Endpunkt den ereignisgesteuerten Modus unterstützt. Die Werte werden vom OEM in einer INF-Datei aufgefüllt.<br/>                                |
| [**PKEY \_ AudioEndpoint \_ JackSubType**](pkey-audioendpoint-jacksubtype.md)<br/>                               | Enthält eine Ausgabekategorie-GUID für ein Audioendpunktgerät. <br/>                                                                                    |



 

## <a name="device-properties"></a>Geräteeigenschaften

Das Core Audio SDK enthält mehrere Geräteeigenschaften von [Audioendpunktgeräten.](audio-endpoint-devices.md) Weitere Informationen finden Sie unter [Geräteeigenschaften.](device-properties.md)

Die folgenden Eigenschaften werden in Functiondiscoverykeys \_ devpkey.h in Windows Vista und höher definiert.



| Eigenschaft                                                                         | BESCHREIBUNG                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PKEY \_ DeviceInterface \_ FriendlyName**](pkey-deviceinterface-friendlyname.md) | Der Angezeigte Name des Audioadapters, an den das Endpunktgerät angefügt ist (z. B. "XYZ-Audioadapter").                                                                               |
| [**PKEY \_ Device \_ DeviceDesc**](pkey-device-devicedesc.md)                       | Die Gerätebeschreibung des Endpunktgeräts (z. B. "Sprecher").                                                                                                                          |
| [**PKEY \_ Device \_ FriendlyName**](pkey-device-friendlyname.md)                   | Der Angezeigte Name des Endpunktgeräts (z. B. "Lautsprecher (XYZ-Audioadapter)").                                                                                                           |
| **\_ \_ PKEY-Gerätecontainer-ID**                                                    | Speichert den Containerbezeichner des PnP-Geräts, das den Audioendpunkt implementiert. Weitere Informationen zu dieser Eigenschaft finden Sie unter "Geräteeigenschaftsreferenz" in der WDK Windows dokumentation. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmierverzeichnis](programming-reference.md)
</dt> </dl>

 

 




