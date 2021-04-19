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
# <a name="opening-the-active-directory-store-and-retrieving-certificates"></a><span data-ttu-id="7edd2-103">Öffnen des Active Directory Stores und Abrufen von Zertifikaten</span><span class="sxs-lookup"><span data-stu-id="7edd2-103">Opening the Active Directory Store and Retrieving Certificates</span></span>

<span data-ttu-id="7edd2-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7edd2-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="7edd2-105">Verwenden Sie stattdessen die .NET Framework, um Sicherheitsfunktionen zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="7edd2-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="7edd2-106">Weitere Informationen finden Sie unter [Alternativen zur Verwendung von CAPICOM](alternatives-to-using-capicom.md).\]</span><span class="sxs-lookup"><span data-stu-id="7edd2-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="7edd2-107">[*Zertifikate*](../secgloss/c-gly.md) können aus einem Active Directory Speicher abgerufen werden, in dem die Zertifikate der Benutzer einer Domäne gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="7edd2-107">[*Certificates*](../secgloss/c-gly.md) can be retrieved from an Active Directory store where the certificates of users of a domain are stored.</span></span> <span data-ttu-id="7edd2-108">Ein Active Directory Speicher kann nur im schreibgeschützten Modus geöffnet werden, und Anwendungen können mithilfe von CAPICOM keine Zertifikate zu einem Active Directory Speicher hinzufügen oder daraus entfernen.</span><span class="sxs-lookup"><span data-stu-id="7edd2-108">An Active Directory store can only be opened in the read-only mode and applications cannot added certificates to or remove certificates from an Active Directory store using CAPICOM.</span></span>

<span data-ttu-id="7edd2-109">Bei einem beliebigen CAPICOM-Fehler wird der negative Dezimalwert **Err. Number** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7edd2-109">On any CAPICOM error, a negative decimal value of **Err.Number** is returned.</span></span> <span data-ttu-id="7edd2-110">Weitere Informationen finden Sie unter [**CAPICOM- \_ Fehler \_ Code**](capicom-error-code.md).</span><span class="sxs-lookup"><span data-stu-id="7edd2-110">For more information, see [**CAPICOM\_ERROR\_CODE**](capicom-error-code.md).</span></span> <span data-ttu-id="7edd2-111">Informationen zu positiven Dezimalwerten von **Err. Number** finden Sie unter Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="7edd2-111">For information about positive decimal values of **Err.Number**, see Winerror.h.</span></span>

<span data-ttu-id="7edd2-112">Im folgenden Beispiel wird gezeigt, wie ein Active Directory Store geöffnet und Zertifikate aus diesem Speicher abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="7edd2-112">The following example shows opening an Active Directory store and retrieving certificates from that store.</span></span>


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



 

 
