---
description: Im folgenden Beispiel wird eine Klartextnachricht aus einer Datei eingelesen, und ein Zertifikatspeicher, der die Zertifikate der vorgesehenen Nachrichtenempfänger enthält, wird geöffnet.
ms.assetid: 7ae672d3-e11d-453c-b9c0-354d21830ae4
title: Senden einer Umschlagdatennachricht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d93c73e22a9ac98e08d12164e78aa585a6b2ba3da6f47bf53675a7320bc206e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900360"
---
# <a name="sending-an-enveloped-data-message"></a>Senden einer Umschlagdatennachricht

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die .NET Framework, um Sicherheitsfeatures zu implementieren. Weitere Informationen finden Sie unter [Alternativen zur Verwendung von CAPICOM](alternatives-to-using-capicom.md).\]

Im folgenden Beispiel wird eine Klartextnachricht aus einer Datei eingelesen, und ein Zertifikatspeicher, der die Zertifikate der vorgesehenen Nachrichtenempfänger enthält, wird geöffnet. Alle Zertifikate im Speicher werden als Empfänger der Nachricht hinzugefügt, die Nachricht wird umgeschrieben, und die umgeschriebene Nachricht wird in eine Datei geschrieben.

Zusätzlicher Code kann hinzugefügt werden, um die Zertifikate anzuzeigen, die als Nachrichtenempfänger hinzugefügt werden, um diese Zertifikate zu überprüfen, bevor sie als beabsichtigte Empfänger hinzugefügt werden, oder um die Zertifikate, die hinzugefügt werden sollen, auf andere Weise zu wählen.

Bei jedem CAPICOM-Fehler wird der negative Dezimalwert **Err.Number** zurückgegeben. Weitere Informationen finden Sie unter [**CAPICOM \_ ERROR \_ CODE**](capicom-error-code.md). Informationen zu positiven Dezimalwerten von **Err.Number finden** Sie unter Winerror.h.


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



 

 



