---
description: Wird von einem Kryptografiedienstanbieter (kryptografischen Service Provider, CSP) verwendet, um das Fenster Handle abzurufen, das der CSP als übergeordnetes Element oder Besitzer einer beliebigen angezeigten Benutzeroberfläche verwenden soll.
ms.assetid: 56f189e7-073b-4b42-b6ab-0147853fe6d5
title: CRYPT_RETURN_HWND Funktionszeiger (cspdk. h)
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
ms.openlocfilehash: 32fadef6c231aa2ca63305a3da9d2142d0abe9c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352305"
---
# <a name="crypt_return_hwnd-function-pointer"></a>Crypt \_ Return- \_ HWND-Funktionszeiger

Die Funktion " **funkreturnhwnd** Callback" wird von einem [*Kryptografiedienstanbieter (kryptografischen Service Provider*](../secgloss/c-gly.md) , CSP) verwendet, um das Fenster Handle abzurufen, das der CSP als übergeordnetes Element oder als Besitzer einer beliebigen angezeigten Benutzeroberfläche verwenden soll.

## <a name="syntax"></a>Syntax


```C++
typedef void ( WINAPI *CRYPT_RETURN_HWND)(
  _Inout_ HWND *phWnd
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*phwnd* \[ in, out\]
</dt> <dd>

Die Adresse einer **HWND** -Variablen, die das übergeordnete Fenster Handle empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Dieser Funktionszeiger gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Cspdk. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cpacquirecontext**](https://www.bing.com/search?q=**CPAcquireContext**)
</dt> <dt>

[**Vtableprovstruc**](vtableprovstruc.md)
</dt> </dl>

 

 
