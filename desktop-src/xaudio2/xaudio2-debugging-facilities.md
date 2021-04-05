---
description: Die Debugversion der XAudio2-Engine überprüft Parameter und stellt ausführliche Warn-und Fehlermeldungen bereit.
ms.assetid: a7aaebf9-98d4-e96c-993d-b0d0b7074788
title: XAudio2-Debugging-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc50e710f30969e024078eeaf2660545e1da45c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752409"
---
# <a name="xaudio2-debugging-facilities"></a>XAudio2-Debugging-Funktionen

Die Debugversion der XAudio2-Engine überprüft Parameter und stellt ausführliche Warn-und Fehlermeldungen bereit.

## <a name="setting-the-debug-logging-level-at-run-time"></a>Festlegen der debugprotokollierungs Stufe zur Laufzeit

Sie können die Ebene der Debuginformationen, die von XAudio2 angezeigt werden, jederzeit festlegen, indem Sie eine [**XAudio2 \_ Debug- \_ Konfigurations**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_debug_configuration) Struktur mit den Flags für den gewünschten Protokolliergrad ausfüllen und die Struktur dann an die [**IXAudio2:: setdebugconfiguration**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-setdebugconfiguration) -Methode übergeben. Werte, die an die **IXAudio2:: setdebugconfiguration** -Methode übergeben werden, überschreiben immer alle Standardwerte, die in der Windows-Registrierung festgelegt wurden.

## <a name="debug-support"></a>Debugunterstützung

Die Debuggingfunktionen sind für XAUDIO2 in Windows 8 immer verfügbar.

Für die DirectX SDK-Versionen von XAUDIO2 müssen Sie die **XAUDIO2 \_ Debug- \_ Engine** verwenden, wenn Sie das XAUDIO2-Objekt mit [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) erstellen, und das System muss die DirectX SDK Developer Runtime installiert haben, damit das Debugging unterstützt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Debugging-Einrichtungen](debugging-facilities.md)
</dt> <dt>

[XAudio2-Programmierreferenz](programming-reference.md)
</dt> </dl>

 

 
