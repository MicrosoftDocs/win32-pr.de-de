---
description: Erhält eine freigegebene Sperre.
ms.assetid: dff9a842-573a-4530-820d-6fd9001e502a
title: 'Csharelocknh:: sharelock-Methode'
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
ms.openlocfilehash: d0c77564deceab29a8bee0cbffbd477559117cbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357651"
---
# <a name="csharelocknhsharelock-method"></a>Csharelocknh:: sharelock-Methode

Erhält eine freigegebene Sperre.

## <a name="syntax"></a>Syntax


```C++
void ShareLock();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Jeder aufgerufene **sharelock** muss mit genau einem [**share Unlock**](csharelocknh--shareunlock.md)-Aufrufvorgang gekoppelt werden. Nur ein Thread, der **sharelock** erfolgreich aufruft, kann **shareunlock** aufrufen. Andernfalls kann ein Deadlock auftreten.

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Share Unlock**](csharelocknh--shareunlock.md)
</dt> </dl>

 

 
