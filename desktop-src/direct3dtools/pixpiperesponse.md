---
description: Eine Enumeration, die zum Senden von Antworten von der Erfassungs-Engine an Grafikdiagnose verwendet wird.
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
ms.openlocfilehash: ad00d7bada935dd27f711499e5975d31709b9940
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122631688"
---
# <a name="span-idvspixenginepixpiperesponsespanpixpiperesponse-enumeration"></a><span id="vspixengine.pixpiperesponse"></span>PixPipeResponse-Enumeration

Eine Enumeration, die zum Senden von Antworten von der Erfassungs-Engine an Grafikdiagnose verwendet wird.

## <a name="syntax"></a>Syntax


```C++
};
```

## <a name="constants"></a>Konstanten

<span id="NEW_DATA_AVAILABLE"></span><span id="new_data_available"></span>**NEUE \_ \_ VERFÜGBARE DATEN**  
Eine Antwort, die angibt, dass neue Daten in das Grafikprotokoll geschrieben wurden und zum Lesen bereit sind.

<span id="EXPERIMENT_DATA"></span><span id="experiment_data"></span>**\_EXPERIMENTDATEN**  
Eine Antwort, die Konfigurationsinformationen zur Aufzeichnungssitzung angibt.

<span id="ERRORCODE"></span><span id="errorcode"></span>**ERRORCODE**  
Eine Antwort, die angibt, dass bei der Erfassungs-Engine ein Fehler aufgetreten ist.

<span id="APPLICATIONCAPTUREINPROGRESS"></span><span id="applicationcaptureinprogress"></span>**APPLICATIONCAPTUREINPROGRESS**  
Eine Antwort, die angibt, dass die Erfassungs-Engine mit der Erfassung von Grafikinformationen begonnen hat. Dies gibt nicht an, dass die Daten noch untersucht werden können.

<span id="PARTIAL_DATA"></span><span id="partial_data"></span>**PARTIELLE \_ DATEN**  
Eine Antwort, die angibt, dass Teildaten in das Grafikprotokoll geschrieben wurden.

<span id="READY"></span><span id="ready"></span>**BEREIT**  
Eine Antwort, die angibt, dass die Erfassungs-Engine bereit ist, mit der Erfassung von Grafikinformationen zu beginnen.

<span id="DONE"></span><span id="done"></span>**FERTIG**  
Intern

<span id="CAPTURESTARTED"></span><span id="capturestarted"></span>**CAPTURESTARTED**  
Eine Antwort, die angibt, dass eine Frameerfassung gestartet wurde.

<span id="STATUS"></span><span id="status"></span>**STATUS**  
Eine Antwort, die Statusinformationen zur erfassten App angibt. z. B. Framerate.

## <a name="requirements"></a>Requirements (Anforderungen)

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



