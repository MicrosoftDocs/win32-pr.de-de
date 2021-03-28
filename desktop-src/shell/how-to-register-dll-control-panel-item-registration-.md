---
description: System Steuerungselemente, die in einer DLL implementiert sind, die die CPlApplet-Funktion exportiert, haben unterschiedliche Registrierungsanforderungen als exe-Dateien.
title: Registrieren von dll-System Steuerungselementen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37b82225dcb40487c60210752b2c15af23f95bd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756505"
---
# <a name="how-to-register-dll-control-panel-items"></a>Registrieren von dll-System Steuerungselementen

> [!Note]  
> Aktuelle Implementierungs Richtlinien gibt an, dass neue System Steuerungselemente als exe-Dateien anstatt als cpl-Dateien implementiert werden sollen. Die folgenden Informationen sind hauptsächlich für Legacy Zwecke enthalten.

 

System Steuerungselemente, die in einer DLL implementiert sind, die die [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) -Funktion exportiert, haben unterschiedliche Registrierungsanforderungen als exe-Dateien. Ab Windows XP sollten im Ordner "Programme" des Ordners der zugehörigen Anwendung neue DLLs für System Steuerungselemente installiert werden. Elemente, die im Verzeichnis "System32" mit der Erweiterung ". cpl" gespeichert sind, müssen nicht registriert werden. Sie werden automatisch in der Systemsteuerung angezeigt. Alle anderen System Steuerungselemente, die **CPlApplet** verwenden, müssen auf eine von zwei Arten registriert werden:

-   Wenn das System Steuerungselement für alle Benutzer verfügbar sein soll, registrieren Sie den Pfad auf Computer Basis, indem Sie den Wert " **reg \_ Expand \_ SZ** " zu **HKEY \_ local \_ Machine** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Systemsteuerung** \\ **CPLS** unter Key festlegen. Legen Sie dabei auf den DLL-Pfad fest.
-   Wenn das System Steuerungselement auf Benutzerbasis verfügbar sein soll, verwenden Sie den **aktuellen HKEY- \_ \_ Benutzer** als Stamm Schlüssel anstelle des **lokalen HKEY- \_ \_** Computers.

In den folgenden zwei Beispielen wird das System Steuerungselement *mycplapp* registriert. Die dll wird MyCpl.cpl benannt und befindet sich im Anwendungsverzeichnis *MyCorp \\ myapp* . Dieses erste Beispiel veranschaulicht die Registrierung pro Computer.

## <a name="instructions"></a>Instructions

### <a name="step-1"></a>Schritt 1:

Fügen Sie diese Informationen in die Registrierung ein, um das vorhanden sein der CPL-Datei zu registrieren.

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

**Windows Vista und höher:** Fügen Sie der Registrierung diese zusätzlichen Informationen hinzu, um eine GUID für das System Steuerungselement bereitzustellen.

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

Durch das Erstellen einer GUID zur eindeutigen Identifizierung des System Steuerungs Elements können Sie der Systemsteuerung Aufgaben Verknüpfungen hinzufügen. Ohne diese GUID gibt es keine Möglichkeit, dass die Aufgaben Verknüpfungen mit dem System Steuerungselement verknüpft werden können. Weitere Informationen finden Sie unter [Erstellen durch suchbarer Aufgaben Verknüpfungen für ein System Steuerungselement](creating-searchable-task-links.md).

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

Wenn Sie einen kanonischen Namen hinzufügen, können Benutzer das System Steuerungselement über eine Befehlszeile starten, indem Sie eingeben `control.exe /name MyCorporation.MyCpl` . Dies ermöglicht es auch, eine Implementierung von einer CPL-Datei in eine exe-Datei zu einem späteren Zeitpunkt zu ändern, ohne dass Programme aufgerufen werden müssen, um Änderungen vorzunehmen, da Sie das Element weiterhin durch den kanonischen Namen öffnen können. Weitere Informationen zu kanonischen Namen finden Sie unter [Ausführen von System Steuerungselementen](executing-control-panel-items.md).

### <a name="step-4"></a>Schritt 4:

**Windows Vista und höher:** Fügen Sie der Registrierung die folgenden Informationen hinzu, um ein System Steuerungselement einer oder mehreren Kategorien zuzuweisen.

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

**Windows XP:** Fügen Sie der Registrierung die folgenden Informationen hinzu, um ein System Steuerungselement einer oder mehreren Kategorien zuzuweisen.

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

In diesem Beispiel wird das Element der Kategorie 3 zugewiesen, d. h. Netzwerk und Internet. Wenn Sie ein Element mehreren Kategorien hinzufügen möchten, geben Sie die Liste als reg- \_ SZ-Wert an, der durch Kommas getrennt ist, z. b. "3, 8". Werte können als Dezimal oder hexadezimal angegeben werden. Beachten Sie, dass die Möglichkeit zum Hinzufügen eines Elements zu mehreren Kategorien nur in Windows XP Service Pack 2 (SP2) und höher möglich ist. Alle möglichen Werte finden Sie unter [Zuweisen von System Steuerungs Kategorien](assigning-control-panel-categories.md) .

### <a name="step-5"></a>Schritt 5:

**Windows Vista und höher:** Fügen Sie der Registrierung die folgenden Informationen hinzu, um auf eine XML-Datei zum Speichern von Aufgaben Verknüpfungen für das Element zu verweisen. Der Wert muss ein REG SZ-Pfad sein, \_ wie hier gezeigt, oder ein Modul und eine Ressourcen-ID (z. b. "C: \\ Program Files \\ MyCorp \\ myapp \\MyApp.exe,-31"), wenn es sich um eine eingebettete Ressource handelt. Der Speicherort der XML-Datei muss vollständig angegeben werden. Eine Umgebungsvariable, z. b .% Program Files%, kann nicht verwendet werden.

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

Weitere Informationen zu Aufgaben Verknüpfungen und zum Erstellen der XML-Datei, um Sie zu speichern, finden Sie unter [Erstellen von durchsuchbaren Aufgaben Verknüpfungen für ein System Steuerungselement](creating-searchable-task-links.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[System Steuerungselemente werden registriert](registering-control-panel-items.md)
</dt> <dt>

[Registrieren von ausführbaren System Steuerungselementen](how-to-register-an-executable-control-panel-item-registration-.md)
</dt> </dl>

 

 
