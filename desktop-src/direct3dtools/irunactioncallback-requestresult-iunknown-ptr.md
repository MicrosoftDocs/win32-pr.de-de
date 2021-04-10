---
description: Eine Rückruffunktion, die verwendet wird, um den Host über Ergebnisse einer Aktion zu benachrichtigen (z. b. einen Frame erfassen), die er angefordert hat.
MS-HAID: vspixengine.IRunActionCallback\_RequestResult\_IUnknown\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Ununaktioncallback:: RequestResult-Methode'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5D6B1599-2CF4-46E7-92DB-5D93DD5AD0EE
api_name:
- IRunActionCallback.RequestResult
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 8f2d5eea98b167af30bfe0412acb10f83f83d3db
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125365"
---
# <a name="span-idvspixengineirunactioncallback_requestresult_iunknown_ptrspanirunactioncallbackrequestresult-method"></a><span id="vspixengine.irunactioncallback_requestresult_iunknown_ptr"></span>Ununaktioncallback:: RequestResult-Methode

Eine Rückruffunktion, die verwendet wird, um den Host über Ergebnisse einer Aktion zu benachrichtigen (z. b. einen Frame erfassen), die er angefordert hat.

## <a name="syntax"></a>Syntax


```C++
HRESULT RequestResult(
   IUnknown * actionResult
);
```

## <a name="parameters"></a>Parameter

*actionResult*   
Das Ergebnis der Aktion.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**Nicht aktionrückruf**](/windows/desktop/direct3dtools/irunactioncallback)

 

 
