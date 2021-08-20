---
description: Ändert eine freigegebene Sperre in eine teilielle Sperre.
ms.assetid: 82122671-b0bd-47ad-9a25-ee8ebd3779be
title: CShareLockNH::SharedToPartial-Methode
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
ms.openlocfilehash: 8f2cc895786655754a3fcf56c6efe745467c12328867b1dc021a257ba1519652
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162205"
---
# <a name="csharelocknhsharedtopartial-method"></a>CShareLockNH::SharedToPartial-Methode

Ändert eine freigegebene Sperre in eine teilielle Sperre.

## <a name="syntax"></a>Syntax


```C++
BOOL SharedToPartial();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn die partielle Sperre erhalten wird. Andernfalls wird **FALSE zurückgegeben,** und die Sperre verbleibt im freigegebenen Modus.

## <a name="remarks"></a>Hinweise

Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Rwnh.dll</dt> </dl> |



 

 
