---
title: Beispielcode zum Hinzufügen eines Mitglieds zu einer Gruppe
description: Dieses Thema enthält Codebeispiele, die einer Gruppe ein Mitglied hinzufügen.
ms.assetid: 306fcadb-a492-41e5-bfb3-8beaaec24fb5
ms.tgt_platform: multiple
keywords:
- 'Active Directory-Beispiele: Active Directory, Hinzufügen eines Mitglieds zu einer Gruppe'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5cccccca0fa701b4f5bc1ce9b350ac1073c6da7614c7292724138b2d433ef2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191293"
---
# <a name="example-code-for-adding-a-member-to-a-group"></a>Beispielcode zum Hinzufügen eines Mitglieds zu einer Gruppe

Dieses Thema enthält Codebeispiele, die einer Gruppe ein Mitglied hinzufügen. In den Beispielen Visual Basic Scripting Edition (VBScript) und C++ wird ein Member hinzugefügt, indem das [**IADs-Objekt,**](/windows/desktop/api/iads/nn-iads-iads) das das Element darstellt, dem [**IADsGroup-Objekt**](/windows/desktop/api/iads/nn-iads-iadsgroup) hinzugefügt wird, das die Gruppe darstellt. Die Visual Basic .NET- und C#-Beispiele ändern die Membereigenschaft des [DirectoryEntry-Objekts,](/dotnet/api/system.directoryservices.directoryentry) das die Gruppe darstellt.


In den folgenden C#-Codebeispielen wird einer Gruppe ein vorhandenes Mitglied hinzugefügt. Die Funktion verwendet den ADsPath des Gruppencontainers und den Distinguished Name des Members, das der Gruppe hinzugefügt werden soll. ADsPath wird verwendet, um ein [DirectoryEntry-Objekt](/dotnet/api/system.directoryservices.directoryentry) zu erstellen, das die Gruppe darstellt. Die [PropertyValueCollection.Add-Methode](/dotnet/api/system.directoryservices.propertyvaluecollection.add#System_DirectoryServices_PropertyValueCollection_Add_System_Object_) fügt der Gruppe das Element hinzu, dessen Distinguished Name an die Funktion übergeben wurde. Die Funktion verwendet dann die [DirectoryEntry.CommitChanges-Methode,](/dotnet/api/system.directoryservices.directoryentry.commitchanges#System_DirectoryServices_DirectoryEntry_CommitChanges) um die neuen Memberinformationen in die Datenbank zu schreiben.

Rufen Sie die Funktion mit den folgenden Parametern auf:

-   *bindString:* ein gültiger ADsPath für einen Gruppencontainer, z. B. "LDAP://fabrikam.com/CN=TestGroup,OU=TestOU,DC=fabrikam,DC=com".
-   *newMember:* Der Distinguished Name des Members, das der Gruppe hinzugefügt werden soll, z. B. "CN=JeffSmith,OU=TestOU,DC=fabrikam,DC=com".


```CSharp
private void AddMemberToGroup(

                                string bindString,

                                string newMember

                                )

{

    try
    {

        DirectoryEntry ent = new DirectoryEntry( bindString );

        ent.Properties["member"].Add(newMember);

        ent.CommitChanges();

    }

    catch (Exception e)
    {

        Console.WriteLine( "An error occurred.");

        Console.WriteLine( "{0}", e.Message);

        return;

    }

}
```




