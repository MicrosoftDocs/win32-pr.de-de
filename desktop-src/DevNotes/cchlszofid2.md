---
description: Decodiert und speichert eine Zeichenfolge.
ms.assetid: 6ababd6e-57b7-49eb-98c9-a4bcb558a377
title: CchLszOfId2-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CchLszOfId2
api_type:
- DllExport
api_location:
- Msjint40.dll
ms.openlocfilehash: 0377b8507507b40c5b17c3d9bb6861e5077f8c7bb763b51c66289ab1819f9cc7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815470"
---
# <a name="cchlszofid2-function"></a>CchLszOfId2-Funktion

Decodiert und speichert eine Zeichenfolge.

## <a name="syntax"></a>Syntax


```C++
UINT CchLszOfId2(
   UINT  id,
   WCHAR *lsz,
   UINT  cbmax
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*id* 
</dt> <dd>

Der Bezeichner der Zeichenfolge in der Ressourcendatei, die decodiert und gespeichert werden soll. Die Gültigkeit der Zeichenfolge wird nicht überprüft.

</dd> <dt>

*lsz* 
</dt> <dd>

Ein Zeiger auf einen Puffer mit der Länge *cbmax*. Zeichenfolgen, die länger als *cbmax* sind, werden abgeschnitten.

</dd> <dt>

*cbmax* 
</dt> <dd>

Die maximale Länge der Zeichenfolge, die im *lsz-Parameter* gespeichert werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt die decodierte Zeichenfolge zurück.

## <a name="remarks"></a>Hinweise

Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msjint40.dll</dt> </dl> |



 

 
