---
description: '<span id="vspixengine.callbackcommandtype"></span>CallbackCommandType-Enumeration: Eine Enumeration, die für die Kommunikation zwischen der Erfassungs-Engine und einem Host (z. B. Visual Studio Grafikdiagnose) verwendet wird.'
MS-HAID: vspixengine.CallbackCommandType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: CallbackCommandType-Enumeration
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
ms.openlocfilehash: 85e1b7d396d125add00824e9b7c94086e0da6be2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090128"
---
# <a name="span-idvspixenginecallbackcommandtypespancallbackcommandtype-enumeration"></a><span data-ttu-id="02f02-103"><span id="vspixengine.callbackcommandtype"></span>CallbackCommandType-Enumeration</span><span class="sxs-lookup"><span data-stu-id="02f02-103"><span id="vspixengine.callbackcommandtype"></span>CallbackCommandType enumeration</span></span>

<span data-ttu-id="02f02-104">Eine Enumeration, die für die Kommunikation zwischen der Erfassungs-Engine und einem Host (z. B. Visual Studio Grafikdiagnose) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="02f02-104">An enum used to communicate between the capture engine and a host (such as Visual Studio Graphics Diagnostics).</span></span>

## <a name="syntax"></a><span data-ttu-id="02f02-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="02f02-105">Syntax</span></span>


```C++
};
```

## <a name="constants"></a><span data-ttu-id="02f02-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="02f02-106">Constants</span></span>

<span data-ttu-id="02f02-107"><span id="BeginCommunicationCallback"></span><span id="begincommunicationcallback"></span><span id="BEGINCOMMUNICATIONCALLBACK"></span>**BeginCommunicationCallback**</span><span class="sxs-lookup"><span data-stu-id="02f02-107"><span id="BeginCommunicationCallback"></span><span id="begincommunicationcallback"></span><span id="BEGINCOMMUNICATIONCALLBACK"></span>**BeginCommunicationCallback**</span></span>  
<span data-ttu-id="02f02-108">Ergebnisse von BeginCommunication.</span><span class="sxs-lookup"><span data-stu-id="02f02-108">Results from BeginCommunication.</span></span>

<span data-ttu-id="02f02-109"><span id="ErrorListCallback"></span><span id="errorlistcallback"></span><span id="ERRORLISTCALLBACK"></span>**ErrorListCallback**</span><span class="sxs-lookup"><span data-stu-id="02f02-109"><span id="ErrorListCallback"></span><span id="errorlistcallback"></span><span id="ERRORLISTCALLBACK"></span>**ErrorListCallback**</span></span>  
<span data-ttu-id="02f02-110">Fehler.</span><span class="sxs-lookup"><span data-stu-id="02f02-110">Errors.</span></span>

<span data-ttu-id="02f02-111"><span id="WarningListCallback"></span><span id="warninglistcallback"></span><span id="WARNINGLISTCALLBACK"></span>**WarningListCallback**</span><span class="sxs-lookup"><span data-stu-id="02f02-111"><span id="WarningListCallback"></span><span id="warninglistcallback"></span><span id="WARNINGLISTCALLBACK"></span>**WarningListCallback**</span></span>  
<span data-ttu-id="02f02-112">Warnungen.</span><span class="sxs-lookup"><span data-stu-id="02f02-112">Warnings.</span></span>

<span data-ttu-id="02f02-113"><span id="MessagesCallback"></span><span id="messagescallback"></span><span id="MESSAGESCALLBACK"></span>**MessagesCallback**</span><span class="sxs-lookup"><span data-stu-id="02f02-113"><span id="MessagesCallback"></span><span id="messagescallback"></span><span id="MESSAGESCALLBACK"></span>**MessagesCallback**</span></span>  
<span data-ttu-id="02f02-114">Meldungen.</span><span class="sxs-lookup"><span data-stu-id="02f02-114">Messages.</span></span>

<span data-ttu-id="02f02-115"><span id="RunExperimentCallback"></span><span id="runexperimentcallback"></span><span id="RUNEXPERIMENTCALLBACK"></span>**RunExperimentCallback**</span><span class="sxs-lookup"><span data-stu-id="02f02-115"><span id="RunExperimentCallback"></span><span id="runexperimentcallback"></span><span id="RUNEXPERIMENTCALLBACK"></span>**RunExperimentCallback**</span></span>  
<span data-ttu-id="02f02-116">Ergebnis von RunExperiment.</span><span class="sxs-lookup"><span data-stu-id="02f02-116">Result from RunExperiment.</span></span>

<span data-ttu-id="02f02-117"><span id="RunActionCallback"></span><span id="runactioncallback"></span><span id="RUNACTIONCALLBACK"></span>**RunActionCallback**</span><span class="sxs-lookup"><span data-stu-id="02f02-117"><span id="RunActionCallback"></span><span id="runactioncallback"></span><span id="RUNACTIONCALLBACK"></span>**RunActionCallback**</span></span>  
<span data-ttu-id="02f02-118">Ergebnis von RunAction.</span><span class="sxs-lookup"><span data-stu-id="02f02-118">Result from RunAction.</span></span>

<span data-ttu-id="02f02-119"><span id="NewFramesCallback"></span><span id="newframescallback"></span><span id="NEWFRAMESCALLBACK"></span>**NewFramesCallback**</span><span class="sxs-lookup"><span data-stu-id="02f02-119"><span id="NewFramesCallback"></span><span id="newframescallback"></span><span id="NEWFRAMESCALLBACK"></span>**NewFramesCallback**</span></span>  
<span data-ttu-id="02f02-120">Ein -Wert, der einen Rückruf angibt, der aufgerufen werden soll, wenn neue Frames erfasst wurden und angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="02f02-120">A value that indicates a callback to be called when new frames have been captured and ready to display.</span></span>

<span data-ttu-id="02f02-121"><span id="BeginCommunicationCallbackLegacy"></span><span id="begincommunicationcallbacklegacy"></span><span id="BEGINCOMMUNICATIONCALLBACKLEGACY"></span>**BeginCommunicationCallbackLegacy**</span><span class="sxs-lookup"><span data-stu-id="02f02-121"><span id="BeginCommunicationCallbackLegacy"></span><span id="begincommunicationcallbacklegacy"></span><span id="BEGINCOMMUNICATIONCALLBACKLEGACY"></span>**BeginCommunicationCallbackLegacy**</span></span>  
<span data-ttu-id="02f02-122">Ergebnisse einer älteren Version von BeginCommunication, die unter Windows 7 und Windows 8 verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="02f02-122">Results from an older version of BeginCommunication used on Windows 7 and Windows 8.</span></span>

<span data-ttu-id="02f02-123"><span id="RunExperimentStatusCallback"></span><span id="runexperimentstatuscallback"></span><span id="RUNEXPERIMENTSTATUSCALLBACK"></span>**RunExperimentStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="02f02-123"><span id="RunExperimentStatusCallback"></span><span id="runexperimentstatuscallback"></span><span id="RUNEXPERIMENTSTATUSCALLBACK"></span>**RunExperimentStatusCallback**</span></span>  
<span data-ttu-id="02f02-124">Ergebnis von RunExperiementProgress.</span><span class="sxs-lookup"><span data-stu-id="02f02-124">Result from RunExperiementProgress.</span></span>

## <a name="requirements"></a><span data-ttu-id="02f02-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="02f02-125">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="02f02-126">Header</span><span class="sxs-lookup"><span data-stu-id="02f02-126">Header</span></span></p></td><td><span data-ttu-id="02f02-127">Vspixengine.h</span><span class="sxs-lookup"><span data-stu-id="02f02-127">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



