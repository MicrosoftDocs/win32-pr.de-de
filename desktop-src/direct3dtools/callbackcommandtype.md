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
# <a name="span-idvspixenginecallbackcommandtypespancallbackcommandtype-enumeration"></a><span id="vspixengine.callbackcommandtype"></span>CallbackCommandType-Enumeration

Eine Enumeration, die für die Kommunikation zwischen der Erfassungs-Engine und einem Host (z. B. Visual Studio Grafikdiagnose) verwendet wird.

## <a name="syntax"></a>Syntax


```C++
};
```

## <a name="constants"></a>Konstanten

<span id="BeginCommunicationCallback"></span><span id="begincommunicationcallback"></span><span id="BEGINCOMMUNICATIONCALLBACK"></span>**BeginCommunicationCallback**  
Ergebnisse von BeginCommunication.

<span id="ErrorListCallback"></span><span id="errorlistcallback"></span><span id="ERRORLISTCALLBACK"></span>**ErrorListCallback**  
Fehler.

<span id="WarningListCallback"></span><span id="warninglistcallback"></span><span id="WARNINGLISTCALLBACK"></span>**WarningListCallback**  
Warnungen.

<span id="MessagesCallback"></span><span id="messagescallback"></span><span id="MESSAGESCALLBACK"></span>**MessagesCallback**  
Meldungen.

<span id="RunExperimentCallback"></span><span id="runexperimentcallback"></span><span id="RUNEXPERIMENTCALLBACK"></span>**RunExperimentCallback**  
Ergebnis von RunExperiment.

<span id="RunActionCallback"></span><span id="runactioncallback"></span><span id="RUNACTIONCALLBACK"></span>**RunActionCallback**  
Ergebnis von RunAction.

<span id="NewFramesCallback"></span><span id="newframescallback"></span><span id="NEWFRAMESCALLBACK"></span>**NewFramesCallback**  
Ein -Wert, der einen Rückruf angibt, der aufgerufen werden soll, wenn neue Frames erfasst wurden und angezeigt werden können.

<span id="BeginCommunicationCallbackLegacy"></span><span id="begincommunicationcallbacklegacy"></span><span id="BEGINCOMMUNICATIONCALLBACKLEGACY"></span>**BeginCommunicationCallbackLegacy**  
Ergebnisse einer älteren Version von BeginCommunication, die unter Windows 7 und Windows 8 verwendet wird.

<span id="RunExperimentStatusCallback"></span><span id="runexperimentstatuscallback"></span><span id="RUNEXPERIMENTSTATUSCALLBACK"></span>**RunExperimentStatusCallback**  
Ergebnis von RunExperiementProgress.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



