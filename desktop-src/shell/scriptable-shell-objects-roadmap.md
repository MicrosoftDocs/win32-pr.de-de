---
description: Die Windows-Shell bietet einen leistungsstarken Satz von Automatisierungs Objekten, mit denen Sie die Shell mit Microsoft-Visual Basic und Skriptsprachen wie Microsoft JScript (kompatibel mit der ECMA 262-Sprachspezifikation) und Microsoft Visual Basic Scripting Edition (VBScript) programmieren können. Sie können diese Objekte verwenden, um auf viele der Funktionen und Dialogfelder der Shell zuzugreifen. Beispielsweise können Sie auf das Dateisystem zugreifen, Programme starten und Systemeinstellungen ändern.
title: Scriptable-Shellobjekte
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 09455fad-a769-42ef-83ba-b745ac819bf3
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 4c39e7e58a9715598056fb74aa154ed8a850f523
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980465"
---
# <a name="scriptable-shell-objects"></a>Scriptable-Shellobjekte

Die Windows-Shell bietet einen leistungsstarken Satz von Automatisierungs Objekten, mit denen Sie die Shell mit Microsoft-Visual Basic und Skriptsprachen wie Microsoft JScript (kompatibel mit der ECMA 262-Sprachspezifikation) und Microsoft Visual Basic Scripting Edition (VBScript) programmieren können. Sie können diese Objekte verwenden, um auf viele der Funktionen und Dialogfelder der Shell zuzugreifen. Beispielsweise können Sie auf das Dateisystem zugreifen, Programme starten und Systemeinstellungen ändern.

In diesem Abschnitt werden die Skript fähigen Shellobjekte vorgestellt.

