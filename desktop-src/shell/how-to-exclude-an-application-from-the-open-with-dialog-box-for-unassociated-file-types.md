---
description: Ausschließen einer Anwendung aus dem Dialogfeld Öffnen mit für den nicht zugeordneten Dateityp.
title: Ausschließen einer Anwendung aus dem Dialog Feld "Öffnen mit" für nicht zugeordnete Dateitypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9443416e95fca112623d487bf58f4fce1d51d13d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104554119"
---
# <a name="how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types"></a>Ausschließen einer Anwendung aus dem Dialog Feld "Öffnen mit" für nicht zugeordnete Dateitypen

Wenn ein Benutzer versucht, eine Datei zu öffnen, die kein Mitglied eines registrierten Dateityps ist (d. h. ein Unbekannter Dateityp), oder wenn ein Benutzer **Öffnen mit** oder **Öffnen mit-> die Option Standardprogramm** aus dem Kontextmenü einer Datei auswählen, zeigt die Shell ein Untermenü oder Dialogfeld an, in dem der Benutzer das zum Öffnen der Datei verwendete Programm angeben kann.

Standardmäßig wird jede Anwendung, die als Unterschlüssel von **HKEY \_ - \_ Klassen**-Stamm \\ **Anwendungen** registriert ist, im Dialogfeld **Öffnen mit** angezeigt. Diese Anwendungen werden in **geöffnet** angezeigt, unabhängig davon, ob die Anwendung für die Behandlung des Dateityps registriert ist.

Verwenden Sie eines der beiden in diesem Thema beschriebenen Verfahren, um zu verhindern, dass eine Anwendung im Dialogfeld **Öffnen mit** angezeigt wird, wenn die Anwendung nicht zum Öffnen bestimmter Dateitypen verwendet werden kann.

## <a name="instructions"></a>Instructions

### <a name="step-1"></a>Schritt 1:

Fügen Sie dem Unterschlüssel der Anwendung einen noopenwith-Eintrag hinzu. Wenn eine Anwendung einen Dateityp verwendet, zeichnet Windows diese Informationen auf, um die Liste der **empfohlenen Programme** zu erstellen. Diese Liste wird im Untermenü **Öffnen mit** angezeigt, wie im folgenden Screenshot dargestellt.

![Screenshot des Kontextmenüs mit dem angezeigten Untermenü "Öffnen mit"](images/file-assoc/openwithsubmenu.png)

Diese empfohlenen Anwendungen werden auch im Abschnitt **Empfohlene Programme** des Dialog Felds **Öffnen mit** angezeigt, wie im folgenden Screenshot gezeigt.

![Screenshot des Dialog Felds "Öffnen mit" mit empfohlenen Programmen](images/file-assoc/openwithdialog.png)

> [!Note]  
> Wenn sich eine Anwendung für den Dateityp in [OpenWithList](fa-file-types.md) oder OpenWithProgIds registriert hat, wird Sie in der Liste **Empfohlene Programme** angezeigt, auch wenn der Eintrag noopenwith festgelegt ist. Beachten Sie auch, dass ein Benutzer unabhängig davon, ob eine Anwendung in einer Liste von empfohlenen Programmen angeboten wird, manuell zu einer beliebigen ausführbaren Datei navigieren kann.

 

Anwendungen können diese Nachverfolgung deaktivieren, indem Sie unter dem Unterschlüssel der Anwendung einen noopenwith-Wert angeben.

Der noopenwith-Eintrag ist ein leerer **reg \_ SZ** -Wert, wie im folgenden Beispiel gezeigt.

```
HKEY_CLASSES_ROOT
   Applications
      MyProgram.exe
         NoOpenWith
```

Das Festlegen des noopenwith-Eintrags hat ebenfalls folgende Auswirkungen:

-   Verhindert, dass eine Datei mithilfe von Drag & amp; Drop an die Sprung Liste der Anwendung angehefnt wird, es sei denn, die Anwendung wird speziell für die Verarbeitung dieses Dateityps registriert.
-   Verhindert, dass das Dialogfeld "allgemeine Datei" und alle Aufrufe der Funktion " [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs) " eine beliebige Datei zur Sprung Liste der Anwendung hinzufügen, es sei denn, die Anwendung ist speziell für die Verarbeitung dieses Dateityps registriert.

### <a name="step-2"></a>Schritt 2:

Die zweite Möglichkeit, um zu verhindern, dass eine Anwendung im Dialogfeld **Öffnen mit** angezeigt wird, ist die Verwendung des unter Schlüssels **SupportedTypes** , um die Erweiterungen von Dateitypen, die von der Anwendung geöffnet werden können, explizit aufzulisten. Dadurch wird verhindert, dass die Anwendung im Dialogfeld **Öffnen mit** für Dateitypen angezeigt wird, die nicht geöffnet werden können. Außerdem bewirkt dies, dass die Anwendung in der Liste der **empfohlenen Programme** angezeigt wird, wie bereits erläutert.

Diese Methode ist besonders nützlich, wenn eine Anwendung eine Datei als bestimmten Dateityp speichern kann, diesen Dateityp jedoch nicht öffnen kann. Eine Anwendung sollte auch das Flag "Fos \_ dontaddtor ecent" über [**ifiledialog:: SetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) festlegen, wenn das Dialogfeld " **Speichern** " aufgerufen wird. Dadurch wird verhindert, dass das Element dem **letzten** oder **häufigen** Teil einer Sprung Liste hinzugefügt wird. Außerdem wird die Nachverfolgung der Anwendung unter [OpenWithList](fa-file-types.md)blockiert.

Jede unterstützte Erweiterung wird als Eintrag unter dem **SupportedTypes** -Unterschlüssel hinzugefügt, wie im folgenden Beispiel gezeigt. Die Einträge sind vom Typ **reg \_ SZ** oder **reg \_ null** ohne zugeordnete Werte.

```
HKEY_CLASSES_ROOT
   Applications
      ApplicationName
         SupportedTypes
            .ext1
            .ext2
            .ext3
```

Wenn ein **SupportedTypes** -Unterschlüssel angegeben wird, können nur Dateien mit diesen Erweiterungen an die Sprung Liste der Anwendung angehefteter oder in der Liste mit **den neuesten** oder **häufigen** Zielen einer Anwendung nachverfolgt werden.

Der noopenwith-Eintrag überschreibt den **SupportedTypes** -Unterschlüssel und blendet die Anwendung im Dialogfeld **Öffnen mit** aus.

 

 
