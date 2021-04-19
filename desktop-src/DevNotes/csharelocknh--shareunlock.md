---
description: Gibt eine freigegebene Sperre frei.
ms.assetid: c2e9eb68-aacb-4196-b09e-d2748efb7fd6
title: 'Csharelocknh:: shareunlock-Methode'
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
ms.openlocfilehash: 80c4311f4bf66000440dac38da6300888a8e5d59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369665"
---
# <a name="csharelocknhshareunlock-method"></a>Csharelocknh:: shareunlock-Methode

Gibt eine freigegebene Sperre frei.

## <a name="syntax"></a>Syntax


```C++
void ShareUnlock();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Jeder aufgerufene [**sharelock**](csharelocknh--sharelock.md) muss mit genau einem **share Unlock**-Aufrufvorgang gekoppelt werden. Nur ein Thread, der **sharelock** erfolgreich aufruft, kann **shareunlock** aufrufen. Andernfalls kann ein Deadlock auftreten.

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Sharelock**](csharelocknh--sharelock.md)
</dt> </dl>

 

 
