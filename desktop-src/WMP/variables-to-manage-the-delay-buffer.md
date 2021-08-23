---
title: Variablen zum Verwalten des Verzögerungspuffers
description: Variablen zum Verwalten des Verzögerungspuffers
ms.assetid: 2c5963a1-04e2-4421-8f56-14c1e059de4e
keywords:
- Windows Media Player-Plug-Ins, Echo-Beispielstreamingressourcen
- Plug-Ins, Echo-Beispielstreamingressourcen
- Digitale Signalverarbeitungs-Plug-Ins, Echo-Beispielstreamingressourcen
- DSP-Plug-Ins, Echo-Beispielstreamingressourcen
- Echo-DSP-Plug-In-Beispiel, Streamingressourcen
- Echo-DSP-Plug-In-Beispiel, Verzögerungspuffer
- Verzögerungspuffer
- Puffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be71bc7f2ded34dcd5f29bc10ce01796b6498d36a9a194a48b0bfdec0e14662
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571740"
---
# <a name="variables-to-manage-the-delay-buffer"></a>Variablen zum Verwalten des Verzögerungspuffers

Sie müssen die Deklarationen für die Membervariablen hinzufügen, die Sie zum Verwalten des Verzögerungspuffers benötigen. Fügen Sie echo.h im Abschnitt "private" die folgenden Deklarationen hinzu:


```C++
DWORD  m_cbDelayBuffer;   // Count of bytes in delay buffer size.
BYTE*  m_pbDelayPointer;  // Movable pointer to delay buffer.
BYTE*  m_pbDelayBuffer;   // Pointer to the head of the delay buffer.

```



Fügen Sie dem CEcho-Konstruktor den folgenden Code hinzu, um die Verzögerungspuffervariablen zu initialisieren:


```C++
m_pbDelayBuffer = NULL;
m_pbDelayPointer = NULL;
m_cbDelayBuffer = 0;

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Arbeiten mit Streamingressourcen**](working-with-streaming-resources.md)
</dt> </dl>

 

 




