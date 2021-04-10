---
description: Header Dateien und System Komponenten
ms.assetid: de2776be-72e6-4391-8e6c-56694d683d57
title: Header Dateien und System Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47c4b93c63e7d32944dfdf2bf6872bd3a3153e4a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127440"
---
# <a name="header-files-and-system-components"></a>Header Dateien und System Komponenten

In der folgenden Tabelle werden die Header Dateien aufgelistet, die die Schnittstellendefinitionen für die vier kernaudiokomponenten enthalten.



|                                              |                              |
|----------------------------------------------|------------------------------|
| Kernaudiokomponente                         | Headerdatei                  |
| [Mmdevice-API](mmdevice-api.md)             | Mmdeviceapi. h                |
| [WASAPI](wasapi.md)                         | AudioClient. h, audiopolicy. h |
| [Debug-opology-API](devicetopology-api.md) | "Tvicetopology. h"             |
| [Endpointvolume-API](endpointvolume-api.md) | Endpointvolume. h             |



 

Eine andere Header Datei, audiosessiontypes. h, definiert Konstanten, die von WASAPI verwendet werden. Diese Header Dateien befinden sich im Verzeichnis% MSSDK% \\ include, wobei% MSSDK% das Stammverzeichnis der Windows SDK Installation auf Ihrem Computer ist.

Jede API in der vorangehenden Tabelle besteht aus einem Satz verwandter com-Schnittstellen. Da einige Aspekte des audiostreamings von geringer Latenz und präziser Synchronisierung abhängen, verwenden die Implementierungen der APIs "mmdevice", "WASAPI", "debuetopology" und "endpointvolume" nicht das Microsoft .NET Framework oder die verwaltete Ausführungsumgebung.

Die Kern-audioapis werden in den Systemkomponenten des Benutzermodus implementiert Audioses.dll und Mmdevapi.dll. Client Anwendungen greifen nicht direkt auf die Einstiegspunkte in diesen DLLs zu. Stattdessen rufen Clients die Funktion **cokreateinstance** oder **cokreateinstanceex** auf, um die [**immdeviceenumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) -Schnittstelle des mmdeviceenumerator-Klassen Objekts abzurufen. Dieses Objekt listet die [audioendpunktgeräte](audio-endpoint-devices.md) im System auf. Die **immdeviceenumerator** -Schnittstelle ist Teil der mmdevice-API. Über diese Schnittstelle können Clients die anderen Schnittstellen in der mmdevice-API (einschließlich der [**immdevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) -Schnittstelle) direkt oder indirekt abrufen. **Immdevice** stellt ein bestimmtes audioendpunktgerät dar. Über **immdevice** können Clients die gerätespezifischen Schnittstellen direkt oder indirekt in der WASAPI, der devicetopology-API und der endpointvolume-API abrufen. Weitere Informationen zu **cokreateinstance** und **cokreateinstanceex** finden Sie in der Windows SDK-Dokumentation. Weitere Informationen zum Zugreifen auf die Schnittstellen in den kernaudioapis finden Sie unter Auflisten von [Audiogeräten](enumerating-audio-devices.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu den Windows Core-audioapis](about-the-windows-core-audio-apis.md)
</dt> </dl>

 

 



