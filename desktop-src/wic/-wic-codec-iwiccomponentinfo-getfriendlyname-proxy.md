---
description: Proxy Funktion für die getfriendlyname-Methode.
ms.assetid: 8ac8f954-c2b9-47a2-88fe-b56710b5630c
title: IWICComponentInfo_GetFriendlyName_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetFriendlyName_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 667571169818169cb7c7ea5a1f4d3d7eb6e1635e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349974"
---
# <a name="iwiccomponentinfo_getfriendlyname_proxy-function"></a>Iwiccomponentinfo \_ getfriendlyname \_ Proxy-Funktion

Proxy Funktion für die [**getfriendlyname**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getfriendlyname) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICComponentInfo_GetFriendlyName_Proxy(
  _In_    IWICComponentInfo *THIS_PTR,
  _In_    UINT              cchFriendlyName,
  _Inout_ WCHAR             *wzFriendlyName,
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

*cchfriendlyname* \[ in\]
</dt> <dd>

Typ: **uint**

Die Größe des *wzfriendlyname* -Puffers.

</dd> <dt>

*wzfriendlyname* \[ in, out\]
</dt> <dd>

Typ: **WCHAR \** _

Ein Zeiger, der den anzeigen amen der Komponente empfängt.

Die zurückgegebene Zeichenfolge ist Gebiets Schema spezifisch, 1033 standardmäßig.

</dd> <dt>

_pcchActual * \[ out\]
</dt> <dd>

Typ: **uint \** _

Ein Zeiger, der die tatsächliche Länge des anzeigen Amens der Komponente empfängt.

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



 

 




