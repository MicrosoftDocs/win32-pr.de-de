---
description: Ein Rückruf, der den Host darüber benachrichtigt, welche Pipelinestufen vom Draw-Aufruf der assocaited-Anforderung verwendet werden.
MS-HAID: vspixengine.IPipeLineStagesCallback\_GetSupportedStages\_DWORD\_PipeLineStage\_arr\_UINT\_UINT
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPipeLineStagesCallback::GetSupportedStages-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F7046A41-5C9C-42FE-B1E2-879A47CE08E3
api_name:
- IPipeLineStagesCallback.GetSupportedStages
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e789158dda43ef3fcb8ead982c38b15f4bd26cb7c8fb291a841d529d8c6dad85
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119405940"
---
# <a name="span-idvspixengineipipelinestagescallback_getsupportedstages_dword_pipelinestage_arr_uint_uintspanipipelinestagescallbackgetsupportedstages-method"></a><span id="vspixengine.ipipelinestagescallback_getsupportedstages_dword_pipelinestage_arr_uint_uint"></span>IPipeLineStagesCallback::GetSupportedStages-Methode

Ein Rückruf, der den Host darüber benachrichtigt, welche Pipelinestufen vom Draw-Aufruf der assocaited-Anforderung verwendet werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSupportedStages(
   DWORD            numColumns,
   PipeLineStage [] count0_pStages,
   UINT             swapChainWidth,
   UINT             swapChainHeight
);
```

## <a name="parameters"></a>Parameter

*numColumns*   
Die Anzahl der zurückgegebenen Phasen.

*count0 \_ pStages*   
Die Pipelinephasen.

*swapChainWidth*   
Die Breite der Vertauschkette, die mit dem Zeichnen-Aufruf assocaited wurde. Dies wird verwendet, wenn Pipelinevorschauimages angefordert werden.

*swapChainHeight*   
Die Höhe der Swapkette, die mit dem Draw-Aufruf assocaited wurde. Dies wird verwendet, wenn Pipelinevorschauimages angefordert werden.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**IPipeLineStagesCallback**](/windows/desktop/direct3dtools/ipipelinestagescallback)

 

 
