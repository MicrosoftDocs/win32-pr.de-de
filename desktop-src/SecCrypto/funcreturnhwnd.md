---
description: Wird von einem Kryptografiedienstanbieter (Cryptographic Service Provider, CSP) verwendet, um das Fensterhand handle zu erhalten, das der CSP als übergeordnetes Element oder Besitzer einer beliebigen angezeigten Benutzeroberfläche verwenden soll.
ms.assetid: 56f189e7-073b-4b42-b6ab-0147853fe6d5
title: CRYPT_RETURN_HWND Funktionszeiger (Cspdk.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRYPT_RETURN_HWND
api_type:
- UserDefined
api_location:
- Cspdk.h
ms.openlocfilehash: 387e1e9140dac8081acf851eb7125a612506783adbeefe1174137ff7f74fae9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006748"
---
# <a name="crypt_return_hwnd-function-pointer"></a>CRYPT \_ RETURN \_ HWND-Funktionszeiger

Die **FuncReturnhWnd-Rückruffunktion** wird von einem Kryptografiedienstanbieter (Cryptographic [*Service Provider,*](../secgloss/c-gly.md) CSP) verwendet, um das Fensterhand handle zu erhalten, das der CSP als übergeordnetes Element oder Besitzer einer angezeigten Benutzeroberfläche verwenden soll.

## <a name="syntax"></a>Syntax


```C++
typedef void ( WINAPI *CRYPT_RETURN_HWND)(
  _Inout_ HWND *phWnd
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*phWnd* \[ in, out\]
</dt> <dd>

Die Adresse einer **HWND-Variablen,** die das übergeordnete Fensterhand handle empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieser Funktionszeiger gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Cspdk.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CPAcquireContext**](https://www.bing.com/search?q=**CPAcquireContext**)
</dt> <dt>

[**VTableProvStruc**](vtableprovstruc.md)
</dt> </dl>

 

 
