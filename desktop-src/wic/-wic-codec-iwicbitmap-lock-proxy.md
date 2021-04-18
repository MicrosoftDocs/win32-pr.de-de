---
description: Proxy Funktion für die Lock-Methode.
ms.assetid: c9d67b35-092b-4f0b-a292-879576a046bf
title: IWICBitmap_Lock_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmap_Lock_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: cf07a0afc0fbd2629ffe54b543271014d5817d71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345693"
---
# <a name="iwicbitmap_lock_proxy-function"></a>IWICBitmap- \_ Sperr \_ Proxy Funktion

Proxy Funktion für die [**Lock**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-lock) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICBitmap_Lock_Proxy(
  _In_        IWICBitmap     *THIS_PTR,
  _In_  const WICRect        *prcLock,
  _In_        DWORD          flags,
  _Out_       IWICBitmapLock **ppILock
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Dies \_ PTR* \[ in\]
</dt> <dd>

Typ: **[**IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) \** _

Zeiger auf dieses [_ *IWICBitmap* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap) -Objekt.

</dd> <dt>

*prclock* \[ in\]
</dt> <dd>

Typ: * Konstante *[**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect) \** _

Das Rechteck, auf das zugegriffen werden soll.

</dd> <dt>

_FLAGS * \[ in\]
</dt> <dd>

Typ: **DWORD**

Der Zugriffsmodus, den Sie für die Sperre erhalten möchten.

</dd> <dt>

*ppilock* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **iwicbitmaplock**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmaplock)\*\***

Ein Zeiger, der den gesperrten Speicher Speicherort empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP mit SP2, nur Windows Vista \[ -Desktop-Apps\]<br/>                                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt> </dl> |



 

 




