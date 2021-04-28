---
description: '<span id="vspixengine.remotecommandtype"></span>RemoteCommandType-Enumeration: Eine Enumeration, die für die Kommunikation zwischen der Erfassungs-Engine und einem Host (z. B. Visual Studio Grafikdiagnose) verwendet wird.'
MS-HAID: vspixengine.RemoteCommandType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: RemoteCommandType-Enumeration
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
ms.openlocfilehash: ed57b9b044613351e99096a8c8cb741b8ad7a269
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110505"
---
# <a name="span-idvspixengineremotecommandtypespanremotecommandtype-enumeration"></a><span data-ttu-id="af8b8-103"><span id="vspixengine.remotecommandtype"></span>RemoteCommandType-Enumeration</span><span class="sxs-lookup"><span data-stu-id="af8b8-103"><span id="vspixengine.remotecommandtype"></span>RemoteCommandType enumeration</span></span>

<span data-ttu-id="af8b8-104">Eine Enumeration, die für die Kommunikation zwischen der Erfassungs-Engine und einem Host (z. B. Visual Studio Grafikdiagnose) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="af8b8-104">An enum used to communicate between the capture engine and a host (such as Visual Studio Graphics Diagnostics).</span></span>

## <a name="syntax"></a><span data-ttu-id="af8b8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="af8b8-105">Syntax</span></span>


```C++
};
```

## <a name="constants"></a><span data-ttu-id="af8b8-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="af8b8-106">Constants</span></span>

<span data-ttu-id="af8b8-107"><span id="BeginCommunication"></span><span id="begincommunication"></span><span id="BEGINCOMMUNICATION"></span>**BeginCommunication**</span><span class="sxs-lookup"><span data-stu-id="af8b8-107"><span id="BeginCommunication"></span><span id="begincommunication"></span><span id="BEGINCOMMUNICATION"></span>**BeginCommunication**</span></span>  
<span data-ttu-id="af8b8-108">Startet die Kommunikation.</span><span class="sxs-lookup"><span data-stu-id="af8b8-108">Starts communication.</span></span>

<span data-ttu-id="af8b8-109"><span id="RunExperiment"></span><span id="runexperiment"></span><span id="RUNEXPERIMENT"></span>**RunExperiment**</span><span class="sxs-lookup"><span data-stu-id="af8b8-109"><span id="RunExperiment"></span><span id="runexperiment"></span><span id="RUNEXPERIMENT"></span>**RunExperiment**</span></span>  
<span data-ttu-id="af8b8-110">Startet eine Grafikdiagnose Aufzeichnungssitzung (ein Experiment).</span><span class="sxs-lookup"><span data-stu-id="af8b8-110">Starts a Graphics Diagnostics capture session (an experiment).</span></span>

<span data-ttu-id="af8b8-111"><span id="RunAction"></span><span id="runaction"></span><span id="RUNACTION"></span>**RunAction**</span><span class="sxs-lookup"><span data-stu-id="af8b8-111"><span id="RunAction"></span><span id="runaction"></span><span id="RUNACTION"></span>**RunAction**</span></span>  
<span data-ttu-id="af8b8-112">Startet eine Erfassung (identisch mit dem Drücken des Druckbildschirms).</span><span class="sxs-lookup"><span data-stu-id="af8b8-112">Starts a capture (same as hitting print screen).</span></span> <span data-ttu-id="af8b8-113">Wird von einem Host gesendet, wenn ein Frame erfasst wird.</span><span class="sxs-lookup"><span data-stu-id="af8b8-113">Sent by a host when capturing a frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="af8b8-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="af8b8-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="af8b8-115">Header</span><span class="sxs-lookup"><span data-stu-id="af8b8-115">Header</span></span></p></td><td><span data-ttu-id="af8b8-116">Vspixengine.h</span><span class="sxs-lookup"><span data-stu-id="af8b8-116">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



