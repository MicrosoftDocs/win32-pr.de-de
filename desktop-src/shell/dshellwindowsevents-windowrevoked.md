---
description: Wird aufgerufen, wenn die Registrierung eines shellfensters widerrufen wird.
title: Dshellwindowsvents. windowwiderruf-Methode
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
ms.openlocfilehash: b036bdde2916c2fa037d1b6e286a2096d9e1d8bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "104983084"
---
# <a name="dshellwindowseventswindowrevoked-method"></a>Dshellwindowsvents. windowwiderruf-Methode

Wird aufgerufen, wenn die Registrierung eines shellfensters widerrufen wird.

## <a name="syntax"></a>Syntax


```JScript
DShellWindowsEvents.WindowRevoked(
  lCookie
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lcookie* \[ in\]
</dt> <dd>

Type: **Integer**

Das Cookie, das das Fenster identifiziert, das widerrufen wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Einem Fenster wird ein Cookie erteilt, wenn es als Shellfenster registriert wird. Weitere Informationen finden Sie unter [**Register**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register).

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| Produkt<br/> | Internet Explorer 5<br/>                                                                                           |
| DLL<br/>     | <dl> <dt>Shdocvw.dll (Version 5.00.2014.0216 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Dshellwindowgvents**](dshellwindowsevents.md)
</dt> <dt>

[**Windowregistered**](dshellwindowsevents-windowregistered.md)
</dt> <dt>

[**Revoke**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-revoke)
</dt> </dl>

 

 




