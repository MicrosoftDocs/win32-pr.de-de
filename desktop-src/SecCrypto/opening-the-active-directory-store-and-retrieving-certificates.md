---
description: Zertifikate können aus einem Active Directory Speicher abgerufen werden, in dem die Zertifikate der Benutzer einer Domäne gespeichert werden.
ms.assetid: 5c4d1629-88f3-41f4-afb3-7791cd590e6c
title: Öffnen des Active Directory Stores und Abrufen von Zertifikaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd60c7414aaec8b069817b47fbd2493bb11d98c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373189"
---
# <a name="opening-the-active-directory-store-and-retrieving-certificates"></a>Öffnen des Active Directory Stores und Abrufen von Zertifikaten

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die .NET Framework, um Sicherheitsfunktionen zu implementieren. Weitere Informationen finden Sie unter [Alternativen zur Verwendung von CAPICOM](alternatives-to-using-capicom.md).\]

[*Zertifikate*](../secgloss/c-gly.md) können aus einem Active Directory Speicher abgerufen werden, in dem die Zertifikate der Benutzer einer Domäne gespeichert werden. Ein Active Directory Speicher kann nur im schreibgeschützten Modus geöffnet werden, und Anwendungen können mithilfe von CAPICOM keine Zertifikate zu einem Active Directory Speicher hinzufügen oder daraus entfernen.

Bei einem beliebigen CAPICOM-Fehler wird der negative Dezimalwert **Err. Number** zurückgegeben. Weitere Informationen finden Sie unter [**CAPICOM- \_ Fehler \_ Code**](capicom-error-code.md). Informationen zu positiven Dezimalwerten von **Err. Number** finden Sie unter Winerror. h.

Im folgenden Beispiel wird gezeigt, wie ein Active Directory Store geöffnet und Zertifikate aus diesem Speicher abgerufen werden.


```VB
Sub OpenADStore()
        On Error GoTo ErrorHandler
        Dim mystore As Store
        Set mystore = New Store
        
        ' Put a string that represents the name of a certificate 
        ' subject in SubjectNameCn. In the following example, 
        ' the * wildcard character is used in the string so that
        ' the Active Directory store will be searched for all 
        ' certificates with a subject name beginning with 'S.'
       
        Dim SubjectNameCn As String
        ' The following uses 'cn=' and the * wildcard character.
        ' Using this string, all certificates in the Active Directory
        ' store with a subject name beginning with an 'S' would
        ' be returned.

        SubjectNameCn = "CN=S*"
        
        ' Active Directory stores can only be opened with read-only
        ' access.
        
         mystore.Open CAPICOM_ACTIVE_DIRECTORY_USER_STORE, _
              SubjectNameCn, CAPICOM_STORE_OPEN_READ_ONLY
        
        If mystore.Certificates.Count < 1 Then
               MsgBox "A certificate for " & SubjectNameCn & _
                      " was not found "
        Else
               MsgBox "The certificate has been retrieved."
        End If
        
        Set mystore = Nothing
        Exit Sub

ErrorHandler:
         
         If Err.Number > 0 Then
               MsgBox "Visual Basic error found:" & Err.Description
         Else
               MsgBox "CAPICOM error found : " & Err.Number
         End If
End Sub
```



 

 
