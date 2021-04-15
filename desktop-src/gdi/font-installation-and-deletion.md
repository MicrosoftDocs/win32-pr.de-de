---
description: Eine Anwendung kann Text nur verwenden, um Text zu zeichnen, wenn diese Schriftart entweder auf einem angegebenen Gerät oder in der Schriftart Tabelle des Systems installiert ist.
ms.assetid: b422b981-8760-4484-9965-f212287c421e
title: Installation und Löschung von Schriftart
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0184054973c769462ed8c1620e5534ff909576ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994022"
---
# <a name="font-installation-and-deletion"></a>Installation und Löschung von Schriftart

Eine Anwendung kann Text nur verwenden, um Text zu zeichnen, wenn diese Schriftart entweder auf einem angegebenen Gerät oder in der Schriftart Tabelle des Systems installiert ist. Die Schriftart Tabelle ist ein internes Array, das alle nicht-Geräte Schriftarten identifiziert, die für eine Anwendung verfügbar sind. Eine Anwendung kann die Namen von Schriftarten abrufen, die zurzeit auf einem Gerät installiert sind oder in der internen Schriftart Tabelle gespeichert werden, indem die [**EnumFontFamilies**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) -oder [**choosefont**](/previous-versions/windows/desktop/legacy/ms646914(v=vs.85)) -Funktionen aufgerufen werden.

Um eine Schriftart temporär zu installieren, müssen Sie [**AddFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourcea) oder [**addfontresourceex**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourceexa)aufrufen. Diese Funktionen laden eine Schriftart, die in einer Schriftart Ressourcen Datei gespeichert ist. Dies ist jedoch eine temporäre Installation, da die Schriftart nach einem Neustart nicht mehr vorhanden ist.

Verwenden Sie eine der folgenden Methoden, um eine Schriftart zu installieren, die nach dem Neustart des Systems beibehalten wird:

-   Wechseln Sie zur Systemsteuerung, klicken Sie auf das **Schriftarten** Symbol, und wählen Sie im Menü **Datei** die Option **neue Schriftarten installieren** aus. Die Schriftart steht auch vor dem Neustart für eine Anwendung zur Verfügung. In einer Terminal Server Situation ist die Schriftart jedoch für die aktuelle Sitzung verfügbar, Sie ist jedoch erst nach einem Neustart für andere Sitzungen verfügbar.
-   Kopieren Sie die Schriftart in den Ordner% windir% \\ Fonts. Wechseln Sie dann zur Systemsteuerung, und klicken Sie auf das **Schriftarten** Symbol, oder rufen Sie [**AddFontResource**](/windows/win32/api/wingdi/nf-wingdi-addfontresourcea) oder [**addfontresourceex**](/windows/win32/api/wingdi/nf-wingdi-addfontresourceexa)auf. Die Schriftart steht auch vor dem Neustart für eine Anwendung zur Verfügung. In einer Terminal Server Situation ist die Schriftart jedoch für die aktuelle Sitzung verfügbar, Sie ist jedoch erst nach einem Neustart für andere Sitzungen verfügbar. Wenn Sie die Schriftart nur in den Ordner% windir% \\ Fonts kopieren, ist die Schriftart erst verfügbar, nachdem das System neu gestartet wurde.

Wenn eine Anwendung mit einer installierten Schriftart abgeschlossen ist, muss Sie diese Schriftart entfernen, indem Sie die [**removefontresource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) -Funktion aufrufen.

Eine Schriftart, die von einem anderen Speicherort als dem% windir% \\ Fonts-Ordner installiert wird, kann nicht geändert werden, wenn Sie in einer aktiven Sitzung geladen wird, einschließlich Sitzung 0. Der Versuch, zu ändern, zu ersetzen oder zu löschen, wird daher blockiert. Wenn eine Änderung an einer Schriftart erforderlich ist:

-   *Temporäre Schriftarten* werden nur in der aktuellen Sitzung geladen. Bevor Sie Änderungen an der Schriftart ausführen, müssen Sie [**removefontresource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) anrufen, um das Entladen der Schriftart durch die aktuelle Sitzung zu erzwingen.
-   *Permanente Schriftarten* bleiben nach dem Neustart installiert und werden von allen erstellten Sitzungen geladen. Ruft [**removefontresource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea) auf, um das Entladen der Schriftart durch die aktuelle Sitzung zu erzwingen. Suchen Sie anschließend im Registrierungsschlüssel Schriftart (**HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Fonts**) den Registrierungs Wert, der der Schriftart zugeordnet ist, und entfernen Sie ihn. Starten Sie schließlich den Computer neu, um sicherzustellen, dass die Schriftart in keiner Sitzung geladen wird. Fahren Sie nach dem Neustart mit ihrer Schriftart Änderung/-Löschung fort.

Wenn eine Anwendung die Funktionen aufruft, die Schriftart Ressourcen hinzufügen und löschen, sollte Sie auch die [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) -Funktion aufrufen und eine [**WM- \_ fontchange**](wm-fontchange.md) -Nachricht an alle Fenster der obersten Ebene im System senden. Mit dieser Meldung werden andere Anwendungen benachrichtigt, dass die interne Schriftart Tabelle von einer Anwendung geändert wurde, die eine Schriftart hinzugefügt oder entfernt hat.

 

 
