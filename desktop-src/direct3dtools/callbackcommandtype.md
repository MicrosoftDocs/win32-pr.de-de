---
description: Eine-Enumeration, die für die Kommunikation zwischen der Aufzeichnungs-Engine und einem Host (z. b. Visual Studio Grafikdiagnose) verwendet wird.
MS-HAID: vspixengine.CallbackCommandType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Callbackcommandtype-Enumeration
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 78E0CD6C-5264-4F66-BAB9-20DC9C0C1EC1
api_name:
- CallbackCommandType
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ac33267677ae95f6a3d5f893b84d6566e564cddd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124663"
---
# <a name="span-idvspixenginecallbackcommandtypespancallbackcommandtype-enumeration"></a><span data-ttu-id="857c9-103"><span id="vspixengine.callbackcommandtype"></span>Callbackcommandtype-Enumeration</span><span class="sxs-lookup"><span data-stu-id="857c9-103"><span id="vspixengine.callbackcommandtype"></span>CallbackCommandType enumeration</span></span>

<span data-ttu-id="857c9-104">Eine-Enumeration, die für die Kommunikation zwischen der Aufzeichnungs-Engine und einem Host (z. b. Visual Studio Grafikdiagnose) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="857c9-104">An enum used to communicate between the capture engine and a host (such as Visual Studio Graphics Diagnostics).</span></span>

## <a name="syntax"></a><span data-ttu-id="857c9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="857c9-105">Syntax</span></span>


```C++
};
```

## <a name="constants"></a><span data-ttu-id="857c9-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="857c9-106">Constants</span></span>

<span data-ttu-id="857c9-107"><span id="BeginCommunicationCallback"></span><span id="begincommunicationcallback"></span><span id="BEGINCOMMUNICATIONCALLBACK"></span>**Begincommunicationcallback**</span><span class="sxs-lookup"><span data-stu-id="857c9-107"><span id="BeginCommunicationCallback"></span><span id="begincommunicationcallback"></span><span id="BEGINCOMMUNICATIONCALLBACK"></span>**BeginCommunicationCallback**</span></span>  
<span data-ttu-id="857c9-108">Ergebnisse von begincommunication.</span><span class="sxs-lookup"><span data-stu-id="857c9-108">Results from BeginCommunication.</span></span>

<span data-ttu-id="857c9-109"><span id="ErrorListCallback"></span><span id="errorlistcallback"></span><span id="ERRORLISTCALLBACK"></span>**Errorlistcallback**</span><span class="sxs-lookup"><span data-stu-id="857c9-109"><span id="ErrorListCallback"></span><span id="errorlistcallback"></span><span id="ERRORLISTCALLBACK"></span>**ErrorListCallback**</span></span>  
<span data-ttu-id="857c9-110">Fehler.</span><span class="sxs-lookup"><span data-stu-id="857c9-110">Errors.</span></span>

<span data-ttu-id="857c9-111"><span id="WarningListCallback"></span><span id="warninglistcallback"></span><span id="WARNINGLISTCALLBACK"></span>**Warninglistcallback**</span><span class="sxs-lookup"><span data-stu-id="857c9-111"><span id="WarningListCallback"></span><span id="warninglistcallback"></span><span id="WARNINGLISTCALLBACK"></span>**WarningListCallback**</span></span>  
<span data-ttu-id="857c9-112">Warnungen.</span><span class="sxs-lookup"><span data-stu-id="857c9-112">Warnings.</span></span>

<span data-ttu-id="857c9-113"><span id="MessagesCallback"></span><span id="messagescallback"></span><span id="MESSAGESCALLBACK"></span>**Messagescallback**</span><span class="sxs-lookup"><span data-stu-id="857c9-113"><span id="MessagesCallback"></span><span id="messagescallback"></span><span id="MESSAGESCALLBACK"></span>**MessagesCallback**</span></span>  
<span data-ttu-id="857c9-114">Meldungen.</span><span class="sxs-lookup"><span data-stu-id="857c9-114">Messages.</span></span>