-   [Shell-Versionen](#shell-versions)
-   [Instanziieren von shellobjekten](#instantiating-shell-objects)
    -   [Späte Bindung](#late-binding)
    -   [HTML-Objekt Element](#html-object-element)
-   [Shellobjekt](#shell-object)
    -   [Security](#security)
-   [Ordner Objekte](#folder-objects)

## <a name="shell-versions"></a>Shell-Versionen

Viele der Shellobjekte wurden in [Version 4,71](versions.md) der Shell verfügbar. Andere sind in Version 5,00 und höher verfügbar. Version 5,00 wurde mit Windows 2000 verfügbar. In der folgenden Tabelle werden die einzelnen Shellobjekte unter der-Version der Shell aufgelistet, in der das Objekt verfügbar wurde.



| Version 4,71                                            | Version 5,00                                          |
|---------------------------------------------------------|-------------------------------------------------------|
| [**Ordner**](folder.md)                                | [**Didiskquotauser**](didiskquotauser-object.md)     |
| [**Folderitemverb**](folderitemverb.md)                | [**Diskquotacontrol**](diskquotacontrol-object.md)   |
| [**Folderitemverbs**](folderitemverbs.md)              | [**Folder2**](folder2-object.md)                     |
| [**Shell**](shell.md)                                  | [**Von folderItem**](folderitem.md)                      |
| [**Shellfolderview**](shellfolderview.md)              | [**Folderitems**](folderitems.md)                    |
| [**Shelluihelper**](shelluihelper.md)                  | [**FolderItems2**](folderitems2-object.md)           |
| [**Shellwindows**](shellwindows.md)                    | [**IShellDispatch2**](ishelldispatch2-object.md)     |
| [**Webviewfoldercontents**](../lwef/webviewfoldercontents.md) | [**IShellLinkDual2**](ishelllinkdual2-object.md)     |
|                                                         | [**Shellfolderitem**](shellfolderitem-object.md)     |
|                                                         | [**Shellfolderviewoc**](shellfolderviewoc-object.md) |
|                                                         | [**Shelllinkobject**](shelllinkobject-object.md)     |



 

## <a name="instantiating-shell-objects"></a>Instanziieren von shellobjekten

Fügen Sie Verweise auf die folgenden Bibliotheken in Ihrem Projekt hinzu, um die Shellobjekte in Visual Basic Anwendungen mit einer frühen Bindung zu instanziieren:

-   Microsoft Internet Controls (shdocvw)
-   Microsoft Shell-Steuerelemente und Automatisierung (shell32)

### <a name="late-binding"></a>Späte Bindung

Sie können auch viele der Shellobjekte mit späterer Bindung instanziieren. Diese Vorgehensweise funktioniert in Visual Basic Anwendungen und in Skripts. Im folgenden Beispiel wird gezeigt, wie das [**Shellobjekt**](shell.md) in JScript instanziiert wird.


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



Im folgenden Beispiel wird gezeigt, wie das [**Folder**](folder.md) -Objekt in VBScript instanziiert wird.


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



Im vorherigen Beispiel ist *sDir* der Pfad zum [**Ordner**](folder.md) Objekt. Beachten Sie, dass die [**shellspecialfolderconstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) -Enumerationswerte im Skript nicht verfügbar sind.

Die ProgID für die einzelnen Shellobjekte ist in der folgenden Tabelle dargestellt.



| Object                                                  | ProgID                                                                                  |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**Didiskquotauser**](didiskquotauser-object.md)       | Microsoft. Diskquota. 1                                                                   |
| [**Diskquotacontrol**](diskquotacontrol-object.md)     | Die Bindung kann nicht spät                                                                        |
| [**Ordner**](folder.md)                                | schel. Shell \_ Application. Namespace ("...")                                               |
| [**Folder2**](folder2-object.md)                       | schel. Shell \_ Application. Namespace ("...")                                               |
| [**Von folderItem**](folderitem.md)                        | schel. Shell \_ Application. Namespace ("..."). Self oder Folder. Items. Item oder Folder. Parser Name |
| [**Folderitems**](folderitems.md)                      | Ordner. Items                                                                            |
| [**FolderItems2**](folderitems2-object.md)             | Ordner. Items                                                                            |
| [**Folderitemverb**](folderitemverb.md)                | Shell. Namespace ("..."). Self. Verbs. Item ()                                                |
| [**Folderitemverbs**](folderitemverbs.md)              | FolderItem. Verbs oder Shell. Namespace ("..."). Selbst. Verben                                   |
| [**IShellDispatch2**](ishelldispatch2-object.md)       | schel. \_Shellanwendung                                                                |
| [**IShellLinkDual2**](ishelllinkdual2-object.md)       | Shell. Namespace ("..."). Self. getlink oder Shell. Namespace ("..."). Elemente (). Getlink           |
| [**Shell**](shell.md)                                  | schel. \_Shellanwendung                                                                |
| [**Shellfolderitem**](shellfolderitem-object.md)       | Shell. Namespace ("..."). Self oder Shell. Namespace ("..."). Elemente ()                           |
| [**Shellfolderview**](shellfolderview.md)              | Die Bindung kann nicht spät                                                                        |
| [**Shellfolderviewoc**](shellfolderviewoc-object.md)   | Die Bindung kann nicht spät                                                                        |
| [**Shelllinkobject**](shelllinkobject-object.md)       | Shell. Namespace ("..."). Self. getlink oder Shell. Namespace ("..."). Elemente (). Getlink           |
| [**Shelluihelper**](shelluihelper.md)                  | Die Bindung kann nicht spät                                                                        |
| [**Shellwindows**](shellwindows.md)                    | schel. \_Shellfenster oder shellwindows. \_ "Netwenum"                                          |
| [**Webviewfoldercontents**](../lwef/webviewfoldercontents.md) | Die Bindung kann nicht spät                                                                        |



 

### <a name="html-object-element"></a>HTML-Objekt Element

Sie können auch das [**Object**](https://msdn.microsoft.com/library/ms535859(v=VS.85).aspx) -Element verwenden, um Shellobjekte auf einer HTML-Seite zu instanziieren. Legen Sie hierzu das **ID** -Attribut des **Object** -Elements auf den Variablennamen fest, den Sie in Ihren Skripts verwenden möchten, und identifizieren Sie das Objekt mit der registrierten Nummer (ClassID). Der folgende HTML-Code erstellt mit dem **Object** -Element eine Instanz des [**shellfolderitem**](shellfolderitem-object.md) -Objekts.


```
<OBJECT ID="oShFolderItem" 
    NAME="Shell Folder Item Object"
    CLASSID="clsid:2fe352ea-fd1f-11d2-b1f4-00c04f8eeb3e">
</OBJECT>
```



In der folgenden Tabelle werden die einzelnen Shellobjekte und die jeweilige ClassID aufgelistet.



|                                                         |                                      |
|---------------------------------------------------------|--------------------------------------|
| [**Didiskquotauser**](didiskquotauser-object.md)       | 7988b571-ec89-11CF-9c00-00aa00a14f56 |
| [**Diskquotacontrol**](diskquotacontrol-object.md)     | 7988b571-ec89-11CF-9c00-00aa00a14f56 |
| [**Ordner**](folder.md)                                | BBCBDE60-C3FF-11CE-8350-444553540000 |
| [**Folder2**](folder2-object.md)                       | f0d2d8ef-3890-11d2-bf8b-00c04fb93661 |
| [**Von folderItem**](folderitem.md)                        | 744129e0-CBE5-11CE-8350-444553540000 |
| [**Folderitems**](folderitems.md)                      | 744129e0-CBE5-11CE-8350-444553540000 |
| [**FolderItems2**](folderitems2-object.md)             | C94F0AD0-F363-11d2-A327-00C04F8EEC7F |
| [**Folderitemverb**](folderitemverb.md)                | 08ec3e00-50b0-11CF-960c-0080c7f4ee85 |
| [**Folderitemverbs**](folderitemverbs.md)              | 1f8352c0-50b0-11CF-960c-0080c7f4ee85 |
| [**IShellDispatch2**](ishelldispatch2-object.md)       | A4C6892C-3BA9-11d2-9DEA-00C04FB16162 |
| [**IShellLinkDual2**](ishelllinkdual2-object.md)       | 317ee249-b12e-11d2-B1E4-00c04f 8eeb3e |
| [**Shell**](shell.md)                                  | 13709620-C279-11CE-A49E-444553540000 |
| [**Shellfolderitem**](shellfolderitem-object.md)       | 2fe352ea-fid1fi-11d2-B1F 4-00c04fi8eeb3e |
| [**Shellfolderview**](shellfolderview.md)              | 62112aa1-ebe4-11CF-a5fb-0020afe7292d |
| [**Shellfolderviewoc**](shellfolderviewoc-object.md)   | 4a3df050-23bd-11d2-939f -00a0c91eedba |
| [**Shelllinkobject**](shelllinkobject-object.md)       | 11219420-1768-11d1-95be-00609797ea4f |
| [**Shelluihelper**](shelluihelper.md)                  | 64ab4bb7-111E-11d1-8f79-00c04fc2fbe1 |
| [**Shellwindows**](shellwindows.md)                    | 9ba05972-f6a8-11CF-A442-00a0c90a8f39 |
| [**Webviewfoldercontents**](../lwef/webviewfoldercontents.md) | 1820fed0-473e-11D0-a96c-00c04f d705a2 |



 

## <a name="shell-object"></a>Shellobjekt

Das [**Shellobjekt**](shell.md) stellt die Objekte in der Shell dar. Sie können die Methoden, die vom Shell-Objekt verfügbar gemacht werden, für Folgendes verwenden:

-   Öffnen, untersuchen und suchen Sie nach Ordnern.
-   Minimieren, wiederherstellen, kaskadieren oder Kacheln öffnen.
-   Starten Sie System Steuerungsanwendungen.
-   Anzeigen von System Dialogfeldern.

Benutzer sind vielleicht am häufigsten mit den Befehlen vertraut, auf die Sie über das **Startmenü** und das Kontextmenü der Taskleiste zugreifen. Das Kontextmenü der Taskleiste wird angezeigt, wenn Benutzer mit der rechten Maustaste auf die Taskleiste klicken. Die folgende HTML-Anwendung (HTA) erzeugt eine Startseite mit Schaltflächen, mit denen viele der Methoden des [**shellobjekts**](shell.md) implementiert werden. Einige dieser Methoden implementieren Features im **Startmenü** und im Kontextmenü der Taskleiste.


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

Als Anwendung wird eine HTA unter einem anderen Sicherheitsmodell als eine Webseite ausgeführt. Um mit einer Webseite zu interagieren, die die Funktionalität der Shellobjekte implementiert, müssen Benutzer die **ActiveX-Steuerelemente initialisieren und Skripts, die nicht als sichere Option gekennzeichnet** sind, für die Sicherheitszone aktivieren, in der Sie die Seite anzeigen.

## <a name="folder-objects"></a>Ordner Objekte

Das [**Folder**](folder.md) -Objekt stellt einen Shellordner dar. Sie können die Methoden, die vom Folder-Objekt verfügbar gemacht werden, für Folgendes verwenden:

-   Hier erhalten Sie Informationen zu einem Ordner.
-   Erstellen Sie Unterordner.
-   Kopieren Sie Datei Objekte, und verschieben Sie Sie in den Ordner.

Das [**folderItem**](folderitem.md) -Objekt stellt ein Element in einem Shellordner dar. Mit den Eigenschaften können Sie Informationen zum Element abrufen. Sie können die Methoden, die von diesem-Objekt verfügbar gemacht werden, zum Ausführen der Verben eines Elements oder zum Abrufen von Informationen über das [**folderitemverbs**](folderitemverbs.md) -Objekt eines Elements verwenden.

Das [**folderitems**](folderitems.md) -Objekt stellt eine Sammlung von Elementen in einem Shellordner dar. Die zugehörigen Methoden und Eigenschaften ermöglichen es Ihnen, Informationen über die Sammlung abzurufen.

Im folgenden Visual Basic Beispiel wird die Beziehung zwischen mehreren Ordner Objekten und deren Verwendung zusammen gezeigt. Wenn der Benutzer auf die Befehls Schaltfläche **cmdgetpath** klickt, zeigt das Programm ein Dialogfeld an, in dem der Benutzer einen Ordner aus **Arbeitsplatz** auswählen kann, wobei ssfdrives der [**shellspecialfolderconstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) -Enumerationswert für **Arbeitsplatz** ist. Wenn der Benutzer einen Ordner auswählt, wird der Pfad des Ordners im Textfeld mit dem Namen " **txtpath**" angezeigt.


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



In VBScript unterscheidet sich diese Funktion etwas, da die Enumerationswerte von [**shellspecialfolderkonstanten**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) nicht im Skript verfügbar sind. Das folgende Beispiel zeigt die VBScript-Entsprechung des vorherigen Beispiels.


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



Im folgenden JScript-Beispiel, bei dem es sich um eine direkte Übersetzung des vorangehenden VBScript-Beispiels handelt, beachten Sie, wie die leeren Klammern "()" verwendet werden, um die [**Elemente**](folder-items.md) und [**Element**](folderitems-item.md) Methoden aufzurufen.


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



 

 
