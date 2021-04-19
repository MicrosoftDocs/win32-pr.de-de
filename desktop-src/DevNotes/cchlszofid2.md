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
ms.openlocfilehash: cba2d09f9865c43a5b64a34783c621c783c7aac3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365587"
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

Der Bezeichner der Zeichenfolge in der Ressourcen Datei, die decodiert und gespeichert werden soll. Die Gültigkeit der Zeichenfolge wird nicht überprüft.

</dd> <dt>

*LSZ* 
</dt> <dd>

Ein Zeiger auf einen Puffer mit einer Länge von *cbmax*. Zeichen folgen, die länger sind als *cbmax* , werden abgeschnitten.

</dd> <dt>

*cbmax* 
</dt> <dd>

Die maximale Länge der Zeichenfolge, die im *LSZ* -Parameter gespeichert werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt die decodierte Zeichenfolge zurück.

## <a name="remarks"></a>Bemerkungen

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msjint40.dll</dt> </dl> |



 

 
