---
description: Gibt eine Sperre frei, die mithilfe von exclusivelock für den freigegebenen Modus abgerufen wurde.
ms.assetid: d38354f0-2eb3-4924-99b5-1331e587ce32
title: 'Csharelocknh:: exclusiveunlock-Methode'
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
ms.openlocfilehash: f5fae5d6131bfcb386d52880b530f3def9464442
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360982"
---
# <a name="csharelocknhexclusiveunlock-method"></a>Csharelocknh:: exclusiveunlock-Methode

Gibt eine Sperre frei, die mithilfe von [**exclusivelock**](csharelocknh--exclusivelock.md) für den freigegebenen Modus abgerufen wurde.

## <a name="syntax"></a>Syntax


```C++
void ExclusiveUnlock();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Jeder Rückruf von [**exclusivelock**](csharelocknh--exclusivelock.md) muss mit genau einem Rückruf von **exclusiveunlock** gekoppelt werden, um das Risiko eines Deadlocks zu vermeiden.

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Exclusivelock**](csharelocknh--exclusivelock.md)
</dt> </dl>

 

 
