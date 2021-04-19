---
title: Cdrom. eject-Methode
description: Die Auswerfen-Methode fügt die CD oder DVD vom Laufwerk ein. | Cdrom. eject-Methode
ms.assetid: f43c7f10-7de2-488c-833a-ecd3ac21744b
keywords:
- Auswerfen-Methode, Windows-Media Player
- Auswerfen-Methode, Windows Media Player, cdrom-Klasse
- Cdrom-Klasse, Windows Media Player, Auswerfen-Methode
topic_type:
- apiref
api_name:
- Cdrom.eject
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78326ca57dcf097344fc073681fae772222ea9ad
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106363922"
---
# <a name="cdromeject-method"></a>Cdrom. eject-Methode

Die **auswerfen** -Methode fügt die CD oder DVD vom Laufwerk ein.

## <a name="syntax"></a>Syntax


```JScript
Cdrom.eject()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn die Laufwerks Tür geöffnet ist, schließt diese Methode die Tür.

Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).

**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein HTML-Schaltflächen Element erstellt, das *CDROM* verwendet. **auswerfen** zum Öffnen der Tür des Laufwerks mit dem laufwerkspezifizierer Index NULL. Das **Player** -Objekt wurde mit ID = "Player" erstellt.


```JScript
<INPUT TYPE = "BUTTON"
       NAME = "EJECTBUTTON"
       VALUE = "EJECT"
       OnClick =  "Player.cdromCollection.item(0).eject()"
>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Version<br/>                  | Windows Media Player Version 7,0 oder höher.<br/>                              |
| DLL<br/>                      | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cdrom-Objekt**](cdrom-object.md)
</dt> <dt>

[**Player. playstate**](player-playstate.md)
</dt> <dt>

[**Settings. mediaaccessrights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestmediaaccessrights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





