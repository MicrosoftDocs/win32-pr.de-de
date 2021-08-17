---
description: Diese Unterroutine akzeptiert eine zu verschlüsselnde Zeichenfolge, eine Kennwortzeichenfolge zum Generieren eines Verschlüsselungsschlüssels und den Namen einer Datei, in die die verschlüsselte Nachricht geschrieben wird.
ms.assetid: 9ad3199a-bca1-4990-80da-80744e349047
title: Verschlüsseln einer Nachricht in CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a3ef531fa75fc4d99a423ffbb6c0edd591caf6b1939f12fea439e7f9fbc80dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117766192"
---
# <a name="encrypting-a-message-in-capicom"></a>Verschlüsseln einer Nachricht in CAPICOM

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die .NET Framework, um Sicherheitsfeatures zu implementieren. Weitere Informationen finden Sie unter [Alternativen zur Verwendung von CAPICOM](alternatives-to-using-capicom.md).\]

Diese Unterroutine akzeptiert eine zu verschlüsselnde Zeichenfolge, eine Kennwortzeichenfolge zum Generieren eines Verschlüsselungsschlüssels und den Namen einer Datei, in die die verschlüsselte Nachricht geschrieben wird. Alle Parameter werden durch Werte an die Unterroutine übergeben. Zum Entschlüsseln der Nachricht muss dieselbe Kennwortzeichenfolge verwendet werden. Wenn das Kennwort verloren geht, kann der Text nicht entschlüsselt werden. Der Datenschutz der Nachricht geht verloren, wenn ein unbeabsichtigter Empfänger Zugriff auf das Kennwort erhält.

> [!Note]  
> CAPICOM unterstützt den PKCS 7 EncryptedData-Inhaltstyp nicht, verwendet jedoch eine nicht \# standardmäßige ASN-Struktur für EncryptedData. Daher kann nur CAPICOM ein CAPICOM EncryptedData-Objekt entschlüsseln.

 

Bei jedem CAPICOM-Fehler wird ein negativer Dezimalwert der **Err.Number-Eigenschaft** zurückgegeben. Weitere Informationen finden Sie unter [**CAPICOM \_ ERROR \_ CODE**](capicom-error-code.md). Informationen zu positiven Dezimalwerten von **Err.Number finden** Sie unter Winerror.h.


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



 

 



