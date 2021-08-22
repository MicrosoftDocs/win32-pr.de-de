---
title: Corpora.eject-Methode
description: Die Eject-Methode wirft die CD oder DVD vom Laufwerk aus. | Corpora.eject-Methode
ms.assetid: f43c7f10-7de2-488c-833a-ecd3ac21744b
keywords:
- Eject-Methode Windows Media Player
- Eject-Methode Windows Media Player , Corpora-Klasse
- Corpora-Klasse Windows Media Player , Eject-Methode
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
ms.openlocfilehash: c9bd1c5a7a79c2a9b76b3a7a1997c43713fe0f3c1ae28e635a235feb82d214ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997680"
---
# <a name="cdromeject-method"></a>Corpora.eject-Methode

Die **Eject-Methode** wirft die CD oder DVD vom Laufwerk aus.

## <a name="syntax"></a>Syntax


```JScript
Cdrom.eject()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Wenn die Laufwerktür geöffnet ist, schließt diese Methode die Tür.

Um diese Methode zu verwenden, ist Lesezugriff auf die Bibliothek erforderlich. Weitere Informationen finden Sie unter [Bibliothekszugriff.](library-access.md)

**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein HTML-Schaltflächenelement erstellt, das *Credo* verwendet. **Werfen Sie aus,** um die Tür des Laufwerks zu öffnen, das über den Index 0 (null) des Laufwerks verfügt. Das **Player-Objekt** wurde mit der ID = "Player" erstellt.


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
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                               |
| Version<br/>                  | Windows Media Player Version 7.0 oder höher.<br/>                              |
| DLL<br/>                      | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Chole-Objekt**](cdrom-object.md)
</dt> <dt>

[**Player.playState**](player-playstate.md)
</dt> <dt>

[**Einstellungen.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Einstellungen.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





