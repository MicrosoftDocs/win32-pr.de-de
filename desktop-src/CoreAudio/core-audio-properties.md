---
description: 'Diese Programmier Referenz für das Core-audiosdk umfasst die folgenden Eigenschaften:'
ms.assetid: db7d68c3-5642-4238-a212-88d3479ce73d
title: Kernaudioeigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41528e66977f1f3b9282cf78ba76e4bae32c5bd6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104522891"
---
# <a name="core-audio-properties"></a>Kernaudioeigenschaften

Diese Programmier Referenz für das Core-audiosdk umfasst die folgenden Eigenschaften:

## <a name="audio-endpoint-properties"></a>Eigenschaften des audioendpunkts

Das Core-audiosdk umfasst mehrere Eigenschaften von [audioendpunktgeräten](audio-endpoint-devices.md). Weitere Informationen finden Sie unter [Eigenschaften für audioendpunkte](audio-endpoint-properties.md).

Die folgenden Eigenschaften sind in "mmdeviceapi. h" in Windows Vista und höher definiert.



| Eigenschaft                                                                                                            | BESCHREIBUNG                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Pkey \_ audioendpoint-Zuordnung \_**](pkey-audioendpoint-association.md)                                          | Ordnet einem audioendpunktgerät eine-PIN-Kategorie (Kernel Streaming) zu.                                                                                |
| [**Pkey \_ audioendpoint \_ controlpanelpageprovider**](pkey-audioendpoint-controlpanelpageprovider.md)                | Gibt die CLSID des registrierten Anbieters der Geräteeigenschaften Erweiterung für das audioendpunkt-Gerät an.                                              |
| [**Pkey \_ audioendpoint \_ Deaktivieren von \_ sysfx**](pkey-audioendpoint-disable-sysfx.md)                                     | Gibt an, ob System Effekte im freigegebenen Modus-Stream aktiviert sind, der zum oder vom audioendpunktgerät fließt.                                       |
| [**Pkey- \_ audioendpoint- \_ FormFactor**](pkey-audioendpoint-formfactor.md)                                            | Gibt die physischen Attribute des audioendpunktgeräts an.                                                                                               |
| [**Pkey- \_ audioendpoint \_ fullrangespeakers**](pkey-audioendpoint-fullrangespeakers.md)                              | Gibt die Kanal konfigurationsmaske für die vollständig gültigen Referenten an, die mit dem audioendpunktgerät verbunden sind.                                         |
| [**Pkey- \_ audioendpunkt- \_ GUID**](pkey-audioendpoint-guid.md)                                                        | Gibt den DirectSound-Geräte Bezeichner an, der dem audioendpunktgerät entspricht.                                                                     |
| [**Pkey \_ audioendpoint \_ physicalspeakers**](pkey-audioendpoint-physicalspeakers.md)                                | Definiert die physische Lautsprecher Konfiguration für das audioendpunktgerät.                                                                                     |
| [**Pkey \_ Audioengine \_ deviceformat**](pkey-audioengine-deviceformat.md)                                            | Gibt das Geräte Format an. Hierbei handelt es sich um das Format, das die Audioengine für den Stream im freigegebenen Modus verwendet, der zum oder vom audioendpunktgerät fließt.       |
| [**Pkey \_ Audioengine- \_ oemformat**](pkey-audioengine-oemformat.md)<br/>                                       | Gibt das Standardformat des Geräts an, das zum Rendern oder Erfassen eines Streams verwendet wird. Die Werte werden vom OEM in einer INF-Datei aufgefüllt. <br/> |
| [**Pkey \_ audioendpoint \_ unterstützt den \_ ereignisbasierten \_ Modus**](pkey-audioendpoint-supports-eventdriven-mode.md)<br/> | Gibt an, ob der Endpunkt den ereignisgesteuerten Modus unterstützt. Die Werte werden vom OEM in einer INF-Datei aufgefüllt.<br/>                                |
| [**Pkey- \_ audioendpoint-" \_ jacksubtype"**](pkey-audioendpoint-jacksubtype.md)<br/>                               | Enthält eine Ausgabe Kategorie-GUID für ein audioendpunktgerät. <br/>                                                                                    |



 

## <a name="device-properties"></a>Geräteeigenschaften

Das Core-audiosdk umfasst verschiedene Geräteeigenschaften von [audioendpunktgeräten](audio-endpoint-devices.md). Weitere Informationen finden Sie unter [Geräteeigenschaften](device-properties.md).

Die folgenden Eigenschaften sind in functiondiscoverykeys \_ devpkey. h in Windows Vista und höher definiert.



| Eigenschaft                                                                         | BESCHREIBUNG                                                                                                                                                                                       |
|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Pkey-Geräte \_ Name (tviceinterface \_ FriendlyName)**](pkey-deviceinterface-friendlyname.md) | Der Anzeige Name des audioadapters, an den das Endpunkt Gerät angefügt wird (z. b. "XYZ-Audioadapter").                                                                               |
| [**Pkey- \_ Gerät \_ devicedebug**](pkey-device-devicedesc.md)                       | Die Geräte Beschreibung des Endpunkt Geräts (z. b. "Sprecher").                                                                                                                          |
| [**Pkey- \_ Gerät \_ FriendlyName**](pkey-device-friendlyname.md)                   | Der Anzeige Name des Endpunkt Geräts (z. b. "Sprecher (XYZ-Audioadapter)").                                                                                                           |
| **Pkey \_ \_ -Geräte-containerid**                                                    | Speichert den Container Bezeichner des PNP-Geräts, das den audioendpunkt implementiert. Weitere Informationen zu dieser Eigenschaft finden Sie unter "Referenz zu Geräteeigenschaften" in der Windows WDK-Dokumentation. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmierverzeichnis](programming-reference.md)
</dt> </dl>

 

 




