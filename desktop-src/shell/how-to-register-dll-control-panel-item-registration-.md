---
description: Systemsteuerung elemente, die in einer DLL implementiert sind, die die CPlApplet-Funktion exportiert, haben andere Registrierungsanforderungen als .exe Dateien.
title: Registrieren von DLL-Systemsteuerung Elementen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b25fffb3b06f93640c5ca8623fb24ffb53c6fd3ecae0b9e23cabafacdceba8f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119593190"
---
# <a name="how-to-register-dll-control-panel-items"></a>Registrieren von DLL-Systemsteuerung Elementen

> [!Note]  
> Aktuelle Implementierungsrichtlinien geben an, dass neue Systemsteuerung als .exe und nicht als .cpl implementiert werden sollen. Die folgenden Informationen sind hauptsächlich für Legacyzwecke enthalten.

 

Systemsteuerung elemente, die in einer DLL implementiert sind, die die [**CPlApplet-Funktion**](/windows/win32/api/cpl/nc-cpl-applet_proc) exportiert, haben andere Registrierungsanforderungen als .exe Dateien. Ab Windows XP sollten neue Systemsteuerung-Element-DLLs im Ordner der zugeordneten Anwendung unter dem Ordner Programme installiert werden. Elemente, die im System32-Verzeichnis mit einer .cpl gespeichert sind, müssen nicht registriert werden. sie werden automatisch in der Systemsteuerung. Alle anderen Systemsteuerung, die **CPlApplet** verwenden, müssen auf zwei Arten registriert werden:

-   Wenn das Systemsteuerung-Element für alle Benutzer verfügbar sein soll, registrieren Sie den Pfad pro Computer, indem Sie dem **Unterschlüssel HKEY \_ LOCAL \_ MACHINE** Software Microsoft Windows **\_ \_** \\  \\  \\  \\ **CurrentVersion** \\ **Systemsteuerung** \\ **Cpls** den Reg EXPAND SZ-Wert hinzufügen, der auf den DLL-Pfad festgelegt ist.
-   Wenn das Systemsteuerung-Element pro Benutzer verfügbar sein soll, verwenden Sie **HKEY \_ CURRENT \_ USER** als Stammschlüssel anstelle von **HKEY \_ LOCAL \_ MACHINE.**

In den folgenden beiden Beispielen wird das *MyCplApp-Systemsteuerung* registriert. Die DLL heißt MyCpl.cpl und befindet sich im *Anwendungsverzeichnis MyCorp \\ MyApp.* Dieses erste Beispiel veranschaulicht die Computerregistrierung.

## <a name="instructions"></a>Anweisungen

### <a name="step-1"></a>Schritt 1:

Fügen Sie diese Informationen der Registrierung hinzu, um das Vorhandensein der .cpl zu registrieren.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Cpls
                     MyCpl = [REG_EXPAND_SZ] %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl
```

### <a name="step-2"></a>Schritt 2:

**Windows Vista und höher:** Fügen Sie der Registrierung diese zusätzlichen Informationen hinzu, um eine GUID für das Systemsteuerung bereitstellen.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.Software.AppId
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = {A newly generated GUID}
```

Indem Sie eine GUID generieren, um das Systemsteuerung eindeutig zu identifizieren, können Sie dem -Element Aufgabenlinks Systemsteuerung. Ohne diese GUID gibt es keine Möglichkeit, dass die Aufgabenlinks dem Systemsteuerung werden. Unter [Erstellen durchsuchbarer Aufgabenlinks finden Sie Systemsteuerung Element](creating-searchable-task-links.md).

### <a name="step-3"></a>Schritt 3:

**Windows Vista und höher:** Fügen Sie der Registrierung die folgenden Informationen hinzu, um einen kanonischen Namen für das Element zu erstellen.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.ApplicationName
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_SZ] MyCorporation.MyCpl
```

Durch Hinzufügen eines kanonischen Namens können Benutzer das Systemsteuerung über die Befehlszeile starten, indem sie `control.exe /name MyCorporation.MyCpl` eingeben. Dies ermöglicht es auch, eine Implementierung von einer .cpl-Datei zu einem späteren Zeitpunkt in eine .exe-Datei zu ändern, ohne dass von aufrufenden Programmen Änderungen vorgenommen werden müssen, da sie das Element weiterhin über seinen kanonischen Namen öffnen können. Weitere Informationen zu kanonischen Namen finden Sie unter [Executing Systemsteuerung Items](executing-control-panel-items.md).

### <a name="step-4"></a>Schritt 4:

**Windows Vista und höher:** Fügen Sie der Registrierung die folgenden Informationen hinzu, um ein Systemsteuerung einer oder mehrere Kategorien zu zuweisen.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.ControlPanel.Category
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_DWORD] 3
```

**Windows XP:** Fügen Sie der Registrierung die folgenden Informationen hinzu, um ein Systemsteuerung einer oder mehrere Kategorien zu zuweisen.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     {305CA226-D286-468e-B848-2B2E8E697B74} 2
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_DWORD] 3
```

In diesem Beispiel wird das Element der Kategorie 3 (Netzwerk und Internet) zugewiesen. Um ein Element mehreren Kategorien hinzuzufügen, geben Sie die Liste als DURCH Kommas getrennten REG SZ-Wert an, z. B. \_ "3,8". Werte können entweder als dezimal oder hexadezimal angegeben werden. Beachten Sie, dass das Hinzufügen eines Elements zu mehreren Kategorien nur in Windows XP Service Pack 2 (SP2) und höher möglich ist. Unter [Zuweisen Systemsteuerung Kategorien finden](assigning-control-panel-categories.md) Sie alle möglichen Werte.

### <a name="step-5"></a>Schritt 5:

**Windows Vista und höher:** Fügen Sie der Registrierung die folgenden Informationen hinzu, um zu erstellen und auf eine XML-Datei zu verweisen, die Aufgabenlinks für das Element enthält. Der Wert muss ein REG SZ-Pfad wie hier gezeigt oder ein Modul und eine Ressourcen-ID (z. B. \_ "C: Programme \\ \\ MyCorp \\ MyAppMyApp.exe,-31") sein, wenn es sich um eine eingebettete Ressource \\ handelt. Der Speicherort der XML-Datei sollte vollständig angegeben werden. Es kann keine Umgebungsvariable wie %ProgramFiles% verwendet werden.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.Software.TasksFileUrl
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_SZ] C:\ProgramFiles\MyCorp\MyApp\MyTasks.xml
```

Weitere Informationen zu Aufgabenlinks und zum Erstellen der XML-Datei, in der sie gespeichert werden, finden Sie unter [Creating Searchable Task Links for a Systemsteuerung Item](creating-searchable-task-links.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrieren Systemsteuerung Elementen](registering-control-panel-items.md)
</dt> <dt>

[Registrieren von ausführbaren Systemsteuerung Elementen](how-to-register-an-executable-control-panel-item-registration-.md)
</dt> </dl>

 

 
