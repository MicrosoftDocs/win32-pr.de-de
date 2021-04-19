---
title: Extern. cancelnavigate-Methode
description: In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. | Extern. cancelnavigate-Methode
ms.assetid: e65d64fb-292c-4413-9727-b24609e78d68
keywords:
- cancelnavigate-Methode, Windows-Media Player
- cancelnavigate-Methode, Windows Media Player, externe Klasse
- Externe Klasse, Windows Media Player, cancelnavigate-Methode
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
ms.openlocfilehash: 55a6cbc0f749fd6ca33d78dfaed1d256634eb9c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370263"
---
# <a name="externalcancelnavigate-method"></a>Extern. cancelnavigate-Methode

> [!Note]  
> In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online-Speicher Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

Die **cancelnavigate** -Methode informiert Windows Media Player, dass eine neue Ermittlungs Seite auch dann nicht angezeigt werden soll, wenn sich die Ansicht im Player geändert hat.

## <a name="syntax"></a>Syntax


```JScript
External.cancelNavigate()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn sich die Ansicht in Windows Media Player ändert, ruft der Player das Plug-in des Online Stores auf, um zu bestimmen, welche Ermittlungs Seite als nächstes angezeigt werden soll. In einigen Fällen kann es jedoch sein, dass der Player im Online Shop weiterhin die vorhandene Ermittlungs Seite anzeigt. Der folgende Prozess bestimmt, ob der Spieler eine neue Ermittlungs Seite anzeigt:

1.  Eine Aktion durch den Benutzer, entweder in der Benutzeroberfläche des Players oder auf der Ermittlungs Seite, fordert an, dass der Spieler seine Ansicht ändert.
2.  Der Player Ruft die [GetTemplate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-gettemplate) -Methode des Plug-Ins auf, um zu bestimmen, welche Ermittlungs Seite als nächstes angezeigt werden soll. Der Player speichert die URL der neuen Ermittlungs Seite, zeigt jedoch derzeit nicht die neue Ermittlungs Seite an.
3.  Der Player löst das [OnViewChange](external-onviewchange-event.md) -Ereignis aus.
4.  Wenn der **OnViewChange** -Ereignishandler auf der Ermittlungs Seite **cancelnavigate** aufruft, zeigt der Spieler nicht die neue Ermittlungs Seite an (in Schritt 2 festgelegt). Stattdessen wird die vorhandene Ermittlungs Seite weiterhin angezeigt. Wenn der **OnViewChange** -Ereignishandler nicht **cancelnavigate** aufruft, zeigt der Spieler die neue Ermittlungs Seite an.

Angenommen, der Spieler zeigt derzeit die Ansicht eines Albums an, bei dem eine bestimmte Spur ausgewählt ist. Außerdem wird angenommen, dass es sich bei der aktuellen Ermittlungs Seite um die Seite handelt, die das gesamte Album darstellt. Wenn der Benutzer auf eine andere Spur desselben Albums klickt, wird die Ansicht des Players leicht geändert, um anzuzeigen, dass die neue Spur ausgewählt ist. Es ist jedoch nicht erforderlich, eine neue Ermittlungs Seite anzuzeigen. Die Suchseite, die das gesamte Album darstellt, ist immer noch die geeignete Seite, die der Player anzeigen kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Externes Objekt für den Typ 1-Online Speicher**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**Extern. changeviewonlinelist**](external-changeviewonlinelist.md)
</dt> <dt>

[**Extern. OnViewChange**](external-onviewchange-event.md)
</dt> </dl>

 

 





