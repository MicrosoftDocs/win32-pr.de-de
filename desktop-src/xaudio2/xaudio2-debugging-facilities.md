---
description: Die Debugversion der XAudio2-Engine überprüft Parameter und stellt detaillierte Warnungen und Fehlermeldungen bereit.
ms.assetid: a7aaebf9-98d4-e96c-993d-b0d0b7074788
title: Debuggen von XAudio2-Einrichtungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dc6a89bb298a2e836e4d8dc63ed0144b9a789950432c5c83f33ec7ad86f4de8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119706990"
---
# <a name="xaudio2-debugging-facilities"></a>Debuggen von XAudio2-Einrichtungen

Die Debugversion der XAudio2-Engine überprüft Parameter und stellt detaillierte Warnungen und Fehlermeldungen bereit.

## <a name="setting-the-debug-logging-level-at-run-time"></a>Festlegen des Debugprotokolliergrads zur Laufzeit

Sie können die Von XAudio2 angezeigten Debuginformationen jederzeit festlegen, indem Sie eine [**XAUDIO2 \_ DEBUG \_ CONFIGURATION-Struktur**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_debug_configuration) mit den Flags für den gewünschten Protokolliergrad ausfüllen und dann die Struktur an die [**IXAudio2::SetDebugConfiguration-Methode**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-setdebugconfiguration) übergeben. Werte, die an die **IXAudio2::SetDebugConfiguration-Methode** übergeben werden, überschreiben immer alle Standardwerte, die in der registrierung Windows festgelegt wurden.

## <a name="debug-support"></a>Debugunterstützung

Die Debugmöglichkeiten sind für XAUDIO2 in Windows 8 immer verfügbar.

Für die DirectX SDK-Versionen von XAUDIO2 müssen Sie die **XAUDIO2-DEBUG-ENGINE \_ \_** verwenden, wenn Sie das XAUDIO2-Objekt mit [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) erstellen, und auf dem System muss die DirectX SDK Developer Runtime installiert sein, damit das Debuggen unterstützt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Debuggen von Einrichtungen](debugging-facilities.md)
</dt> <dt>

[XAudio2-Programmierreferenz](programming-reference.md)
</dt> </dl>

 

 
