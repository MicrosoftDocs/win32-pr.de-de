---
title: DVD. titlemenu-Methode
description: Die titlemenu-Methode beendet die Titel Wiedergabe und zeigt das Menü Titel an.
ms.assetid: 3be3e7cd-5969-4051-ae63-ff070a19fe51
keywords:
- titlemenu-Methode, Windows-Media Player
- titlemenu-Methode, Windows Media Player, DVD-Klasse
- DVD-Klasse, Windows Media Player, titlemenu-Methode
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
ms.openlocfilehash: e9351603d5307415f57610422a83d3586067bdcb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340588"
---
# <a name="dvdtitlemenu-method"></a>DVD. titlemenu-Methode

Die **titlemenu** -Methode beendet die Titel Wiedergabe und zeigt das Menü Titel an.

## <a name="syntax"></a>Syntax


```JScript
DVD.titleMenu()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Jede DVD wird unterschiedlich verfasst. Die DVD muss ein Menü enthalten, damit diese Methode funktioniert. Einige DVDs werden so erstellt, dass die **topmenu** -und **titlemenu** -Methoden dasselbe Menü öffnen. Die **titlemenu** -Methode ruft in der Regel das Titelmenü auf, aber es kann stattdessen das oberste Menü aufrufen, wenn kein Titel Menü verfügbar ist.

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

[**DVD. topmenu**](dvd-topmenu.md)
</dt> </dl>

 

 





