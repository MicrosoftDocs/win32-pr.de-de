---
description: Eine-Enumeration, die für die Kommunikation zwischen der Aufzeichnungs-Engine und einem Host (z. b. Visual Studio Grafikdiagnose) verwendet wird.
MS-HAID: vspixengine.RemoteCommandType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Remotecommandtype-Enumeration
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B517F70C-2BFB-42E7-8597-AC5915AB2DE0
api_name:
- RemoteCommandType
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 63b94ace0818e2057a87c0f3962bb3967843bcfc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104041280"
---
# <a name="span-idvspixengineremotecommandtypespanremotecommandtype-enumeration"></a><span data-ttu-id="e9751-103"><span id="vspixengine.remotecommandtype"></span>Remotecommandtype-Enumeration</span><span class="sxs-lookup"><span data-stu-id="e9751-103"><span id="vspixengine.remotecommandtype"></span>RemoteCommandType enumeration</span></span>

<span data-ttu-id="e9751-104">Eine-Enumeration, die für die Kommunikation zwischen der Aufzeichnungs-Engine und einem Host (z. b. Visual Studio Grafikdiagnose) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e9751-104">An enum used to communicate between the capture engine and a host (such as Visual Studio Graphics Diagnostics).</span></span>

## <a name="syntax"></a><span data-ttu-id="e9751-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e9751-105">Syntax</span></span>


```C++
};
```

## <a name="constants"></a><span data-ttu-id="e9751-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="e9751-106">Constants</span></span>

<span data-ttu-id="e9751-107"><span id="BeginCommunication"></span><span id="begincommunication"></span><span id="BEGINCOMMUNICATION"></span>**Begincommunication**</span><span class="sxs-lookup"><span data-stu-id="e9751-107"><span id="BeginCommunication"></span><span id="begincommunication"></span><span id="BEGINCOMMUNICATION"></span>**BeginCommunication**</span></span>  
<span data-ttu-id="e9751-108">Startet die Kommunikation.</span><span class="sxs-lookup"><span data-stu-id="e9751-108">Starts communication.</span></span>

<span data-ttu-id="e9751-109"><span id="RunExperiment"></span><span id="runexperiment"></span><span id="RUNEXPERIMENT"></span>**Runexperiment**</span><span class="sxs-lookup"><span data-stu-id="e9751-109"><span id="RunExperiment"></span><span id="runexperiment"></span><span id="RUNEXPERIMENT"></span>**RunExperiment**</span></span>  
<span data-ttu-id="e9751-110">Startet eine Grafikdiagnose Erfassungs Sitzung (ein Experiment).</span><span class="sxs-lookup"><span data-stu-id="e9751-110">Starts a Graphics Diagnostics capture session (an experiment).</span></span>

<span data-ttu-id="e9751-111"><span id="RunAction"></span><span id="runaction"></span><span id="RUNACTION"></span>**Runaction**</span><span class="sxs-lookup"><span data-stu-id="e9751-111"><span id="RunAction"></span><span id="runaction"></span><span id="RUNACTION"></span>**RunAction**</span></span>  
<span data-ttu-id="e9751-112">Startet eine Erfassung (identisch mit dem Bildschirm zum Drucken).</span><span class="sxs-lookup"><span data-stu-id="e9751-112">Starts a capture (same as hitting print screen).</span></span> <span data-ttu-id="e9751-113">Wird von einem Host gesendet, wenn ein Frame erfasst wird.</span><span class="sxs-lookup"><span data-stu-id="e9751-113">Sent by a host when capturing a frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9751-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e9751-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="e9751-115">Header</span><span class="sxs-lookup"><span data-stu-id="e9751-115">Header</span></span></p></td><td><span data-ttu-id="e9751-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="e9751-116">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



