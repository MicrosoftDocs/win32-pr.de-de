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
# <a name="span-idvspixengineremotecommandtypespanremotecommandtype-enumeration"></a><span id="vspixengine.remotecommandtype"></span>Remotecommandtype-Enumeration

Eine-Enumeration, die für die Kommunikation zwischen der Aufzeichnungs-Engine und einem Host (z. b. Visual Studio Grafikdiagnose) verwendet wird.

## <a name="syntax"></a>Syntax


```C++
};
```

## <a name="constants"></a>Konstanten

<span id="BeginCommunication"></span><span id="begincommunication"></span><span id="BEGINCOMMUNICATION"></span>**Begincommunication**  
Startet die Kommunikation.

<span id="RunExperiment"></span><span id="runexperiment"></span><span id="RUNEXPERIMENT"></span>**Runexperiment**  
Startet eine Grafikdiagnose Erfassungs Sitzung (ein Experiment).

<span id="RunAction"></span><span id="runaction"></span><span id="RUNACTION"></span>**Runaction**  
Startet eine Erfassung (identisch mit dem Bildschirm zum Drucken). Wird von einem Host gesendet, wenn ein Frame erfasst wird.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



