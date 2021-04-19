---
title: Design. showerrordialog
description: Die showerrordialog-Methode zeigt das Standardfehler Dialogfeld an.
ms.assetid: cec9ecfd-6665-4b0a-a09c-49120d557a80
keywords:
- Design. showerrordialog-Fenster Media Player
topic_type:
- apiref
api_name:
- THEME.showErrorDialog
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0cdc1f9df13ec460ce780507e1bde38a2996f915
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367039"
---
# <a name="themeshowerrordialog"></a>Design. showerrordialog

Die **showerrordialog** -Methode zeigt das Standardfehler Dialogfeld an.

``` syntax
        theme.showErrorDialog()
```

## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn **Settings. enableerrordialogs** false ist, kann diese Methode verwendet werden, um das Fehler Dialogfeld Programm gesteuert anzuzeigen. Wenn in der Fehler Warteschlange keine Fehler vorliegen, wird das Fehler Dialogfeld nicht angezeigt.

Für Windows Media Player 9-Serie oder höher muss diese Methode vom Fehler Ereignishandler aufgerufen werden. Windows Media Player 9 oder höher löscht die Fehler Warteschlange für Skins, nachdem das Fehler Ereignis ausgelöst wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Design-Element**](theme-element.md)
</dt> <dt>

[**Settings. enableerrordialogs**](settings-enableerrordialogs.md)
</dt> </dl>

 

 





