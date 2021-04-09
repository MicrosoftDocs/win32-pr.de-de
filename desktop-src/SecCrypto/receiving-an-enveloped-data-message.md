---
description: Zum Entschlüsseln einer eingeschlossenen Nachricht entspricht der Empfänger einem Zertifikat aus dem eigenen Speicher, das über einen verfügbaren privaten Schlüssel mit einem Zertifikat in der eingeschlossenen Nachricht verfügt.
ms.assetid: 536f9977-102c-4df9-9d07-97b4b434b845
title: Empfangen einer eingeschlossenen Daten Nachricht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d32276193e8fd03904aed1ad626cd3ed241c654
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868203"
---
# <a name="receiving-an-enveloped-data-message"></a><span data-ttu-id="5fc0f-103">Empfangen einer eingeschlossenen Daten Nachricht</span><span class="sxs-lookup"><span data-stu-id="5fc0f-103">Receiving an Enveloped Data Message</span></span>

<span data-ttu-id="5fc0f-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5fc0f-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="5fc0f-105">Verwenden Sie stattdessen die .NET Framework, um Sicherheitsfunktionen zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="5fc0f-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="5fc0f-106">Weitere Informationen finden Sie unter [Alternativen zur Verwendung von CAPICOM](alternatives-to-using-capicom.md).\]</span><span class="sxs-lookup"><span data-stu-id="5fc0f-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="5fc0f-107">Zum Entschlüsseln einer eingeschlossenen Nachricht entspricht der Empfänger einem [*Zertifikat*](../secgloss/c-gly.md) aus dem eigenen Speicher, das über einen verfügbaren privaten Schlüssel mit einem Zertifikat in der eingeschlossenen Nachricht verfügt.</span><span class="sxs-lookup"><span data-stu-id="5fc0f-107">To decrypt an enveloped message, the recipient matches a [*certificate*](../secgloss/c-gly.md) from the My store that has an available private key with a certificate in the enveloped message.</span></span> <span data-ttu-id="5fc0f-108">Wenn eine Entsprechung gefunden wird, wird der verschlüsselte Schlüssel, der diesem Zertifikat zugeordnet ist, entschlüsselt, und der entschlüsselte Schlüssel wird zum Entschlüsseln der eingeschlossenen Nachricht verwendet.</span><span class="sxs-lookup"><span data-stu-id="5fc0f-108">If a match is found, the encrypted key associated with that certificate is decrypted and that decrypted key is used to decrypt the enveloped message.</span></span> <span data-ttu-id="5fc0f-109">Ein Nachrichtenempfänger, der nicht über ein übereinstimmendes Zertifikat mit einem verfügbaren privaten Schlüssel verfügt, kann die Nachricht nicht entschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="5fc0f-109">A message recipient that does not have a matching certificate with an available private key cannot decrypt the message.</span></span>

<span data-ttu-id="5fc0f-110">Im folgenden Beispiel wird ein Dateiname an die Unterroutine übergeben, die Datei wird geöffnet, und eine eingehüllte Nachricht wird gelesen.</span><span class="sxs-lookup"><span data-stu-id="5fc0f-110">In the example that follows, a file name is passed into the subroutine, that file is opened and an enveloped message is read in.</span></span> <span data-ttu-id="5fc0f-111">Die eingeschlossene Nachricht wird dann entschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="5fc0f-111">The enveloped message is then decrypted.</span></span> <span data-ttu-id="5fc0f-112">Die Schritte zum Abgleichen eines Benutzer Zertifikats mit einem Zertifikat in der eingeschlossenen Nachricht, das Entschlüsseln des Verschlüsselungsschlüssels und schließlich das Entschlüsseln der Nachricht, werden alle im Hintergrund durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="5fc0f-112">The steps of matching a user certificate with a certificate in the enveloped message, of decrypting the encryption key, and finally of decrypting the message are all done behind the scenes.</span></span> <span data-ttu-id="5fc0f-113">Ein Fehler wird ausgelöst, wenn eine Zertifikat Übereinstimmung nicht gefunden wurde oder wenn das Entschlüsseln fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="5fc0f-113">An error is raised if a certificate match is not found or if the decryption fails.</span></span>

<span data-ttu-id="5fc0f-114">Bei einem beliebigen CAPICOM-Fehler wird der negative Dezimalwert **Err. Number** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5fc0f-114">On any CAPICOM error, a negative decimal value of **Err.Number** is returned.</span></span> <span data-ttu-id="5fc0f-115">Weitere Informationen finden Sie unter [**CAPICOM- \_ Fehler \_ Code**](capicom-error-code.md).</span><span class="sxs-lookup"><span data-stu-id="5fc0f-115">For more information, see [**CAPICOM\_ERROR\_CODE**](capicom-error-code.md).</span></span> <span data-ttu-id="5fc0f-116">Informationen zu positiven Dezimalwerten von **Err. Number** finden Sie unter Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="5fc0f-116">For information about positive decimal values of **Err.Number**, see Winerror.h.</span></span>


```VB
Sub ReceiveMessage(ByVal InFile As String)
On Error GoTo ErrorHandler

'Declare an EnvelopedData object

Dim Envmessage As New EnvelopedData

'Declare a string variable to hold the encrypted message.

Dim Encrypted As String

' Open an input file and read in the encrypted message
Open InFile For Input As #1
Input #1, Encrypted
Close #1

' If the length of the input string is greater than 0, 
' an encrypted message string is available. Decrypt the message.
' Note: to decrypt the message, a certificate with access to
' a user's private key must be available, and that certificate must
' match one of the certificates in the Recipients collection of 
' certificates.
If Len(Encrypted) > 0 Then
    ' Receive and decrypt the message
    Envmessage.Decrypt encrypted
    
    ' Display the decrypted message.
    MsgBox Envmessage.Content
Else
    MsgBox "No enveloped message was read in."
End If
' Release the EncryptedData object.
Set Envmessage = Nothing
Exit Sub

ErrorHandler:
If Err.Number > 0 Then
    MsgBox "Visual Basic error found:" & Err.Description
Else
    MsgBox "CAPICOM error found : " & Err.Number
End If
End Sub
```



 

 
