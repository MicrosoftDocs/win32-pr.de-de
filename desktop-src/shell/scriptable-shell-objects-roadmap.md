---
description: Die Windows Shell bietet einen leistungsstarken Satz von Automatisierungsobjekten, mit denen Sie die Shell mit Microsoft Visual Basic und Skriptsprachen wie Microsoft JScript (kompatibel mit der ECMA 262-Sprachspezifikation) und Microsoft Visual Basic Scripting Edition (VBScript) programmieren können. Sie können diese Objekte verwenden, um auf viele der Funktionen und Dialogfelder der Shell zu zugreifen. Beispielsweise können Sie auf das Dateisystem zugreifen, Programme starten und Systemeinstellungen ändern.
title: Skriptfähige Shellobjekte
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 09455fad-a769-42ef-83ba-b745ac819bf3
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e8685b44d00d3f48e8de2a567218ef08c1cb5070
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581778"
---
# <a name="scriptable-shell-objects"></a>Skriptfähige Shellobjekte

Die Windows Shell bietet einen leistungsstarken Satz von Automatisierungsobjekten, mit denen Sie die Shell mit Microsoft Visual Basic und Skriptsprachen wie Microsoft JScript (kompatibel mit der ECMA 262-Sprachspezifikation) und Microsoft Visual Basic Scripting Edition (VBScript) programmieren können. Sie können diese Objekte verwenden, um auf viele der Funktionen und Dialogfelder der Shell zu zugreifen. Beispielsweise können Sie auf das Dateisystem zugreifen, Programme starten und Systemeinstellungen ändern.

In diesem Abschnitt werden die skriptierbaren Shellobjekte erläutert.

