---
description: Eine Rückruffunktion, die verwendet wird, um den Host über den Fortschritt der Engines zu benachrichtigen. Dies dient auch als Möglichkeit für den Host, zu ermitteln, ob die Engine noch ausgeführt wird.
title: IStatusCallback::Status-Methode
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
ms.openlocfilehash: edf48e62389224a01af7e52aa7e87f3db63b3740
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622306"
---
# <a name="span-idvspixengineistatuscallback_status_dword_dword_dwordspanistatuscallbackstatus-method"></a><span id="vspixengine.istatuscallback_status_dword_dword_dword"></span>IStatusCallback::Status-Methode

Eine Rückruffunktion, die verwendet wird, um den Host über den Fortschritt der Engine zu benachrichtigen. Dies dient auch als Möglichkeit für den Host, zu ermitteln, ob die Engine noch ausgeführt wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT Status(
   DWORD dwMillisecondsElapsed,
   DWORD dwFramesCaptured,
   DWORD dwFramesElapsed
);
```

## <a name="parameters"></a>Parameter

*dwMillisecondsElapsed*   
Die seit dem letzten Aufruf von Status verstrichene Zeit in Millisekunden.

*dwFramesCaptured*   
Die Anzahl der Frames, die seit dem letzten Aufruf von Status erfasst wurden.

*dwFramesElapsed*   
Die Anzahl der Frames, die seit dem letzten Aufruf von Status verstrichen sind.

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, gibt **sie** S_OK. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Requirements (Anforderungen)

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Siehe auch

[**IStatusCallback**](/windows/desktop/direct3dtools/istatuscallback)

 

 
