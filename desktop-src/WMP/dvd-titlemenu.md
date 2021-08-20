---
title: DVD.titleMenu-Methode
description: Die titleMenu-Methode beendet die Titelwiedergabe und zeigt das Titelmenü an.
ms.assetid: 3be3e7cd-5969-4051-ae63-ff070a19fe51
keywords:
- titleMenu-Windows Media Player
- titleMenu-Methode Windows Media Player , DVD-Klasse
- DVD-Klasse Windows Media Player , titleMenu-Methode
topic_type:
- apiref
api_name:
- DVD.titleMenu
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1954ea52d5a67dc502278c7f1e821a06c4e2b849dc4040e690275b6d1b0ef0bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996880"
---
# <a name="dvdtitlemenu-method"></a>DVD.titleMenu-Methode

Die **titleMenu-Methode** beendet die Titelwiedergabe und zeigt das Titelmenü an.

## <a name="syntax"></a>Syntax


```JScript
DVD.titleMenu()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Jede DVD wird anders verfasst. Die DVD muss ein Menü enthalten, damit diese Methode funktioniert. Einige DVDs werden so verfasst, dass die **methoden topMenu** und **titleMenu** das gleiche Menü öffnen. Die **titleMenu-Methode** ruft in der Regel das Titelmenü auf, kann aber stattdessen das obere Menü aufrufen, wenn kein Titelmenü verfügbar ist.

**Windows Media Player 10 Mobile:** Diese Methode ist immer erfolgreich, führt jedoch nicht den beabsichtigten Vorgang aus.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                               |
| Version<br/>                  | Windows Media Player für Windows XP oder höher.<br/>                           |
| DLL<br/>                      | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DVD-Objekt**](dvd-object.md)
</dt> <dt>

[**DVD.topMenu**](dvd-topmenu.md)
</dt> </dl>

 

 





