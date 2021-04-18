---
description: Ab Windows Vista ersetzt TextInputPanel den "tabinputpanel", um die Bildschirmdarstellung und das Verhalten des Tablet-Eingabe Bereichs zu steuern. in den folgenden Abschnitten wird beschrieben, wie Sie den Eingabebereich mithilfe der Anwendungs Programmierschnittstellen für den Text Eingabebereich programmieren. TextInputPanel für Benutzer von "tzinputpanelusing" im Eingabebereich "Automatische vervollstänteaktivierung" Textkorrektur für benutzerdefinierte frei Hand Collector. der Texteingabebereich wird in eine ausführbare Datei mit dem Namen "TabTip.exe" implementiert. Wenn Sie TabTip.exe mit dem/SeekDesktop-Parameter ausführen, wird versucht, eine reduzierte Funktionalitäts Version des Eingabe Panels auf einem nicht dem Standard interaktiven Desktop auszuführen Bei den meisten erstellten Desktops wird der Eingabebereich automatisch in diesem Modus ausgeführt. Dieser Parameter bietet die Möglichkeit, Sie in ungewöhnlichen Anwendungsszenarien zu starten, die andernfalls den automatischen Start verhindern. Wenn der Eingabebereich bereits auf dem Desktop ausgeführt wird, hat dieser Parameter keine Auswirkungen, und die Instanz von TabTip.exe wird sofort beendet.
ms.assetid: af0a2946-88d0-4f2e-98ca-446398aeb6b8
title: Programmieren des Text Eingabe Panels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5e6b379a26199e602fc68402d77fa89fb4f8fbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351110"
---
# <a name="programming-the-text-input-panel"></a>Programmieren des Text Eingabe Panels

Ab Windows Vista ersetzt [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) das [**tabinputpanel**](peninputpanel-class.md) zum Steuern der Bildschirmdarstellung und des Verhaltens des Tablet-Eingabe Bereichs.

In den folgenden Abschnitten wird beschrieben, wie Sie den Eingabebereich mit dem Text Eingabe Panel-Anwendungs Programmierschnittstellen programmieren.

-   [TextInputPanel für Benutzer von "" in "".](textinputpanel-for-users-of-peninputpanel.md)
-   [Verwenden des Auto Vervollständigen-Eingabe Bereichs](using-input-panel-autocomplete.md)
-   [Aktivieren der Text Korrektur für benutzerdefinierte frei Hand Sammler](enabling-text-correction-for-custom-ink-collectors.md)

> [!Note]  
> Der Text Eingabebereich wird in eine ausführbare Datei mit dem Namen TabTip.exe implementiert. Wenn Sie TabTip.exe mit dem */SeekDesktop* -Parameter ausführen, wird versucht, eine reduzierte Funktionalitäts Version des Eingabe Panels auf einem [**nicht dem Standard**](/windows/win32/api/winuser/nf-winuser-createdesktopa)interaktiven Desktop auszuführen Bei den meisten erstellten Desktops wird der Eingabebereich automatisch in diesem Modus ausgeführt. Dieser Parameter bietet die Möglichkeit, Sie in ungewöhnlichen Anwendungsszenarien zu starten, die andernfalls den automatischen Start verhindern. Wenn der Eingabebereich bereits auf dem Desktop ausgeführt wird, hat dieser Parameter keine Auswirkungen, und die Instanz von TabTip.exe wird sofort beendet.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmieren des Eingabe Bereichs mithilfe der Klasse "pinputpanel"](programming-the-input-panel-using-the-peninputpanel-class.md)
</dt> </dl>

 

 
