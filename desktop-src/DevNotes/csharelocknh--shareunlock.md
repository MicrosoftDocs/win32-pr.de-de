---
description: Gibt eine freigegebene Sperre frei.
ms.assetid: c2e9eb68-aacb-4196-b09e-d2748efb7fd6
title: CShareLockNH::ShareUnlock-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.ShareUnlock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 2bf59b6e1aa0f6718cece105007a8ba502291c23868aca6ec55283dd7292f8b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162185"
---
# <a name="csharelocknhshareunlock-method"></a>CShareLockNH::ShareUnlock-Methode

Gibt eine freigegebene Sperre frei.

## <a name="syntax"></a>Syntax


```C++
void ShareUnlock();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Jeder Aufruf von [**ShareLock**](csharelocknh--sharelock.md) muss mit genau einem Aufruf von **ShareUnlock** gekoppelt werden. Nur ein Thread, der **ShareLock** erfolgreich aufruft, kann **ShareUnlock** aufrufen. Andernfalls kann ein Deadlock auftreten.

Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ShareLock**](csharelocknh--sharelock.md)
</dt> </dl>

 

 
