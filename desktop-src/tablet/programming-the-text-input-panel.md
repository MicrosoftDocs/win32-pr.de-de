---
description: Ab Windows Vista ersetzt TextInputPanel das PenInputPanel zum Steuern der Darstellung und des Verhaltens des Tablet-Eingabebereichs auf dem Bildschirm. In den folgenden Abschnitten wird die Programmierung des Eingabebereichs mithilfe der Anwendungsprogrammierschnittstellen des Texteingabebereichs beschrieben. TextInputPanel für Benutzer von PenInputPanelUsing Input Panel AutoCompleteEnabling Text Correction for Custom Ink CollectorsNote The Text Input Panel is implemented in an executable file namens TabTip.exe. Beim Ausführen von TabTip.exe mit dem Parameter /SeekDesktop wird versucht, eine reduzierte Funktionalitätsversion des Eingabebereichs auf einem nicht standardmäßigen interaktiven Desktop auszuführen, wie mit CreateDesktop erstellt. Für die meisten erstellten Desktops wird der Eingabebereich automatisch bereits in diesem Modus ausgeführt. Dieser Parameter bietet die Möglichkeit, ihn in ungewöhnlichen Anwendungsszenarien zu starten, die andernfalls den automatischen Start verhindern. Wenn der Eingabebereich bereits auf dem Desktop ausgeführt wird, hat dieser Parameter keine Auswirkungen, und die Instanz von TabTip.exe wird sofort beendet.
ms.assetid: af0a2946-88d0-4f2e-98ca-446398aeb6b8
title: Programmieren des Texteingabebereichs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 366eb0a0d1770291ba2251247364fb68e14789d19fa053800ecaeec5ef4652d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118716124"
---
# <a name="programming-the-text-input-panel"></a>Programmieren des Texteingabebereichs

Ab Windows Vista ersetzt [**textInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) das [**PenInputPanel**](peninputpanel-class.md) zum Steuern der Darstellung und des Verhaltens des Tablet-Eingabebereichs auf dem Bildschirm.

In den folgenden Abschnitten wird die Programmierung des Eingabebereichs mithilfe der Anwendungsprogrammierschnittstellen des Texteingabebereichs beschrieben.

-   [TextInputPanel für Benutzer von PenInputPanel](textinputpanel-for-users-of-peninputpanel.md)
-   [Verwenden von AutoVervollständigen im Eingabebereich](using-input-panel-autocomplete.md)
-   [Aktivieren der Textkorrektur für benutzerdefinierte Ink Collectors](enabling-text-correction-for-custom-ink-collectors.md)

> [!Note]  
> Der Texteingabebereich wird in einer ausführbaren Datei namens TabTip.exe implementiert. Beim Ausführen von TabTip.exe mit dem *Parameter /SeekDesktop* wird versucht, eine version mit eingeschränkter Funktionalität des Eingabebereichs auf einem nicht standardmäßigen interaktiven Desktop auszuführen, wie mit [**CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa)erstellt. Für die meisten erstellten Desktops wird der Eingabebereich automatisch bereits in diesem Modus ausgeführt. Dieser Parameter bietet die Möglichkeit, ihn in ungewöhnlichen Anwendungsszenarien zu starten, die andernfalls den automatischen Start verhindern. Wenn der Eingabebereich bereits auf dem Desktop ausgeführt wird, hat dieser Parameter keine Auswirkungen, und die Instanz von TabTip.exe wird sofort beendet.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmieren des Eingabebereichs mit der PenInputPanel-Klasse](programming-the-input-panel-using-the-peninputpanel-class.md)
</dt> </dl>

 

 
