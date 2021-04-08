---
title: Festlegen von Eigenschaften für animierte oder verschiebenden Objekten
description: Verwenden Sie für Animations Steuerelemente, z. b. das beim Kopieren von Dateien angezeigte Animations Steuerelement, die \_ Objekt Rolle "Rollen System \_ Animation"
ms.assetid: 8c5ebbc3-4066-452b-8f37-2fb595adea53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1551899305968471bf1425b5cc043be8329c2bd4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037423"
---
# <a name="setting-properties-for-animated-or-moving-objects"></a>Festlegen von Eigenschaften für animierte oder verschiebenden Objekten

Verwenden Sie für Animations Steuerelemente, z. b. das beim Kopieren von Dateien angezeigte Animations Steuerelement, die Objekt Rolle " [**Rollen \_ System \_ Animation**](object-roles.md) " Verwenden Sie für Grafiken, die gelegentlich animiert werden, die [**Rollen \_ System- \_ Grafik**](object-roles.md) Objekt Rolle, wobei der [**Zustand**](state-property.md) auf " [**Zustands \_ System \_ animiert**](object-state-constants.md)" festgelegt ist.

Verwenden Sie [**das \_ \_ animierte Flag "State System**](object-state-constants.md) ", um ein Objekt zu markieren, dessen Darstellung sich schnell ändert. Clients verwenden dieses Flag, um zu vermeiden, dass Benutzer wiederholt benachrichtigt werden, was eigentlich eine einzelne Reihe von visuellen Änderungen ist.

Ein Beispiel hierfür ist der Marquee-Text, der bei einem Bildlauf auf dem Bildschirm progressiv offengelegt wird. Solchen Objekten wird das-Attribut des [**Zustands \_ Systems \_ animiert**](object-state-constants.md). In den meisten Fällen gibt die [**Wert**](value-property.md) Zeichenfolge des Objekts den gesamten Text wieder, auch wenn der Teil derzeit nicht sichtbar ist. Es wird nicht empfohlen, die **Wert** Zeichenfolge häufig so zu ändern, dass Sie dem derzeit sichtbaren Text entspricht, da Sie zu viele [**Ereignis \_ Objekt- \_ ValueChange**](event-constants.md) -Ereignisse liefert, die keine nützlichen Informationen vermitteln.

Beispielsweise in einem Fenster, das einen rechteckigen Bereich enthält, der das Wort "yes!" anzeigt. bei einem Wechsel in einem Abbildung-acht-Muster ist die [**Rolle**](role-property.md) eine [**Grafik des Rollen \_ \_ Systems**](object-roles.md), die [**value**](value-property.md) -Eigenschaft ist die angezeigte Zeichenfolge, die [**Location**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation) -Eigenschaft ist das umschließende Rechteck um den Text, und das Attribut des animierten Attributs des [**Zustands \_ Systems \_**](object-state-constants.md) wird festgelegt. Die [**Beschreibung**](description-property.md) lautet "Word ' yes!". bewegt sich in einem Abbildung-acht-Muster um den Bildschirm. " Der Server generiert nur [**Ereignis \_ Objekt- \_ StateChange**](event-constants.md) -Ereignisse, wenn das Objekt die Animation startet oder beendet.

 

 




