---
description: Führt ein Experiment aus.
MS-HAID: vspixengine.IPixEngine\_RunExperiment\_Experiment\_IRunExperimentCallback\_ptr\_INewFramesCallback\_ptr\_IFileIOCallback\_ptr\_DWORD\_ExperimentTrigger\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Ipixengine:: runexperiment-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: A2EEC278-C074-44B3-94DC-E2D9DC770576
api_name:
- IPixEngine.RunExperiment
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c656d57dda496b6c1d8c128dc5e832ec40ef13f7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124333"
---
# <a name="span-idvspixengineipixengine_runexperiment_experiment_irunexperimentcallback_ptr_inewframescallback_ptr_ifileiocallback_ptr_dword_experimenttrigger_arrspanipixenginerunexperiment-method"></a><span data-ttu-id="8a076-103"><span id="vspixengine.ipixengine_runexperiment_experiment_irunexperimentcallback_ptr_inewframescallback_ptr_ifileiocallback_ptr_dword_experimenttrigger_arr"></span>Ipixengine:: runexperiment-Methode</span><span class="sxs-lookup"><span data-stu-id="8a076-103"><span id="vspixengine.ipixengine_runexperiment_experiment_irunexperimentcallback_ptr_inewframescallback_ptr_ifileiocallback_ptr_dword_experimenttrigger_arr"></span>IPixEngine::RunExperiment method</span></span>

<span data-ttu-id="8a076-104">Führt ein Experiment aus.</span><span class="sxs-lookup"><span data-stu-id="8a076-104">Runs an experiment.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a076-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a076-105">Syntax</span></span>


```C++
HRESULT RunExperiment(
   Experiment               experiment,
   IRunExperimentCallback * pRequestCallback,
   INewFramesCallback*      callbacks,
   IFileIOCallback*         pFileIOCallback,
   DWORD                    triggersCount,
   ExperimentTrigger []     count4_triggersBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="8a076-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a076-106">Parameters</span></span>

<span data-ttu-id="8a076-107">*Experiments* </span><span class="sxs-lookup"><span data-stu-id="8a076-107">*experiment* </span></span>  
<span data-ttu-id="8a076-108">Beschreibt das auszutestende Experiment.</span><span class="sxs-lookup"><span data-stu-id="8a076-108">Describes the experiment to be run.</span></span>

<span data-ttu-id="8a076-109">*prequestcallback* </span><span class="sxs-lookup"><span data-stu-id="8a076-109">*pRequestCallback* </span></span>  
<span data-ttu-id="8a076-110">Die Adresse einer Funktion, die verwendet wird, um den Host zu benachrichtigen, dass die Engine das Experiment gestartet hat.</span><span class="sxs-lookup"><span data-stu-id="8a076-110">The address of a function used to notify the host that engine has started the experiment.</span></span>

<span data-ttu-id="8a076-111">*Rückrufe* </span><span class="sxs-lookup"><span data-stu-id="8a076-111">*callbacks* </span></span>  
<span data-ttu-id="8a076-112">Die Adresse einer Funktion, die verwendet wird, um den Host zu benachrichtigen, dass neue Frames aufgezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="8a076-112">The address of a function used to notify the host that new frames have been captured.</span></span>

<span data-ttu-id="8a076-113">*pfileiocallback* </span><span class="sxs-lookup"><span data-stu-id="8a076-113">*pFileIOCallback* </span></span>  
<span data-ttu-id="8a076-114">Die Adresse einer Funktion, die verwendet wird, um den Host von Datei-e/a-Fehlern beim Parsen zu Benachrichtigen</span><span class="sxs-lookup"><span data-stu-id="8a076-114">The address of a function used to notify the host of file IO errors during parsing.</span></span>

<span data-ttu-id="8a076-115">*Triggers count* </span><span class="sxs-lookup"><span data-stu-id="8a076-115">*triggersCount* </span></span>  
<span data-ttu-id="8a076-116">Die Anzahl der Trigger im Experiment.</span><span class="sxs-lookup"><span data-stu-id="8a076-116">The number of triggers in the experiment.</span></span>

<span data-ttu-id="8a076-117">*count4 \_ triggersbuffer* </span><span class="sxs-lookup"><span data-stu-id="8a076-117">*count4\_triggersBuffer* </span></span>  
<span data-ttu-id="8a076-118">Erfassungs Trigger.</span><span class="sxs-lookup"><span data-stu-id="8a076-118">Capture triggers.</span></span>

## <a name="return-value"></a><span data-ttu-id="8a076-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8a076-119">Return value</span></span>

<span data-ttu-id="8a076-120">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="8a076-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8a076-121">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8a076-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a076-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8a076-122">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="8a076-123">Header</span><span class="sxs-lookup"><span data-stu-id="8a076-123">Header</span></span></p></td><td><span data-ttu-id="8a076-124">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="8a076-124">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="8a076-125"><span id="see_also"></span>Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8a076-125"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="8a076-126">**Ipixengine**</span><span class="sxs-lookup"><span data-stu-id="8a076-126">**IPixEngine**</span></span>](/windows/desktop/direct3dtools/ipixengine)

 

 
