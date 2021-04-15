---
description: Eine Enumeration, mit der Phasen des Fortschritts in der Frame-Analyse angegeben werden.
MS-HAID: vspixengine.OFFLINEANALYSISSTAGE
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Offlineanalysisstage-Enumeration
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
ms.openlocfilehash: bf12b70acf70a654fe74b23d4bd3a196467797fe
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521371"
---
# <a name="span-idvspixengineofflineanalysisstagespanofflineanalysisstage-enumeration"></a><span id="vspixengine.offlineanalysisstage"></span>Offlineanalysisstage-Enumeration

Eine Enumeration, mit der Phasen des Fortschritts in der Frame-Analyse angegeben werden.

## <a name="syntax"></a>Syntax


```C++
};
```

## <a name="constants"></a>Konstanten

<span id="OfflineAnalysisStage_NotStarted"></span><span id="offlineanalysisstage_notstarted"></span><span id="OFFLINEANALYSISSTAGE_NOTSTARTED"></span>**Offlineanalysisstage \_ notstarted**  
Die Frame-Analyse wurde noch nicht gestartet.

<span id="OfflineAnalysisStage_Initializing"></span><span id="offlineanalysisstage_initializing"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING"></span>**Offlineanalysisstage \_ initialisieren**  
Die Frame-Analyse wird initialisiert (Anforderung ausgegeben).

<span id="OfflineAnalysisStage_Initializing_LinkOk"></span><span id="offlineanalysisstage_initializing_linkok"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING_LINKOK"></span>**Offlineanalysisstage \_ Initialisieren von \_ linkok**  
Die Frame-Analyse wird initialisiert (Link hergestellt).

<span id="OfflineAnalysisStage_Initializing_ManifestOk"></span><span id="offlineanalysisstage_initializing_manifestok"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING_MANIFESTOK"></span>**Offlineanalysisstage \_ Initialisieren von \_ ManifestOk**  
Die Frame-Analyse wird initialisiert (das Manifest wurde erfolgreich analysiert).

<span id="OfflineAnalysisStage_Initializing_ToolOk"></span><span id="offlineanalysisstage_initializing_toolok"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING_TOOLOK"></span>**Offlineanalysisstage \_ Initialisieren von " \_ deolok"**  
Die Frame-Analyse wird initialisiert (Analyseprogramm laden).

<span id="OfflineAnalysisStage_Analyzing"></span><span id="offlineanalysisstage_analyzing"></span><span id="OFFLINEANALYSISSTAGE_ANALYZING"></span>**Offlineanalysisstage- \_ Analyse**  
Die Frame-Analyse wird ausgeführt.

<span id="OfflineAnalysisStage_AnalysisCompleted"></span><span id="offlineanalysisstage_analysiscompleted"></span><span id="OFFLINEANALYSISSTAGE_ANALYSISCOMPLETED"></span>**Offlineanalysisstage- \_ Analyse abgeschlossen**  
Die Frame-Analyse wurde abgeschlossen ("Complete"-Ereignis gesendet).

<span id="OfflineAnalysisStage_AnalysisCompleted_Successful"></span><span id="offlineanalysisstage_analysiscompleted_successful"></span><span id="OFFLINEANALYSISSTAGE_ANALYSISCOMPLETED_SUCCESSFUL"></span>**Die offlineanalysisstage- \_ Analyse wurde \_ erfolgreich abgeschlossen.**  
Die Frame-Analyse wurde erfolgreich abgeschlossen.

<span id="OfflineAnalysisStage_AnalysisCompleted_OutputFileExists"></span><span id="offlineanalysisstage_analysiscompleted_outputfileexists"></span><span id="OFFLINEANALYSISSTAGE_ANALYSISCOMPLETED_OUTPUTFILEEXISTS"></span>**Offlineanalysisstage \_ analysisabgeschlossene \_ outputfilevorhanden**  
Frame-Analyse abgeschlossen und Ausgabedatei vorhanden.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



