---
description: Dialogfeld "ChooseFont() Win32 Common"
ms.assetid: ee1df9f2-585f-4208-ad49-a0f6ba76f53a
title: Dialogfeld "ChooseFont() Win32 Common"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95edc873d6984b5db312d3a86fc926f72817a5170672ad315d07e209d98c4398
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098530"
---
# <a name="choosefont-win32-common-dialog"></a>Dialogfeld "ChooseFont() Win32 Common"

## <a name="affected-platforms"></a>Betroffene Plattformen

**Clients** – Windows 7  
**Server** – Windows Server 2008 R2  









## <a name="feature-impact"></a>Auswirkungen auf Features

**Schweregrad –** Niedrig  
**Frequency** - Medium  




## <a name="description"></a>BESCHREIBUNG

Windows 7 enthält mehrere Updates des allgemeinen Dialogfelds ChooseFont() Win32. Diese lassen sich in zwei Kategorien unterteilen:

-   Visuelle Aktualisierung des Dialogfelds
-   Unterstützung für neue Funktion zum Ein-/Ausblenden von Schriftarten

Die **Dialogaktualisierung** aktualisiert die Standardvorlage, um den Dialog mit anderen Dialoglayouts in Windows in Einklang zu bringen. Es führt WYSIWYG in die Schriftartanzeigelisten ein, um Benutzern die Auswahl von Schriftarten zu erleichtern. Es enthält auch einen Link zur Schriftarten-CPL, um Benutzern, die ihre Schriftartlisten anpassen möchten, einfachen Zugriff zu bieten.

**Schriftarten ein-/ausblenden** ist eine neue Windows 7-Plattformfunktion, bei der Schriftarten, die nicht für die Spracheinstellungen des aktuellen Benutzers geeignet sind (Eingabemethoden), standardmäßig nicht in Schriftartauswahllisten angezeigt werden. Benutzer können die Schriftarten anpassen, die in der Schriftarten-CPL angezeigt werden sollen, oder diese Funktion deaktivieren.

## <a name="manifestation-of-impact"></a>Auswirkungen

**Visuelle Aktualisierung des Dialogfelds**

Wir haben zwei neue Vorlagen in Windows 7 eingeführt (eine für Anwendungen, die Version 6 oder höher von comctl32.dll laden, und eine andere für Anwendungen, die frühere Versionen laden).

-   Aus Gründen der Anwendungskompatibilität werden diese neuen Vorlagen nur für Anwendungen geladen, die die ChooseFont-Nachrichtenwarteschlange nicht einbinden. Anwendungen, die die Nachrichtenwarteschlange verknüpfen, sehen weiterhin das alte Dialoglayout.
-   Anwendungen, die ihre eigenen Vorlagen bereitstellen, können sie weiterhin verwenden.

Anwendungen, die die neuen Vorlagen nicht erhalten, sehen keine Änderungen am Dialoglayout von Vista. Sie sollten jedoch weiterhin die neue VORSCHAUversion der SCHRIFTART "WYSIWYG" erhalten.

**Anzeigen/Ausblenden von Schriftarten**

Für alle Versionen von ChooseFont verwendet das Dialogfeld die Schriftarteinstellungen des aktuellen Benutzers zum Ein-/Ausblenden, um die anzuzeigende Schriftartliste zu bestimmen. Dies führt dazu, dass in den meisten Instanzen weniger Schriftartlisten angezeigt werden.

## <a name="end-user-mitigation"></a>Entschärfung durch Endbenutzer

**Schriftarten ein-/ausblenden:** Um das Ausblenden von Schriftarten zu deaktivieren, sollten Benutzer zur Seite Schriftart Einstellungen in der Schriftarten-CPL wechseln und die Auswahl von aufheben.

Kontrollkästchen "Schriftarten basierend auf Spracheinstellungen ausblenden"

## <a name="developer-mitigation"></a>Entschärfung durch Entwickler

-   **Visuelle Aktualisierung:** Anwendungsentwickler, die ihre eigenen Vorlagen bereitstellen, möchten diese möglicherweise aktualisieren, damit sie mit der entsprechenden neuen Windows 7-Vorlage in Einklang stehen. Die neuen Vorlagen sind in der Vorlagendatei Font.dlg verfügbar.

    **Hinweis:** Die neue veröffentlichte Vorlage enthält ein zusätzliches SysLink-Steuerelement, das eine Verknüpfung bereitstellt, mit der Benutzer die Schriftarten-CPL starten können, um weitere Schriftarten anzuzeigen. Für die Linksteuerung ist Version 6 der Windows common control library (comctl32.dll) erforderlich. Entwickler sollten ein Manifest oder eine Direktive bereitstellen, das bzw. die die Verwendung von Version 6 der DLL angibt, falls verfügbar. Wenn eine Anwendung eine frühere Version der allgemeinen Steuerelementbibliothek verwendet, verwenden Sie stattdessen den Steuerelementtyp "PUSHBUTTON".

-   **Schriftarten ein-/ausblenden:** Entwickler können dieses Feature deaktivieren, indem sie ein zusätzliches Flag (CF \_ INACTIVEFONTS) im Flagmember der CHOOSEFONT-Struktur bereitstellen. Wenn Sie dieses Flag festlegen, werden alle installierten Schriftarten in der Schriftartliste angezeigt.
-   **Schriftarten ein-/ausblenden:** Anwendungen, die ChooseFont-Hilfeinhalte bereitstellen, möchten möglicherweise Inhalte hinzufügen, um zu erklären, warum die Schriftartliste reduziert wird, und Benutzer an die Schriftarten-CPL leiten, um ihre Schriftartlisten anzupassen.

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Kompatibilitäts-, Leistungs-, Zuverlässigkeits- und Benutzerfreundlichkeitstests

Entwickler, deren Anwendungen die ChooseFont-Nachrichtenwarteschlange verknüpfen, um das Dialogfeld anzupassen, sollten überprüfen, ob ihre Anwendungen alle vorhandenen Funktionen beibehalten.

Anwendungen, die die Schriftartliste mit Flags stark kürzen, sollten sicherstellen, dass die angezeigte Schriftartliste akzeptabel bleibt.

 

 



