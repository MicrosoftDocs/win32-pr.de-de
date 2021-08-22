---
title: External.cancelNavigate-Methode
description: Hinweis In diesem Thema werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. | External.cancelNavigate-Methode
ms.assetid: e65d64fb-292c-4413-9727-b24609e78d68
keywords:
- cancelNavigate-Windows Media Player
- cancelNavigate-Methode Windows Media Player , Externe Klasse
- Externe Klasse Windows Media Player , cancelNavigate-Methode
topic_type:
- apiref
api_name:
- External.cancelNavigate
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 152594a427282a27c493f33f648b8a889a855f40a5fb13de69b7cc342099eed2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649430"
---
# <a name="externalcancelnavigate-method"></a>External.cancelNavigate-Methode

> [!Note]  
> In diesem Thema werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt.

 

Die **cancelNavigate-Methode** informiert Windows Media Player, dass keine neue Ermittlungsseite angezeigt werden soll, obwohl sich die Ansicht im Player geändert hat.

## <a name="syntax"></a>Syntax


```JScript
External.cancelNavigate()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Wenn sich die Ansicht in Windows Media Player, ruft der Player das Plug-In des Onlineshops auf, um zu bestimmen, welche Ermittlungsseite als Nächstes angezeigt werden soll. In einigen Fällen möchte der Onlineshop jedoch möglicherweise, dass der Player weiterhin die vorhandene Ermittlungsseite anzeigen soll. Der folgende Prozess bestimmt, ob der Player eine neue Ermittlungsseite anzeigt:

1.  Eine Aktion des Benutzers, entweder auf der Benutzeroberfläche des Players oder auf der Ermittlungsseite, fordert an, dass der Player seine Ansicht ändert.
2.  Der Player ruft die [GetTemplate-Methode](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) des Plug-Ins auf, um zu bestimmen, welche Ermittlungsseite als Nächstes angezeigt werden soll. Der Player speichert die URL der neuen Ermittlungsseite, aber die neue Ermittlungsseite wird derzeit nicht angezeigt.
3.  Der Player löst das [OnViewChange-Ereignis](external-onviewchange-event.md) aus.
4.  Wenn der **OnViewChange-Ereignishandler** auf der Ermittlungsseite **cancelNavigate** aufruft, zeigt der Player die neue Ermittlungsseite (in Schritt 2 bestimmt) nicht an. Stattdessen wird weiterhin die vorhandene Ermittlungsseite angezeigt. Wenn der **OnViewChange-Ereignishandler** **cancelNavigate** nicht aufruft, zeigt der Player die neue Ermittlungsseite an.

Angenommen, der Player zeigt derzeit die Ansicht eines Albums an, für das ein bestimmter Titel ausgewählt ist. Gehen Sie außerdem davon aus, dass die aktuelle Ermittlungsseite die Seite ist, die das gesamte Album darstellt. Wenn der Benutzer auf einen anderen Titel als dasselbe Album klickt, ändert sich die Ansicht des Players geringfügig, um zu zeigen, dass der neue Titel ausgewählt ist. Es ist jedoch nicht notwendig, eine neue Ermittlungsseite anzuzeigen. Die Ermittlungsseite, die das gesamte Album darstellt, ist immer noch die geeignete Seite, auf der der Player angezeigt werden kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Externes Objekt für Onlinespeicher vom Typ 1**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External.changeViewOnlineList**](external-changeviewonlinelist.md)
</dt> <dt>

[**External.OnViewChange**](external-onviewchange-event.md)
</dt> </dl>

 

 





