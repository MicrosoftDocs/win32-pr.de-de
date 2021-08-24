---
title: Abrufen einer Zeichenfolge, die einen Filter beschreibt
description: Abrufen einer Zeichenfolge, die einen Filter beschreibt
ms.assetid: 47390448-eaa6-4bea-bd90-549fa37e739a
keywords:
- Audiokomprimierungs-Manager (ACM), Abrufen von Zeichenfolgen, die Filter beschreiben
- ACM (Audiokomprimierungs-Manager),Abrufen von Zeichenfolgen, die Filter beschreiben
- ACM-Beispiele,Abrufen von Zeichenfolgen, die Filter beschreiben
- Abrufen von Zeichenfolgen, die Filter beschreiben
- acmFilterTagDetails-Funktion
- acmFilterDetails-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84bf182846da280f4810c84c75a02e76baaae9082ecaf2df8ea1797fd867e8b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689130"
---
# <a name="retrieving-a-string-that-describes-a-filter"></a>Abrufen einer Zeichenfolge, die einen Filter beschreibt

Eine Anwendung muss häufig eine Zeichenfolge anzeigen, die das aktuelle Format beschreibt. Diese Aufgabe kann problemlos mit den Funktionen [**acmFilterTagDetails**](/windows/desktop/api/Msacm/nf-msacm-acmfiltertagdetails) und [**acmFilterDetails**](/windows/desktop/api/Msacm/nf-msacm-acmfilterdetails) ausgeführt werden. Diese Funktionen müssen mit dem entsprechenden Filter- oder Filtertag aufgerufen werden. Im folgenden Beispiel wird gezeigt, wie diese Funktionen verwendet werden.


```C++
#include <mmsystem.h>
#include <mmreg.h>
#include <msacm.h>

BOOL GetFilterDescription 
( 
    LPWAVEFILTER  pwfltr, 
    LPTSTR        pszFilterTag, 
    DWORD         cchFilterTag, // Size of pszFilterTag buffer.
    LPTSTR        pszFilter,
    DWORD         cchFilter     // Size of pszFilter buffer.

) 
{ 
    MMRESULT      mmr; 
    errno_t       errno;
 
    // Retrieve the name for the filter tag of the specified filter. 
    if (NULL != pszFilterTag) { 
        ACMFILTERTAGDETAILS aftd; 
 
        // Initialize all unused members of the ACMFILTERTAGDETAILS 
        // structure to zero. 
        memset(&aftd, 0, sizeof(aftd)); 
 
        // Fill in the required members of the ACMFILTERTAGDETAILS 
        // structure for the ACM_FILTERTAGDETAILSF_FILTERTAG query. 
        aftd.cbStruct = sizeof(aftd); 
        aftd.dwFilterTag = pwfltr->dwFilterTag; 
 
        // Ask the ACM to find the first available driver that 
        // supports the specified filter tag. 
        mmr = acmFilterTagDetails(NULL, &aftd, 
            ACM_FILTERTAGDETAILSF_FILTERTAG); 
        if (MMSYSERR_NOERROR != mmr) { 
            // No ACM driver is available that supports the 
            // specified filter tag. 
            return FALSE; 
        } 
 
        // Copy the filter tag name into the calling application's 
        // buffer. 

        errno = wcscpy_s(pszFilterTag, cchFilterTag, aftd.szFilterTag); 
        if (errno != 0)
        {
            return FALSE;
        }
    } 
 
    // Retrieve the description of the attributes for the specified 
    // filter. 
    if (NULL != pszFilter) { 
        ACMFILTERDETAILS afd; 
 
        // Initialize all unused members of the ACMFILTERDETAILS 
        // structure to zero. 
        memset(&afd, 0, sizeof(afd)); 
 
        // Fill in the required members of the ACMFILTERDETAILS 
        // structure for the ACM_FILTERDETAILSF_FILTER query. 
        afd.cbStruct    = sizeof(afd); 
        afd.dwFilterTag = pwfltr->dwFilterTag; 
        afd.pwfltr      = pwfltr; 
        afd.cbwfltr     = pwfltr->cbStruct; 
 
        // Ask the ACM to find the first available driver that 
        // supports the specified filter. 
        mmr = acmFilterDetails(NULL, &afd, ACM_FILTERDETAILSF_FILTER); 
        if (MMSYSERR_NOERROR != mmr) { 
            // No ACM driver is available that supports the 
            // specified filter. 
            return FALSE; 
        } 
 
        // Copy the description string into the caller's buffer. 
        errno = wcscpy_s(pszFilter, cchFilter, afd.szFilter); 
        if (errno != 0)
        {
            return FALSE;
        }
    } 
 
    return TRUE; 
}
 
```



 

 




