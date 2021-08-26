---
title: Informationen zu VERFORMTransform
description: Informationen zu VERFORMTransform
ms.assetid: 889f2d82-148a-4a7e-b78c-37ec86b37e0b
keywords:
- Windows Media Player-Plug-Ins,Schnittstellen
- Plug-Ins, Schnittstellen
- Plug-Ins für die digitale Signalverarbeitung, Schnittstellen
- DSP-Plug-Ins, Schnittstellen
- Schnittstellen,DSP-Plug-Ins
- Windows Media Player-Plug-Ins, EINETRANSFORM-Schnittstelle
- Plug-Ins, EINETRANSFORM-Schnittstelle
- Plug-Ins für die digitale Signalverarbeitung, EINETRANSFORM-Schnittstelle
- DSP-Plug-Ins, EINETRANSFORM-Schnittstelle
- BENUTZEROBERFLÄCHETransform-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3b410702d63657261faa2fc8e7db123e05dcdc12c3096a49f8c0e2e36a41ff4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903580"
---
# <a name="about-imftransform"></a>Informationen zu VERFORMTransform

Die **BENUTZEROBERFLÄCHETransform-Schnittstelle** ist eine der Schnittstellen, die von einem DSP-Plug-In im Dualmodus implementiert werden müssen. Windows Media Player ruft die Methoden der -SCHNITTSTELLE VON 10002222277666666666666666666666666666666666666666666666666666666666666666666666666666666  Die vollständige Dokumentation der **BENUTZEROBERFLÄCHETransform-Schnittstelle** finden Sie im Media Foundation abschnitt des Windows SDK.

Die Methoden von **CATEGORIZETransform** können wie folgt kategorisiert werden.

## <a name="methods-that-handle-format-negotiation"></a>Methoden zur Behandlung der Formataushandlung

Windows Media Player die folgenden Methoden auf, um Informationen zu den vom Plug-In unterstützten Datenformaten zu erhalten.

-   **GetStreamCount**
-   **GetStreamLimits**
-   **GetInputStreamInfo**
-   **GetOutputStreamInfo**
-   **GetInputAvailableType**
-   **GetOutputAvailableType**
-   **SetInputType**
-   **SetOutputType**
-   **Getattributes**
-   **GetInputStreamAttributes**
-   **GetOutputStreamAttributes**
-   **GetStreamIDs**

## <a name="methods-that-specify-or-retrieve-state-information"></a>Methoden, die Zustandsinformationen angeben oder abrufen

Windows Media Player ruft die folgenden Methoden auf, um Werte im Zusammenhang mit dem aktuellen Zustand des Plug-Ins zu erhalten oder zu festlegen.

-   **SetInputType**
-   **SetOutputType**
-   **GetInputCurrentType**
-   **GetOutputCurrentType**
-   **GetInputStatus**
-   **AddInputStreams**
-   **DeleteInputStreams**
-   **GetOutputStatus**
-   **SetOutputBounds**

> [!Note]  
> **SetInputType und** **SetOutputType** werden sowohl für die Formataushandlung als auch zum Angeben und Abrufen von Zustandsinformationen verwendet.

 

## <a name="methods-that-handle-buffering-and-processing-data"></a>Methoden zum Verarbeiten von Pufferung und Verarbeitung von Daten

Windows Media Player die folgenden Methoden auf, um die verschiedenen Prozesse zu initiieren, die das Plug-In für die Verarbeitung digitaler Signale ausführt.

-   **ProcessInput**
-   **ProcessOutput**
-   **ProcessMessage**
-   **ProcessEvent**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erforderliche Schnittstellen**](required-interfaces.md)
</dt> </dl>

 

 




