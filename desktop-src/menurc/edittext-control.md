---
title: EDITTEXT-Steuerelement
description: Definiert ein Bearbeitungssteuer steuerelement, das zur EDIT-Klasse gehört.
ms.assetid: 9dc4be90-9503-4c97-813d-db246869ba3c
keywords:
- EDITTEXT-Steuerelementmenüs und andere Ressourcen
topic_type:
- apiref
api_name:
- EDITTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b287f01b89aaa3e378309e8f98f777acc475bcca962557305021aaf471926ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847390"
---
# <a name="edittext-control"></a>EDITTEXT-Steuerelement

Definiert ein Bearbeitungssteuer steuerelement, das zur EDIT-Klasse gehört. Es wird ein rechteckiger Bereich erstellt, in dem der Benutzer Text eingeben und bearbeiten kann. Das Steuerelement zeigt einen Cursor an, wenn der Benutzer darauf klickt. Der Benutzer kann dann mithilfe der Tastatur Text eingeben oder den vorhandenen Text bearbeiten. Zu den Bearbeitungsschlüsseln gehören die Tasten BACKSPACE und DELETE. Der Benutzer kann auch die Maus verwenden, um zu löschende Zeichen auszuwählen oder den Ort auszuwählen, an dem neue Zeichen eingefügt werden sollen.

``` syntax
EDITTEXT id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*Stil*
</dt> <dd>

Steuerelementstile. Dieser Wert kann eine Kombination aus den Bearbeitungsklassenstilen und den folgenden Stilen sein: **WS \_ TABSTOP,** **WS \_ GROUP,** **WS \_ VSCROLL,** **WS \_ HSCROLL** und **WS \_ DISABLED**.

Wenn Sie keinen Stil angeben, ist der Standardstil `ES_LEFT | WS_BORDER | WS_TABSTOP` .

</dd> </dl>

Weitere Informationen zur allgemeinen Syntax einer Steuerelement-Anweisung finden Sie unter [Allgemeine Steuerelementparameter](common-control-parameters.md).

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die Verwendung der **EDITTEXT-Anweisung** veranschaulicht:

``` syntax
EDITTEXT  3, 10, 10, 100, 10
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Bearbeiten von Steuerelementen](../controls/about-edit-controls.md)
</dt> </dl>

 

 