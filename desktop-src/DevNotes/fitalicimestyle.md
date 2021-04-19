---
description: Gibt an, ob ein nicht-Farbstil den kursiv Formatierungs Stil aufweist.
ms.assetid: 4295c0b1-6e37-4fa9-9015-68bcc4784cda
title: Fitalicimestyle-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FItalicIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 828e701773d666830473e92afc73f80ccdae3bc3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359652"
---
# <a name="fitalicimestyle-function"></a>Fitalicimestyle-Funktion

Gibt an, ob ein nicht-Farbstil den kursiv Formatierungs Stil aufweist.

## <a name="syntax"></a>Syntax


```C++
BOOL __cdecl FItalicIMEStyle(
  _In_ const IMESTYLE *pimestyle
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pimestyle* \[ in\]
</dt> <dd>

Eine **imestyle** -Struktur, die von der [**pimestylefromattr**](pimestylefromattr.md) -Funktion zurückgegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

**True** , wenn der Stil den kursiv Formatierungs Stil aufweist.

## <a name="remarks"></a>Bemerkungen

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Imeshare.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Pimestylefromattr**](pimestylefromattr.md)
</dt> </dl>

 

 
