---
description: Ein Shell-Erweiterungshandlerobjekt muss registriert werden, bevor die Shell es verwenden kann. In diesem Thema wird allgemein beschrieben, wie Ein Shell-Erweiterungshandler registriert wird.
ms.assetid: e4b98c18-746b-4909-8821-f25de9d15373
title: Registrieren von Shellerweiterungshandlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec883f6e843bdfbf663108c0acda123d786262916f4a347d9433e7fd5f77baca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111210"
---
# <a name="registering-shell-extension-handlers"></a>Registrieren von Shellerweiterungshandlern

Ein Shell-Erweiterungshandlerobjekt muss registriert werden, bevor die Shell es verwenden kann. In diesem Thema wird allgemein beschrieben, wie Ein Shell-Erweiterungshandler registriert wird.

Jedes Mal, wenn Sie einen Shell-Erweiterungshandler erstellen oder ändern, ist es wichtig, das System zu benachrichtigen, dass Sie eine Änderung vorgenommen haben. Rufen Sie dazu [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify)auf, und geben Sie dabei das **SHCNE \_ ASSOCCHANGED-Ereignis** an. Wenn Sie **SHChangeNotify nicht aufrufen,** wird die Änderung möglicherweise erst erkannt, wenn das System neu gestartet wird.

