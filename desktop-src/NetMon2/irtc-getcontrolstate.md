---
description: 'IRTC::GetControlState-Methode: Die GetControlState-Methode ruft den Zustand der Erfassung ab, der angibt, ob die Erfassung ausgeführt wird oder angehalten wird.'
ms.assetid: ae0cf869-bf5b-4c23-a924-014554053c92
title: IRTC::GetControlState-Methode (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.GetControlState
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: bf3f4b70f1b06f5f985d459af361dc27f320d84465f5ef86f2d956339bf90ac3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778790"
---
# <a name="irtcgetcontrolstate-method"></a>IRTC::GetControlState-Methode

Die **GetControlState-Methode** ruft den Zustand der Erfassung [*ab,*](c.md)der angibt, ob die Erfassung ausgeführt wird oder angehalten wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDMETHODCALLTYPE GetControlState(
  [out] BOOL *IsRunnning,
  [out] BOOL *IsPaused
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*IsRunnning* \[ out\]
</dt> <dd>

Gibt an, dass die aktuelle Erfassung ausgeführt wird, einschließlich, ob die Erfassung angehalten wurde.

</dd> <dt>

*IsPaused* \[ out\]
</dt> <dd>

Gibt an, dass die aktuelle Erfassung angehalten wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Methode erfolgreich ist, ist der Rückgabewert NMERR \_ SUCCESS.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:



| Rückgabecode                                                                                          | Beschreibung                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ NICHT \_ VERBUNDEN**</dt> </dl> | Der NPP ist nicht mit dem Netzwerk verbunden. Rufen [Sie IRTC::Verbinden](irtc-connect.md) auf, um das NPP mit dem Netzwerk zu verbinden.<br/> |
| <dl> <dt>**NMERR \_ NOT \_ REALTIME**</dt> </dl>  | Der NPP ist mit dem Netzwerk verbunden, aber nicht mit der [IRTC::Verbinden-Methode.](irtc-connect.md)<br/>                     |



 

## <a name="remarks"></a>Hinweise

Diese Methode kann jedes Mal aufgerufen werden, wenn die NPP mit dem Netzwerk verbunden ist. Mit dieser Methode können Sie herausfinden, ob eine Erfassung ausgeführt wird, ob die Erfassung angehalten wurde oder ob die Erfassung beendet wurde, die NPP aber weiterhin verbunden ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[IRTC](irtc.md)
</dt> <dt>

[IRTC::Verbinden](irtc-connect.md)
</dt> <dt>

[IRTC::P ause](irtc-pause.md)
</dt> <dt>

[IRTC::Start](irtc-start.md)
</dt> <dt>

[IRTC::Stop](irtc-stop.md)
</dt> </dl>

 

 




