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
# <a name="span-idvspixenginepixpiperesponsespanpixpiperesponse-enumeration"></a><span data-ttu-id="9afe9-103"><span id="vspixengine.pixpiperesponse"></span>Pixpiperesponse-Enumeration</span><span class="sxs-lookup"><span data-stu-id="9afe9-103"><span id="vspixengine.pixpiperesponse"></span>PixPipeResponse enumeration</span></span>

<span data-ttu-id="9afe9-104">Eine Enumeration, mit der Antworten von der Aufzeichnungs-Engine an Grafikdiagnose gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="9afe9-104">An enum used to send responses from the capture engine to Graphics Diagnostics.</span></span>

## <a name="syntax"></a><span data-ttu-id="9afe9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9afe9-105">Syntax</span></span>


```C++
};
```

## <a name="constants"></a><span data-ttu-id="9afe9-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="9afe9-106">Constants</span></span>

<span data-ttu-id="9afe9-107"><span id="NEW_DATA_AVAILABLE"></span><span id="new_data_available"></span>**neue \_ Daten \_ verfügbar**</span><span class="sxs-lookup"><span data-stu-id="9afe9-107"><span id="NEW_DATA_AVAILABLE"></span><span id="new_data_available"></span>**NEW\_DATA\_AVAILABLE**</span></span>  
<span data-ttu-id="9afe9-108">Eine Antwort, die angibt, dass neue Daten in das Grafik Protokoll geschrieben wurden und für den Lesevorgang bereit sind.</span><span class="sxs-lookup"><span data-stu-id="9afe9-108">A response which indicates that new data has been written to the graphics log and is ready to be read.</span></span>

<span data-ttu-id="9afe9-109"><span id="EXPERIMENT_DATA"></span><span id="experiment_data"></span>**Experiment \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="9afe9-109"><span id="EXPERIMENT_DATA"></span><span id="experiment_data"></span>**EXPERIMENT\_DATA**</span></span>  
<span data-ttu-id="9afe9-110">Eine Antwort, die Konfigurationsinformationen über die Aufzeichnungs Sitzung angibt.</span><span class="sxs-lookup"><span data-stu-id="9afe9-110">A response which indicates configuration information about the capture session.</span></span>

<span data-ttu-id="9afe9-111"><span id="ERRORCODE"></span><span id="errorcode"></span>**ERRORCODE**</span><span class="sxs-lookup"><span data-stu-id="9afe9-111"><span id="ERRORCODE"></span><span id="errorcode"></span>**ERRORCODE**</span></span>  
<span data-ttu-id="9afe9-112">Eine Antwort, die angibt, dass bei der Aufzeichnungs-Engine ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="9afe9-112">A response which indicates that the capture engine has encountered an error.</span></span>

<span data-ttu-id="9afe9-113"><span id="APPLICATIONCAPTUREINPROGRESS"></span><span id="applicationcaptureinprogress"></span>**Applicationcaptureinprogress**</span><span class="sxs-lookup"><span data-stu-id="9afe9-113"><span id="APPLICATIONCAPTUREINPROGRESS"></span><span id="applicationcaptureinprogress"></span>**APPLICATIONCAPTUREINPROGRESS**</span></span>  
<span data-ttu-id="9afe9-114">Eine Antwort, die angibt, dass die Aufzeichnungs-Engine mit dem Erfassen von Grafik Informationen begonnen hat.</span><span class="sxs-lookup"><span data-stu-id="9afe9-114">A response which indicates that the capture engine has started capturing graphics information.</span></span> <span data-ttu-id="9afe9-115">Dies deutet nicht darauf hin, dass Daten noch untersucht werden können.</span><span class="sxs-lookup"><span data-stu-id="9afe9-115">This does not indicate that data is available to be examined yet.</span></span>

<span data-ttu-id="9afe9-116"><span id="PARTIAL_DATA"></span><span id="partial_data"></span>**partielle \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="9afe9-116"><span id="PARTIAL_DATA"></span><span id="partial_data"></span>**PARTIAL\_DATA**</span></span>  
<span data-ttu-id="9afe9-117">Eine Antwort, die angibt, dass partielle Daten in das Grafik Protokoll geschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="9afe9-117">A response which indicates that partial data has been written to the graphics log.</span></span>

<span data-ttu-id="9afe9-118"><span id="READY"></span><span id="ready"></span>**Vorgefertigten**</span><span class="sxs-lookup"><span data-stu-id="9afe9-118"><span id="READY"></span><span id="ready"></span>**READY**</span></span>  
<span data-ttu-id="9afe9-119">Eine Antwort, die angibt, dass die Aufzeichnungs-Engine bereit ist, mit der Erfassung von Grafik Informationen zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="9afe9-119">A response which indicates that the capture engine is ready to start capturing graphics information.</span></span>

<span data-ttu-id="9afe9-120"><span id="DONE"></span><span id="done"></span>**Ausgeführt**</span><span class="sxs-lookup"><span data-stu-id="9afe9-120"><span id="DONE"></span><span id="done"></span>**DONE**</span></span>  
<span data-ttu-id="9afe9-121">Intern</span><span class="sxs-lookup"><span data-stu-id="9afe9-121">Internal</span></span>

<span data-ttu-id="9afe9-122"><span id="CAPTURESTARTED"></span><span id="capturestarted"></span>**Capturestarted**</span><span class="sxs-lookup"><span data-stu-id="9afe9-122"><span id="CAPTURESTARTED"></span><span id="capturestarted"></span>**CAPTURESTARTED**</span></span>  
<span data-ttu-id="9afe9-123">Eine Antwort, die angibt, dass eine Frame-Erfassung gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="9afe9-123">A response which indicates that a frame capture has started.</span></span>

<span data-ttu-id="9afe9-124"><span id="STATUS"></span><span id="status"></span>**Stands**</span><span class="sxs-lookup"><span data-stu-id="9afe9-124"><span id="STATUS"></span><span id="status"></span>**STATUS**</span></span>  
<span data-ttu-id="9afe9-125">Eine Antwort, die Statusinformationen zur erfassten App angibt. Beispiel: Framerate.</span><span class="sxs-lookup"><span data-stu-id="9afe9-125">A response which indicates status information about the app being captured; for example, framerate.</span></span>

## <a name="requirements"></a><span data-ttu-id="9afe9-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9afe9-126">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="9afe9-127">Header</span><span class="sxs-lookup"><span data-stu-id="9afe9-127">Header</span></span></p></td><td><span data-ttu-id="9afe9-128">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="9afe9-128">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



