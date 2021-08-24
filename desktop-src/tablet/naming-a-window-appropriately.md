---
description: Übersicht über die richtige Benennung eines Fensters und das Festlegen der Fensterbeschriftung für den Tablet PC.
ms.assetid: 9d064188-53a1-4cb5-b516-99610d7b8134
title: Benennen eines Fensters entsprechend
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41f2109568306e8817c518eecd8761ab00a2b1ecb8c54d4388b78e3eb456278d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883400"
---
# <a name="naming-a-window-appropriately"></a>Benennen eines Fensters entsprechend

Weisen Sie jedem Fenster eine benutzerfreundliche Beschriftung zu, auch wenn das Fenster oder seine Beschriftung unsichtbar ist. Dadurch kann die Sprachfunktion das Fenster und die Fensterhierarchie identifizieren. Diese Empfehlung gilt für alle Fenster: Fenster der obersten Ebene mit sichtbaren Frames; untergeordnete Fenster, z. B. unverankerte Paletten; benutzerdefinierte Steuerelemente; Symbolleisten; und bereiche innerhalb eines Fensters, wenn sie als untergeordnete Fenster implementiert werden.

Es gibt drei Möglichkeiten, die Fensterbeschriftung festzulegen:

-   Legen Sie die Zeichenfolge im Ressourcenskript fest, wenn [**Sie CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) oder verwandte Funktionen aufrufen.
-   Rufen Sie die [**SetWindowText-Funktion**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta) auf.
-   Definieren Sie den Namen von Steuerelementen in Dialogfeldern mithilfe der unter Benennen von [Steuerelementen in Dialogfeldern beschriebenen](naming-controls-in-dialog-boxes.md)Verfahren. Dies ist die einzige Methode zum Bezeichnen eines Bearbeitungssteuerelements, da das Festlegen der systeminternen Bezeichnung der Steuerelemente den Inhalt der Steuerelemente ändert.

Sie können die Beschriftung abfragen, indem Sie entweder Microsoft Active Accessibility oder die WM \_ GETTEXT-Nachricht verwenden.

Weitere Informationen zum Abfragen der Beschriftung mit Active Accessibility finden Sie im Abschnitt [Barrierefreiheit.](/windows/desktop/accessibility)

 

 
