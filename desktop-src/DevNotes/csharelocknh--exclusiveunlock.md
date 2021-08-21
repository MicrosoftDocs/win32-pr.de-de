---
description: Gibt eine Sperre frei, die mit ExclusiveLock im freigegebenen Modus aktiviert wurde.
ms.assetid: d38354f0-2eb3-4924-99b5-1331e587ce32
title: CShareLockNH::ExclusiveUnlock-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.ExclusiveUnlock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 20d614f733b1668e3dea7619629cf2833f1d6af40384e679aea79a7a48279724
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118667836"
---
# <a name="csharelocknhexclusiveunlock-method"></a>CShareLockNH::ExclusiveUnlock-Methode

Gibt eine Sperre frei, die mit [**ExclusiveLock**](csharelocknh--exclusivelock.md) im freigegebenen Modus aktiviert wurde.

## <a name="syntax"></a>Syntax


```C++
void ExclusiveUnlock();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Jeder Aufruf von [**ExclusiveLock**](csharelocknh--exclusivelock.md) muss mit genau einem Aufruf von **ExclusiveUnlock** gekoppelt werden, um das Risiko eines Deadlocks zu vermeiden.

Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ExclusiveLock**](csharelocknh--exclusivelock.md)
</dt> </dl>

 

 
