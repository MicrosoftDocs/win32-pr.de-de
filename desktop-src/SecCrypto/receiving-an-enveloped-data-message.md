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
# <a name="receiving-an-enveloped-data-message"></a>Empfangen einer eingeschlossenen Daten Nachricht

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die .NET Framework, um Sicherheitsfunktionen zu implementieren. Weitere Informationen finden Sie unter [Alternativen zur Verwendung von CAPICOM](alternatives-to-using-capicom.md).\]

Zum Entschlüsseln einer eingeschlossenen Nachricht entspricht der Empfänger einem [*Zertifikat*](../secgloss/c-gly.md) aus dem eigenen Speicher, das über einen verfügbaren privaten Schlüssel mit einem Zertifikat in der eingeschlossenen Nachricht verfügt. Wenn eine Entsprechung gefunden wird, wird der verschlüsselte Schlüssel, der diesem Zertifikat zugeordnet ist, entschlüsselt, und der entschlüsselte Schlüssel wird zum Entschlüsseln der eingeschlossenen Nachricht verwendet. Ein Nachrichtenempfänger, der nicht über ein übereinstimmendes Zertifikat mit einem verfügbaren privaten Schlüssel verfügt, kann die Nachricht nicht entschlüsseln.

Im folgenden Beispiel wird ein Dateiname an die Unterroutine übergeben, die Datei wird geöffnet, und eine eingehüllte Nachricht wird gelesen. Die eingeschlossene Nachricht wird dann entschlüsselt. Die Schritte zum Abgleichen eines Benutzer Zertifikats mit einem Zertifikat in der eingeschlossenen Nachricht, das Entschlüsseln des Verschlüsselungsschlüssels und schließlich das Entschlüsseln der Nachricht, werden alle im Hintergrund durchgeführt. Ein Fehler wird ausgelöst, wenn eine Zertifikat Übereinstimmung nicht gefunden wurde oder wenn das Entschlüsseln fehlschlägt.

Bei einem beliebigen CAPICOM-Fehler wird der negative Dezimalwert **Err. Number** zurückgegeben. Weitere Informationen finden Sie unter [**CAPICOM- \_ Fehler \_ Code**](capicom-error-code.md). Informationen zu positiven Dezimalwerten von **Err. Number** finden Sie unter Winerror. h.


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



 

 
