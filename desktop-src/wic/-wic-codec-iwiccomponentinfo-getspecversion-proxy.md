---
description: Proxy Funktion für die getspecversion-Methode.
ms.assetid: 363e55c2-d6e8-4ddc-a063-c5be08232a67
title: IWICComponentInfo_GetSpecVersion_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICComponentInfo_GetSpecVersion_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: a7b9b0a44eb5fd8404eecc3ad355ec280583d690
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355455"
---
# <a name="iwiccomponentinfo_getspecversion_proxy-function"></a>Iwiccomponentinfo \_ getspecversion- \_ Proxy Funktion

Proxy Funktion für die [**getspecversion**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccomponentinfo-getspecversion) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICComponentInfo_GetSpecVersion_Proxy(
  _In_    IWICComponentInfo *THIS_PTR,
  _In_    UINT              cchSpecVersion,
  _Inout_ WCHAR             *wzSpecVersion,
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

*cchspecversion* \[ in\]
</dt> <dd>

Typ: **uint**

Die Größe des *wzspecversion* -Puffers.

</dd> <dt>

*wzspecversion* \[ in, out\]
</dt> <dd>

Typ: **WCHAR \** _

Wenn diese Methode zurückgegeben wird, enthalten Sie eine Kultur invarient-Zeichenfolge der Spezifikations Version der Komponente. Das Versions Formular ist NN. NN. NN. NN.

</dd> <dt>

_pcchActual * \[ out\]
</dt> <dd>

Typ: **uint \** _

Ein Zeiger, der die tatsächliche Länge der Spezifikations Version der Komponente empfängt.

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



 

 




