---
title: Einstellungen.requestMediaAccessRights-Methode
description: Die requestMediaAccessRights-Methode fordert eine angegebene Zugriffsebene auf die Bibliothek an. | Einstellungen.requestMediaAccessRights-Methode
ms.assetid: 076b749b-9b25-483c-aa1f-60fc4367e4e0
keywords:
- requestMediaAccessRights-Methode Windows Media Player
- requestMediaAccessRights-Methode Windows Media Player , Einstellungen-Klasse
- Einstellungen-Klasse Windows Media Player , requestMediaAccessRights-Methode
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
ms.openlocfilehash: 1e157e7b4495c8d90964d62a9045eebb202126906f0022e97c4983220e47ac03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118569311"
---
# <a name="settingsrequestmediaaccessrights-method"></a>Einstellungen.requestMediaAccessRights-Methode

Die **requestMediaAccessRights-Methode** fordert eine angegebene Zugriffsebene auf die Bibliothek an.

## <a name="syntax"></a>Syntax


```JScript
bRetVal = Settings.requestMediaAccessRights(
  access
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Zugriff* \[ In\]
</dt> <dd>

**Zeichenfolge,** die die gewünschte Zugriffsrechteebene angibt. Enthält einen der folgenden Werte.



| Zeichenfolge | Beschreibung                      |
|--------|----------------------------------|
| Keine   | Nur aktuelle Elementzugriffsrechte. |
| Lesen   | Nur Lesezugriffsrechte.         |
| Voll   | Lese-/Schreibzugriffsrechte.        |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt einen **booleschen** Wert zurück, der angibt, ob die angeforderten Zugriffsrechte gewährt wurden.

## <a name="remarks"></a>Hinweise

Eine Webseite muss zunächst die Berechtigung des Benutzers anfordern, Informationen aus der Bibliothek zu lesen oder Daten in die Bibliothek zu schreiben. Beim Aufrufen dieser Methode wird der Benutzer mit einem Dialogfeld aufgefordert, in dem die angegebene Berechtigungsebene angefordert wird. Dies bedeutet, dass der Code auf bestimmte Methoden, Eigenschaften und Ereignisse nicht zugreifen kann, wenn die entsprechenden Zugriffsrechte nicht erteilt wurden. Die aktuelle Zugriffsrechteebene kann mit *Einstellungen* abgerufen werden. **mediaAccessRights**.

**Windows Media Player 10 Mobile:** Diese Methode gibt immer **true** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player serie 9 oder höher.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Einstellungen Objekt**](settings-object.md)
</dt> <dt>

[**Einstellungen.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> </dl>

 

 





