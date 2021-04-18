---
description: Eine Rückruffunktion, die zum Benachrichtigen des Hosts über den Fortschritt des Engines verwendet wird. Dadurch kann der Host auch feststellen, dass die Engine weiterhin ausgeführt wird.
title: 'Istatuscallback:: Status-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4DC2A05F-506C-4AB4-98E1-58827056700D
api_name:
- IStatusCallback.Status
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 09fba28486bd6f1c43e4b0c4fb0dfcf495e0722b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106340094"
---
# <a name="span-idvspixengineistatuscallback_status_dword_dword_dwordspanistatuscallbackstatus-method"></a><span id="vspixengine.istatuscallback_status_dword_dword_dword"></span>Istatuscallback:: Status-Methode

Eine Rückruffunktion, die verwendet wird, um den Host über den Fortschritt der Engine zu benachrichtigen. Dadurch kann der Host auch feststellen, dass die Engine weiterhin ausgeführt wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT Status(
   DWORD dwMillisecondsElapsed,
   DWORD dwFramesCaptured,
   DWORD dwFramesElapsed
);
```

## <a name="parameters"></a>Parameter

*dwmillisecondselapsed*   
Die seit dem letzten Aufruf des Status verstrichene Zeit in Millisekunden.

*dwframesaufgezeichnet*   
Die Anzahl der Frames, die seit dem letzten Status aufgerufen wurden.

*dwframesverstrichene*   
Die Anzahl der Frames, die seit dem letzten Status aufgerufen wurden.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**Istatus Callback**](/windows/desktop/direct3dtools/istatuscallback)

 

 
