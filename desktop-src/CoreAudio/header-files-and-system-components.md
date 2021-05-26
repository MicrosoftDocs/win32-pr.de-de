---
description: Headerdateien und Systemkomponenten
ms.assetid: de2776be-72e6-4391-8e6c-56694d683d57
title: Headerdateien und Systemkomponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77a47125853b51a71f2f05dacf4534ce33cfedec
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2021
ms.locfileid: "110424290"
---
# <a name="header-files-and-system-components"></a>Headerdateien und Systemkomponenten

In der folgenden Tabelle sind die Headerdateien aufgeführt, die die Schnittstellendefinitionen für die vier Core Audio-Komponenten enthalten.



| Kernaudiokomponente                         | Headerdatei                  |
|----------------------------------------------|------------------------------|
| [MMDevice-API](mmdevice-api.md)             | Mmdeviceapi.h                |
| [WASAPI](wasapi.md)                         | Audioclient.h, Audiopolicy.h |
| [DeviceTopology-API](devicetopology-api.md) | Devicetopology.h             |
| [EndpointVolume-API](endpointvolume-api.md) | Endpointvolume.h             |



 

Eine andere Headerdatei, Audiosessiontypes.h, definiert Konstanten, die von WASAPI verwendet werden. Diese Headerdateien befinden sich im Verzeichnis %MSSdk% include, wobei %MSSdk% das Stammverzeichnis der Windows SDK auf Ihrem Computer \\ ist.

Jede API in der obigen Tabelle besteht aus einem Satz verwandter COM-Schnittstellen. Da einige Aspekte des Audiostreamings von geringer Latenz und präziser Synchronisierung abhängen, verwenden die Implementierungen der APIs MMDevice, WASAPI, DeviceTopology und EndpointVolume nicht das Microsoft .NET Framework oder die Verwaltete Ausführungsumgebung.

Die Core Audio-APIs werden in den Systemkomponenten des Benutzermodus Audioses.dll und Mmdevapi.dll. Clientanwendungen greifen nicht direkt auf die Einstiegspunkte in diesen DLLs zu. Stattdessen rufen Clients die **Funktion CoCreateInstance** oder **CoCreateInstanceEx** auf, um die [**IMMDeviceEnumerator-Schnittstelle**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) des MMDeviceEnumerator-Klassenobjekts zu erhalten. Dieses Objekt listet die [Audioendpunktgeräte](audio-endpoint-devices.md) im System auf. Die **IMMDeviceEnumerator-Schnittstelle** ist Teil der MMDevice-API. Über diese Schnittstelle können Clients direkt oder indirekt die anderen Schnittstellen in der MMDevice-API abrufen, einschließlich der [**IMMDevice-Schnittstelle.**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) **IMMDevice** stellt ein bestimmtes Audioendpunktgerät dar. Über **IMMDevice** können Clients die gerätespezifischen Schnittstellen in WASAPI, der DeviceTopology-API und der EndpointVolume-API direkt oder indirekt abrufen. Weitere Informationen zu **CoCreateInstance** und **CoCreateInstanceEx** finden Sie in der Windows SDK-Dokumentation. Weitere Informationen zum Zugriff auf die Schnittstellen in den Core Audio-APIs finden Sie unter [Aufzählen von Audiogeräten.](enumerating-audio-devices.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu Windows Core-Audio-APIs](about-the-windows-core-audio-apis.md)
</dt> </dl>

 

 



