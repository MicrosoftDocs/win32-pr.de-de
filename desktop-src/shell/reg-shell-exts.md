---
description: Ein shellerweiterungshandlerobjekt muss registriert werden, bevor es von der Shell verwendet werden kann. In diesem Thema wird eine allgemeine Erörterung der Registrierung eines Shellerweiterungs Handlers erläutert.
ms.assetid: e4b98c18-746b-4909-8821-f25de9d15373
title: Registrieren von Shellerweiterungs Handlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca50bfaff984884b74ecc8572d4af9d96c55d0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980201"
---
# <a name="registering-shell-extension-handlers"></a>Registrieren von Shellerweiterungs Handlern

Ein shellerweiterungshandlerobjekt muss registriert werden, bevor es von der Shell verwendet werden kann. In diesem Thema wird eine allgemeine Erörterung der Registrierung eines Shellerweiterungs Handlers erläutert.

Jedes Mal, wenn Sie einen Shellerweiterungs Handler erstellen oder ändern, ist es wichtig, das System zu benachrichtigen, dass Sie eine Änderung vorgenommen haben. Rufen Sie hierzu " [**shchangenotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify)" auf, und geben Sie das **shcne-Ereignis " \_ assocchanged** " an. Wenn Sie **shchangenotify** nicht aufrufen, wird die Änderung möglicherweise erst erkannt, wenn das System neu gestartet wird.