Es gibt einige zusätzliche Faktoren, die für Windows 2000-Systeme gelten. Weitere Informationen finden Sie im Abschnitt [Registrieren von Shell-Erweiterungshandlern für Windows 2000-Systeme.](#registering-shell-extension-handlers)

Wie bei allen Component Object Model-Objekten (COM) müssen Sie eine GUID für den Handler erstellen, indem Sie ein Tool wie Guidgen.exe verwenden, das mit dem Windows Software Development Kit (SDK) bereitgestellt wird. Erstellen Sie unter **HKEY \_ CLASSES \_ ROOT** CLSID einen Unterschlüssel, dessen Name die Zeichenfolgenform \\  dieser GUID ist. Da Es sich bei Shell-Erweiterungshandlern um Prozessserver handelt, müssen Sie auch einen **InprocServer32-Unterschlüssel** unter diesem GUID-Unterschlüssel erstellen, bei dem der (Standard)-Wert auf den Pfad der DLL des Handlers festgelegt ist. Verwenden Sie das Apartmentthreadingmodell. Das folgende Beispiel soll dies erläutern:

```
HKEY_CLASSES_ROOT
   CLSID
      {00021500-0000-0000-C000-000000000046}
         InprocServer32
            (Default) = %windir%\System32\Example.dll
            ThreadingModel = Apartment
```

Jedes Mal, wenn die Shell eine Aktion mit einem Shell-Erweiterungshandler durchführen kann, überprüft sie den entsprechenden Registrierungsunterschlüssel. Der Unterschlüssel, unter dem ein Erweiterungshandler registriert ist, steuert, wann er aufgerufen wird. Beispielsweise ist es üblich, einen Kontextmenühandler namens zu verwenden, wenn die Shell ein Kontextmenü für einen Member eines [Dateityps anzeigt.](fa-file-types.md) In diesem Fall muss der Handler unter dem Unterschlüssel **ProgID** des Dateityps registriert werden.

In diesem Thema werden die folgenden Themen behandelt:

-   [Handlernamen](#handler-names)
-   [Vordefinierte Shellobjekte](#predefined-shell-objects)
-   [Beispiel für eine Erweiterungshandlerregistrierung](#example-of-an-extension-handler-registration)
    -   [Registrieren von Shellerweiterungshandlern](#registering-shell-extension-handlers)
-   [Zugehörige Themen](#related-topics)

## <a name="handler-names"></a>Handlernamen

Um einen Shell-Erweiterungshandler zu aktivieren, erstellen Sie einen Unterschlüssel mit dem Namen des Handlerunterschlüssels (siehe unten) unter dem **ShellEx-Unterschlüssel** der **ProgID** (für Dateitypen) oder des Shell-Objekttypnamens (für vordefinierte Shellobjekte). [ \_ \_](handlers.md)

Wenn Sie beispielsweise einen Kontextmenü-Erweiterungshandler für MyProgram.1 registrieren möchten, erstellen Sie zunächst den folgenden Unterschlüssel:

```
HKEY_CLASSES_ROOT
   MyProgram.1
      ShellEx
         ContextMenuHandlers
```

Erstellen Sie für die folgenden Handler unterhalb des Unterschlüssels "HandlerUnterschlüsselname" einen Unterschlüssel namens als Zeichenfolgenversion des Klassenbezeichners (CLSID) der Shellerweiterung. Mehrere Erweiterungen können unter dem Namen des Handlerunterschlüssels registriert werden, indem mehrere Unterschlüssel erstellt werden.



| Handler                 | Schnittstelle          | Name des Handlerunterschlüssels       |
|-------------------------|--------------------|---------------------------|
| Spaltenanbieterhandler | IColumnProvider    | **ColumnHandlers**        |
| Kontextmenühandler   | IContextMenu       | **ContextMenuHandlers**   |
| Copyhook-Handler        | ICopyHook          | **CopyHookHandlers**      |
| Drag &amp; Drop-Handler   | IContextMenu       | **DragDropHandlers**      |
| Eigenschaftenblatthandler  | IShellPropSheetExt | **PropertySheetHandlers** |



 

Für die folgenden Handler ist der Standardwert des Schlüssels "Handler Subkey Name" die Zeichenfolgenversion der CLSID der Shellerweiterung. Für diese Handler kann nur eine Erweiterung registriert werden.



| Handler                 | Schnittstelle            | Name des Handlerunterschlüssels                        |
|-------------------------|----------------------|--------------------------------------------|
| Datenhandler            | Idataobject          | **Datahandler**                            |
| Drop-Handler            | Idroptarget          | **DropHandler**                            |
| Symbolhandler            | IExtractIconA/W      | **IconHandler**                            |
| Handler für Miniaturansichtsbilder | IThumbnailProvider   | **{E357FCCD-A995-4576-B01F-234630154E96}** |
| QuickInfo-Handler         | IQueryInfo           | **{00021500-0000-0000-C000-000000000046}** |
| Shelllink (ANSI)       | IShellLinkA          | **{000214EE-0000-0000-C000-000000000046}** |
| Shelllink (UNICODE)    | IShellLinkW          | **{000214F9-0000-0000-C000-000000000046}** |
| Strukturierter Speicher      | Istorage             | **{0000000B-0000-0000-C000-000000000046}** |
| Metadaten                | IPropertySetStorage  | **PropertyHandler**                        |
| An Startmenü anheften       | IStartMenuPinnedList | **{a2a9545d-a0c2-42b4-9708-a0b2badd77c8}** |
| An Taskleiste anheften          |                      | **{90AA3A4E-1CBA-4233-B8BB-535773D48449}** |



 

Die Unterschlüssel, die zum Hinzufügen  von **"An Startmenü** anheften" und "An Taskleiste an Taskleiste anheften" zum Kontextmenü eines Elements angegeben werden, sind nur für Dateitypen erforderlich, die den [Eintrag IsShortCut](./links.md) enthalten.

## <a name="predefined-shell-objects"></a>Vordefinierte Shellobjekte

Die Shell definiert zusätzliche Objekte unter **HKEY \_ CLASSES \_ ROOT,** die auf die gleiche Weise wie Dateitypen erweitert werden können. Um beispielsweise einen Eigenschaftenblatthandler für alle Dateien hinzuzufügen, können Sie sich unter dem **Unterschlüssel PropertySheetHandlers** registrieren.

```
HKEY_CLASSES_ROOT
   *
      shellex
         PropertySheetHandlers
```

Die folgende Tabelle enthält die verschiedenen Unterschlüssel von **HKEY \_ CLASSES \_ ROOT,** unter denen Erweiterungshandler registriert werden können. Beachten Sie, dass viele Erweiterungshandler nicht unter allen aufgelisteten Unterschlüsseln registriert werden können. Weitere Informationen finden Sie in der Dokumentation des jeweiligen Handlers.



| Unterschlüssel                    | Beschreibung                                                          | Mögliche Handler                                |
|---------------------------|----------------------------------------------------------------------|--------------------------------------------------|
| **\***                    | Alle Dateien                                                            | Kontextmenü, Eigenschaftenblatt, Verben (siehe unten) |
| **AllFileSystemObjects**  | Alle Dateien und Dateiordner                                           | Kontextmenü, Eigenschaftenblatt, Verben             |
| **Ordner**                | Alle Ordner                                                          | Kontextmenü, Eigenschaftenblatt, Verben             |
| **Verzeichnis**             | Dateiordner                                                         | Kontextmenü, Eigenschaftenblatt, Verben             |
| **\\Verzeichnishintergrund** | Hintergrund des Dateiordners                                               | Nur Kontextmenü                               |
| **DesktopBackground**     | Desktophintergrund (Windows 7 und höher)                            | Kontextmenü, Verben                             |
| **Laufwerk**                 | Alle Laufwerke in MyComputer, z. B. "C: \\ "                             | Kontextmenü, Eigenschaftenblatt, Verben             |
| **Network**               | Gesamtes Netzwerk (unter "Meine Netzwerkorte")                             | Kontextmenü, Eigenschaftenblatt, Verben             |
| **\\Netzwerktyp\\\#**     | Alle Objekte vom Typ \# (siehe unten)                                   | Kontextmenü, Eigenschaftenblatt, Verben             |
| **Netshare**              | Alle Netzwerkfreigaben                                                   | Kontextmenü, Eigenschaftenblatt, Verben             |
| **NetServer**             | Alle Netzwerkserver                                                  | Kontextmenü, Eigenschaftenblatt, Verben             |
| *\_ \_ Netzwerkanbietername* | Alle vom Netzwerkanbieter bereitgestellten Objekte "*\_ \_ Netzwerkanbietername*" | Kontextmenü, Eigenschaftenblatt, Verben             |
| **Drucker**              | Alle Drucker                                                         | Kontextmenü, Eigenschaftenblatt                    |
| **Audiocd**               | Audio-CD auf CD-Laufwerk                                                 | Nur Verben                                       |
| **Dvd**                   | DVD-Laufwerk (Windows 2000)                                             | Kontextmenü, Eigenschaftenblatt, Verben             |



 

### <a name="notes"></a>Hinweise

-   Auf das Kontextmenü des Dateiordners wird zugegriffen, indem Sie mit der rechten Maustaste auf einen Dateiordner klicken, jedoch nicht auf den Inhalt des Ordners.
-   "Verben" sind spezielle Befehle, die unter **HKEY \_ CLASSES \_ ROOT** \\ *Subkey* Shell Verb registriert \\  \\ sind.
-   Für **Den** \\ **Netzwerktyp** \\ **\#** ist " " ein \# Netzwerkanbietertypcode im Dezimalformat. Der Typcode des Netzwerkanbieters ist das obere Wort eines Netzwerktyps. Die Liste der Netzwerktypen wird in der Headerdatei Winnetwk.h angegeben (WNNC \_ \_ \* NET-Werte). Beispielsweise ist WNNC \_ NET \_ SHIVA 0x00330000, sodass der entsprechende Typunterschlüssel **HKEY \_ CLASSES \_ ROOT** \\ **Network** \\ **Type** \\ **51** wäre.
-   "*\_ \_ Netzwerkanbietername*" ist ein Netzwerkanbietername, wie durch [**WNetGetProviderName**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetprovidernamea)angegeben, wobei die Leerzeichen in Unterstriche konvertiert werden. Wenn beispielsweise der Microsoft-Netzwerknetzwerkanbieter installiert ist, lautet der Anbietername "Microsoft Windows Network" und der entsprechende *\_ \_ Netzwerkanbietername* **Microsoft Windows \_ \_ Network.**

## <a name="example-of-an-extension-handler-registration"></a>Beispiel für die Registrierung eines Erweiterungshandlers

Um einen bestimmten Handler zu aktivieren, erstellen Sie einen Unterschlüssel unter dem Unterschlüssel des Erweiterungshandlertyps mit dem Namen des Handlers. Die Shell verwendet nicht den Namen des Handlers, muss sich jedoch von allen anderen Namen unter diesem Typunterschlüssel unterscheiden. Legen Sie den Standardwert des Unterschlüssels name auf die Zeichenfolgenform der GUID des Handlers fest.

Das folgende Beispiel veranschaulicht Registrierungseinträge, die Kontextmenü- und Eigenschaftenblatterweiterungshandler mithilfe eines Beispieldateityps vom Typ ".myp" aktivieren.

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

### <a name="registering-shell-extension-handlers"></a>Registrieren von Shellerweiterungshandlern

Das in diesem Abschnitt beschriebene Registrierungsverfahren muss für alle Windows Systeme befolgt werden. Bei späteren Systemen kann jedoch ein zusätzlicher Schritt erforderlich sein. Da diese neueren Versionen von Windows für die Verwendung in einer verwalteten Umgebung konzipiert sind, kann der Zugriff auf die Registrierung administratorisch eingeschränkt werden, was einen etwas anderen Installationsansatz erfordert als im vorherigen Abschnitt beschrieben.

> [!Note]  
> Setupprogramme sollten in der Regel nicht direkt in die Registrierung schreiben. Stattdessen sollte das Setup mit Windows Installer-Paketen durchgeführt werden. Mit diesen Tools wird sichergestellt, dass Software gut ausgeführt wird und Zugriff auf Funktionen wie die Benutzerklassenregistrierung bietet.

 

Shellerweiterungshandler werden im Shellprozess ausgeführt. Da es sich um einen Systemprozess handelt, kann der Administrator eines Systems Shellerweiterungshandler auf die Handler  in einer genehmigten Liste beschränken, indem er den Wert EnforceShellExtensionSecurity des Explorer-Schlüssels auf 1 festlegt, wie hier gezeigt:

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

Um einen Shellerweiterungshandler in der genehmigten Liste zu platzieren, erstellen Sie einen **REG \_ SZ-Wert,** dessen Name die Zeichenfolgenform der GUID des Handlers unter dem Unterschlüssel **Genehmigt** ist.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Shell Extensions
                  Approved
```

Im folgenden Beispiel werden beispielsweise die Handler *MyCommand* und *MyPropSheet* der genehmigten Liste hinzugefügt.

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

Die Shell verwendet nicht den Wert, der der GUID zugewiesen ist, sollte jedoch festgelegt werden, um die Überprüfung der Registrierung zu vereinfachen.

Ihre Setupanwendung kann dem Unterschlüssel **Genehmigt** nur Werte hinzufügen, wenn die Person, die die Anwendung installiert, über ausreichende Berechtigungen verfügt. Wenn beim Versuch, einen Erweiterungshandler hinzuzufügen, ein Fehler auftritt, sollten Sie den Benutzer darüber informieren, dass Administratorrechte erforderlich sind, um die Anwendung vollständig zu installieren. Wenn der Handler für die Anwendung wichtig ist, sollten Sie das Setup nicht erfolgreich ausführen und den Benutzer benachrichtigen, sich an einen Administrator zu wenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Initialisieren von Shellerweiterungshandlern](int-shell-exts.md)
</dt> </dl>

 

 
