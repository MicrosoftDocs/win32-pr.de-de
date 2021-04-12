---
description: Proxy Funktion für die getcolors-Methode.
ms.assetid: 31590de3-f35c-4253-9a80-2f59c795bf3f
title: IWICPalette_GetColors_Proxy-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_GetColors_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e39e8825b78175fabb5a37e331236e7bf0d9ed73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216971"
---
# <a name="iwicpalette_getcolors_proxy-function"></a>Iwicpalette \_ getcolors- \_ Proxy Funktion

Proxy Funktion für die [**getcolors**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-getcolors) -Methode.

## <a name="syntax"></a>Syntax


```C++
HRESULT IWICPalette_GetColors_Proxy(
  _In_  IWICPalette *THIS_PTR,
  _In_  UINT        colorCount,
  _Out_ WICColor    *pColors,
  _Out_ UINT        *pcActualColors
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Dies \_ PTR* \[ in\]
</dt> <dd>

Typ: **[**iwicpalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) \** _

Zeiger auf dieses [_ *iwicpalette* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette) -Objekt.

</dd> <dt>

*colorcount* \[ in\]
</dt> <dd>

Typ: **uint**

Die Größe des *pcolors* -Arrays.

</dd> <dt>

*pcolors* \[ vorgenommen\]
</dt> <dd>

Typ: **wiccolor \** _

Ein Zeiger, der die Farben der Palette empfängt.

</dd> <dt>

_pcActualColors * \[ out\]
</dt> <dd>

Typ: **uint \** _

Die tatsächliche Größe, die zum Abrufen der Palettenfarben benötigt wird.

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



 

 




