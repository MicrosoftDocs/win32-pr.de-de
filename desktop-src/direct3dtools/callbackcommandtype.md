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
# <a name="span-idvspixenginecallbackcommandtypespancallbackcommandtype-enumeration"></a><span id="vspixengine.callbackcommandtype"></span>Callbackcommandtype-Enumeration

Eine-Enumeration, die für die Kommunikation zwischen der Aufzeichnungs-Engine und einem Host (z. b. Visual Studio Grafikdiagnose) verwendet wird.

## <a name="syntax"></a>Syntax


```C++
};
```

## <a name="constants"></a>Konstanten

<span id="BeginCommunicationCallback"></span><span id="begincommunicationcallback"></span><span id="BEGINCOMMUNICATIONCALLBACK"></span>**Begincommunicationcallback**  
Ergebnisse von begincommunication.

<span id="ErrorListCallback"></span><span id="errorlistcallback"></span><span id="ERRORLISTCALLBACK"></span>**Errorlistcallback**  
Fehler.

<span id="WarningListCallback"></span><span id="warninglistcallback"></span><span id="WARNINGLISTCALLBACK"></span>**Warninglistcallback**  
Warnungen.

<span id="MessagesCallback"></span><span id="messagescallback"></span><span id="MESSAGESCALLBACK"></span>**Messagescallback**  
Meldungen.

<span id="RunExperimentCallback"></span><span id="runexperimentcallback"></span><span id="RUNEXPERIMENTCALLBACK"></span>**Runexperimentcallback**  
Ergebnis von runexperiment.

<span id="RunActionCallback"></span><span id="runactioncallback"></span><span id="RUNACTIONCALLBACK"></span>**Runaktioncallback**  
Ergebnis von runaction.

<span id="NewFramesCallback"></span><span id="newframescallback"></span><span id="NEWFRAMESCALLBACK"></span>**Newframescallback**  
Ein Wert, der einen Rückruf angibt, der aufgerufen werden soll, wenn neue Frames aufgezeichnet und bereit sind, angezeigt zu werden.

<span id="BeginCommunicationCallbackLegacy"></span><span id="begincommunicationcallbacklegacy"></span><span id="BEGINCOMMUNICATIONCALLBACKLEGACY"></span>**Begincommunicationcallbacklegacy**  
Ergebnisse aus einer älteren Version von begincommunication, die unter Windows 7 und Windows 8 verwendet wird.

<span id="RunExperimentStatusCallback"></span><span id="runexperimentstatuscallback"></span><span id="RUNEXPERIMENTSTATUSCALLBACK"></span>**Runexperimentstatus Rückruf**  
Ergebnis von runexperiementprogress.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



