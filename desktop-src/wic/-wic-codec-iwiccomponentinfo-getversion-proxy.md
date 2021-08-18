---
description: Proxyfunktion für die GetVersion-Methode.
ms.assetid: b064b065-bc02-4943-b208-ce5e40c12aa2
title: IWICComponentInfo_GetVersion_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetVersion_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 5a781aacbe0b5b9dd35a94c2ce906ee546e0b1da6b426a6848b6aafed2721cb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965219"
---
# <a name="iwiccomponentinfo_getversion_proxy-function"></a>\_IWICComponentInfo-GetVersion-Proxyfunktion \_

Proxyfunktion für die [**GetVersion-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getversion)

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICComponentInfo_GetVersion_Proxy(
  _In_    IWICComponentInfo *THIS_PTR,
  _In_    UINT              cchVersion,
  _Inout_ WCHAR             *wzVersion,
  _Out_   UINT              *pcchActual
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*DIES \_ PTR* \[ in\]
</dt> <dd>

Typ: **[ **IWICComponentInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)\***

Zeiger auf dieses [**IWICComponentInfo-Objekt.**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccomponentinfo)

</dd> <dt>

*cchVersion* \[ In\]
</dt> <dd>

Typ: **UINT**

Die Größe des *wzVersion-Puffers.*

</dd> <dt>

*wzVersion* \[ in, out\]
</dt> <dd>

Typ: **WCHAR \***

Ein Zeiger, der eine kulturinvariante Zeichenfolge der Version der Komponente empfängt.

</dd> <dt>

*pcchActual* \[ out\]
</dt> <dd>

Typ: **UINT \***

Ein Zeiger, der die tatsächliche Länge der Version der Komponente empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Funktion erfolgreich ausgeführt wird, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP mit SP2, nur Windows \[ Vista-Desktop-Apps\]<br/>                                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 

 




