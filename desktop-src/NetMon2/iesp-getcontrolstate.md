---
description: Die getcontrolstate-Methode ruft den Status der Erfassung ab, der angibt, ob die Erfassung ausgeführt wird oder angehalten wird.
ms.assetid: 19cc3095-3aa3-4482-95f5-959b19f76cea
title: 'IESP:: getcontrolstate-Methode (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.GetControlState
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: c791d5dc1f5d5321268fef2fb5cf91e04d9ecff3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353016"
---
# <a name="iespgetcontrolstate-method"></a>IESP:: getcontrolstate-Methode

Die **getcontrolstate** -Methode ruft den Status der [*Erfassung*](c.md)ab, der angibt, ob die Erfassung ausgeführt wird oder angehalten wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDMETHODCALLTYPE GetControlState(
  [out] BOOL *IsRunnning,
  [out] BOOL *IsPaused
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Isrunnning* \[ vorgenommen\]
</dt> <dd>

Indikator, dass die aktuelle Erfassung ausgeführt wird, einschließlich, wenn die Erfassung angehalten wurde.

</dd> <dt>

*IsPaused* \[ vorgenommen\]
</dt> <dd>

Indikator, dass die aktuelle Erfassung angehalten wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:



| Rückgabecode                                                                                          | Beschreibung                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**nmerr \_ nicht \_ verbunden**</dt> </dl> | Der npp ist nicht mit dem Netzwerk verbunden. Wenden Sie [iESP:: Connect](iesp-connect.md) an, um die NPP mit dem Netzwerk zu verbinden.<br/> |
| <dl> <dt>**nmerr \_ nicht \_ ESP**</dt> </dl>       | Der npp ist mit dem Netzwerk verbunden, jedoch nicht mit der [iESP:: Connect](iesp-connect.md) -Methode.<br/>                     |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode kann jedes Mal aufgerufen werden, wenn der NPP mit dem Netzwerk verbunden ist. Mit dieser Methode können Sie herausfinden, ob eine Erfassung ausgeführt wird, ob die Erfassung angehalten wurde oder ob die Erfassung angehalten wurde, aber der npp ist weiterhin verbunden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[IESP](iesp.md)
</dt> <dt>

[IESP:: Connect](iesp-connect.md)
</dt> <dt>

[IESP::P ause](iesp-pause.md)
</dt> <dt>

[IESP:: Start](iesp-start.md)
</dt> <dt>

[IESP:: Beendigung](iesp-stop.md)
</dt> </dl>

 

 




