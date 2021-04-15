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
# <a name="span-idvspixengineofflineanalysisstagespanofflineanalysisstage-enumeration"></a><span data-ttu-id="93129-103"><span id="vspixengine.offlineanalysisstage"></span>Offlineanalysisstage-Enumeration</span><span class="sxs-lookup"><span data-stu-id="93129-103"><span id="vspixengine.offlineanalysisstage"></span>OFFLINEANALYSISSTAGE enumeration</span></span>

<span data-ttu-id="93129-104">Eine Enumeration, mit der Phasen des Fortschritts in der Frame-Analyse angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="93129-104">An enum used to indicate stages of progress in frame analysis.</span></span>

## <a name="syntax"></a><span data-ttu-id="93129-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="93129-105">Syntax</span></span>


```C++
};
```

## <a name="constants"></a><span data-ttu-id="93129-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="93129-106">Constants</span></span>

<span data-ttu-id="93129-107"><span id="OfflineAnalysisStage_NotStarted"></span><span id="offlineanalysisstage_notstarted"></span><span id="OFFLINEANALYSISSTAGE_NOTSTARTED"></span>**Offlineanalysisstage \_ notstarted**</span><span class="sxs-lookup"><span data-stu-id="93129-107"><span id="OfflineAnalysisStage_NotStarted"></span><span id="offlineanalysisstage_notstarted"></span><span id="OFFLINEANALYSISSTAGE_NOTSTARTED"></span>**OfflineAnalysisStage\_NotStarted**</span></span>  
<span data-ttu-id="93129-108">Die Frame-Analyse wurde noch nicht gestartet.</span><span class="sxs-lookup"><span data-stu-id="93129-108">Frame analysis not yet started.</span></span>

<span data-ttu-id="93129-109"><span id="OfflineAnalysisStage_Initializing"></span><span id="offlineanalysisstage_initializing"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING"></span>**Offlineanalysisstage \_ initialisieren**</span><span class="sxs-lookup"><span data-stu-id="93129-109"><span id="OfflineAnalysisStage_Initializing"></span><span id="offlineanalysisstage_initializing"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING"></span>**OfflineAnalysisStage\_Initializing**</span></span>  
<span data-ttu-id="93129-110">Die Frame-Analyse wird initialisiert (Anforderung ausgegeben).</span><span class="sxs-lookup"><span data-stu-id="93129-110">Frame analysis initializing (request issued).</span></span>

<span data-ttu-id="93129-111"><span id="OfflineAnalysisStage_Initializing_LinkOk"></span><span id="offlineanalysisstage_initializing_linkok"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING_LINKOK"></span>**Offlineanalysisstage \_ Initialisieren von \_ linkok**</span><span class="sxs-lookup"><span data-stu-id="93129-111"><span id="OfflineAnalysisStage_Initializing_LinkOk"></span><span id="offlineanalysisstage_initializing_linkok"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING_LINKOK"></span>**OfflineAnalysisStage\_Initializing\_LinkOk**</span></span>  
<span data-ttu-id="93129-112">Die Frame-Analyse wird initialisiert (Link hergestellt).</span><span class="sxs-lookup"><span data-stu-id="93129-112">Frame analysis initializing (link established).</span></span>

<span data-ttu-id="93129-113"><span id="OfflineAnalysisStage_Initializing_ManifestOk"></span><span id="offlineanalysisstage_initializing_manifestok"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING_MANIFESTOK"></span>**Offlineanalysisstage \_ Initialisieren von \_ ManifestOk**</span><span class="sxs-lookup"><span data-stu-id="93129-113"><span id="OfflineAnalysisStage_Initializing_ManifestOk"></span><span id="offlineanalysisstage_initializing_manifestok"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING_MANIFESTOK"></span>**OfflineAnalysisStage\_Initializing\_ManifestOk**</span></span>  
<span data-ttu-id="93129-114">Die Frame-Analyse wird initialisiert (das Manifest wurde erfolgreich analysiert).</span><span class="sxs-lookup"><span data-stu-id="93129-114">Frame analysis initializing (manifest parsed successfully).</span></span>

