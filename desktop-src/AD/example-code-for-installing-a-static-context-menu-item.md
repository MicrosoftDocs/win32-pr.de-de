---
title: Beispiel Code für die Installation eines statischen Kontextmenü Elements
description: Im folgenden Codebeispiel werden zwei Skripts verwendet.
ms.assetid: 22d6a220-7712-4b07-a6d9-67dd748358a6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33a8b6eb65706ad3adc9fd4c10b4c60f96a72848
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104470876"
---
# <a name="example-code-for-installing-a-static-context-menu-item"></a><span data-ttu-id="e4b75-103">Beispiel Code für die Installation eines statischen Kontextmenü Elements</span><span class="sxs-lookup"><span data-stu-id="e4b75-103">Example Code for Installing a Static Context Menu Item</span></span>

<span data-ttu-id="e4b75-104">Im folgenden Codebeispiel werden zwei Skripts verwendet.</span><span class="sxs-lookup"><span data-stu-id="e4b75-104">The following code example uses two scripts.</span></span> <span data-ttu-id="e4b75-105">Das erste Skript (Frommenu.vbs) ist der Befehl, der ausgeführt wird, wenn das Menü Element ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="e4b75-105">The first script (Frommenu.vbs) is the command that is run when the menu item is selected.</span></span> <span data-ttu-id="e4b75-106">Das zweite Skript (Addmenu.vbs) installiert das Kontextmenü Element des Anzeige Spezifizierers, um das Skript Frommenu.vbs auszuführen.</span><span class="sxs-lookup"><span data-stu-id="e4b75-106">The second script (Addmenu.vbs) installs the display specifier context menu item to execute the script Frommenu.vbs.</span></span> <span data-ttu-id="e4b75-107">In diesem Beispiel wird das Gebiets Schema 409 (US-Englisch) angenommen und das Kontextmenü des Benutzer Objekts in Active Directory administrativen Snap-Ins erweitert.</span><span class="sxs-lookup"><span data-stu-id="e4b75-107">This example assumes locale 409 (US English) and extends the user object's context menu in Active Directory administrative snap-ins.</span></span>

<span data-ttu-id="e4b75-108">So führen Sie den Beispielcode aus</span><span class="sxs-lookup"><span data-stu-id="e4b75-108">To run the example code</span></span>

1.  <span data-ttu-id="e4b75-109">Kopieren Sie den Code für Frommenu.vbs unten, öffnen Sie den Editor, fügen Sie den Code in den Editor ein, speichern Sie die Datei als C: \\frommenu.vbs, und schließen Sie Notepad.</span><span class="sxs-lookup"><span data-stu-id="e4b75-109">Copy the code for Frommenu.vbs below, open Notepad, paste the code into Notepad, save the file as C:\\frommenu.vbs, and close Notepad.</span></span>
2.  <span data-ttu-id="e4b75-110">Kopieren Sie den Code für Addmenu.vbs unten, öffnen Sie den Editor, fügen Sie den Code in den Editor ein, speichern Sie die Datei als C: \\addmenu.vbs, und schließen Sie Notepad.</span><span class="sxs-lookup"><span data-stu-id="e4b75-110">Copy the code for Addmenu.vbs below, open Notepad, paste the code into Notepad, save the file as C:\\addmenu.vbs, and close Notepad.</span></span>
3.  <span data-ttu-id="e4b75-111">Führen Sie Addmenu.vbs aus.</span><span class="sxs-lookup"><span data-stu-id="e4b75-111">Run Addmenu.vbs.</span></span>
4.  <span data-ttu-id="e4b75-112">Starten Sie das Snap-in Active Directory Benutzer und Computer.</span><span class="sxs-lookup"><span data-stu-id="e4b75-112">Start the Active Directory Users and Computers snap-in.</span></span>

<span data-ttu-id="e4b75-113">FROMMENU.VBS</span><span class="sxs-lookup"><span data-stu-id="e4b75-113">FROMMENU.VBS</span></span>


```VB
'Frommenu.vbs is the script run when the menu item is chosen.
 
''''''''''''''''''''
' Parse the arguments
' First arg is ADsPath of the selected object. Second is Class.
''''''''''''''''''''
On Error Resume Next
 
Set oArgs = WScript.Arguments
sText = "This script was run from a display specifier context menu." & vbCrLf & "Selected Item:"
If oArgs.Count > 1 Then
    sText = sText & vbCrLf & "  ADsPath: " & oArgs.item(0)
    sText = sText & vbCrLf & "  Class: " & oArgs.item(1)
Else
    sText = sText & vbCrLf & "Arg Count: " & oArgs.Count
End If
show_items sText
Err.Number = 0
sBind = oArgs.item(0)
Set dsobj= GetObject(sBind)
If (Err.Number <> 0) Then
    BailOnFailure Err.Number, "on GetObject method"
End If
objname = dsobj.Get("name")
If (Err.Number <> 0) Then
    BailOnFailure Err.Number, "on Get method"
End If
sText = "Use ADsPath from first argument to bind and get RDN (name) property."
sText = sText & vbCrLf & "Name: " & objname
show_items sText
 
''''''''''''''''''''
' Display subroutines
''''''''''''''''''''
Sub show_items(strText)
    MsgBox strText, vbInformation, "Script from Context Menu"
End Sub
 
Sub BailOnFailure(ErrNum, ErrText)    strText = "Error 0x" & Hex(ErrNum) & " " & ErrText
    MsgBox strText, vbInformation, "ADSI Error"
    WScript.Quit
End Sub
```



<span data-ttu-id="e4b75-114">ADDMENU.VBS</span><span class="sxs-lookup"><span data-stu-id="e4b75-114">ADDMENU.VBS</span></span>


```VB
' Addmenu.vbs adds the menu item to run Frommenu.vbs 
' from user object's context menu in the admin snap-ins.
On Error Resume Next
Set root= GetObject("LDAP://rootDSE")
If (Err.Number <> 0) Then
    BailOnFailure Err.Number, "on GetObject method"
End If
sConfig = root.Get("configurationNamingContext")
'hardcoded for user class.
sClass = "user"
'hardcoded for US English
sLocale = "409"
sPath = "LDAP://cn=" & sClass & "-Display,cn=" & sLocale & ",cn=DisplaySpecifiers," & sConfig
show_items "Display Specifier: " & sPath
Set obj= GetObject(sPath)
If (Err.Number <> 0) Then
    BailOnFailure Err.Number, "on GetObject method"
End If
'TODO--check if this is already there.
'Add the value for the context menu
sValue = "5,Run My Test Script,c:\frommenu.vbs"
vValue = Array(sValue)
obj.PutEx 3, "adminContextMenu", vValue
If (Err.Number <> 0) Then
    BailOnFailure Err.Number, "on IADs::PutEx method"
End If
' Commit the change.
obj.SetInfo
If (Err.Number <> 0) Then
    BailOnFailure Err.Number, "on IADs::SetInfo method"
End If
 
show_items "Success! Added value to adminContextMenu property of user-Display: " & sValue
 
''''''''''''''''''''
' Display subroutines
''''''''''''''''''''
Sub show_items(strText)
    MsgBox strText, vbInformation, "Add admin context menu"
End Sub
 
Sub BailOnFailure(ErrNum, ErrText)    strText = "Error 0x" & Hex(ErrNum) & " " & ErrText
    MsgBox strText, vbInformation, "ADSI Error"
    WScript.Quit
End Sub
```



 

 




