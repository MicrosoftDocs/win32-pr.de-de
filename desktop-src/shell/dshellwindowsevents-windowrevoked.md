---
description: Wird aufgerufen, wenn die Registrierung eines Shellfensters widerrufen wird.
title: DShellWindowsEvents.WindowRevoked-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DShellWindowsEvents.WindowRevoked
api_type:
- COM
api_location:
- Shdocvw.dll
ms.assetid: 92e8653f-7f41-4e0b-97e5-429fddc51951
ms.openlocfilehash: 571808962d65d25d4fb08f8d4cb57ffd1d51da67a7ba60def191edcf2fe19575
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459847"
---
# <a name="dshellwindowseventswindowrevoked-method"></a>DShellWindowsEvents.WindowRevoked-Methode

Wird aufgerufen, wenn die Registrierung eines Shellfensters widerrufen wird.

## <a name="syntax"></a>Syntax


```JScript
DShellWindowsEvents.WindowRevoked(
  lCookie
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lCookie* \[ In\]
</dt> <dd>

Typ: **Ganze Zahl**

Das Cookie, das das gesperrte Fenster identifiziert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Einem Fenster wird ein Cookie gewährt, wenn es als Shellfenster registriert ist. Weitere Informationen finden Sie unter [**Registrieren von**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| Product (Produkt)<br/> | Internet Explorer 5<br/>                                                                                           |
| DLL<br/>     | <dl> <dt>Shdocvw.dll (Version 5.00.2014.0216 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**DShellWindowsEvents**](dshellwindowsevents.md)
</dt> <dt>

[**WindowRegistered**](dshellwindowsevents-windowregistered.md)
</dt> <dt>

[**Widerrufen**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-revoke)
</dt> </dl>

 

 




