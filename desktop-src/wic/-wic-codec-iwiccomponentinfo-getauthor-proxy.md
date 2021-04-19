---
description: Proxy Funktion für die getauthor-Methode.
ms.assetid: fb76009e-cc01-4dec-9403-04bf6b53db80
title: IWICComponentInfo_GetAuthor_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetAuthor_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: f181a567ae4089870d324c7a7e0d67a34b965b5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364195"
---
# <a name="iwiccomponentinfo_getauthor_proxy-function"></a>Iwiccomponentinfo \_ getauthor- \_ Proxy Funktion

Proxy Funktion für die [**getauthor**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getauthor) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICComponentInfo_GetAuthor_Proxy(
  _In_    IWICComponentInfo *THIS_PTR,
  _In_    UINT              cchAuthor,
  _Inout_ WCHAR             *wzAuthor,
  _Out_   UINT              *pcchActual
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Dies \_ PTR* \[ in\]
</dt> <dd>

Typ: **[**iwiccomponentinfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) \** _

Zeiger auf dieses [_ *iwiccomponentinfo* *](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo) -Objekt.

</dd> <dt>

*cchauthor* \[ in\]
</dt> <dd>

Typ: **uint**

Die Größe des *wzauthor* -Puffers.

</dd> <dt>

*wzauthor* \[ in, out\]
</dt> <dd>

Typ: **WCHAR \** _

Ein Zeiger, der den Namen des Autors der Komponente empfängt.

Die zurückgegebene Zeichenfolge ist Gebiets Schema spezifisch, 1033 standardmäßig.

</dd> <dt>

_pcchActual * \[ out\]
</dt> <dd>

Typ: **uint \** _

Ein Zeiger, der die tatsächliche Länge des Autoren namens der Komponente empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Type: _ *HRESULT**

Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]<br/>                                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt> </dl> |



 

 




