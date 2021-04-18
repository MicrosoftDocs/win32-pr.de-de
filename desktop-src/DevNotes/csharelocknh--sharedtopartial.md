---
description: Ändert eine freigegebene Sperre in eine partielle Sperre.
ms.assetid: 82122671-b0bd-47ad-9a25-ee8ebd3779be
title: 'Csharelocknh:: sharedtopartial-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.SharedToPartial
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: a997c5a437063a4c55b74d837dc77fd506688158
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368495"
---
# <a name="csharelocknhsharedtopartial-method"></a>Csharelocknh:: sharedtopartial-Methode

Ändert eine freigegebene Sperre in eine partielle Sperre.

## <a name="syntax"></a>Syntax


```C++
BOOL SharedToPartial();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn die teilsperre abgerufen wird. Andernfalls wird " **false** " zurückgegeben, und die Sperre bleibt im freigegebenen Modus.

## <a name="remarks"></a>Bemerkungen

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



 

 
