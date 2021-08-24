---
description: Erhält eine freigegebene Sperre.
ms.assetid: dff9a842-573a-4530-820d-6fd9001e502a
title: CShareLockNH::ShareLock-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.ShareLock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 7fd398228c6d0feb7e63133e8faeefd7a2fd3359bf62e80a8f398a3467424b90
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654830"
---
# <a name="csharelocknhsharelock-method"></a>CShareLockNH::ShareLock-Methode

Erhält eine freigegebene Sperre.

## <a name="syntax"></a>Syntax


```C++
void ShareLock();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Jeder Aufruf von **ShareLock** muss mit genau einem Aufruf von [**ShareUnlock gekoppelt werden.**](csharelocknh--shareunlock.md) Nur ein Thread, der **ShareLock erfolgreich aufruft,** kann **ShareUnlock aufrufen.** Andernfalls kann ein Deadlock auftreten.

Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ShareUnlock**](csharelocknh--shareunlock.md)
</dt> </dl>

 

 
