---
description: Eine Enumeration, mit der Antworten von der Aufzeichnungs-Engine an Grafikdiagnose gesendet werden.
MS-HAID: vspixengine.PixPipeResponse
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Pixpiperesponse-Enumeration
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
ms.openlocfilehash: 09ab253be5e02cc7329195016a406758b7a82e2b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106340078"
---
# <a name="span-idvspixenginepixpiperesponsespanpixpiperesponse-enumeration"></a><span id="vspixengine.pixpiperesponse"></span>Pixpiperesponse-Enumeration

Eine Enumeration, mit der Antworten von der Aufzeichnungs-Engine an Grafikdiagnose gesendet werden.

## <a name="syntax"></a>Syntax


```C++
};
```

## <a name="constants"></a>Konstanten

<span id="NEW_DATA_AVAILABLE"></span><span id="new_data_available"></span>**neue \_ Daten \_ verfügbar**  
Eine Antwort, die angibt, dass neue Daten in das Grafik Protokoll geschrieben wurden und für den Lesevorgang bereit sind.

<span id="EXPERIMENT_DATA"></span><span id="experiment_data"></span>**Experiment \_ Daten**  
Eine Antwort, die Konfigurationsinformationen über die Aufzeichnungs Sitzung angibt.

<span id="ERRORCODE"></span><span id="errorcode"></span>**ERRORCODE**  
Eine Antwort, die angibt, dass bei der Aufzeichnungs-Engine ein Fehler aufgetreten ist.

<span id="APPLICATIONCAPTUREINPROGRESS"></span><span id="applicationcaptureinprogress"></span>**Applicationcaptureinprogress**  
Eine Antwort, die angibt, dass die Aufzeichnungs-Engine mit dem Erfassen von Grafik Informationen begonnen hat. Dies deutet nicht darauf hin, dass Daten noch untersucht werden können.

<span id="PARTIAL_DATA"></span><span id="partial_data"></span>**partielle \_ Daten**  
Eine Antwort, die angibt, dass partielle Daten in das Grafik Protokoll geschrieben wurden.

<span id="READY"></span><span id="ready"></span>**Vorgefertigten**  
Eine Antwort, die angibt, dass die Aufzeichnungs-Engine bereit ist, mit der Erfassung von Grafik Informationen zu beginnen.

<span id="DONE"></span><span id="done"></span>**Ausgeführt**  
Intern

<span id="CAPTURESTARTED"></span><span id="capturestarted"></span>**Capturestarted**  
Eine Antwort, die angibt, dass eine Frame-Erfassung gestartet wurde.

<span id="STATUS"></span><span id="status"></span>**Stands**  
Eine Antwort, die Statusinformationen zur erfassten App angibt. Beispiel: Framerate.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



