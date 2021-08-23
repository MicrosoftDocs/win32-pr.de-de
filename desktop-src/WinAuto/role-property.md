---
title: Role-Eigenschaft
description: Die Role-Eigenschaft beschreibt das Benutzeroberflächenelement eines Objekts. Alle -Objekte unterstützen die Role-Eigenschaft.
ms.assetid: f6abf95b-a77a-406d-9ca0-4663adc8245f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2881b301537e9a25dabb260b84bc889cef4e4a6f9f6a5a2c8fab540d78daf8c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133723"
---
# <a name="role-property"></a>Role-Eigenschaft

Die **Role-Eigenschaft** beschreibt das Benutzeroberflächenelement eines Objekts. Alle -Objekte unterstützen die **Role-Eigenschaft.**

In vielen Fällen ist die Rolle des Objekts offensichtlich. Beispielsweise verfügen Fenster über die Rolle [**ROLE \_ SYSTEM \_ WINDOW,**](object-roles.md) und Pushschaltflächen verfügen über die Rolle [**ROLE SYSTEM \_ \_ PUSHBUTTON.**](object-roles.md)

Die **Role-Eigenschaft** wird durch Aufrufen von [**IAccessible::get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)abgerufen.

## <a name="identifying-an-objects-role"></a>Identifizieren der Rolle eines Objekts

Microsoft Active Accessibility stellt in oleacc.h definierte [Rollenkonstanten](object-roles.md)bereit, die allgemeine Objektrollen identifizieren. Es wird empfohlen, dass Serverentwickler diese vordefinierten Rollenwerte verwenden. Wenn eine vordefinierte Rollenkonstante zurückgegeben wird, verwenden Clients die [**GetRoleText-Funktion,**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) um eine lokalisierte Zeichenfolge abzurufen, die die Rolle beschreibt.

Verwenden Sie für Animationssteuerelemente, z. B. das Beim Kopieren von Dateien angezeigte Animationssteuerelement, [**ROLE \_ SYSTEM \_ ANIMATION**](object-roles.md). Grafiken, die gelegentlich animiert werden, werden als [**ROLE \_ SYSTEM \_ GRAPHIC**](object-roles.md) beschrieben, wobei die [**State-Eigenschaft**](state-property.md) auf STATE SYSTEM ANIMATED festgelegt [**\_ \_ ist.**](object-state-constants.md)

Beachten Sie, dass einige Rollen nicht einfach zu beschreiben sind. Beispielsweise ermöglicht die Ansicht mit großen Symbolen eines Ordners die willkürliche Anordnung von Symbolen, sodass seine Rolle als [**ROLE \_ SYSTEM \_ GROUPING**](object-roles.md)beschrieben werden kann. Ein Steuerelement, das Elemente in festen Zeilen und Spalten bereitstellt, kann auch über die Rolle [**ROLE \_ SYSTEM TABLE \_ verfügen.**](object-roles.md) Da eine Rolle verwendet wird, um das Verwendungsmodell einem Endbenutzer mitzuteilen, ist es wichtig, die entsprechende Rolle zu verwenden. Wenn ihr Steuerelement beispielsweise wie eine Schaltfläche fungiert, verwenden Sie [**ROLE \_ SYSTEM \_ PUSHBUTTON**](object-roles.md).

 

 




