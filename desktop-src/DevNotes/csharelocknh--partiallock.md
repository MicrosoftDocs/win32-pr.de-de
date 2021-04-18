---
description: Verhindert, dass mehr als ein Thread eine Sperre erhält.
ms.assetid: 9cdcc6d5-b2f1-4c88-b859-1c15a80e70a9
title: Csharelocknh::P artizuweisung-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.PartialLock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 0b7b7d55c9fd8d979aa14f12939df922e7a89099
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366039"
---
# <a name="csharelocknhpartiallock-method"></a>Csharelocknh::P artizuweisung-Methode

Verhindert, dass mehr als ein Thread eine Sperre erhält.

## <a name="syntax"></a>Syntax


```C++
void PartialLock();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Obwohl **partitenzuweisung** wirksam ist, können andere Threads, die [**sharelock**](csharelocknh--sharelock.md) aufrufen, die Sperre eingeben.

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



 

 
