---
description: Zertifikate können aus einem Active Directory-Speicher abgerufen werden, in dem die Zertifikate der Benutzer einer Domäne gespeichert werden.
ms.assetid: 5c4d1629-88f3-41f4-afb3-7791cd590e6c
title: Öffnen des Active Directory-Store und Abrufen von Zertifikaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd2dc5810e97669e40b27bc374bee09f16c0a7c9a3b2bd4a1fa2951e1249a737
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117979121"
---
# <a name="opening-the-active-directory-store-and-retrieving-certificates"></a>Öffnen des Active Directory-Store und Abrufen von Zertifikaten

\[CAPICOM ist eine nur 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die .NET Framework, um Sicherheitsfeatures zu implementieren. Weitere Informationen finden Sie unter [Alternativen zur Verwendung von CAPICOM.](alternatives-to-using-capicom.md)\]

[*Zertifikate*](../secgloss/c-gly.md) können aus einem Active Directory-Speicher abgerufen werden, in dem die Zertifikate der Benutzer einer Domäne gespeichert werden. Ein Active Directory-Speicher kann nur im schreibgeschützten Modus geöffnet werden, und Anwendungen können keine Zertifikate zu einem Active Directory-Speicher mit CAPICOM hinzufügen oder aus diesem entfernen.

Bei einem CAPICOM-Fehler wird ein negativer Dezimalwert von **Err.Number** zurückgegeben. Weitere Informationen finden Sie unter [**CAPICOM \_ ERROR \_ CODE**](capicom-error-code.md). Informationen zu positiven Dezimalwerten von **Err.Number** finden Sie unter Winerror.h.

Das folgende Beispiel zeigt das Öffnen eines Active Directory-Speichers und das Abrufen von Zertifikaten aus diesem Speicher.


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



 

 