<span data-ttu-id="93129-115"><span id="OfflineAnalysisStage_Initializing_ToolOk"></span><span id="offlineanalysisstage_initializing_toolok"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING_TOOLOK"></span>**Offlineanalysisstage \_ Initialisieren von " \_ deolok"**</span><span class="sxs-lookup"><span data-stu-id="93129-115"><span id="OfflineAnalysisStage_Initializing_ToolOk"></span><span id="offlineanalysisstage_initializing_toolok"></span><span id="OFFLINEANALYSISSTAGE_INITIALIZING_TOOLOK"></span>**OfflineAnalysisStage\_Initializing\_ToolOk**</span></span>  
<span data-ttu-id="93129-116">Die Frame-Analyse wird initialisiert (Analyseprogramm laden).</span><span class="sxs-lookup"><span data-stu-id="93129-116">Frame analysis initializing (analyzer loading).</span></span>

<span data-ttu-id="93129-117"><span id="OfflineAnalysisStage_Analyzing"></span><span id="offlineanalysisstage_analyzing"></span><span id="OFFLINEANALYSISSTAGE_ANALYZING"></span>**Offlineanalysisstage- \_ Analyse**</span><span class="sxs-lookup"><span data-stu-id="93129-117"><span id="OfflineAnalysisStage_Analyzing"></span><span id="offlineanalysisstage_analyzing"></span><span id="OFFLINEANALYSISSTAGE_ANALYZING"></span>**OfflineAnalysisStage\_Analyzing**</span></span>  
<span data-ttu-id="93129-118">Die Frame-Analyse wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="93129-118">Frame analysis is running.</span></span>

<span data-ttu-id="93129-119"><span id="OfflineAnalysisStage_AnalysisCompleted"></span><span id="offlineanalysisstage_analysiscompleted"></span><span id="OFFLINEANALYSISSTAGE_ANALYSISCOMPLETED"></span>**Offlineanalysisstage- \_ Analyse abgeschlossen**</span><span class="sxs-lookup"><span data-stu-id="93129-119"><span id="OfflineAnalysisStage_AnalysisCompleted"></span><span id="offlineanalysisstage_analysiscompleted"></span><span id="OFFLINEANALYSISSTAGE_ANALYSISCOMPLETED"></span>**OfflineAnalysisStage\_AnalysisCompleted**</span></span>  
<span data-ttu-id="93129-120">Die Frame-Analyse wurde abgeschlossen ("Complete"-Ereignis gesendet).</span><span class="sxs-lookup"><span data-stu-id="93129-120">Frame analysis completed ('complete' event sent).</span></span>

<span data-ttu-id="93129-121"><span id="OfflineAnalysisStage_AnalysisCompleted_Successful"></span><span id="offlineanalysisstage_analysiscompleted_successful"></span><span id="OFFLINEANALYSISSTAGE_ANALYSISCOMPLETED_SUCCESSFUL"></span>**Die offlineanalysisstage- \_ Analyse wurde \_ erfolgreich abgeschlossen.**</span><span class="sxs-lookup"><span data-stu-id="93129-121"><span id="OfflineAnalysisStage_AnalysisCompleted_Successful"></span><span id="offlineanalysisstage_analysiscompleted_successful"></span><span id="OFFLINEANALYSISSTAGE_ANALYSISCOMPLETED_SUCCESSFUL"></span>**OfflineAnalysisStage\_AnalysisCompleted\_Successful**</span></span>  
<span data-ttu-id="93129-122">Die Frame-Analyse wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="93129-122">Frame analysis completed successfully.</span></span>

<span data-ttu-id="93129-123"><span id="OfflineAnalysisStage_AnalysisCompleted_OutputFileExists"></span><span id="offlineanalysisstage_analysiscompleted_outputfileexists"></span><span id="OFFLINEANALYSISSTAGE_ANALYSISCOMPLETED_OUTPUTFILEEXISTS"></span>**Offlineanalysisstage \_ analysisabgeschlossene \_ outputfilevorhanden**</span><span class="sxs-lookup"><span data-stu-id="93129-123"><span id="OfflineAnalysisStage_AnalysisCompleted_OutputFileExists"></span><span id="offlineanalysisstage_analysiscompleted_outputfileexists"></span><span id="OFFLINEANALYSISSTAGE_ANALYSISCOMPLETED_OUTPUTFILEEXISTS"></span>**OfflineAnalysisStage\_AnalysisCompleted\_OutputFileExists**</span></span>  
<span data-ttu-id="93129-124">Frame-Analyse abgeschlossen und Ausgabedatei vorhanden.</span><span class="sxs-lookup"><span data-stu-id="93129-124">Frame analysis completed and output file exists.</span></span>

## <a name="requirements"></a><span data-ttu-id="93129-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="93129-125">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="93129-126">Header</span><span class="sxs-lookup"><span data-stu-id="93129-126">Header</span></span></p></td><td><span data-ttu-id="93129-127">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="93129-127">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



