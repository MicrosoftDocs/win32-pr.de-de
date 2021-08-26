---
description: Für Systemsteuerung Elemente, die als .exe implementiert werden, sind keine speziellen Exporte oder Nachrichtenbehandlung erforderlich. Jede .exe kann als Befehlsobjekt registriert werden, um mit einem Einstiegspunkt im Ordner Systemsteuerung werden.
title: Registrieren von ausführbaren Systemsteuerung Elementen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b81e52e18bd2cd1c48d5d260b08844784a5286dd2cd4d9d5ec782a86f624fc42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009430"
---
# <a name="how-to-register-executable-control-panel-items"></a>Registrieren von ausführbaren Systemsteuerung Elementen

Für Systemsteuerung Elemente, die als .exe implementiert werden, sind keine speziellen Exporte oder Nachrichtenbehandlung erforderlich. Jede .exe kann als Befehlsobjekt registriert werden, um mit einem Einstiegspunkt im Ordner Systemsteuerung werden.

Hier wird ein Beispiel verwendet, um die Registrierungsanforderungen zu veranschaulichen. Das Beispiel zeigt, wie sie ein Systemsteuerung namens **My Einstellungen** als Befehlsobjekt registrieren, sodass es im Fenster Systemsteuerung wird. Das **Fenster Einstellungen** wird auch angezeigt, wenn der Befehl ausgeführt `MyApp.exe /settings` wird.

## <a name="instructions"></a>Anweisungen

### <a name="step-1"></a>Schritt 1:

Generieren Sie eine GUID für das Systemsteuerung Element. Die GUID identifiziert das Systemsteuerung eindeutig. In diesem Beispiel `{0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}` ist die GUID des Systemsteuerung Elements.

### <a name="step-2"></a>Schritt 2:

Fügen Sie der Registrierung mithilfe der GUID als Namen wie folgt einen Unterschlüssel hinzu.

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

Die Daten für den Standardeintrag sind einfach der REG \_ SZ-Name des Systemsteuerung Elements. Der Eintrag Standard kann hilfreich sein, um den GUID-Eintrag zu identifizieren, ist aber optional.

### <a name="step-3"></a>Schritt 3:

Wenn Sie die GUID als Namen verwenden, fügen Sie der Registrierung wie folgt einen Unterschlüssel und seine Einträge hinzu.

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

-   **Default**. REG \_ SZ. Der Anzeigename für das Systemsteuerung Element.
-   **LocalizedString**. Optional. REG \_ SZ oder REG EXPAND \_ \_ SZ. Der Modulname und die Zeichenfolgentabellen-ID des lokalisierten Namens des Systemsteuerung Elements. Das Format ist ein "at"-Zeichen (@), gefolgt vom Namen des .exe oder .dll, das die Zeichenfolgentabelle mehrsprachige Benutzeroberfläche (FORMAT) enthält. Umgebungsvariablen können als Ersatz für einen Teil des Pfads verwendet werden. Auf den Pfad- und Dateinamen folgen ein Komma (,) und ein Bindestrich (-), gefolgt von der ID in der Zeichenfolgentabelle.

    Wenn das Modul über keine Zeichenfolgentabelle verfügt, kann dieser Eintrag einfach die Anzeigenamenzeichenfolge sein. Wenn Sie anstelle einer Zeichenfolgentabelle nur die Anzeigenamenzeichenfolge verwenden, wird der Name nicht an die aktuelle Anzeigesprache angepasst.

-   **InfoTip**. REG \_ SZ oder REG EXPAND \_ \_ SZ. Eine Beschreibung des Systemsteuerung Elements. Diese Informationen werden in einem InfoTip angezeigt, der angezeigt wird, wenn der Mauszeiger auf das Symbol des Elements zeigt. Die Syntax ist identisch mit der für LocalizedString, einschließlich der Option, einfach eine Zeichenfolge anstelle eines Zeichenfolgentabellenverweises bereitstellen zu können.
-   **System.ApplicationName**. REG \_ SZ. Der kanonische Name des Elements. Der Befehl des `control.exe /name System.ApplicationName` Formulars öffnet das Element, z. B. `control.exe /name MyCorporation.MySettings` . Weitere [Informationen zur Verwendung Systemsteuerung](executing-control-panel-items.md) finden Sie unter Ausführen von Control.exe.
-   **System.ControlPanel.Category**. REG \_ SZ. Ein -Wert, der die Systemsteuerung kategorien deklariert, in denen das Element angezeigt wird. Mehrere Kategorien werden durch Kommas getrennt. Im obigen Beispiel gibt der Eintrag an, dass das My **Einstellungen-Element** sowohl in den Kategorien Darstellung als auch **Personalisierung** und **Programme angezeigt werden** soll. Unter [Zuweisen Systemsteuerung Kategorien finden](assigning-control-panel-categories.md) Sie mögliche Kategoriewerte.
-   **System.Software.TasksFileUrl**. REG \_ SZ oder REG EXPAND \_ \_ SZ. Der Pfad der XML-Datei, die [Aufgabenlinks definiert.](creating-searchable-task-links.md) Dies kann ein direkter Dateipfad sein, wie im Beispiel gezeigt, oder eine eingebettete Ressource, die als Modulname und Ressourcen-ID wie "%ProgramFiles% \\ MyCorp \\ MyApp \\MyApp.exe,-31" angegeben ist.

### <a name="step-4"></a>Schritt 4:

Fügen Sie unter demselben GUID-Unterschlüssel der Registrierung den folgenden Unterschlüssel hinzu, um den Pfad der Datei mit dem Symbol und der Ressourcen-ID des Bilds in dieser Datei anzuzeigen.

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         DefaultIcon
            (Default) = %ProgramFiles%\MyCorp\MyApp.exe,-2
```

Beachten Sie, dass die Syntax den zuvor erläuterten LocalizedString- und InfoTip-Einträgen ähnelt, aber kein @-Zeichen als Präfix im REG SZ- oder REG EXPAND SZ-Eintrag verwendet wird, der den Pfad \_ \_ \_ angibt.

### <a name="step-5"></a>Schritt 5:

Fügen Sie der Registrierung die folgenden Informationen hinzu, um den Befehl zur Verfügung zu stellen, der vom System aufgerufen wird, wenn der Benutzer die Systemsteuerung.

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

[Registrieren Systemsteuerung Elementen](registering-control-panel-items.md)
</dt> <dt>

[Registrieren von DLL-Systemsteuerung Elementen](how-to-register-dll-control-panel-item-registration-.md)
</dt> </dl>

 

 



