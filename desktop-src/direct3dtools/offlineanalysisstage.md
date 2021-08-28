---
description: Eine Enumeration, die verwendet wird, um Phasen des Fortschritts in der Frameanalyse anzugeben.
MS-HAID: vspixengine.OFFLINEANALYSISSTAGE
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: OFFLINEANALYSISSTAGE-Enumeration
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 85D0288C-113A-4ABE-8EDB-ABB8F009956A
api_name:
- OFFLINEANALYSISSTAGE
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: da78be36b9999d6c082b3c683dfd7e0e5ae18ef5
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627986"
---
# <a name="span-idvspixengineofflineanalysisstagespanofflineanalysisstage-enumeration"></a><span id="vspixengine.offlineanalysisstage"></span>OFFLINEANALYSISSTAGE-Enumeration

Eine Enumeration, die verwendet wird, um Phasen des Fortschritts in der Frameanalyse anzugeben.

## <a name="syntax"></a>Syntax


```C++
};
```

## <a name="constants"></a>Konstanten

<span id="OfflineAnalysisStage_NotStarted"></span><span id="offlineanalysisstage_notstarted"></span><span id="OFFLINEANALYSISSTAGE_NOTSTARTED"></span>**OfflineAnalysisStage \_ NotStarted**  
Die Frameanalyse wurde noch nicht gestartet.

<span id="OfflineAnalysisStage_Initializing"></span><span id="offlineanalysisstage_initializing"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING"></span>**OfflineAnalysisStage-Initialisierung \_**  
Initialisierung der Frameanalyse (Anforderung ausgestellt).

<span id="OfflineAnalysisStage_Initializing_LinkOk"></span><span id="offlineanalysisstage_initializing_linkok"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING_LINKOK"></span>**OfflineAnalysisStage \_ Initializing \_ LinkOk**  
Initialisierung der Frameanalyse (Link eingerichtet).

<span id="OfflineAnalysisStage_Initializing_ManifestOk"></span><span id="offlineanalysisstage_initializing_manifestok"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING_MANIFESTOK"></span>**OfflineAnalysisStage \_ Initializing \_ ManifestOk**  
Initialisierung der Frameanalyse (Manifest erfolgreich analysiert).

<span id="OfflineAnalysisStage_Initializing_ToolOk"></span><span id="offlineanalysisstage_initializing_toolok"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING_TOOLOK"></span>**\_OfflineAnalysisStage-InitialisierungstoolOk \_**  
Initialisierung der Frameanalyse (Laden des Analysetools).

<span id="OfflineAnalysisStage_Analyzing"></span><span id="offlineanalysisstage_analyzing"></span><span id="OFFLINEANALYSISSTAGE_ANALYZING"></span>**OfflineAnalysisStage-Analyse \_**  
Die Frameanalyse wird ausgeführt.

<span id="OfflineAnalysisStage_AnalysisCompleted"></span><span id="offlineanalysisstage_analysiscompleted"></span><span id="OFFLINEANALYSISSTAGE_ANALYSISCOMPLETED"></span>**OfflineAnalysisStage \_ AnalysisCompleted**  
Frameanalyse abgeschlossen ("Complete"-Ereignis gesendet).

<span id="OfflineAnalysisStage_AnalysisCompleted_Successful"></span><span id="offlineanalysisstage_analysiscompleted_successful"></span><span id="OFFLINEANALYSISSTAGE_ANALYSISCOMPLETED_SUCCESSFUL"></span>**OfflineAnalysisStage \_ AnalysisCompleted \_ Successful**  
Die Frameanalyse wurde erfolgreich abgeschlossen.

<span id="OfflineAnalysisStage_AnalysisCompleted_OutputFileExists"></span><span id="offlineanalysisstage_analysiscompleted_outputfileexists"></span><span id="OFFLINEANALYSISSTAGE_ANALYSISCOMPLETED_OUTPUTFILEEXISTS"></span>**OfflineAnalysisStage \_ AnalysisCompleted \_ OutputFileExists**  
Die Frameanalyse wurde abgeschlossen, und die Ausgabedatei ist vorhanden.

## <a name="requirements"></a>Requirements (Anforderungen)

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



