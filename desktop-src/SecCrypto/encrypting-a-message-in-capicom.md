---
description: Diese Unterroutine nimmt eine zu verschlüsselnde Zeichenfolge, eine Kenn Wort Zeichenfolge, die verwendet werden soll, um einen Verschlüsselungsschlüssel zu generieren, und den Namen einer Datei, in die die verschlüsselte Nachricht geschrieben wird.
ms.assetid: 9ad3199a-bca1-4990-80da-80744e349047
title: Verschlüsseln einer Nachricht in CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8039586736c09673644cacc90759e8d5f25b6e1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355315"
---
# <a name="encrypting-a-message-in-capicom"></a><span data-ttu-id="e2fcf-103">Verschlüsseln einer Nachricht in CAPICOM</span><span class="sxs-lookup"><span data-stu-id="e2fcf-103">Encrypting a Message in CAPICOM</span></span>

<span data-ttu-id="e2fcf-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e2fcf-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="e2fcf-105">Verwenden Sie stattdessen die .NET Framework, um Sicherheitsfunktionen zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="e2fcf-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="e2fcf-106">Weitere Informationen finden Sie unter [Alternativen zur Verwendung von CAPICOM](alternatives-to-using-capicom.md).\]</span><span class="sxs-lookup"><span data-stu-id="e2fcf-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="e2fcf-107">Diese Unterroutine nimmt eine zu verschlüsselnde Zeichenfolge, eine Kenn Wort Zeichenfolge, die verwendet werden soll, um einen Verschlüsselungsschlüssel zu generieren, und den Namen einer Datei, in die die verschlüsselte Nachricht geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="e2fcf-107">This subroutine takes a string to be encrypted, a password string to be used to generate an encryption key, and the name of a file where the encrypted message will be written.</span></span> <span data-ttu-id="e2fcf-108">Alle Parameter werden durch-Werte an die Unterroutine übergeben.</span><span class="sxs-lookup"><span data-stu-id="e2fcf-108">All parameters are passed into the subroutine by values.</span></span> <span data-ttu-id="e2fcf-109">Zum Entschlüsseln der Nachricht muss dieselbe Kenn Wort Zeichenfolge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e2fcf-109">To decrypt the message, the same password string must be used.</span></span> <span data-ttu-id="e2fcf-110">Wenn das Kennwort verloren geht, kann der Text nicht entschlüsselt werden.</span><span class="sxs-lookup"><span data-stu-id="e2fcf-110">If the password is lost, the text cannot be decrypted.</span></span> <span data-ttu-id="e2fcf-111">Der Datenschutz der Nachricht geht verloren, wenn ein unbeabsichtigter Empfänger Zugriff auf das Kennwort erlangt.</span><span class="sxs-lookup"><span data-stu-id="e2fcf-111">The privacy of the message is lost if an unintended recipient gains access to the password.</span></span>

> [!Note]  
> <span data-ttu-id="e2fcf-112">CAPICOM unterstützt den PKCS \# 7-Inhaltstyp "verschlüsselteddata" nicht, sondern verwendet eine nicht dem Standard entsprechende ASN-Struktur für "verschlüsselteddata".</span><span class="sxs-lookup"><span data-stu-id="e2fcf-112">CAPICOM does not support the PKCS \#7 EncryptedData content type but uses a nonstandard ASN structure for EncryptedData.</span></span> <span data-ttu-id="e2fcf-113">Folglich kann nur CAPICOM ein CAPICOM-Objekt "verschlüsselteddata" entschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="e2fcf-113">As a result, only CAPICOM can decrypt a CAPICOM EncryptedData object.</span></span>

 

<span data-ttu-id="e2fcf-114">Bei einem beliebigen CAPICOM-Fehler wird ein negativer Dezimalwert der **Err. Number** -Eigenschaft zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e2fcf-114">On any CAPICOM error, a negative decimal value of the **Err.Number** property is returned.</span></span> <span data-ttu-id="e2fcf-115">Weitere Informationen finden Sie unter [**CAPICOM- \_ Fehler \_ Code**](capicom-error-code.md).</span><span class="sxs-lookup"><span data-stu-id="e2fcf-115">For more information, see [**CAPICOM\_ERROR\_CODE**](capicom-error-code.md).</span></span> <span data-ttu-id="e2fcf-116">Informationen zu positiven Dezimalwerten von **Err. Number** finden Sie unter Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="e2fcf-116">For information about positive decimal values of **Err.Number**, see Winerror.h.</span></span>


```VB
Sub EncryptMessage(ByVal TobeEncrypted As String, ByVal hidden _
    As String, ByVal filename As String)

    On Error GoTo ErrorHandler

    ' Declare and initialize an EncryptedData object.
    ' Algorithm.Name and KeyLength do not need to be set.

    Dim message As New EncryptedData
    message.Content = Tobeencrypted
    message.SetSecret(hidden)
    ' Optionally, the encryption algorithm and key length can be set.
    ' If these properties are not set, the default algorithm and key 
    ' length are used.
    ' Information about the algorithm and key length is saved with 
    ' the encrypted string and the individual decrypting the message
    ' does not need to set these properties.

    message.Algorithm.Name = CAPICOM_ENCRYPTION_ALGORITHM_DES

    ' Declare the string that will hold the encrypted message.

    Dim encryptedmessage As String

    ' Encrypt the message storing the result in the encryptedmessage
    ' string.
    encryptedmessage = message.Encrypt

    ' Optionally, check the length of the encrypted string to 
    ' make sure that the encrypt method worked. 

    If Len(encryptedmessage) < 1 Then
        MsgBox("no message encrypted. ")
    Else
        MsgBox(" Message is " & Len(encryptedmessage) & " characters")

        ' Open an output file and write the encrypted message to the
        ' file. The file is not opened if there is no message
        ' to write.
    Open filename For Output As #1
    Write #1, encryptedmessage
    Close #1
        MsgBox("Encrypted message written to file ")
    End If

    ' Release the EncryptedData object.
    message = Nothing

    Exit Sub

ErrorHandler:
    If Err.Number > 0 Then
        MsgBox("Visual Basic error found:" & Err.Description)
    Else
        MsgBox("CAPICOM error found : " & Err.Number)
    End If
End Sub
```



 

 



