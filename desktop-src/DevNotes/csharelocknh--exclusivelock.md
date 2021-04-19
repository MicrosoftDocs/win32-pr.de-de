---
description: Erhält eine Lese-/Schreibsperre.
ms.assetid: fd212dd9-034b-4e0c-9111-e3460ea6f133
title: 'Csharelocknh:: exclusivelock-Methode'
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
ms.openlocfilehash: 8b35b544c10e6dde2887e75971d747feade5517e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362067"
---
# <a name="csharelocknhexclusivelock-method"></a>Csharelocknh:: exclusivelock-Methode

Erhält eine Lese-/Schreibsperre.

## <a name="syntax"></a>Syntax


```C++
void ExclusiveLock();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Jeder Rückruf von **exclusivelock** muss mit genau einem Rückruf von [**exclusiveunlock**](csharelocknh--exclusiveunlock.md) gekoppelt werden, um das Risiko eines Deadlocks zu vermeiden.

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Exclusiveunlock**](csharelocknh--exclusiveunlock.md)
</dt> </dl>

 

 
