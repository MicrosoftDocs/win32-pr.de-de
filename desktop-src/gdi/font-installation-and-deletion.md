---
description: Eine Anwendung kann eine Schriftart nur verwenden, um Text zu zeichnen, wenn sich diese Schriftart entweder auf einem angegebenen Gerät befindet oder in der Schriftarttabelle des Systems installiert ist.
ms.assetid: b422b981-8760-4484-9965-f212287c421e
title: Installation und Löschung von Schriftarten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 112cfbff6bebdfc2fa4d46993f1fa60dcc19285bc3e16ebc2fd929e3a43ba679
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037928"
---
# <a name="font-installation-and-deletion"></a>Installation und Löschung von Schriftarten

Eine Anwendung kann eine Schriftart nur verwenden, um Text zu zeichnen, wenn sich diese Schriftart entweder auf einem angegebenen Gerät befindet oder in der Schriftarttabelle des Systems installiert ist. Die Schriftarttabelle ist ein internes Array, das alle Nichtgeräteschriftarten identifiziert, die für eine Anwendung verfügbar sind. Eine Anwendung kann die Namen von Schriftarten abrufen, die derzeit auf einem Gerät installiert oder in der internen Schriftarttabelle gespeichert sind, indem die [**Funktionen EnumFontFamilies**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) oder [**ChooseFont aufgerufen**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) werden.

Um eine Schriftart vorübergehend zu installieren, rufen [**Sie AddFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourcea) oder [**AddFontResourceEx auf.**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourceexa) Diese Funktionen laden eine Schriftart, die in einer Font-Resource-Datei gespeichert ist. Dies ist jedoch eine temporäre Installation, da die Schriftart nach einem Neustart nicht vorhanden ist.

Verwenden Sie eine der folgenden Methoden, um eine Schriftart zu installieren, die nach dem Neustart des Systems erhalten bleibt:

-   Wechseln Sie zum Systemsteuerung, klicken Sie auf das **Symbol Schriftarten,** und wählen Sie **im** Menü Datei die Option Neue **Schriftarten installieren** aus. Die Schriftart ist für eine Anwendung bereits vor dem Neustart verfügbar. In einer Terminalserversituation ist die Schriftart jedoch für die aktuelle Sitzung verfügbar, aber erst nach einem Neustart für andere Sitzungen.
-   Kopieren Sie die Schriftart in den Ordner \\ %windir%-Schriftarten. Wechseln Sie dann entweder zum Systemsteuerung klicken  Sie auf das Symbol Schriftarten, oder rufen Sie [**AddFontResource**](/windows/win32/api/wingdi/nf-wingdi-addfontresourcea) oder [**AddFontResourceEx auf.**](/windows/win32/api/wingdi/nf-wingdi-addfontresourceexa) Die Schriftart ist für eine Anwendung bereits vor dem Neustart verfügbar. In einer Terminalserversituation ist die Schriftart jedoch für die aktuelle Sitzung verfügbar, aber erst nach einem Neustart für andere Sitzungen. Wenn Sie die Schriftart nur in den Ordner %windir%-Schriftarten kopieren, ist die Schriftart erst \\ verfügbar, nachdem das System neu gestartet wurde.

Wenn eine Anwendung die Verwendung einer installierten Schriftart beendet, muss sie diese Schriftart entfernen, indem sie die [**RemoveFontResource-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) aufruft.

Eine Schriftart, die von einem anderen Speicherort als dem Ordner %windir%-Schriftarten installiert wird, kann nicht geändert werden, wenn sie in eine aktive Sitzung geladen wird, einschließlich \\ Sitzung 0. Jeder Versuch, änderungen, zu ersetzen oder zu löschen, wird daher blockiert. Wenn eine Änderung an einer Schriftart erforderlich ist:

-   *Temporäre Schriftarten* werden nur in der aktuellen Sitzung geladen. Rufen Sie vor dem Versuch von Schriftartänderungen [**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) auf, um zu erzwingen, dass die aktuelle Sitzung die Schriftart entlädt.
-   *Permanente Schriftarten* bleiben nach dem Neustart installiert und werden von allen erstellten Sitzungen geladen. Rufen [**Sie RemoveFontResource auf,**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) um zu erzwingen, dass die aktuelle Sitzung die Schriftart entlädt. Suchen und entfernen Sie dann im Registrierungsschlüssel der Schriftart (**HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Windows NT \_ \\ \\ \\ \\ CurrentVersion \\ Fonts**) den Registrierungswert, der der Schriftart zugeordnet ist. Starten Sie abschließend den Computer neu, um sicherzustellen, dass die Schriftart in einer Sitzung nicht geladen wird. Fahren Sie nach dem Neustart mit der Änderung/Löschung der Schriftart fort.

Wenn eine Anwendung die Funktionen aufruft, die Schriftartressourcen hinzufügen und löschen, sollte sie auch die [**SendMessage-Funktion**](/windows/win32/api/winuser/nf-winuser-sendmessage) aufrufen und eine [**WM \_ FONTCHANGE-Nachricht**](wm-fontchange.md) an alle Fenster der obersten Ebene im System senden. Diese Meldung benachrichtigt andere Anwendungen, dass die interne Schriftarttabelle von einer Anwendung geändert wurde, die eine Schriftart hinzugefügt oder entfernt hat.

 

 
