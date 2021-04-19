---
title: Informationen über IMF Transform
description: Informationen über IMF Transform
ms.assetid: 889f2d82-148a-4a7e-b78c-37ec86b37e0b
keywords:
- Windows Media Player-Plug-ins, Schnittstellen
- Plug-ins, Schnittstellen
- Plug-Ins für die digitale Signalverarbeitung, Schnittstellen
- DSP-Plug-ins, Schnittstellen
- Schnittstellen, DSP-Plug-ins
- Windows Media Player-Plug-ins, IMF Transform-Schnittstelle
- Plug-ins, IMF Transform-Schnittstelle
- Plug-Ins für die digitale Signalverarbeitung, IMF Transform-Schnittstelle
- DSP-Plug-ins, IMF Transform-Schnittstelle
- IMF Transform-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eb58ab84070a8cb9390e4525b9b642f15a29f14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341836"
---
# <a name="about-imftransform"></a>Informationen über IMF Transform

Die **IMF Transform** -Schnittstelle ist eine der Schnittstellen, die von einem DSP-Plug-in mit zwei Modi implementiert werden müssen. Windows Media Player Ruft die Methoden der **imftransform** -Schnittstelle auf, um Daten für das Plug-in bereitzustellen und verarbeitete Daten vom Plug-in abzurufen. Eine umfassende Dokumentation der **IMF Transform** -Schnittstelle finden Sie im Abschnitt Media Foundation des Windows SDK.

Die Methoden von **IMF Transform** können wie folgt kategorisiert werden.

## <a name="methods-that-handle-format-negotiation"></a>Methoden, die die Format Aushandlung behandeln

Windows Media Player Ruft die folgenden Methoden auf, um Informationen zu den vom Plug-in unterstützten Datenformaten zu erhalten.

-   **Getstreamcount**
-   **Getstreamlimits**
-   **Getinputstreaminfo**
-   **Getoutputstreaminfo**
-   **Getinputavailabletype**
-   **Getoutputavailabletype**
-   **"Ttinputtype"**
-   **Setoutputtype**
-   **GetAttributes**
-   **Getinputstreamattribute**
-   **Getoutputstreamattribute**
-   **Getstreamids**

## <a name="methods-that-specify-or-retrieve-state-information"></a>Methoden zum angeben oder Abrufen von Zustandsinformationen

Windows Media Player Ruft die folgenden Methoden auf, um Werte zu erhalten, die sich auf den aktuellen Status des Plug-ins beziehen, oder legt diese fest.

-   **"Ttinputtype"**
-   **Setoutputtype**
-   **Getinputcurrenttype**
-   **Getoutputcurrenttype**
-   **Getinputstatus**
-   **Addinputstreams**
-   **Delta Input Streams**
-   **Getoutputstatus**
-   **Setoutputbounds**

> [!Note]  
> **Setinputtype** und **setoutputtype** werden sowohl für die Format Aushandlung als auch für das angeben und Abrufen von Zustandsinformationen verwendet.

 

## <a name="methods-that-handle-buffering-and-processing-data"></a>Methoden, die die Pufferung und Verarbeitung von Daten verarbeiten

Windows Media Player Ruft die folgenden Methoden auf, um die verschiedenen Prozesse zu initiieren, die das Plug-in für die digitale Signalverarbeitung durchführt.

-   **ProcessInput**
-   **ProcessOutput**
-   **ProcessMessage**
-   **ProcessEvent**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erforderliche Schnittstellen**](required-interfaces.md)
</dt> </dl>

 

 




