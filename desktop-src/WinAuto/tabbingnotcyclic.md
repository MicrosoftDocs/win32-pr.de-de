---
title: Tabbingnotzyklische
description: Tabbingnotzyklische
ms.assetid: F6BCC613-1EA1-438C-AC09-8A282870E021
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e08fd2e9f6613e07840f432b646c1bdc06a34b5f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039213"
---
# <a name="tabbingnotcyclic"></a>Tabbingnotzyklische

## <a name="text"></a>Text

Die Tabstopps in dieser Anwendung sind nicht zyklisch. Die vorwärts-oder rückwärts {0} zeitablaufzeiten werden nicht an dasselbe Steuerelement zurückgegeben.

## <a name="type"></a>type

Fehler

## <a name="description"></a>BESCHREIBUNG

Bei Verwendung der Standardtastatur Navigation (Tab oder UMSCHALT + TAB) ist es nicht möglich, die Elementstruktur des Überprüfungs Ziels zu durchlaufen, bis das Start Element zum Endelement (mit der gleichen Anzahl von Tastatureingaben) wird, indem die Richtung des Durchlaufs umgekehrt wird. Wenn z. b. die x-Zeiten der Tabulator Taste (Tab) von Element a (0) zu Element a (x) und dann nach unten (UMSCHALT + TAB) x nicht angezeigt wird, führt das Element a (0) nicht zum Fokus.

Dieses Problem bewirkt, dass Personen, die sich auf einen Bildschirm oder eine Tastatur für die Navigation verlassen, Probleme verursachen, da es keine vorhersagbare Möglichkeit gibt, zu einem Steuerelement zurückzukehren, nachdem es besucht wurde.

## <a name="possible-causes"></a>Mögliche Ursachen

-   Das Element oder das übergeordnete Element ist ein benutzerdefiniertes Steuerelement, das die Tabstopps nicht korrekt implementiert. Beispielsweise ist die Eigenschaft MSAA State nicht ordnungsgemäß festgelegt.
-   Einige Anwendungen, z. b. der Editor, weisen dieses Verhalten Innately auf.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Richtlinien zur Gestaltung einer tastaturgesteuerten Benutzeroberfläche](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> </dl>

 

 