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
# <a name="span-idvspixengineipixengine_runexperiment_experiment_irunexperimentcallback_ptr_inewframescallback_ptr_ifileiocallback_ptr_dword_experimenttrigger_arrspanipixenginerunexperiment-method"></a><span id="vspixengine.ipixengine_runexperiment_experiment_irunexperimentcallback_ptr_inewframescallback_ptr_ifileiocallback_ptr_dword_experimenttrigger_arr"></span>Ipixengine:: runexperiment-Methode

Führt ein Experiment aus.

## <a name="syntax"></a>Syntax


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

## <a name="parameters"></a>Parameter

*Experiments*   
Beschreibt das auszutestende Experiment.

*prequestcallback*   
Die Adresse einer Funktion, die verwendet wird, um den Host zu benachrichtigen, dass die Engine das Experiment gestartet hat.

*Rückrufe*   
Die Adresse einer Funktion, die verwendet wird, um den Host zu benachrichtigen, dass neue Frames aufgezeichnet wurden.

*pfileiocallback*   
Die Adresse einer Funktion, die verwendet wird, um den Host von Datei-e/a-Fehlern beim Parsen zu Benachrichtigen

*Triggers count*   
Die Anzahl der Trigger im Experiment.

*count4 \_ triggersbuffer*   
Erfassungs Trigger.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**Ipixengine**](/windows/desktop/direct3dtools/ipixengine)

 

 
