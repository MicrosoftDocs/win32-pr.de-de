---
title: IWMPSettings2 requestmediaaccessrights-Methode
description: Die requestmediaaccessrights-Methode fordert eine angegebene Zugriffsebene auf die Bibliothek an. | IWMPSettings2 requestmediaaccessrights-Methode
ms.assetid: ea33852c-d1e0-45cf-8954-2a1e2fe51910
keywords:
- requestmediaaccessrights-Methode, Windows Media Player
- requestmediaaccessrights-Methode, Windows Media Player, IWMPSettings2-Schnittstelle
- IWMPSettings2 Interface Windows Media Player, requestmediaaccessrights-Methode
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
ms.openlocfilehash: c609afffc1d9b228d908d905e0eb1a6ef8741032
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352998"
---
# <a name="iwmpsettings2requestmediaaccessrights-method"></a>IWMPSettings2:: requestmediaaccessrights-Methode

Die **requestmediaaccessrights** -Methode fordert eine angegebene Zugriffsebene auf die Bibliothek an.

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

*bstraudesiredaccess* \[ in\]
</dt> <dd>

Ein **System. String** -Wert, der einem der folgenden Werte entspricht.



| Wert | BESCHREIBUNG                      |
|-------|----------------------------------|
| none  | Nur die aktuellen Element Zugriffsrechte. |
| Lesen  | Nur Lese Zugriffsrechte.         |
| Voll  | Lese-/Schreibzugriffsrechte.        |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ein **System. boolescher** Wert, der angibt, ob die angeforderten Zugriffsrechte erteilt wurden.

## <a name="remarks"></a>Bemerkungen

Eine Webseite muss zuerst die Berechtigung des Benutzers anfordern, Informationen aus der Bibliothek zu lesen oder Daten in die Bibliothek zu schreiben. Beim Aufrufen dieser Methode wird der Benutzer zu einem Dialogfeld aufgefordert, das die angegebene Berechtigungsebene anfordert. Dies bedeutet, dass auf bestimmte Methoden, Eigenschaften und Ereignisse von Code aus nicht zugegriffen werden kann, wenn die entsprechenden Zugriffsrechte nicht erteilt wurden. Die aktuelle Zugriffsrechte Ebene kann mithilfe von **IWMPSettings2. mediaaccessrights** abgerufen werden.

Anwendungen, die auf dem Computer des Benutzers ausgeführt werden, müssen diese Methode nicht verwenden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMPSettings2-Schnittstelle (VB und c#)**](iwmpsettings2--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. mediaaccessrights (VB und c#)**](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





