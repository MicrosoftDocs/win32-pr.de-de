---
title: Role-Eigenschaft
description: Die Role-Eigenschaft beschreibt das Benutzeroberflächen Element eines Objekts. Alle-Objekte unterstützen die Role-Eigenschaft.
ms.assetid: f6abf95b-a77a-406d-9ca0-4663adc8245f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f2b285d9242542f83c6b4478df93e888a7a23cd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339193"
---
# <a name="role-property"></a>Role-Eigenschaft

Die **Role** -Eigenschaft beschreibt das Benutzeroberflächen Element eines Objekts. Alle-Objekte unterstützen die **Role** -Eigenschaft.

In vielen Fällen ist die Rolle des Objekts offensichtlich. Beispielsweise verfügen Windows über die Rolle " [**Rollen \_ System \_**](object-roles.md) " und die Schaltflächen "Rollensystem" über die [**\_ \_ PUSHBUTTON**](object-roles.md) -Rolle.

Die **Role** -Eigenschaft wird durch Aufrufen von [**ibarrierefreie:: get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)abgerufen.

## <a name="identifying-an-objects-role"></a>Identifizieren der Rolle eines Objekts

Microsoft Active Accessibility stellt [Rollen Konstanten](object-roles.md)bereit, die in Oleacc. h definiert sind und die allgemeine Objekt Rollen identifizieren. Es wird empfohlen, dass Server Entwickler diese vordefinierten Rollen Werte verwenden. Wenn eine vordefinierte Rollen Konstante zurückgegeben wird, verwenden Clients die [**getroletext**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta) -Funktion, um eine lokalisierte Zeichenfolge abzurufen, die die Rolle beschreibt.

Verwenden Sie für Animations Steuerelemente wie das beim Kopieren von Dateien angezeigte Animations Steuerelement die [**\_ \_ Animation des Rollen Systems**](object-roles.md). Grafiken, die gelegentlich animiert werden, werden als [**Rollen \_ System- \_ Grafik**](object-roles.md) beschrieben, wobei die Eigenschaft [**State**](state-property.md) auf [**State \_ System \_ animiert**](object-state-constants.md)festgelegt ist.

Beachten Sie, dass einige Rollen nicht leicht zu beschreiben sind. Beispielsweise ermöglicht die Ansicht "großes Symbol" eines Ordners eine beliebige Anordnung von Symbolen, sodass seine Rolle als [**Rollen \_ System \_ Gruppierung**](object-roles.md)beschrieben wird. Oder ein Steuerelement, das Elemente in festgelegten Zeilen und Spalten bereitstellt, kann über die [**Rollen \_ System- \_ Tabellen**](object-roles.md) Rolle verfügen. Da eine Rolle verwendet wird, um das Verwendungs Modell an einen Endbenutzer zu übermitteln, ist es wichtig, die entsprechende Rolle zu verwenden. Wenn das Steuerelement z. b. wie eine Schaltfläche funktioniert, verwenden Sie das [**Rollen \_ System- \_ PUSHBUTTON**](object-roles.md).

 

 




