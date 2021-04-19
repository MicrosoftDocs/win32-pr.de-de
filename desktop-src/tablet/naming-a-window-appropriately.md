---
description: Übersicht über das Ordnungs gerechte Benennen eines Fensters und Festlegen der Fenster Beschriftung für den Tablet PC.
ms.assetid: 9d064188-53a1-4cb5-b516-99610d7b8134
title: Entsprechendes Benennen eines Fensters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaee320f621acf834d7c0ec5978a9e42f0811e31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356931"
---
# <a name="naming-a-window-appropriately"></a>Entsprechendes Benennen eines Fensters

Weisen Sie jedem Fenster eine benutzerfreundliche Beschriftung zu, auch wenn das Fenster oder die Beschriftung unsichtbar ist. Dies ermöglicht es der Sprachfunktion, das Fenster und die Fenster Hierarchie zu identifizieren. Diese Empfehlung gilt für alle Fenster: Fenster der obersten Ebene mit sichtbaren Frames. untergeordnete Fenster, z. b. Gleit Komma Zahlen; benutzerdefinierte Steuerelemente; Symbolleisten und Bereiche innerhalb eines Fensters, wenn Sie als untergeordnete Fenster implementiert werden.

Es gibt drei Möglichkeiten, die Fenster Beschriftung festzulegen:

-   Legen Sie die Zeichenfolge im Ressourcen Skript fest, wenn Sie [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) oder verwandte Funktionen aufrufen.
-   Aufrufen der [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta) -Funktion.
-   Definieren Sie den Namen der Steuerelemente in Dialogfeldern, indem Sie die unter Benennen von Steuer [Elementen in Dialogfeldern](naming-controls-in-dialog-boxes.md)beschriebenen Verfahren verwenden. Dies ist die einzige Methode für die Bezeichnung eines Bearbeitungs Steuer Elements, da der Inhalt der Steuerelemente durch Festlegen der systeminternen Bezeichnung Steuerelemente geändert wird.

Sie können die Beschriftung entweder mithilfe von Microsoft Active Accessibility oder der WM \_ gettext-Nachricht Abfragen.

Weitere Informationen zum Abfragen der Beschriftung mithilfe Active Accessibility finden Sie im Abschnitt zur [Barrierefreiheit](/windows/desktop/accessibility) .

 

 