Für Windows 2000-Systeme gelten einige zusätzliche Faktoren. Weitere Informationen finden Sie im Abschnitt [Registrieren von Shellerweiterungs Handlern auf Windows 2000-Systemen](#registering-shell-extension-handlers) .

Wie bei Component Object Model allen COM-Objekten müssen Sie mithilfe eines Tools wie Guidgen.exe, das mit dem Windows Software Development Kit (SDK) bereitgestellt wird, eine GUID für den Handler erstellen. Erstellen Sie unter **HKEY \_ Classes \_ root** \\ **CLSID** einen Unterschlüssel, dessen Name die Zeichen folgen Form dieser GUID ist. Da es sich bei Shellerweiterungs Handlern um Prozess interne Server handelt, müssen Sie auch unter diesem GUID-Unterschlüssel einen **InProcServer32** -Unterschlüssel erstellen, wobei der (standardmäßige) Wert auf den Pfad der DLL des Handler festgelegt ist. Verwenden Sie das Apartment Threading Modell. Das folgende Beispiel soll dies erläutern:

```
HKEY_CLASSES_ROOT
   CLSID
      {00021500-0000-0000-C000-000000000046}
         InprocServer32
            (Default) = %windir%\System32\Example.dll
            ThreadingModel = Apartment
```

Jedes Mal, wenn die Shell eine Aktion ausführt, die einen Shellerweiterungs Handler einschließen kann, prüft Sie den entsprechenden Registrierungs Unterschlüssel. Der Unterschlüssel, unter dem ein Erweiterungs Handler registriert ist, wenn er aufgerufen wird. Beispielsweise ist es üblich, dass ein Kontextmenü Handler aufgerufen wird, wenn die Shell ein Kontextmenü für einen Member eines [Dateityps](fa-file-types.md)anzeigt. In diesem Fall muss der Handler unter dem **ProgID** -Unterschlüssel des Dateityps registriert werden.

In diesem Thema werden die folgenden Themen behandelt:

-   [Handlernamen](#handler-names)
-   [Vordefinierte Shellobjekte](#predefined-shell-objects)
-   [Beispiel für eine erweiterungshandlerregistrierung](#example-of-an-extension-handler-registration)
    -   [Registrieren von Shellerweiterungs Handlern](#registering-shell-extension-handlers)
-   [Zugehörige Themen](#related-topics)

## <a name="handler-names"></a>Handlernamen

Erstellen Sie zum Aktivieren eines Shellerweiterungs Handlers einen Unterschlüssel mit dem Namen des unter Schlüssels des Handlers (siehe unten) unter dem **shellex** -Unterschlüssel der **ProgID** (für Dateitypen) oder dem shellobjekttypnamen (für [vordefinierte \_ \_ Shellobjekte](handlers.md)).

Wenn Sie z. b. einen Erweiterungs Handler für das Kontextmenü für MyProgram. 1 registrieren möchten, erstellen Sie zunächst den folgenden Unterschlüssel:

```
HKEY_CLASSES_ROOT
   MyProgram.1
      ShellEx
         ContextMenuHandlers
```

Erstellen Sie für die folgenden Handler einen Unterschlüssel unter dem Unterschlüssel Name des unter Schlüssels "Handler", der als Zeichen folgen Version des Klassen Bezeichners (CLSID) der Shellerweiterung bezeichnet wird. Mehrere Erweiterungen können unter dem Namen des unter Schlüssels des Handlers registriert werden, indem mehrere Unterschlüssel erstellt werden.



| Handler                 | Schnittstelle          | Name des unter Schlüssels des Handlers       |
|-------------------------|--------------------|---------------------------|
| Spalten Anbieter Handler | Icolumnprovider    | **Columnhandlers**        |
| Kontextmenü Handler   | IContextMenu       | **ContextMenuHandlers**   |
| Copyhook-Handler        | Icopyhook          | **Copyhuokhandlers**      |
| Drag &amp; Drop-Handler   | IContextMenu       | **Dragdrophandlers**      |
| Eigenschaftenblatthandler  | Ishellpropsheetext | **Propertysheethandlers** |



 

Bei den folgenden Handlern ist der Standardwert für den Schlüssel Name des unter Schlüssels "Handler" die Zeichen folgen Version der CLSID der Shellerweiterung. Für diese Handler kann nur eine Erweiterung registriert werden.



| Handler                 | Schnittstelle            | Name des unter Schlüssels des Handlers                        |
|-------------------------|----------------------|--------------------------------------------|
| Daten Handler            | IDataObject          | **DataHandler**                            |
| Drop-Handler            | IDropTarget          | **Drophandler**                            |
| Symbol Handler            | Iextracticona/W      | **Iconhandler**                            |
| Miniatur Ansichts Bild Handler | IThumbnailProvider   | **{E357FCCD-A995-4576-B01F-234630154E96}** |
| QuickInfo-Handler         | Iqueryinfo           | **{00021500-0000-0000-C000-000000000046}** |
| Shelllink (ANSI)       | IShellLinkA          | **{000214ee-0000-0000-C000-000000000046}** |
| Shelllink (Unicode)    | Ishelllinkw          | **{0002149-0000-0000-C000-000000000046}** |
| Strukturierter Speicher      | IStorage             | **{0000000b-0000-0000-C000-000000000046}** |
| Metadaten                | IPropertySetStorage  | **Propertyhandler**                        |
| An Startmenü anheften       | Istartmenupinnedlist | **{a2a9545d-a0c2-42b4-9708-a0b2badd77c8}** |
| An Taskleiste anheften          |                      | **{90aa3a4e-1cba-4233-B8BB-535773d48449}** |



 

Die angegebenen Unterschlüssel zum Hinzufügen einer **PIN zum Startmenü** und zum Anheften **an die Taskleiste** an das Kontextmenü eines Elements sind nur für Dateitypen erforderlich, die den [IsShortcut](./links.md) -Eintrag enthalten.

## <a name="predefined-shell-objects"></a>Vordefinierte Shellobjekte

Die Shell definiert zusätzliche Objekte unter **HKEY \_ Classes \_ root** , die auf die gleiche Weise wie Dateitypen erweitert werden können. Wenn Sie z. b. einen Eigenschaften Blatt Handler für alle Dateien hinzufügen möchten, können Sie sich unter dem **propertysheethandlers** -Unterschlüssel registrieren.

```
HKEY_CLASSES_ROOT
   *
      shellex
         PropertySheetHandlers
```

In der folgenden Tabelle sind die verschiedenen Unterschlüssel von **HKEY- \_ Klassen \_ root** , unter denen Erweiterungs Handler registriert werden können, zu finden. Beachten Sie, dass viele Erweiterungs Handler nicht unter allen aufgelisteten unter Schlüsseln registriert werden können. Weitere Informationen finden Sie in der Dokumentation des jeweiligen Handlers.



| Unterschlüssel                    | BESCHREIBUNG                                                          | Mögliche Handler                                |
|---------------------------|----------------------------------------------------------------------|--------------------------------------------------|
| **\** _                    | Alle Dateien                                                            | Kontextmenü, Eigenschaften Blatt, Verben (siehe unten) |
| _ *AllFilesystemObjects**  | Alle Dateien und Datei Ordner                                           | Kontextmenü, Eigenschaften Blatt, Verben             |
| **Ordner**                | Alle Ordner                                                          | Kontextmenü, Eigenschaften Blatt, Verben             |
| **Verzeichnis**             | Datei Ordner                                                         | Kontextmenü, Eigenschaften Blatt, Verben             |
| **Verzeichnis \\ Hintergrund** | Hintergrund des Datei Ordners                                               | Nur Kontextmenü                               |
| **DesktopBackground**     | Desktop Hintergrund (Windows 7 und höher)                            | Kontextmenü, Verben                             |
| **Laufwerk**                 | Alle Laufwerke in "MyComputer", z. b. "C: \\ "                             | Kontextmenü, Eigenschaften Blatt, Verben             |
| **Network**               | Gesamtes Netzwerk (unter "meine Netzwerk Plätze")                             | Kontextmenü, Eigenschaften Blatt, Verben             |
| **\\Netzwerktyp\\\#**     | Alle Objekte des Typs \# (siehe unten)                                   | Kontextmenü, Eigenschaften Blatt, Verben             |
| **NetShare**              | Alle Netzwerkfreigaben                                                   | Kontextmenü, Eigenschaften Blatt, Verben             |
| **Netserver**             | Alle Netzwerkserver                                                  | Kontextmenü, Eigenschaften Blatt, Verben             |
| *Name des Netzwerk \_ Anbieters \_* | Alle Objekte, die vom Netzwerkanbieter "*Netzwerk \_ Anbieter \_ Name*" bereitgestellt werden | Kontextmenü, Eigenschaften Blatt, Verben             |
| **Drucker**              | Alle Drucker                                                         | Kontextmenü, Eigenschaften Blatt                    |
| **AudioCD**               | AudioCD in CD-Laufwerk                                                 | Nur Verben                                       |
| **DVD**                   | DVD-Laufwerk (Windows 2000)                                             | Kontextmenü, Eigenschaften Blatt, Verben             |



 

### <a name="notes"></a>Notizen

-   Der Zugriff auf das Kontextmenü des Datei Ordners wird durch einen Rechtsklick innerhalb eines Datei Ordners, aber nicht über den Inhalt des Ordners erreicht.
-   "Verbs" sind spezielle Befehle, die unter **HKEY \_ Classes \_ root** \\ *subkey* \\ **Shell** \\ **Verb** registriert sind.
-   Für den \\ **Netzwerktyp** \\ **\#** \# ist "" ein Netzwerk Anbietertyp Code in Dezimal. Der Typ Code des Netzwerk Anbieters ist das hohe Wort eines Netzwerk Typs. Die Liste der Netzwerktypen wird in der "winnetwk. h"-Header Datei (wnnc \_ net \_ \* Values) angegeben. Beispielsweise ist wnnc \_ net \_ Shiva 0x00330000, daher wäre der entsprechende typunter Schlüssel **HKEY \_ Classes \_ root** \\ **Network** \\ **Type** \\ **51**.
-   der *Name \_ des \_ Netzwerk Anbieters wird* von [**wnetgetprovidername**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetprovidernamea)angegeben, wobei die Leerzeichen in Unterstriche konvertiert werden. Wenn z. b. der Microsoft-Netzwerk Netzwerkanbieter installiert ist, lautet sein Anbieter Name "Microsoft Windows-Netzwerk", und der entsprechende *Netzwerk \_ Anbieter \_ Name* lautet **Microsoft \_ Windows- \_ Netzwerk**.

## <a name="example-of-an-extension-handler-registration"></a>Beispiel für eine erweiterungshandlerregistrierung

Um einen bestimmten Handler zu aktivieren, erstellen Sie unter dem Typ Unterschlüssel des Erweiterungs Handlers einen Unterschlüssel mit dem Namen des Handlers. Die Shell verwendet nicht den Namen des Handlers, aber Sie muss sich von allen anderen Namen unter diesem typunter Schlüssel unterscheiden. Legen Sie den Standardwert des Namens unter Schlüssels auf die Zeichen folgen Form der GUID des Handlers fest.

Das folgende Beispiel veranschaulicht Registrierungseinträge, die Erweiterungs Handler für Kontextmenü und Eigenschaften Seiten mithilfe des Dateityps example. MYP ermöglichen.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   CLSID
      {00000000-1111-2222-3333-444444444444}
         InProcServer32
            (Default) = C:\MyDir\MyCommand.dll
            ThreadingModel = Apartment
      {11111111-2222-3333-4444-555555555555}
         InProcServer32
            (Default) = C:\MyDir\MyPropSheet.dll
            ThreadingModel = Apartment
   MyProgram.1
      (Default) = MyProgram Application
      Shellex
         ContextMenuHandler
            MyCommand
               (Default) = {00000000-1111-2222-3333-444444444444}
         PropertySheetHandlers
            MyPropSheet
               (Default) = {11111111-2222-3333-4444-555555555555}
```

### <a name="registering-shell-extension-handlers"></a>Registrieren von Shellerweiterungs Handlern

Das in diesem Abschnitt beschriebene Registrierungsverfahren muss für alle Windows-Systeme befolgt werden. Bei späteren Systemen ist jedoch möglicherweise ein zusätzlicher Schritt erforderlich. Da diese neueren Versionen von Windows für die Verwendung in einer verwalteten Umgebung entworfen wurden, kann der Zugriff auf die Registrierung administrativ eingeschränkt werden, was einen etwas anderen Ansatz für die Installation erfordert, als im vorherigen Abschnitt beschrieben.

> [!Note]  
> Setup Programme sollten in der Regel nicht direkt in die Registrierung schreiben. Stattdessen sollte Setup mit Windows Installer Paketen durchgeführt werden. Diese Tools stellen sicher, dass die Software ordnungsgemäß ausgeführt wird und den Zugriff auf Funktionen wie die benutzerspezifische Klassen Registrierung ermöglicht.

 

Shellerweiterungs Handler werden im Shellprozess ausgeführt. Da es sich um einen System Prozess handelt, kann der Administrator eines Systems shellerweiterungshandler auf die in einer genehmigten Liste beschränken, indem der EnforceShellExtensionSecurity-Wert des **Explorer** -Schlüssels auf 1 festgelegt wird, wie hier gezeigt:

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
                  Explorer
                     EnforceShellExtensionSecurity = 1
```

Zum Platzieren eines Shellerweiterungs Handlers in der genehmigten Liste erstellen Sie einen **reg \_ SZ** -Wert, dessen Name die Zeichen folgen Form der GUID des Handlers unter dem **genehmigten** Unterschlüssel ist.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Shell Extensions
                  Approved
```

Im folgenden Beispiel werden z. b. die Handler *myCommand* und *mypropsheet* der genehmigten Liste hinzugefügt.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Shell Extensions
                  Approved
                     {00000000-1111-2222-3333-444444444444} = MyCommand
                     {11111111-2222-3333-4444-555555555555} = MyPropSheet
```

Die Shell verwendet nicht den Wert, der der GUID zugewiesen ist, sondern sollte so festgelegt werden, dass die Überprüfung der Registrierung erleichtert wird.

Die Setup Anwendung kann dem **genehmigten** Unterschlüssel nur Werte hinzufügen, wenn die Person, die die Anwendung installiert, über ausreichende Berechtigungen verfügt. Wenn beim Versuch, einen Erweiterungs Handler hinzuzufügen, ein Fehler auftritt, sollten Sie den Benutzer darüber informieren, dass Administratorrechte erforderlich sind, um die Anwendung vollständig zu installieren. Wenn der Handler für die Anwendung unverzichtbar ist, sollten Sie das Setup fehlschlagen und den Benutzer bitten, sich an einen Administrator zu wenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Initialisieren von Shellerweiterungs Handlern](int-shell-exts.md)
</dt> </dl>

 

 
