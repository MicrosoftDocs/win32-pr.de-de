---
title: DVD. topmenu-Methode
description: Die topmenu-Methode beendet die Titel Wiedergabe und zeigt das obere Menü (oder das Stamm Menü) für den aktuellen Titel an.
ms.assetid: 9998e8d1-e5e7-4003-bf27-da319a1a3058
keywords:
- topmenu-Methoden Fenster Media Player
- topmenu-Methode, Windows Media Player, DVD-Klasse
- DVD-Klasse, Windows Media Player, topmenu-Methode
topic_type:
- apiref
api_name:
- DVD.topMenu
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2be2b0fdafb10039b24f1d77e65f4b105889da85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477379"
---
# <a name="dvdtopmenu-method"></a>DVD. topmenu-Methode

Die **topmenu** -Methode beendet die Titel Wiedergabe und zeigt das obere Menü (oder das Stamm Menü) für den aktuellen Titel an.

## <a name="syntax"></a>Syntax


```JScript
DVD.topMenu()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Jede DVD wird unterschiedlich verfasst. Die DVD muss ein Menü enthalten, damit diese Methode funktioniert. Einige DVDs werden so erstellt, dass die **topmenu** -und **titlemenu** -Methoden dasselbe Menü öffnen. Die **topmenu** -Methode ruft normalerweise das Top-Menü (oder das Stamm Menü) auf, aber es kann stattdessen das Titelmenü aufrufen, wenn kein Stamm Menü verfügbar ist.

**Windows Media Player 10 Mobile:** Diese Methode ist immer erfolgreich, führt jedoch nicht den beabsichtigten Vorgang aus.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                               |
| Version<br/>                  | Windows Media Player für Windows XP oder höher.<br/>                           |
| DLL<br/>                      | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**DVD-Objekt**](dvd-object.md)
</dt> <dt>

[**DVD. titlemenu**](dvd-titlemenu.md)
</dt> </dl>

 

 