-   [Shellversionen](#shell-versions)
-   [Instanziieren von Shellobjekten](#instantiating-shell-objects)
    -   [Späte Bindung](#late-binding)
    -   [HTML OBJECT-Element](#html-object-element)
-   [Shell-Objekt](#shell-object)
    -   [Security](#security)
-   [Ordnerobjekte](#folder-objects)

## <a name="shell-versions"></a>Shellversionen

Viele der Shell-Objekte wurden in Version [4.71 der](versions.md) Shell verfügbar. Andere sind in Version 5.00 und höher verfügbar. Version 5.00 ist ab Windows 2000 verfügbar. In der folgenden Tabelle sind alle Shell-Objekte unter der Version der Shell aufgeführt, in der das Objekt verfügbar wurde.



| Version 4.71                                            | Version 5.00                                          |
|---------------------------------------------------------|-------------------------------------------------------|
| [**Ordner**](folder.md)                                | [**DIDiskQuotaUser**](didiskquotauser-object.md)     |
| [**FolderItemVerb**](folderitemverb.md)                | [**DiskQuotaControl**](diskquotacontrol-object.md)   |
| [**FolderItemVerbs**](folderitemverbs.md)              | [**Ordner2**](folder2-object.md)                     |
| [**Shell**](shell.md)                                  | [**FolderItem**](folderitem.md)                      |
| [**ShellFolderView**](shellfolderview.md)              | [**FolderItems**](folderitems.md)                    |
| [**ShellUIHelper**](shelluihelper.md)                  | [**FolderItems2**](folderitems2-object.md)           |
| [**ShellWindows**](shellwindows.md)                    | [**IShellDispatch2**](ishelldispatch2-object.md)     |
| [**WebViewFolderContents**](../lwef/webviewfoldercontents.md) | [**IShellLinkDual2**](ishelllinkdual2-object.md)     |
|                                                         | [**ShellFolderItem**](shellfolderitem-object.md)     |
|                                                         | [**ShellFolderViewOC**](shellfolderviewoc-object.md) |
|                                                         | [**ShellLinkObject**](shelllinkobject-object.md)     |



 

## <a name="instantiating-shell-objects"></a>Instanziieren von Shellobjekten

Fügen Sie Verweise auf die folgenden Bibliotheken in Ihrem Projekt hinzu, um die Shellobjekte in Visual Basic Anwendungen mit früher Bindung zu instanziieren:

-   Microsoft-Internetsteuerelemente (SHDocVw)
-   Microsoft Shell-Steuerelemente und -Automatisierung (Shell32)

### <a name="late-binding"></a>Späte Bindung

Sie können auch viele der Shell-Objekte mit später Bindung instanziieren. Dieser Ansatz funktioniert in Visual Basic Anwendungen und Skripts. Das folgende Beispiel zeigt, wie sie das [**Shell-Objekt**](shell.md) in der JScript.


```
<SCRIPT LANGUAGE="JScript">
<!--
    function fnCreateShell()    
    {
        // Instantiate the Shell object and invoke its FileRun method.
        var oShell = new ActiveXObject("shell.application");
        oshell.FileRun;
    }
-->
</SCRIPT>
```



Das folgende Beispiel zeigt, wie das [**Folder-Objekt**](folder.md) in VBScript instanziiert wird.


```
<SCRIPT LANGUAGE="VBScript">
<!--
    function fnCreateFolder()
        dim oShell    
        dim oFolder
        dim sDir

        sDir = "C:\SomePath" 
        set oShell = CreateObject("shell.application")
        set oFolder = oShell.NameSpace(sDir)  
    end function
-->  
</SCRIPT>
```



Im vorherigen Beispiel ist *sDir* der Pfad zum [**Folder-Objekt.**](folder.md) Beachten Sie, [**dass die ShellSpecialFolderConstants-Enumerationswerte**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) im Skript nicht verfügbar sind.

Die ProgID für jedes der Shell-Objekte ist in der folgenden Tabelle dargestellt.



| Object                                                  | ProgID                                                                                  |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**DIDiskQuotaUser**](didiskquotauser-object.md)       | Microsoft.DiskQuota.1                                                                   |
| [**DiskQuotaControl**](diskquotacontrol-object.md)     | Späte Bindung nicht möglich                                                                        |
| [**Ordner**](folder.md)                                | Muschel. Shell \_ Application.NameSpace("...")                                               |
| [**Ordner2**](folder2-object.md)                       | Muschel. Shell \_ Application.NameSpace("...")                                               |
| [**FolderItem**](folderitem.md)                        | Muschel. Shell \_ Application.NameSpace("..."). Self oder Folder.Items.Item oder Folder.ParseName |
| [**FolderItems**](folderitems.md)                      | Folder.Items                                                                            |
| [**FolderItems2**](folderitems2-object.md)             | Folder.Items                                                                            |
| [**FolderItemVerb**](folderitemverb.md)                | Shell.NameSpace("..."). Self.Verbs.Item()                                                |
| [**FolderItemVerbs**](folderitemverbs.md)              | FolderItem.Verbs oder Shell.NameSpace("..."). Self.Verbs                                   |
| [**IShellDispatch2**](ishelldispatch2-object.md)       | Muschel. \_Shellanwendung                                                                |
| [**IShellLinkDual2**](ishelllinkdual2-object.md)       | Shell.NameSpace("..."). Self.GetLink oder Shell.NameSpace("..."). Items(). GetLink           |
| [**Shell**](shell.md)                                  | Muschel. \_Shellanwendung                                                                |
| [**ShellFolderItem**](shellfolderitem-object.md)       | Shell.NameSpace("..."). Self oder Shell.NameSpace("..."). Items()                           |
| [**ShellFolderView**](shellfolderview.md)              | Späte Bindung nicht möglich                                                                        |
| [**ShellFolderViewOC**](shellfolderviewoc-object.md)   | Späte Bindung nicht möglich                                                                        |
| [**ShellLinkObject**](shelllinkobject-object.md)       | Shell.NameSpace("..."). Self.GetLink oder Shell.NameSpace("..."). Items(). GetLink           |
| [**ShellUIHelper**](shelluihelper.md)                  | Späte Bindung nicht möglich                                                                        |
| [**ShellWindows**](shellwindows.md)                    | Muschel. Shell \_ Windows oder ShellWindows. \_ NewEnum                                          |
| [**WebViewFolderContents**](../lwef/webviewfoldercontents.md) | Späte Bindung nicht möglich                                                                        |



 

### <a name="html-object-element"></a>HTML OBJECT-Element

Sie können auch das [**OBJECT-Element**](https://msdn.microsoft.com/library/ms535859(v=VS.85).aspx) verwenden, um Shellobjekte auf einer HTML-Seite zu instanziieren. Legen Sie hierzu das **ID-Attribut** des **OBJECT-Elements** auf den Variablennamen fest, den Sie in Ihren Skripts verwenden, und identifizieren Sie das Objekt anhand seiner registrierten Nummer (CLASSID). Der folgende HTML-Code erstellt eine Instanz des [**ShellFolderItem-Objekts**](shellfolderitem-object.md) mithilfe des **OBJECT-Elements.**


```
<OBJECT ID="oShFolderItem" 
    NAME="Shell Folder Item Object"
    CLASSID="clsid:2fe352ea-fd1f-11d2-b1f4-00c04f8eeb3e">
</OBJECT>
```



In der folgenden Tabelle sind jedes Shell-Objekt und die entsprechende CLASSID aufgeführt.



| Shellobjekt                                           | Classid                              |
|--------------------------------------------------------|--------------------------------------|
| [**DIDiskQuotaUser**](didiskquotauser-object.md)       | 7988B571-EC89-11cf-9C00-00AA00A14F56 |
| [**DiskQuotaControl**](diskquotacontrol-object.md)     | 7988B571-EC89-11cf-9C00-00AA00A14F56 |
| [**Ordner**](folder.md)                                | SOLLBDE60-C3FF-11CE-8350-444553540000 |
| [**Folder2**](folder2-object.md)                       | f0d2d8ef-3890-11d2-bf8b-00c04fb93661 |
| [**FolderItem**](folderitem.md)                        | 744129E0-CBE5-11CE-8350-444553540000 |
| [**FolderItems**](folderitems.md)                      | 744129E0-CBE5-11CE-8350-444553540000 |
| [**FolderItems2**](folderitems2-object.md)             | C94F0AD0-F363-11d2-A327-00C04F8EEC7F |
| [**FolderItemVerb**](folderitemverb.md)                | 08EC3E00-50B0-11CF-960C-0080C7F4EE85 |
| [**FolderItemVerbs**](folderitemverbs.md)              | 1F8352C0-50B0-11CF-960C-0080C7F4EE85 |
| [**IShellDispatch2**](ishelldispatch2-object.md)       | A4C6892C-3BA9-11d2-9DEA-00C04FB16162 |
| [**IShellLinkDual2**](ishelllinkdual2-object.md)       | 317EE249-F12E-11d2-B1E4-00C04F8EEB3E |
| [**Shell**](shell.md)                                  | 13709620-C279-11CE-A49E-444553540000 |
| [**ShellFolderItem**](shellfolderitem-object.md)       | 2fe352ea-fd1f-11d2-b1f4-00c04f8eeb3e |
| [**ShellFolderView**](shellfolderview.md)              | 62112AA1-EBE4-11cf-A5FB-0020AFE7292D |
| [**ShellFolderViewOC**](shellfolderviewoc-object.md)   | 4a3df050-23bd-11d2-939f-00a0c91eedba |
| [**ShellLinkObject**](shelllinkobject-object.md)       | 11219420-1768-11d1-95BE-00609797EA4F |
| [**ShellUIHelper**](shelluihelper.md)                  | 64AB4BB7-111E-11D1-8F79-00C04FC2FBE1 |
| [**ShellWindows**](shellwindows.md)                    | 9BA05972-F6A8-11CF-A442-00A0C90A8F39 |
| [**WebViewFolderContents**](../lwef/webviewfoldercontents.md) | 1820FED0-473E-11D0-A96C-00C04FD705A2 |



 

## <a name="shell-object"></a>Shell-Objekt

Das [**Shell-Objekt**](shell.md) stellt die Objekte in der Shell dar. Sie können die vom Shell-Objekt verfügbar gemachten Methoden für Folgendes verwenden:

-   Öffnen, Durchsuchen und Suchen nach Ordnern.
-   Fenster minimieren, wiederherstellen, kaskadieren oder Kachel öffnen.
-   Starten Sie Systemsteuerung Anwendungen.
-   Systemdialogfelder anzeigen.

Benutzer sind vielleicht am besten mit den Befehlen vertraut, auf die sie über das **Startmenü** und das Kontextmenü der Taskleiste zugreifen. Das Kontextmenü der Taskleiste wird angezeigt, wenn Benutzer mit der rechten Maustaste auf die Taskleiste klicken. Die folgende HTML-Anwendung (HTA) erzeugt eine Startseite mit Schaltflächen, die viele methoden des [**Shell-Objekts**](shell.md) implementieren. Einige dieser Methoden implementieren Features im **Startmenü** und im Kontextmenü der Taskleiste.


```
<HTML>
<HEAD>
    <TITLE>Start Page</TITLE>
    
    <OBJECT ID="oShell"
        CLASSID="clsid:13709620-C279-11CE-A49E-444553540000">
    </OBJECT>
    
    <STYLE>
        INPUT {width: 200} 
    </STYLE>  
    
    <SCRIPT LANGUAGE="VBScript">
    <!--
        function fnStart(sMethod)
            select case sMethod
              case 0    
                  'Minimizes all windows on the desktop
                oshell.Shell_MinimizeAll
              case 1  
                  'Displays the Run dialog box
                oshell.FileRun
              case 2  
                  'Displays the Shut Down Windows dialog box
                oshell.Shell_ShutdownWindows
              case 3  
                  'Displays the Find dialog box
                oshell.Shell_FindFilesr
              case 4  
                  'Displays the Date/Time dialog box
                oshell.Shell_SetTime 
              case 5  
                  'Displays the Internet Properties dialog box
                oshell.Shell_ControlPanelItem "INETCPL.cpl"
              case 6  
                  'Explores the My Documents folder
                oshell.Shell_Explore "C:\My Documents"
              case 7  
                  'Enables user to select folder from Program Files
                oshell.Shell_BrowseForFolder 0, "My Programs", 0, "C:\Program Files" 
              case 8  
                  'Opens the Favorites folder
                oshell.Shell_Open "C:\WINDOWS\Favorites"
              case 9  
                  'Displays the Taskbar Properties dialog box
                oshell.Shell_TrayProperties
            end select  
        end function      
    -->
    </SCRIPT>
</HEAD>

<BODY>
    <H1>Start...</H1>
    <INPUT type="button" value="Edit Taskbar Properties" onclick="fnStart(9)"><br>
    <INPUT type="button" value="Open Favorites Folder" onclick="fnStart(8)"><br>
    <INPUT type="button" value="Browse Program Files" onclick="fnStart(7)"><br>
    <INPUT type="button" value="Explore My Documents" onclick="fnStart(6)"><br>
    <INPUT type="button" value="Modify Internet Properties" onclick="fnStart(5)"><br>
    <INPUT type="button" value="Set System Time" onclick="fnStart(4)"><br>
    <INPUT type="button" value="Find a File or Folder" onclick="fnStart(3)"><br>
    <INPUT type="button" value="Shut Down Windows" onclick="fnStart(2)"><br>
    <INPUT type="button" value="Run" onclick="fnStart(1)">     
    <INPUT type="button" value="Minimize All Windows" onclick="fnStart(0)">     
</BODY>
</HTML>
```



### <a name="security"></a>Sicherheit

Als Anwendung wird ein HTA unter einem anderen Sicherheitsmodell als eine Webseite ausgeführt. Um mit einer Webseite zu interagieren, die die Funktionalität der Shell-Objekte implementiert, müssen Benutzer die **Option Initialisieren und Skripts ActiveX Steuerelemente** aktivieren, die nicht als sichere Option für die Sicherheitszone markiert sind, in der sie die Seite anzeigen.

## <a name="folder-objects"></a>Ordnerobjekte

Das [**Folder-Objekt**](folder.md) stellt einen Shellordner dar. Sie können die vom Folder-Objekt verfügbar gemachten Methoden für Folgendes verwenden:

-   Abrufen von Informationen zu einem Ordner.
-   Erstellen Sie Unterordner.
-   Kopieren und Verschieben von Dateiobjekten in den Ordner.

Das [**FolderItem-Objekt**](folderitem.md) stellt ein Element in einem Shellordner dar. Seine Eigenschaften ermöglichen es Ihnen, Informationen über das Element abzurufen. Sie können die von diesem -Objekt verfügbar gemachten Methoden verwenden, um die Verben eines Elements auszuführen oder Informationen zum [**FolderItemVerbs-Objekt**](folderitemverbs.md) eines Elements abzurufen.

Das [**FolderItems-Objekt**](folderitems.md) stellt eine Auflistung von Elementen in einem Shellordner dar. Mithilfe der Methoden und Eigenschaften können Sie Informationen über die Auflistung abrufen.

Das folgende Visual Basic Beispiel zeigt die Beziehung zwischen mehreren Ordnerobjekten und wie sie zusammen verwendet werden können. Wenn der Benutzer auf die Befehlsschaltfläche **cmdGetPath** klickt, zeigt das Programm ein Dialogfeld an, in dem der Benutzer einen Ordner aus **Arbeitsplatz** auswählen kann, wobei ssfDRIVES der [**ShellSpecialFolderConstants-Enumerationswert**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) für **Arbeitsplatz** ist. Wenn der Benutzer einen Ordner ausgibt, wird der Pfad des Ordners im Textfeld **txtPath** angezeigt.


```
Private Sub cmdGetPath_Click()
    Dim oShell As New Shell
    Dim oFolder As Folder
    Dim oFolderItem As FolderItem
 
    Set oFolder = oshell.Shell_BrowseForFolder(Me.hWnd, "Select a Folder", 0, ssfDrives)
   
    Set oFolderItem = oFolderItems.Item

    txtPath.Text = oFolderItem.Path
End Sub
```



In VBScript unterscheidet sich diese Funktion geringfügig, da die [**ShellSpecialFolderConstants-Enumerationswerte**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) im Skript nicht verfügbar sind. Das folgende Beispiel zeigt die VBScript-Entsprechung des vorherigen Beispiels.


```
<SCRIPT LANGUAGE="VBScript">
<!--
    function fnGetMyPathVB() 
        dim oShell
        dim oFolder
        dim oFolderItem
        
        set oShell = CreateObject("shell.application")      
        set oFolder = oshell.Shell_BrowseForFolder(0, "Choose a Folder", 0)             
        set oFolderItem = oFolder.Items.Item         
        
        document.all.item("myPath").innerText = oFolderItem.Path                                
    end function
-->
</SCRIPT>
```



Beachten Sie im folgenden JScript Beispiel, bei dem es sich um eine direkte Übersetzung des vorherigen VBScript-Beispiels handelt, wie die leeren Klammern "()" zum Aufrufen der [**Items-**](folder-items.md) und [**Item-Methoden**](folderitems-item.md) verwendet werden.


```
<SCRIPT LANGUAGE="JavaScript">
<!--
    function fnGetMyPathJ() 
    {       
        var oShell = new ActiveXObject("shell.application");
                    
        var oFolder = new Object;                   
        oFolder = oshell.Shell_BrowseForFolder(0, "Choose a folder", 0);
                                
        var oFolderItem = new Object;       
        oFolderItem = oFolder.Items().Item();                               
        
        document.all.item("myPath").innerText = oFolderItem.Path;
    }    
-->
</SCRIPT>
```



 

 
