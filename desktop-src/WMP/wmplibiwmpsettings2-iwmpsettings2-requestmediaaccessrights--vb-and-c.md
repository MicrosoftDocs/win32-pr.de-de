---
title: IWMPSettings2 requestMediaAccessRights-Methode
description: Die requestMediaAccessRights-Methode fordert eine angegebene Zugriffsebene auf die Bibliothek an. | IWMPSettings2 requestMediaAccessRights-Methode
ms.assetid: ea33852c-d1e0-45cf-8954-2a1e2fe51910
keywords:
- requestMediaAccessRights-Windows Media Player
- requestMediaAccessRights-Methode Windows Media Player , IWMPSettings2-Schnittstelle
- IWMPSettings2-Schnittstelle Windows Media Player , requestMediaAccessRights-Methode
topic_type:
- apiref
api_name:
- IWMPSettings2.requestMediaAccessRights
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aba44540717059945f273be23d2e3c63b3c10cfc6d21d35ee1c4756ea1503708
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568487"
---
# <a name="iwmpsettings2requestmediaaccessrights-method"></a>IWMPSettings2::requestMediaAccessRights-Methode

Die **requestMediaAccessRights-Methode** fordert eine angegebene Zugriffsebene auf die Bibliothek an.

## <a name="syntax"></a>Syntax


```CSharp
public System.Boolean requestMediaAccessRights(
  System.String bstrDesiredAccess
);
```


```VB

Public Function requestMediaAccessRights( _
  ByVal bstrDesiredAccess As System.String _
) As System.Boolean
Implements IWMPSettings2.requestMediaAccessRights
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrDesiredAccess* \[ In\]
</dt> <dd>

Eine **System.String,** bei der es sich um einen der folgenden Werte handelt.



| Wert | Beschreibung                      |
|-------|----------------------------------|
| Keine  | Nur Zugriffsrechte für aktuelle Elemente. |
| Lesen  | Nur Lesezugriffsrechte.         |
| Voll  | Lese-/Schreibzugriffsrechte.        |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein **system.boolesscher Wert,** der angibt, ob die angeforderten Zugriffsrechte gewährt wurden.

## <a name="remarks"></a>Hinweise

Eine Webseite muss zunächst die Berechtigung des Benutzers anfordern, Informationen aus der Bibliothek zu lesen oder Daten in die Bibliothek zu schreiben. Wenn Sie diese Methode aufrufen, wird der Benutzer mit einem Dialogfeld aufgefordert, das die angegebene Berechtigungsebene an fordert. Dies bedeutet, dass auf bestimmte Methoden, Eigenschaften und Ereignisse im Code nicht zugegriffen werden kann, wenn die entsprechenden Zugriffsrechte nicht erteilt wurden. Die aktuelle Zugriffsrechteebene kann mithilfe von **IWMPSettings2.mediaAccessRights abgerufen werden.**

Anwendungen, die auf dem Computer des Benutzers ausgeführt werden, müssen diese Methode nicht verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**IWMPSettings2-Schnittstelle (VB und C#)**](iwmpsettings2--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.mediaAccessRights (VB und C#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





