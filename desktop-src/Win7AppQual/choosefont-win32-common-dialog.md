---
description: .
ms.assetid: ee1df9f2-585f-4208-ad49-a0f6ba76f53a
title: Ausgewählter Win32-Dialog Feld ()
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e55a31d1f4d5530e04fe455135952eb94cc4bda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352760"
---
# <a name="choosefont-win32-common-dialog"></a>Ausgewählter Win32-Dialog Feld ()

## <a name="affected-platforms"></a>Betroffene Plattformen

**Clients** -Windows 7  
**Server** -Windows Server 2008 R2  









## <a name="feature-impact"></a>Auswirkungen von Features

**Schweregrad** -niedrig  
**Frequency** -Medium  




## <a name="description"></a>BESCHREIBUNG

Windows 7 enthält mehrere Updates für das allgemeine Win32-Dialogfeld (). Diese werden in zwei Kategorien unterteilt:

-   Visuelle Aktualisierung des Dialog Felds
-   Unterstützung für neue Funktionen zum Anzeigen/Ausblenden von Schriftarten

Die **Dialogfeld Aktualisierung** aktualisiert die Standardvorlage, damit das Dialogfeld mit anderen Dialog Layouts in Windows in Einklang gebracht wird. Es führt WYSIWYG in die Schriftart Anzeigelisten ein, um Benutzern die Auswahl von Schriftarten zu erleichtern. Außerdem ist ein Link zu den Schriftarten cpl enthalten, um Benutzern, die Ihre Schriftart Listen anpassen möchten, einen einfachen Zugriff zu ermöglichen.

**Schriftarten anzeigen/ausblenden** ist ein neues Feature für die Windows 7-Plattform, bei dem Schriftarten, die nicht für die Spracheinstellungen des aktuellen Benutzers geeignet sind (Eingabemethoden) standardmäßig nicht in den Schriftart Auswahllisten angezeigt werden. Benutzer können die Schriftarten anpassen, die in der Schriftarten-cpl angezeigt werden sollen, oder Sie können diese Funktion deaktivieren.

## <a name="manifestation-of-impact"></a>Erscheinung der Auswirkung

**Visuelle Aktualisierung des Dialog Felds**

Wir haben zwei neue Vorlagen in Windows 7 eingeführt (eine für Anwendungen, die Version 6 oder höher von comctl32.dll laden, und eine andere für Anwendungen, die frühere Versionen laden).

-   Aus Gründen der Anwendungs Kompatibilität werden diese neuen Vorlagen nur für Anwendungen geladen, die nicht mit der Nachrichten Warteschlange "choosefont" kompatibel sind. Anwendungen, die die Nachrichten Warteschlange anschließen, sehen weiterhin das alte Dialogfeld Layout.
-   Anwendungen, die ihre eigenen Vorlagen bereitstellen, werden Sie weiterhin verwenden können.

Anwendungen, die die neuen Vorlagen nicht erhalten, sehen keine Dialog layoutlayoutänderungen von Vista. Sie sollten jedoch immer noch die neue WYSIWYG-Schriftart Vorschau erhalten.

**Schriftarten anzeigen/ausblenden**

Für alle Versionen von Choice Font werden im Dialogfeld die Schriftart Einstellungen für das Anzeigen/Ausblenden des aktuellen Benutzers verwendet, um die anzuzeigende Schriftart Liste zu ermitteln. Dies führt dazu, dass in den meisten Fällen weniger Schriftart Listen angezeigt werden.

## <a name="end-user-mitigation"></a>Entschärfung durch Endbenutzer

**Schriftarten anzeigen/ausblenden:** Um das Ausblenden der Schriftart zu deaktivieren, sollten Benutzer in der Schriftarten-cpl zur Seite Schriftart Einstellungen wechseln und die Option "

Kontrollkästchen "Schriftarten basierend auf Spracheinstellungen ausblenden"

## <a name="developer-mitigation"></a>Entwickler Entschärfung

-   **Visuelle Aktualisierung:** Anwendungsentwickler, die eigene Vorlagen bereitstellen, können diese aktualisieren, damit Sie mit der entsprechenden neuen Vorlage für Windows 7 übereinstimmen. Die neuen Vorlagen sind in der Vorlagen Datei Font. DLG verfügbar.

    **Hinweis:** Die neue veröffentlichte Vorlage enthält ein zusätzliches Syslink-Steuerelement, das eine Verknüpfung bereitstellt, mit der Benutzer die Schriftarten-cpl starten können, um weitere Schriftarten anzuzeigen. Das Link Steuerelement erfordert Version 6 der allgemeinen Windows-Steuerelement Bibliothek (comctl32.dll). Entwickler sollten ein Manifest oder eine Direktive bereitstellen, das die Verwendung von Version 6 der DLL angibt, falls verfügbar. Verwenden Sie stattdessen den Steuer Objekttyp "PUSHBUTTON", wenn eine Anwendung eine frühere Version der allgemeinen Steuerelement Bibliothek verwendet.

-   **Schriftarten anzeigen/ausblenden:** Entwickler können diese Funktion deaktivieren, indem Sie ein zusätzliches Flag (CF \_ inactivefonts) im Flags-Member der choosefont-Struktur bereitstellen. Das Festlegen dieses Flags bewirkt, dass alle installierten Schriftarten in der Schriftart Liste angezeigt werden.
-   **Schriftarten anzeigen/ausblenden:** Anwendungen, die Hilfe Inhalte zur Auswahl von Informationen bereitstellen, möchten möglicherweise Inhalt hinzufügen, um zu erklären, warum die Schriftart Liste reduziert ist, und die Benutzer an die Schriftarten-cpl weiterleiten, um deren Schriftart

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Tests der Kompatibilität, Leistung, Zuverlässigkeit und Benutzerfreundlichkeit

Entwickler, deren Anwendungen die ausgewählte Meldungs Warteschlange zum Anpassen des Dialog Felds anschließen, sollten überprüfen, ob Ihre Anwendungen alle vorhandenen Funktionen beibehalten.

Anwendungen, die die Schriftart Liste stark mithilfe von Flags kürzen, sollten sicherstellen, dass die Liste der dargestellten Schriftart weiterhin akzeptabel ist.

 

 



