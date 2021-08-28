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
ms.openlocfilehash: 73accd6f73a7c33219c83a3285837d2e1c7c133a
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122631718"
---
# <a name="span-idvspixengineremotecommandtypespanremotecommandtype-enumeration"></a><span id="vspixengine.remotecommandtype"></span>RemoteCommandType-Enumeration

Eine Enumeration, die für die Kommunikation zwischen der Erfassungs-Engine und einem Host (z. B. Visual Studio Grafikdiagnose) verwendet wird.

## <a name="syntax"></a>Syntax


```C++
};
```

## <a name="constants"></a>Konstanten

<span id="BeginCommunication"></span><span id="begincommunication"></span><span id="BEGINCOMMUNICATION"></span>**BeginCommunication**  
Startet die Kommunikation.

<span id="RunExperiment"></span><span id="runexperiment"></span><span id="RUNEXPERIMENT"></span>**RunExperiment**  
Startet eine Grafikdiagnose Aufzeichnungssitzung (ein Experiment).

<span id="RunAction"></span><span id="runaction"></span><span id="RUNACTION"></span>**RunAction**  
Startet eine Erfassung (identisch mit dem Drücken des Druckbildschirms). Wird von einem Host gesendet, wenn ein Frame erfasst wird.

## <a name="requirements"></a>Requirements (Anforderungen)

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



