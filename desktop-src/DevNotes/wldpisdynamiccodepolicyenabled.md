---
description: Ruft einen Wert ab, der den Erzwingungsstatus der Device Guard-Richtlinie für dynamischen .NET-Code beschreibt.
ms.assetid: 11E6C631-0FF8-4DB2-931A-1012B3CA4357
title: WldpIsDynamicCodePolicyEnabled-Funktion (Wldp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpIsDynamicCodePolicyEnabled
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: 12643bd542acac908c560a2094fb02e69d6d1aae62308e4ca4ece3be8bb85c2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118666361"
---
# <a name="wldpisdynamiccodepolicyenabled-function"></a>WldpIsDynamicCodePolicyEnabled-Funktion

Ruft einen Wert ab, der den Erzwingungsstatus der Device Guard-Richtlinie für dynamischen .NET-Code beschreibt.

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI WldpIsDynamicCodePolicyEnabled(
  _Out_ PBOOL  isEnabled
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*isEnabled* \[ out\]
</dt> <dd>

Bei Erfolg gibt **TRUE** zurück, wenn die Device Guard-Richtlinie die Richtlinie für dynamischen .NET-Code erzwingt. andernfalls gibt **false** zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt **S \_ OK** zurück, wenn erfolgreich ist, oder andernfalls einen Fehlercode.

## <a name="remarks"></a>Hinweise

Dynamischer Code bezieht sich auf dynamisch generierten .NET CRL-Code.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, nur Desktop-Apps der Version 1803 \[\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2016 Nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Wldp.h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




