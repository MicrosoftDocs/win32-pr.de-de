---
description: Für System Steuerungselemente, die als exe-Dateien implementiert sind, sind keine speziellen Exporte oder Nachrichten Behandlung erforderlich. Beliebige exe-Dateien können als Befehls Objekt registriert werden, damit Sie im Ordnersystem Steuerung mit einem Einstiegspunkt angezeigt werden.
title: Registrieren von ausführbaren System Steuerungselementen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 778bac10fea661f73c0967401a7c708ebf6b8273
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042244"
---
# <a name="how-to-register-executable-control-panel-items"></a>Registrieren von ausführbaren System Steuerungselementen

Für System Steuerungselemente, die als exe-Dateien implementiert sind, sind keine speziellen Exporte oder Nachrichten Behandlung erforderlich. Beliebige exe-Dateien können als Befehls Objekt registriert werden, damit Sie im Ordnersystem Steuerung mit einem Einstiegspunkt angezeigt werden.

Hier wird ein Beispiel verwendet, um die Registrierungsanforderungen zu veranschaulichen. Das Beispiel zeigt, wie ein System Steuerungselement namens **meine Einstellungen** als Befehls Objekt registriert wird, sodass es im Fenstersystem Steuerung angezeigt wird. Das Fenster **meine Einstellungen** wird auch angezeigt, wenn der Befehl `MyApp.exe /settings` ausgeführt wird.

## <a name="instructions"></a>Instructions

### <a name="step-1"></a>Schritt 1:

Generieren Sie eine GUID für das System Steuerungselement. Durch die GUID wird das System Steuerungselement eindeutig identifiziert. In diesem Beispiel `{0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}` ist die GUID des System Steuerungs Elements.

### <a name="step-2"></a>Schritt 2:

Fügen Sie der Registrierung unter Verwendung der GUID als Name einen Unterschlüssel wie folgt hinzu.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  ControlPanel
                     NameSpace
                        {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
                           (Default) = My Settings
```

Die Daten für den Standardeintrag sind einfach der reg \_ SZ-Name des System Steuerungs Elements. Der Standardeintrag kann nützlich sein, um den GUID-Eintrag zu identifizieren, ist aber optional.

### <a name="step-3"></a>Schritt 3:

Fügen Sie der Registrierung unter Verwendung der GUID als Name einen Unterschlüssel und die zugehörigen Einträge wie folgt hinzu.

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         (Default) = My Settings
         LocalizedString = @%ProgramFiles%\MyCorp\MyApp.exe,-9
         InfoTip = @%ProgramFiles%\MyCorp\MyApp.exe,-5
         System.ApplicationName = MyCorporation.MySettings
         System.ControlPanel.Category = 1,8
         System.Software.TasksFileUrl = %ProgramFiles%\MyCorp\MyApp\MyTaskLinks.xml
```

-   **Default**. REG \_ SZ. Der Anzeige Name für das System Steuerungselement.
-   **LocalizedString**. Optional. Reg \_ SZ oder reg \_ Expand \_ SZ. Der Modulname und die Zeichen folgen Tabellen-ID des lokalisierten Namens des System Steuerungs Elements. Das Format ist ein "at"-Zeichen (@), gefolgt vom Namen der exe-oder DLL-Datei, die die MUI-Zeichen folgen Tabelle (mehrsprachige Benutzeroberfläche) enthält. Umgebungsvariablen können als Ersatz für einen Teil des Pfads verwendet werden. Auf den Pfad und den Dateinamen folgt ein Komma (,) und ein Bindestrich (-), gefolgt von der ID in der Zeichen folgen Tabelle.

    Wenn das Modul nicht über eine Zeichen folgen Tabelle verfügt, kann dieser Eintrag einfach die Anzeige Name-Zeichenfolge sein. Wenn Sie anstelle einer Zeichen folgen Tabelle nur die Anzeige Name-Zeichenfolge verwenden, wird der Name nicht an die aktuelle Anzeige Sprache angepasst.

-   **Infotipp**. Reg \_ SZ oder reg \_ Expand \_ SZ. Eine Beschreibung des System Steuerungs Elements. Diese Informationen werden in einem infotip angezeigt, der angezeigt wird, wenn mit dem Mauszeiger auf das Element Symbol gezeigt wird. Die Syntax ist identisch mit der, die für LocalizedString verwendet wird, einschließlich der Option, einfach anstelle eines Zeichen folgen Tabellen Verweises eine Zeichenfolge bereitzustellen.
-   **System. ApplicationName**. REG \_ SZ. Der kanonische Name des Elements. Der Befehl des Formulars `control.exe /name System.ApplicationName` öffnet das Element, z. b `control.exe /name MyCorporation.MySettings` .. Weitere Informationen zur Verwendung von Control.exe finden Sie unter [Ausführen von System Steuerungselementen](executing-control-panel-items.md) .
-   **System. ControlPanel. Category**. REG \_ SZ. Ein-Wert, der die System Steuerungs Kategorien deklariert, in denen das Element angezeigt wird. Mehrere Kategorien werden durch Kommas getrennt. Im obigen Beispiel gibt der-Eintrag an, dass das Element **meine Einstellungen** in den Kategorien Darstellung **und Personalisierung** und **Programme** angezeigt werden soll. Weitere Kategoriewerte finden Sie unter [Zuweisen von System Steuerungs Kategorien](assigning-control-panel-categories.md) .
-   **System. Software. tasksfileurl**. Reg \_ SZ oder reg \_ Expand \_ SZ. Der Pfad der XML-Datei, die [Aufgaben Verknüpfungen](creating-searchable-task-links.md)definiert. Dies kann ein direkter Dateipfad sein, wie im Beispiel gezeigt, oder eine eingebettete Ressource, die als Modulname und Ressourcen-ID angegeben ist, z. b. "% Program Files% \\ MyCorp \\ myapp \\MyApp.exe,-31".

### <a name="step-4"></a>Schritt 4:

Fügen Sie unter demselben GUID-Unterschlüssel der Registrierung den folgenden Unterschlüssel hinzu, um den Pfad der Datei anzugeben, die das Symbol und die Ressourcen-ID des Bilds in dieser Datei enthält.

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         DefaultIcon
            (Default) = %ProgramFiles%\MyCorp\MyApp.exe,-2
```

Beachten Sie, dass die Syntax in der Regel mit den oben erläuterten lokaltzeichen-und infotip-Einträgen vergleichbar ist, dass kein @-Zeichen als Präfix im reg \_ SZ-oder reg Expand-SZ-Eintrag verwendet wird, \_ \_ der den Pfad angibt.

### <a name="step-5"></a>Schritt 5:

Fügen Sie der Registrierung die folgenden Informationen hinzu, um den Befehl bereitzustellen, der vom System aufgerufen wird, wenn der Benutzer die Systemsteuerung öffnet.

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         Shell
            Open
               Command
                  (Default) = [REG_EXPAND_SZ] %ProgramFiles%\MyCorp\MyApp.exe /Settings
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System Steuerungselemente werden registriert](registering-control-panel-items.md)
</dt> <dt>

[Registrieren von dll-System Steuerungselementen](how-to-register-dll-control-panel-item-registration-.md)
</dt> </dl>

 

 



