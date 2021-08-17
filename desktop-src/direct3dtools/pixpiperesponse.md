---
description: Eine Enum, die zum Senden von Antworten von der Erfassungs-Engine an Grafikdiagnose.
MS-HAID: vspixengine.PixPipeResponse
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: PixPipeResponse-Enumeration
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5BFEE25D-3E03-493E-AFEF-DD8C70C53FC5
api_name:
- PixPipeResponse
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b28971a4a4011422fae5f37c11b4d8fc665cce7c0989842ab81dda027777c253
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119264"
---
# <a name="span-idvspixenginepixpiperesponsespanpixpiperesponse-enumeration"></a><span id="vspixengine.pixpiperesponse"></span>PixPipeResponse-Enumeration

Eine Enum, die zum Senden von Antworten von der Erfassungs-Engine an Grafikdiagnose.

## <a name="syntax"></a>Syntax


```C++
};
```

## <a name="constants"></a>Konstanten

<span id="NEW_DATA_AVAILABLE"></span><span id="new_data_available"></span>**NEUE \_ DATEN \_ VERFÜGBAR**  
Eine Antwort, die angibt, dass neue Daten in das Grafikprotokoll geschrieben wurden und gelesen werden können.

<span id="EXPERIMENT_DATA"></span><span id="experiment_data"></span>**\_EXPERIMENTDATEN**  
Eine Antwort, die Konfigurationsinformationen zur Erfassungssitzung angibt.

<span id="ERRORCODE"></span><span id="errorcode"></span>**Errorcode**  
Eine Antwort, die angibt, dass bei der Erfassungs-Engine ein Fehler aufgetreten ist.

<span id="APPLICATIONCAPTUREINPROGRESS"></span><span id="applicationcaptureinprogress"></span>**APPLICATIONCAPTUREINPROGRESS**  
Eine Antwort, die angibt, dass die Erfassungs-Engine mit dem Erfassen von Grafikinformationen begonnen hat. Dies deutet nicht darauf hin, dass daten noch untersucht werden können.

<span id="PARTIAL_DATA"></span><span id="partial_data"></span>**PARTIELLE \_ DATEN**  
Eine Antwort, die angibt, dass partielle Daten in das Grafikprotokoll geschrieben wurden.

<span id="READY"></span><span id="ready"></span>**Bereit**  
Eine Antwort, die angibt, dass die Erfassungs-Engine zum Erfassen von Grafikinformationen bereit ist.

<span id="DONE"></span><span id="done"></span>**fertig**  
Intern

<span id="CAPTURESTARTED"></span><span id="capturestarted"></span>**CAPTURESTARTED**  
Eine Antwort, die angibt, dass eine Frameerfassung gestartet wurde.

<span id="STATUS"></span><span id="status"></span>**Status**  
Eine Antwort, die Statusinformationen zur erfassten App angibt. Beispiel: Framerate.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



