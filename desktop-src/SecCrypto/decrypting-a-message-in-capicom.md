---
description: Diese Unterroutine nimmt eine Kenn Wort Zeichenfolge zum Generieren eines Sitzungs Verschlüsselungsschlüssels und den Namen einer Datei an, aus der eine verschlüsselte Nachricht gelesen wird. Alle Parameter werden durch-Werte an die Unterroutine übergeben.
ms.assetid: 70f23d93-2bca-419b-9de7-e52ce4fb1350
title: Entschlüsseln einer Nachricht in CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba984bad7d9289eaf89725e9598a4330f16b49ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347580"
---
# <a name="decrypting-a-message-in-capicom"></a>Entschlüsseln einer Nachricht in CAPICOM

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die .NET Framework, um Sicherheitsfunktionen zu implementieren. Weitere Informationen finden Sie unter [Alternativen zur Verwendung von CAPICOM](alternatives-to-using-capicom.md).\]

Diese Unterroutine nimmt eine Kenn Wort Zeichenfolge zum Generieren eines Sitzungs Verschlüsselungsschlüssels und den Namen einer Datei an, aus der eine verschlüsselte Nachricht gelesen wird. Alle Parameter werden durch-Werte an die Unterroutine übergeben.

> [!Note]  
> CAPICOM unterstützt den PKCS \# 7-Inhaltstyp "verschlüsselteddata" nicht, sondern verwendet eine nicht dem Standard entsprechende ASN-Struktur für "verschlüsselteddata". Daher kann nur CAPICOM ein CAPICOM-Objekt "verschlüsselteddata" entschlüsseln.

 

Wenn das Entschlüsseln fehlschlägt, wird der Wert **Err. Number** geprüft, um zu bestimmen, ob der Fehler durch die Verwendung eines Kennworts verursacht wurde, das nicht mit dem Kennwort für die Verschlüsselung der Nachricht identisch war. In diesem Fall wird der Fehler "Erstellungs ungültige \_ \_ Daten" zurückgegeben.

Bei einem beliebigen CAPICOM-Fehler wird der negative Dezimalwert **Err. Number** zurückgegeben. Weitere Informationen finden Sie unter [**CAPICOM- \_ Fehler \_ Code**](capicom-error-code.md). Informationen zu positiven Dezimalwerten von **Err. Number** finden Sie unter Winerror. h.


```VB
Sub DecryptMessage(ByVal hidden As String, ByVal filename As String)
On Error goto ErrorHandler

'Declare an EncryptedData object

Dim message As New EncryptedData

'Declare a string variable to hold the encrypted message.
Dim encrypted As String

' Open an input file and read in the encrypted message
Open filename For Input As #1
Input #1, encrypted
Close #1

' If a message was read in (the length of the input string is 
' greater than 0), set the password and decrypt the message.
If Len(encrypted) > 0 then
    ' Set the password used to generate the key
    ' used to decrypt the message. If the password
    ' not the same as the password used when the message
    ' was encrypted, decryption will fail.
    ' The algorithm name and key length set in the encrypting
    ' process are automatically used to decrypt the message. 
    message.SetSecret hidden
    message.Decrypt encrypted
    ' Display the decrypted message.
    MsgBox message.Content
else
    msgbox "No encrypted message was read in.
endif

' Release the EncryptedData object and exit the subroutine.
Set message = Nothing
Exit Sub

ErrorHandler:
If Err.Number > 0 Then
    MsgBox "Visual Basic error found:" & Err.Description
Else
'    Check for a bad password error.
    If Err.Number = -2146893819 Then
        MsgBox "Error. The password may not be correct."
    Else
        MsgBox "CAPICOM error found : " & Err.Number
    End If
End If
End Sub
```



 

 



