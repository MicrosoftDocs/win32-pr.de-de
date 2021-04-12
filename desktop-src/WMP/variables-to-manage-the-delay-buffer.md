---
title: Variablen zum Verwalten des Verzögerungs Puffers
description: Variablen zum Verwalten des Verzögerungs Puffers
ms.assetid: 2c5963a1-04e2-4421-8f56-14c1e059de4e
keywords:
- Windows Media Player-Plug-ins, Echo Sample Streaming Resources
- Plug-ins, Echo Sample Streaming-Ressourcen
- Plug-Ins für die digitale Signalverarbeitung, Echo Sample Streaming-Ressourcen
- DSP-Plug-ins, Echo Sample Streaming-Ressourcen
- Echo DSP-Plug-in-Beispiel, Streamingressourcen
- Echo DSP-Plug-in-Beispiel, Verzögerungs Puffer
- Verzögerungs Puffer
- Puffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09d7f9657d16d0805ff2fc85d2238635fbfa6e5e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206925"
---
# <a name="variables-to-manage-the-delay-buffer"></a>Variablen zum Verwalten des Verzögerungs Puffers

Sie müssen die Deklarationen für die Element Variablen hinzufügen, die Sie zum Verwalten des Verzögerungs Puffers benötigen. Fügen Sie Echo. h im Abschnitt "private" die folgenden Deklarationen hinzu:


```C++
DWORD  m_cbDelayBuffer;   // Count of bytes in delay buffer size.
BYTE*  m_pbDelayPointer;  // Movable pointer to delay buffer.
BYTE*  m_pbDelayBuffer;   // Pointer to the head of the delay buffer.

```



Fügen Sie dem Cecho-Konstruktor den folgenden Code hinzu, um die Verzögerungs Puffer Variablen zu initialisieren:


```C++
m_pbDelayBuffer = NULL;
m_pbDelayPointer = NULL;
m_cbDelayBuffer = 0;

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Arbeiten mit Streamingressourcen**](working-with-streaming-resources.md)
</dt> </dl>

 

 