Die folgenden Visual Basic .NET-Codebeispiele fügen einer Gruppe ein vorhandenes Mitglied hinzu. Die Funktion verwendet den ADsPath des Gruppencontainers und den Distinguished Name des Members, das der Gruppe hinzugefügt werden soll. ADsPath wird verwendet, um ein [DirectoryEntry-Objekt](/dotnet/api/system.directoryservices.directoryentry) zu erstellen, das die Gruppe darstellt. Die [PropertyValueCollection.Add-Methode](/dotnet/api/system.directoryservices.propertyvaluecollection.add#System_DirectoryServices_PropertyValueCollection_Add_System_Object_) fügt der Gruppe das Element hinzu, dessen Distinguished Name an die Funktion übergeben wurde. Die Funktion verwendet dann die [DirectoryEntry.CommitChanges-Methode,](/dotnet/api/system.directoryservices.directoryentry.commitchanges#System_DirectoryServices_DirectoryEntry_CommitChanges) um die neuen Memberinformationen in die Datenbank zu schreiben.

Rufen Sie die Funktion mit den folgenden Parametern auf:

-   *bindString:* ein gültiger ADsPath für einen Gruppencontainer, z. B. "LDAP://fabrikam.com/CN=TestGroup,OU=TestOU,DC=fabrikam,DC=com".
-   *newMember:* Der Distinguished Name des Members, das der Gruppe hinzugefügt werden soll, z. B. "CN=JeffSmith,OU=TestOU,DC=fabrikam,DC=com".


```VB
Private Sub AddMemberToGroup(ByVal bindString As String, 
                                      ByVal newMember As String)

    Try

        Dim ent As New DirectoryEntry(bindString)

        ent.Properties("member").Add(newMember)

        ent.CommitChanges()

    Catch e As Exception

        Console.WriteLine("An error occurred.")

        Console.WriteLine("{0}", e.Message)

        Return

    End Try

End Sub
```




Im folgenden VBScript-Beispiel wird einer Gruppe ein vorhandenes Element hinzugefügt. Das Skript fügt den Benutzer Jeff Smith der Gruppe TestGroup hinzu.


```VB
Option Explicit

On Error Resume Next

Dim scriptResult        ' Script success or failure

Dim groupPath           ' ADsPath to the group container

Dim group               ' Group object

Dim memberPath          ' ADsPath to the member

Dim member              ' Member object

Dim groupMemberList     ' Used to display group members

Dim errorText           ' Error handing text

scriptResult = False

groupPath = "LDAP://fabrikam.com/CN=TestGroup,OU=TestOU,DC=fabrikam,DC=com"

memberPath = "LDAP://CN=JeffSmith,OU=TestOU,DC=fabrikam,DC=com"

WScript.Echo("Retrieving group object")

Set group = GetObject(groupPath)

If Err.number <> vbEmpty then

    Call ErrorHandler("Could not create group object.")

End If

Call ShowMembers(groupPath)     'Optional function call

WScript.Echo("Retrieving new member object")

Set member = GetObject(memberPath)

If Err.number <> vbEmpty then

    Call ErrorHandler("Could not get new member object.")

End If

WScript.Echo("Adding member to group.")

group.Add(member.ADsPath)

If Err.number <> vbEmpty then

    Call ErrorHandler("Could not add member to group.")

End If

Call ShowMembers(groupPath)     ' Optional function call

scriptResult = True

Call FinalResult(scriptResult)

'****************************************************************
' This function displays the members of a group. The function
' takes the ADsPath of the group.
'****************************************************************

Sub ShowMembers(groupPath)

    Dim groupMember

    Dim groupMemberList

    Dim groupObject

    Set groupObject = GetObject(groupPath)

    Set groupMemberList = groupObject.Members

    Select Case groupMemberList.Count

        Case 1 

            WScript.Echo vbcrlf & "The group has one member."

        Case 0

            WScript.Echo vbcrlf & "The group has no members."

        Case Else

            WScript.Echo vbcrlf & "The group has " & groupMemberList.Count & " members."

    End Select

    If groupMemberList.Count > 0 then

        WScript.Echo vbcrlf & "Here is a member list."

        For Each groupMember in groupMemberList

            WScript.Echo groupMember.Name

        Next

        WScript.Echo vbcrlf

    End If

    Set groupObject = Nothing

    Set groupMemberList = Nothing

End Sub

'****************************************************************
' This function shows if the script succeeded or failed. The 
' function processed the scriptResult variable.
'****************************************************************

Sub FinalResult(scriptResult)

    WScript.Echo vbcrlf

    If scriptResult = False then

        WScript.Echo "Script failed."

    Else

        WScript.Echo("Script successfully completed.")

    End If

    WScript.Quit

End Sub

'****************************************************************
' This function handles errors that occur in the script.
'****************************************************************

Sub ErrorHandler( errorText )

    WScript.Echo(vbcrlf & errorText)

    WScript.Echo("Error number: " & Err.number)

    WScript.Echo("Error Description: " & Err.Description)

    Err.Clear 

    Call FinalResult(scriptResult)

End Sub

```




Im folgenden C++-Codebeispiel wird einer Gruppe ein vorhandenes Element hinzugefügt.


```C++
/////////////////////////////////////////////////////////////
/*  AddMemberToGroup() - Adds the passed directory object as a member 
                         of passed group
 
    Parameters
 
        IADsGroup * pGroup   - Group to hold the new IDirectoryObject.
        IADs* pIADsNewMember - Object which will become a member 
                               of the group. Object can be a user, 
                               contact, or group.
*/
HRESULT AddMemberToGroup(IADsGroup * pGroup, IADs* pIADsNewMember)
{
    HRESULT hr = E_INVALIDARG;
    if ((!pGroup)||(!pIADsNewMember))
        return hr;
 
    // Use the IADs::get_ADsPath() member to get the ADsPath.
    // When the ADsPath string is returned, to add the new
    // member to the group, call the IADsGroup::Add() member,
    // passing in the ADsPath string.
    // Query the new member for its AdsPath.
    // This is a fully qualified LDAP path to the object to add.
    BSTR bsNewMemberPath;
    hr = pIADsNewMember->get_ADsPath(&bsNewMemberPath); 
    if (SUCCEEDED(hr))
    {
 
        // Use the IADsGroup interface to add the new member.
        // Pass the LDAP path to the 
        // new member to the IADsGroup::Add() member
        hr = pGroup->Add(bsNewMemberPath);
 
        // Free the string returned from IADs::get_ADsPath()
        SysFreeString(bsNewMemberPath);
    }
    return hr;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Hinzufügen von Mitgliedern zu Gruppen in einer Domäne](adding-members-to-groups-in-a-domain.md)
</dt> <dt>

[DirectoryEntry](/dotnet/api/system.directoryservices.directoryentry)
</dt> <dt>

[DirectoryEntry.CommitChanges](/dotnet/api/system.directoryservices.directoryentry.commitchanges#System_DirectoryServices_DirectoryEntry_CommitChanges)
</dt> <dt>

[**Iads**](/windows/desktop/api/iads/nn-iads-iads)
</dt> <dt>

[**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup)
</dt> <dt>

[PropertyValueCollection.Add](/dotnet/api/system.directoryservices.propertyvaluecollection.add#System_DirectoryServices_PropertyValueCollection_Add_System_Object_)
</dt> </dl>

 

 