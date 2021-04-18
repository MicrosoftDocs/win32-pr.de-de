---
title: Settings. mediaaccessrights
description: Die mediaaccessrights-Eigenschaft ruft einen Wert ab, der die Rechte angibt, die derzeit für den Bibliotheks Zugriff gewährt werden.
ms.assetid: 744e696d-29d2-44b1-a296-5b5d007b689f
keywords:
- Settings. mediaaccessrights-Fenster Media Player
topic_type:
- apiref
api_name:
- Settings.mediaAccessRights
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36bcfb667a1aa09e84ae90324736291d421a3941
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368499"
---
# <a name="settingsmediaaccessrights"></a>Settings. mediaaccessrights

Die **mediaaccessrights** -Eigenschaft ruft einen Wert ab, der die Rechte angibt, die derzeit für den Bibliotheks Zugriff gewährt werden.

## <a name="syntax"></a>Syntax

Player. Settings. mediaaccessrights

## <a name="possible-values"></a>Mögliche Werte

Diese Eigenschaft ist eine schreibgeschützte **Zeichenfolge**.



| Wert | BESCHREIBUNG                      |
|-------|----------------------------------|
| none  | Nur die aktuellen Element Zugriffsrechte. |
| Lesen  | Nur Lese Zugriffsrechte.         |
| Voll  | Lese-/Schreibzugriffsrechte.        |



 

## <a name="remarks"></a>Bemerkungen

Eine Webseite muss zuerst die Berechtigung des Benutzers anfordern, Informationen aus der Bibliothek zu lesen oder Daten in die Bibliothek zu schreiben. Dies bedeutet, dass auf bestimmte Methoden, Eigenschaften und Ereignisse von Code aus nicht zugegriffen werden kann, wenn die entsprechenden Zugriffsrechte nicht erteilt wurden. Zum Abrufen von Zugriffsrechten Ruft die Anwendung *Einstellungen* auf. **requestmediaaccessrights**, wobei ein Parameter übergeben wird, der die gewünschte Zugriffsrechte Ebene angibt.

**Windows Media Player 10 Mobile**: Diese Eigenschaft gibt immer **Full** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 9 oder höher.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Einstellungs Objekt**](settings-object.md)
</dt> <dt>

[**Settings. requestmediaaccessrights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





