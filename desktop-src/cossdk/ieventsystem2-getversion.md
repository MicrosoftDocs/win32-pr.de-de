---
description: Ruft die Versionsnummer des Ereignissystems ab.
ms.assetid: 6355f1b3-e1e7-435f-9795-d92464e004ae
title: IEventSystem2::GetVersion-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEventSystem2.GetVersion
api_type:
- COM
api_location: ''
ms.openlocfilehash: 77452ccebac71cb8de8357fee0199bc04b690d59cf8d113d57a5850db0771315
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070620"
---
# <a name="ieventsystem2getversion-method"></a>IEventSystem2::GetVersion-Methode

Ruft die Versionsnummer des Ereignissystems ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetVersion(
  [out] int *pnVersion
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pnVersion* \[ out\]
</dt> <dd>

Die Versionsnummer des Ereignissystems.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode kann die Standardrückgabewerte E \_ INVALIDARG, E \_ OUTOFMEMORY, E \_ UNEXPECTED, E \_ FAIL und S \_ OK zurückgeben.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IEventSystem2**](ieventsystem2.md)
</dt> </dl>

 

 




