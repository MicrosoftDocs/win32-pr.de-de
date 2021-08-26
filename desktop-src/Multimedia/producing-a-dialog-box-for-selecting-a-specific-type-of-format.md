---
title: Erstellen eines Dialogfelds zum Auswählen eines bestimmten Formattyps
description: Erstellen eines Dialogfelds zum Auswählen eines bestimmten Formattyps
ms.assetid: e454f9d6-5cbf-4e1b-937e-771cf1dd38ba
keywords:
- Audiokomprimierungs-Manager (ACM), Erstellen von Dialogfeldern
- ACM (Audiokomprimierungs-Manager),Erstellen von Dialogfeldern
- ACM-Beispiele, Erstellen von Dialogfeldern
- Erstellen von Dialogfeldern
- acmFormatChoose-Funktion
- Audiokomprimierungs-Manager (ACM), Auswählen von Formattypen
- ACM (Audiokomprimierungs-Manager),Auswählen von Formattypen
- ACM-Beispiele, Auswählen von Formattypen
- Auswählen von Formattypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f25f7b196fcb9462a3b61dd8e351ed75276c7df7bf46cec233dd8eac7deda5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037650"
---
# <a name="producing-a-dialog-box-for-selecting-a-specific-type-of-format"></a>Erstellen eines Dialogfelds zum Auswählen eines bestimmten Formattyps

Möglicherweise möchten Sie, dass eine Anwendung dem Benutzer ermöglicht, ein Format aus einer eingeschränkten Liste von Formaten in einem Dialogfeld auszuwählen. Einschränkungen können die Anzahl der Kanäle, die Samplingrate, das Formattag waveform-audio oder die Anzahl der Bits pro Stichprobe einschränken. In all diesen Fällen können Sie die Liste mithilfe der Funktion [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) generieren und die Member **fdwEnum** und **pwfxEnum** der [**ACMFORMATCHOOSE-Struktur**](/windows/win32/api/msacm/ns-msacm-acmformatchoose) festlegen. Dieser Prozess wird anhand des folgenden Beispiels veranschaulicht.


```C++
MMRESULT            mmr; 
ACMFORMATCHOOSE     afc; 
WAVEFORMATEX        wfxSelection; 
WAVEFORMATEX        wfxEnum; 
 
// Initialize the ACMFORMATCHOOSE members. 
memset(&afc, 0, sizeof(afc)); 
 
afc.cbStruct    = sizeof(afc); 
afc.fdwStyle    = 0L;               // no special style flags 
afc.hwndOwner   = hwnd;             // hwnd of parent window 
afc.pwfx        = &wfxSelection;    // wfx to receive selection 
afc.cbwfx       = sizeof(wfxSelection); 
afc.pszTitle    = TEXT("16 Bit PCM Selection"); 
 
//  Request that all 16-bit PCM formats be displayed for the user 
//  to select from. 
memset(&wfxEnum, 0, sizeof(wfxEnum)); 
wfxEnum.wFormatTag = WAVE_FORMAT_PCM; 
wfxEnum.wBitsPerSample = 16; 
afc.fdwEnum = ACM_FORMATENUMF_WFORMATTAG | 
    ACM_FORMATENUMF_WBITSPERSAMPLE; 
afc.pwfxEnum = &wfxEnum; 
mmr = acmFormatChoose(&afc); 
if ((MMSYSERR_NOERROR != mmr) && (ACMERR_CANCELED != mmr)) 
{ 
    // There was a fatal error in bringing up the list 
    // dialog box (probably invalid input parameters). 
} 
 
```



 

 




