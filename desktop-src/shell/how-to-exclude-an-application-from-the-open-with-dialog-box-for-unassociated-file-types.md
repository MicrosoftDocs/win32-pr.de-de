---
description: Hier erfahren Sie, wie Sie eine Anwendung für einen nicht assoziierten Dateityp vom Öffnen mit ausschließen.
title: Ausschließen einer Anwendung aus dem Dialogfeld "Öffnen mit" für nicht zuordnende Dateitypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d90ae5ab49128df1eedd9b760286ce54f6b6498cbe00d4a945145a80f956cde
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119350912"
---
# <a name="how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types"></a>Ausschließen einer Anwendung aus dem Dialogfeld "Öffnen mit" für nicht zuordnende Dateitypen

Wenn ein Benutzer versucht, eine Datei zu öffnen, die kein Mitglied eines registrierten **Dateityps** ist (d. h. ein unbekannter Dateityp), oder wenn ein Benutzer Öffnen mit oder **Öffnen mit -> Standardprogramm** auswählen aus dem Kontextmenü einer Datei auswählt, zeigt die Shell ein Untermenü oder Dialogfeld an, in dem der Benutzer das Programm angeben kann, das zum Öffnen der Datei verwendet wird.

Standardmäßig wird jede Anwendung, die als Unterschlüssel von **HKEY \_ CLASSES \_ ROOT** Applications registriert ist, im dialogfeld \\  **Öffnen mit** angezeigt. Diese Anwendungen werden **in** Öffnen mit unabhängig davon, ob die Anwendung für die Handhabung des Dateityps registriert ist.

Um zu verhindern, dass eine Anwendung im Dialogfeld **Öffnen mit** angezeigt wird, wenn die Anwendung nicht zum Öffnen bestimmter Dateitypen verwendet werden soll oder nicht, verwenden Sie eine der beiden in diesem Thema beschriebenen Techniken.

## <a name="instructions"></a>Anweisungen

### <a name="step-1"></a>Schritt 1:

Fügen Sie dem Unterschlüssel der Anwendung einen NoOpenWith-Eintrag hinzu. Wenn eine Anwendung einen Dateityp verwendet, Windows diese Informationen auf, um die Liste **Empfohlene Programme zu** erstellen. Diese Liste wird im **unteren** Öffnen mit angezeigt, wie im folgenden Screenshot gezeigt.

![Screenshot des Kontextmenüs mit geöffneten Untermenüs](images/file-assoc/openwithsubmenu.png)

Diese empfohlenen Anwendungen werden auch im Abschnitt  Empfohlene Programme des **Dialogfelds** Öffnen mit angezeigt, wie im folgenden Screenshot gezeigt.

![Screenshot des Dialogfelds "Öffnen mit" mit empfohlenen Programmen](images/file-assoc/openwithdialog.png)

> [!Note]  
> Wenn sich eine Anwendung in [openWithList oder OpenWithProgIDs](fa-file-types.md) für den Dateityp  registriert hat, wird sie auch dann in der Liste Empfohlene Programme angezeigt, wenn der Eintrag NoOpenWith festgelegt ist. Denken Sie außerdem daran, dass ein Benutzer unabhängig davon, ob eine Anwendung in einer Liste empfohlener Programme angeboten wird, manuell zu jeder ausführbaren Datei navigieren kann.

 

Anwendungen können diese Nachverfolgung deaktivieren, indem sie einen NoOpenWith-Wert unter dem Unterschlüssel der Anwendung angeben.

Der Eintrag NoOpenWith ist ein leerer **REG \_ SZ-Wert,** wie im folgenden Beispiel gezeigt.

```
HKEY_CLASSES_ROOT
   Applications
      MyProgram.exe
         NoOpenWith
```

Das Festlegen des Eintrags NoOpenWith hat auch die folgenden Auswirkungen:

-   Verhindert das Anheften einer Datei an die Anwendungsdatei Sprungliste Drag & Drop, es sei denn, die Anwendung ist speziell für die Handhabung dieses Dateityps registriert.
-   Verhindert, dass das Allgemeine Dateidialogfeld und alle Aufrufe der [**SHAddToRecentDocs-Funktion**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs) dem Sprungliste der Anwendung dateien hinzufügen, es sei denn, die Anwendung ist speziell für die Handhabung dieses Dateityps registriert.

### <a name="step-2"></a>Schritt 2:

Die zweite Möglichkeit, zu verhindern, dass eine Anwendung im Dialogfeld **Öffnen mit** angezeigt wird, besteht in der Verwendung des **Unterschlüssels SupportedTypes,** um die Erweiterungen von Dateitypen, die die Anwendung öffnen kann, explizit auflisten zu können. Dadurch wird verhindert, dass  die Anwendung im Dialogfeld Öffnen mit für Dateitypen angezeigt wird, die nicht geöffnet werden können. Außerdem wird die Anwendung in  der Liste Empfohlene Programme angezeigt, wie zuvor erläutert.

Diese Methode ist besonders nützlich, wenn eine Anwendung eine Datei als einen bestimmten Dateityp speichern kann, diesen Dateityp jedoch nicht öffnen kann. Eine Anwendung sollte beim Aufrufen des Dialogfelds Speichern auch das FOS \_ DONTADDTORECENT-Flag über [**IFileDialog::SetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) festlegen.  Dadurch wird verhindert, dass das Element dem Zuletzt **verwendeten** Teil oder **häufigen Teil** einer Sprungliste. Außerdem wird verhindert, dass die Anwendung unter [OpenWithList nachverfolgt wird.](fa-file-types.md)

Jede unterstützte Erweiterung wird als Eintrag unter dem **Unterschlüssel SupportedTypes** hinzugefügt, wie im folgenden Beispiel gezeigt. Die Einträge sind vom Typ **REG \_ SZ oder** REG **\_ NULL** ohne zugeordnete Werte.

```
HKEY_CLASSES_ROOT
   Applications
      ApplicationName
         SupportedTypes
            .ext1
            .ext2
            .ext3
```

Wenn ein **SupportedTypes-Unterschlüssel** bereitgestellt wird, können nur Dateien mit diesen Erweiterungen an den Sprungliste der Anwendung angeheftet  oder in der Liste Zuletzt verwendete oder häufige Ziele einer Anwendung nachverfolgt werden. 

Der Eintrag NoOpenWith überschreibt den **Unterschlüssel SupportedTypes** und blendet die Anwendung im Öffnen mit **aus.**

 

 
