---
description: Gibt an, ob der angegebene nicht-Farbstil unterstrichen ist.
ms.assetid: 72056bf7-0a18-4ad3-a8c4-d2335a7218ae
title: Idulimestyle-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IdUlIMEStyle
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 262f726e8b2201b809a9416a67c2af860acee65e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372186"
---
# <a name="idulimestyle-function"></a>Idulimestyle-Funktion

Gibt an, ob der angegebene nicht-Farbstil unterstrichen ist.

## <a name="syntax"></a>Syntax


```C++
UINT __cdecl IdUlIMEStyle(
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

Diese Funktion kann einen der folgenden Werte zurückgegeben.

<dl> <dt>

**Imesty \_ UL \_ Min** . (2002)
</dt> <dt>

**Imesty \_ UL \_ None** (2002)
</dt> <dt>

**Imesty \_ UL ( \_ einzeln** ) (2003)
</dt> <dt>

**Imesty \_ UL- \_ gepunktete** (2005)
</dt> <dt>

**Imesty \_ UL \_ Thick** (2006)
</dt> <dt>

**Imesty \_ UL \_ niedriger** (2011)
</dt> <dt>

**Imesty \_ UL Thick \_ Lower** (2012)
</dt> <dt>

**Imesty \_ UL \_ thickdithlower** (2013)
</dt> <dt>

**Imesty \_ UL \_ dithlower** (2014)
</dt> <dt>

**Imesty \_ \_Max. UL** (2014)
</dt> </dl>

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

 

 
