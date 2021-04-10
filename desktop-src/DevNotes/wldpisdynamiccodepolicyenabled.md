---
description: Ruft einen Wert ab, der den Erzwingungs Status der Device Guard-Richtlinie für dynamischen .NET-Code beschreibt.
ms.assetid: 11E6C631-0FF8-4DB2-931A-1012B3CA4357
title: Wldpisdynamiccodepolicyaktivierte Funktion (wldp. h)
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
ms.openlocfilehash: 4df0555f89e9c575a7d97b69a5252c17936eb3d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125852"
---
# <a name="wldpisdynamiccodepolicyenabled-function"></a>Wldpisdynamiccodepolicyaktivierte Funktion

Ruft einen Wert ab, der den Erzwingungs Status der Device Guard-Richtlinie für dynamischen .NET-Code beschreibt.

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI WldpIsDynamicCodePolicyEnabled(
  _Out_ PBOOL  isEnabled
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*isaktiviert* \[ vorgenommen\]
</dt> <dd>

Bei Erfolg wird " **wahr** " zurückgegeben, wenn die Device Guard-Richtlinie die dynamische .NET-Code Richtlinie erzwingt Andernfalls wird **false** zurückgegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt bei Erfolg **S \_ OK** zurück oder andernfalls einen Fehlercode.

## <a name="remarks"></a>Bemerkungen

Dynamischer Code bezieht sich auf dynamisch generierten .net-CRL-Code.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1803, \[ nur Desktop-Apps\]<br/>                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2016 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Wldp. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




