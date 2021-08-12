---
description: Er erhält eine Reader-/Writersperre.
ms.assetid: fd212dd9-034b-4e0c-9111-e3460ea6f133
title: CShareLockNH::ExclusiveLock-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.ExclusiveLock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 16a5d2ba49d5ff1c25079a99a979d7a0fb4a51ee64d54fa4042152d7b010dc1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118667963"
---
# <a name="csharelocknhexclusivelock-method"></a>CShareLockNH::ExclusiveLock-Methode

Er erhält eine Reader-/Writersperre.

## <a name="syntax"></a>Syntax


```C++
void ExclusiveLock();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Jeder Aufruf von **ExclusiveLock** muss mit genau einem Aufruf von [**ExclusiveUnlock**](csharelocknh--exclusiveunlock.md) gekoppelt werden, um das Risiko eines Deadlocks zu vermeiden.

Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ExclusiveUnlock**](csharelocknh--exclusiveunlock.md)
</dt> </dl>

 

 
