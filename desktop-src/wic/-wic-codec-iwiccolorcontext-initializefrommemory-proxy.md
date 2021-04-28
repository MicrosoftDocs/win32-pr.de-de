---
description: IWICColorContext_InitializeFromMemory_Proxy- Proxyfunktion für die InitializeFromMemory-Methode.
ms.assetid: d98fe40c-c3f1-4c46-a558-1910e3dee51b
title: IWICColorContext_InitializeFromMemory_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICColorContext_InitializeFromMemory_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e77bbcf1e430891b031b2e77bc168c33f781eacf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097218"
---
# <a name="iwiccolorcontext_initializefrommemory_proxy-function"></a>IWICColorContext \_ InitializeFromMemory-Proxyfunktion \_

Proxyfunktion für die [**InitializeFromMemory-Methode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwiccolorcontext-initializefrommemory)

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICColorContext_InitializeFromMemory_Proxy(
  _In_       IWICColorContext *THIS_PTR,
  _In_ const BYTE             *pbBuffer,
  _In_       UINT             cbBufferSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*THIS \_ PTR* \[ in\]
</dt> <dd>

Typ: **[ **IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)\***

</dd> <dt>

*pbBuffer* \[ In\]
</dt> <dd>

Typ: **const \* BYTE**

Der Puffer, der zum Initialisieren von [**IWICColorContext verwendet wird.**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext)

</dd> <dt>

*cbBufferSize* \[ In\]
</dt> <dd>

Typ: **UINT**

Die Größe des *pbBuffer-Puffers.*

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Funktion erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderungen | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP mit SP2, nur Windows \[ Vista-Desktop-Apps\]<br/>                                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2008-Desktop-Apps\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 

 




