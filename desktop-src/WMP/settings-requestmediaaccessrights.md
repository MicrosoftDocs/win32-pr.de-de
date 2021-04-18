---
title: Settings. requestmediaaccessrights-Methode
description: Die requestmediaaccessrights-Methode fordert eine angegebene Zugriffsebene auf die Bibliothek an. | Settings. requestmediaaccessrights-Methode
ms.assetid: 076b749b-9b25-483c-aa1f-60fc4367e4e0
keywords:
- requestmediaaccessrights-Methode, Windows Media Player
- requestmediaaccessrights-Methode, Windows Media Player, Settings-Klasse
- Einstellungs Klasse Windows Media Player, requestmediaaccessrights-Methode
topic_type:
- apiref
api_name:
- Settings.requestMediaAccessRights
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abfeed45666ee1f63bf995b211030b0b840c4279
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351297"
---
# <a name="settingsrequestmediaaccessrights-method"></a>Settings. requestmediaaccessrights-Methode

Die **requestmediaaccessrights** -Methode fordert eine angegebene Zugriffsebene auf die Bibliothek an.

## <a name="syntax"></a>Syntax


```JScript
bRetVal = Settings.requestMediaAccessRights(
  access
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Zugriff* \[ in\]
</dt> <dd>

**Zeichenfolge** , die die gewünschte Zugriffsrechte Ebene angibt. Enthält einen der folgenden Werte.



| Zeichenfolge | Beschreibung                      |
|--------|----------------------------------|
| none   | Nur die aktuellen Element Zugriffsrechte. |
| Lesen   | Nur Lese Zugriffsrechte.         |
| Voll   | Lese-/Schreibzugriffsrechte.        |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen **booleschen** Wert zurück, der angibt, ob die angeforderten Zugriffsrechte erteilt wurden.

## <a name="remarks"></a>Bemerkungen

Eine Webseite muss zuerst die Berechtigung des Benutzers anfordern, Informationen aus der Bibliothek zu lesen oder Daten in die Bibliothek zu schreiben. Beim Aufrufen dieser Methode wird der Benutzer zu einem Dialogfeld aufgefordert, das die angegebene Berechtigungsebene anfordert. Dies bedeutet, dass auf bestimmte Methoden, Eigenschaften und Ereignisse von Code aus nicht zugegriffen werden kann, wenn die entsprechenden Zugriffsrechte nicht erteilt wurden. Die aktuelle Zugriffsrechte Ebene kann mithilfe von *Einstellungen* abgerufen werden. **mediaaccessrights**.

**Windows Media Player 10 Mobile**: Diese Methode gibt immer " **true**" zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 9 oder höher.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Einstellungs Objekt**](settings-object.md)
</dt> <dt>

[**Settings. mediaaccessrights**](settings-mediaaccessrights.md)
</dt> </dl>

 

 





