---
description: Wird aufgerufen, wenn ein Fenster als Shellfenster registriert wird.
title: Dshellwindowsvents. windowregistered-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DShellWindowsEvents.WindowRegistered
api_type:
- COM
api_location:
- Shdocvw.dll
ms.assetid: 7faf758a-daa0-47f5-9f95-61fe3d8286ea
ms.openlocfilehash: b12ed98c6b2a11e5886ed9e76d324a1a6842cda8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "104983068"
---
# <a name="dshellwindowseventswindowregistered-method"></a>Dshellwindowsvents. windowregistered-Methode

Wird aufgerufen, wenn ein Fenster als Shellfenster registriert wird.

## <a name="syntax"></a>Syntax


```JScript
DShellWindowsEvents.WindowRegistered(
  lCookie
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lcookie* \[ in\]
</dt> <dd>

Type: **Integer**

Das Cookie, das das registrierte Fenster identifiziert.

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

[**Windows-gesperrt**](dshellwindowsevents-windowrevoked.md)
</dt> <dt>

[**Register**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register)
</dt> <dt>

[**Register ausstehend**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-registerpending)
</dt> </dl>

 

 