<span data-ttu-id="857c9-115"><span id="RunExperimentCallback"></span><span id="runexperimentcallback"></span><span id="RUNEXPERIMENTCALLBACK"></span>**Runexperimentcallback**</span><span class="sxs-lookup"><span data-stu-id="857c9-115"><span id="RunExperimentCallback"></span><span id="runexperimentcallback"></span><span id="RUNEXPERIMENTCALLBACK"></span>**RunExperimentCallback**</span></span>  
<span data-ttu-id="857c9-116">Ergebnis von runexperiment.</span><span class="sxs-lookup"><span data-stu-id="857c9-116">Result from RunExperiment.</span></span>

<span data-ttu-id="857c9-117"><span id="RunActionCallback"></span><span id="runactioncallback"></span><span id="RUNACTIONCALLBACK"></span>**Runaktioncallback**</span><span class="sxs-lookup"><span data-stu-id="857c9-117"><span id="RunActionCallback"></span><span id="runactioncallback"></span><span id="RUNACTIONCALLBACK"></span>**RunActionCallback**</span></span>  
<span data-ttu-id="857c9-118">Ergebnis von runaction.</span><span class="sxs-lookup"><span data-stu-id="857c9-118">Result from RunAction.</span></span>

<span data-ttu-id="857c9-119"><span id="NewFramesCallback"></span><span id="newframescallback"></span><span id="NEWFRAMESCALLBACK"></span>**Newframescallback**</span><span class="sxs-lookup"><span data-stu-id="857c9-119"><span id="NewFramesCallback"></span><span id="newframescallback"></span><span id="NEWFRAMESCALLBACK"></span>**NewFramesCallback**</span></span>  
<span data-ttu-id="857c9-120">Ein Wert, der einen Rückruf angibt, der aufgerufen werden soll, wenn neue Frames aufgezeichnet und bereit sind, angezeigt zu werden.</span><span class="sxs-lookup"><span data-stu-id="857c9-120">A value that indicates a callback to be called when new frames have been captured and ready to display.</span></span>

<span data-ttu-id="857c9-121"><span id="BeginCommunicationCallbackLegacy"></span><span id="begincommunicationcallbacklegacy"></span><span id="BEGINCOMMUNICATIONCALLBACKLEGACY"></span>**Begincommunicationcallbacklegacy**</span><span class="sxs-lookup"><span data-stu-id="857c9-121"><span id="BeginCommunicationCallbackLegacy"></span><span id="begincommunicationcallbacklegacy"></span><span id="BEGINCOMMUNICATIONCALLBACKLEGACY"></span>**BeginCommunicationCallbackLegacy**</span></span>  
<span data-ttu-id="857c9-122">Ergebnisse aus einer älteren Version von begincommunication, die unter Windows 7 und Windows 8 verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="857c9-122">Results from an older version of BeginCommunication used on Windows 7 and Windows 8.</span></span>

<span data-ttu-id="857c9-123"><span id="RunExperimentStatusCallback"></span><span id="runexperimentstatuscallback"></span><span id="RUNEXPERIMENTSTATUSCALLBACK"></span>**Runexperimentstatus Rückruf**</span><span class="sxs-lookup"><span data-stu-id="857c9-123"><span id="RunExperimentStatusCallback"></span><span id="runexperimentstatuscallback"></span><span id="RUNEXPERIMENTSTATUSCALLBACK"></span>**RunExperimentStatusCallback**</span></span>  
<span data-ttu-id="857c9-124">Ergebnis von runexperiementprogress.</span><span class="sxs-lookup"><span data-stu-id="857c9-124">Result from RunExperiementProgress.</span></span>

## <a name="requirements"></a><span data-ttu-id="857c9-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="857c9-125">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="857c9-126">Header</span><span class="sxs-lookup"><span data-stu-id="857c9-126">Header</span></span></p></td><td><span data-ttu-id="857c9-127">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="857c9-127">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



