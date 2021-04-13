---
title: Erstellen eines Dialog Felds zum Auswählen eines bestimmten Format Typs
description: Erstellen eines Dialog Felds zum Auswählen eines bestimmten Format Typs
ms.assetid: e454f9d6-5cbf-4e1b-937e-771cf1dd38ba
keywords:
- Audiokomprimierungs-Manager (ACM), Erstellen von Dialogfeldern
- ACM (Audiokomprimierungs-Manager), Erstellen von Dialogfeldern
- ACM-Beispiele, Erstellen von Dialogfeldern
- Erstellen von Dialogfeldern
- acmformatchoose-Funktion
- Audiokomprimierungs-Manager (ACM), auswählen von Format Typen
- ACM (Audiokomprimierungs-Manager), auswählen von Format Typen
- ACM-Beispiele, auswählen von Format Typen
- Auswählen von Format Typen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfc5d73d1b03f22923e6001d65898c05e2bd853e
ms.sourcegitcommit: cb844c9ab17577ce171fd7b03add668645867bc7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/27/2020
ms.locfileid: "104314434"
---
# <a name="producing-a-dialog-box-for-selecting-a-specific-type-of-format"></a>Erstellen eines Dialog Felds zum Auswählen eines bestimmten Format Typs

Möglicherweise möchten Sie, dass eine Anwendung es dem Benutzer ermöglicht, ein Format aus einer eingeschränkten Liste von Formaten in einem Dialogfeld auszuwählen. Einschränkungen können die Anzahl der Kanäle, die Samplingrate, das Waveform-Audioformat oder die Anzahl der Bits pro Stichprobe einschränken. In all diesen Fällen können Sie die Liste mithilfe der [**acmformatchoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) -Funktion generieren und die Member **fdwenum** und **pwfxenum** der [**acmformatchoose**](/windows/win32/api/msacm/ns-msacm-acmformatchoose) -Struktur festlegen. Dieser Prozess wird anhand des folgenden Beispiels veranschaulicht.


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



 

 




