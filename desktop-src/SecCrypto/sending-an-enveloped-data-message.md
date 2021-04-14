---
description: Im folgenden Beispiel wird eine Klartext-Nachricht aus einer Datei gelesen, und ein Zertifikat Speicher, der die Zertifikate der gewünschten Nachrichtenempfänger enthält, wird geöffnet.
ms.assetid: 7ae672d3-e11d-453c-b9c0-354d21830ae4
title: Senden einer eingeschlossenen Daten Nachricht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f59c04418a2f1d0186ddc0d88c30e7cc790c715b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393633"
---
# <a name="sending-an-enveloped-data-message"></a><span data-ttu-id="12c0b-103">Senden einer eingeschlossenen Daten Nachricht</span><span class="sxs-lookup"><span data-stu-id="12c0b-103">Sending an Enveloped Data Message</span></span>

<span data-ttu-id="12c0b-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="12c0b-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="12c0b-105">Verwenden Sie stattdessen die .NET Framework, um Sicherheitsfunktionen zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="12c0b-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="12c0b-106">Weitere Informationen finden Sie unter [Alternativen zur Verwendung von CAPICOM](alternatives-to-using-capicom.md).\]</span><span class="sxs-lookup"><span data-stu-id="12c0b-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="12c0b-107">Im folgenden Beispiel wird eine Klartext-Nachricht aus einer Datei gelesen, und ein Zertifikat Speicher, der die Zertifikate der gewünschten Nachrichtenempfänger enthält, wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="12c0b-107">In the following example, a plaintext message is read in from a file, and a certificate store that contains the certificates of the intended message recipients is opened.</span></span> <span data-ttu-id="12c0b-108">Alle Zertifikate im Speicher werden als Empfänger der Nachricht hinzugefügt, die Nachricht ist umgeschrieben, und die eingeschlossene Nachricht wird in eine Datei geschrieben.</span><span class="sxs-lookup"><span data-stu-id="12c0b-108">All of the certificates in the store are added as recipients of the message, the message is enveloped, and the enveloped message is written to a file.</span></span>

<span data-ttu-id="12c0b-109">Zusätzlicher Code kann hinzugefügt werden, um die Zertifikate anzuzeigen, die als Nachrichtenempfänger hinzugefügt werden, um diese Zertifikate zu überprüfen, bevor Sie als beabsichtigte Empfänger hinzugefügt werden, oder um die hinzu zufügenden Zertifikate anderweitig auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="12c0b-109">Additional code can be added to display the certificates being added as message recipients, to verify those certificates before they are added as intended recipients, or to otherwise choose those that are to be added.</span></span>

<span data-ttu-id="12c0b-110">Bei einem beliebigen CAPICOM-Fehler wird der negative Dezimalwert **Err. Number** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="12c0b-110">On any CAPICOM error, a negative decimal value of **Err.Number** is returned.</span></span> <span data-ttu-id="12c0b-111">Weitere Informationen finden Sie unter [**CAPICOM- \_ Fehler \_ Code**](capicom-error-code.md).</span><span class="sxs-lookup"><span data-stu-id="12c0b-111">For more information, see [**CAPICOM\_ERROR\_CODE**](capicom-error-code.md).</span></span> <span data-ttu-id="12c0b-112">Informationen zu positiven Dezimalwerten von **Err. Number** finden Sie unter Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="12c0b-112">For information about positive decimal values of **Err.Number**, see Winerror.h.</span></span>


```VB
Sub Envelope(ByVal InFile As String, ByVal OutFile As String, _
             ByVal StoreName As String)

On Error GoTo ErrorHandler

'Open the input file and read the message to be enveloped.

Dim Text As String
Open InFile For Input As #1
Input #1, Text
Close #1
If Len(Text) < 1 Then
    MsgBox "No message to be enveloped."
    Exit Sub
End If

'Open the store containing the certificates of
'the message recipients.

Dim CertStore As New Store
CertStore.Open CAPICOM_CURRENT_USER_STORE, StoreName, _
    CAPICOM_STORE_OPEN_READ_ONLY

' Check for an empty certificate store.

If CertStore.Certificates.Count < 1 Then
    MsgBox "There are no recipient certificates available."
    Set CertStore = Nothing
    Exit Sub
End If

' Declare and initialize an EnvelopedData object

Dim EnvMessage As New EnvelopedData
EnvMessage.Content = Text
Dim I As Integer
For I = 1 To CertStore.Certificates.Count
    EnvMessage.Recipients.Add CertStore.Certificates.Item(I)
    ' The following line can be uncommented to see a prompt
    ' for each certificate in the store.
    ' CertStore.Certificates.Item(I).Display
Next I

'  Set the encryption algorithm and key length. Comment out
'  or remove the following lines to use the default algorithm
'  and key length. The triple DES algorithm and 128 bit key
'  length may not be supported.
Envmessage.Algorithm.Name = ENCRYPTION_ALGORITHM_RC4
Envmessage.Algorithm.KeyLength = KEY_LENGTH_128_BITS

'Declare the string that will hold the enveloped message.

Dim EnvelopedMessage As String

'Encrypt the message into EnvelopedMessage. The enveloped message
'string contains everything that an intended recipient will need to
'decrypt the message, including information on the 
'encryption algorithm key length.
EnvelopedMessage = EnvMessage.Encrypt

' Optionally, check the length of the encrypted string to make sure 
' that the encrypt method worked.

If Len(EnvelopedMessage) < 1 Then
    MsgBox "no message encrypted. "
Else
    MsgBox " Message is " & Len(EnvelopedMessage) & " characters"

    ' Open an output file and write the encrypted message to the 
    ' file. The file is not opened if there is no message to write.
    Open OutFile For Output As #2
    Write #2, EnvelopedMessage
    Close #2
    MsgBox "The message written to file "
End If

' Release the EncryptedData object and the Store object.
Set Envmessage = Nothing
Set CertStore = Nothing

Exit Sub

ErrorHandler:
If Err.Number > 0 Then
    MsgBox "Visual Basic error found : " & Err.Description
Else
    MsgBox "CAPICOM error found : " & Err.Number
End If
End Sub
```



 

 



