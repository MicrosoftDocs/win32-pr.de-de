---
description: Wenn ein signiertes Dokument empfangen wird, kann die Gültigkeit der Signatur oder der Signaturen überprüft werden.
ms.assetid: 088915d8-768c-4378-a9dd-9347a428aff9
title: Überprüfen der Signatur in einem Dokument
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f2886edcb9629011ddf1a0b5fb45a12a11f0556
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865451"
---
# <a name="verifying-the-signature-on-a-document"></a>Überprüfen der Signatur in einem Dokument

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die .NET Framework, um Sicherheitsfunktionen zu implementieren. Weitere Informationen finden Sie unter [Alternativen zur Verwendung von CAPICOM](alternatives-to-using-capicom.md).\]

Wenn ein signiertes Dokument empfangen wird, kann die Gültigkeit der Signatur oder der Signaturen überprüft werden. Eine Signatur kann auf Folgendes geprüft werden:

-   Gültigkeit des Signatur Hashs
-   Gültigkeit des Zertifikats des Signatur Gebers

Der Signatur [*Hash*](../secgloss/h-gly.md) wird mithilfe des [*öffentlichen Schlüssels*](../secgloss/p-gly.md) des Signatur Gebers entschlüsselt, der im [*Zertifikat*](../secgloss/c-gly.md)des Signatur Gebers gefunden wurde und als Teil der Signatur enthalten ist. Wenn die entschlüsselte Signatur mit einem neuen Hash des ursprünglichen Dokuments übereinstimmt, wurde die Signatur vom Besitzer des privaten Schlüssels erstellt, der dem öffentlichen Schlüssel zugeordnet ist, der zum Entschlüsseln des Hashwerts verwendet wird. Außerdem wird sichergestellt, dass das Dokument, auf dem die Signatur basiert, sichergestellt ist, dass es nach dem Erstellen der Signatur nicht geändert wurde.

Das Zertifikat, das den öffentlichen Schlüssel und die Identität des Signatur Gebers bereitgestellt hat, kann auch auf Gültigkeit überprüft werden, z. b. ob das Zertifikat widerrufen wurde, ob das Zertifikat veraltet ist oder ob das Zertifikat von einem vertrauenswürdigen Zertifikat Aussteller ausgestellt wurde.

Im folgenden Beispiel werden der signierte Inhalt und das **SignedData** -Objekt aus einer Datei gelesen, und die Signatur und die Gültigkeit des Zertifikats, das zum Erstellen der Signatur verwendet wird, werden überprüft.

> [!Note]  
> Wenn die Signatur nicht kryptografisch gültig ist oder das Zertifikat des Signatur Gebers ungültig ist, wird eine Ausnahme ausgelöst, und das überprüfende Programm muss die Ausnahme behandeln. Bei einem beliebigen CAPICOM-Fehler wird der negative Dezimalwert **Err. Number** zurückgegeben. Weitere Informationen finden Sie unter [**CAPICOM- \_ Fehler \_ Code**](capicom-error-code.md). Informationen zu positiven Dezimalwerten von **Err. Number** finden Sie unter Winerror. h.

 


```VB
Sub VerifySig(ByVal FileToVerify As String, ByVal FileBase As String)
On Error GoTo ErrorHandler

Dim sdContent As String
Dim sdCheck As String
Dim mySD As SignedData
Set mySD = New SignedData

' Open a file and read the signature.
Open FileToVerify For Input As #1
Input #1, sdCheck
Close #1

' Open a file and input the plaintext content that was signed.
Open FileBase For Input As #2
Input #2, sdContent
Close #1

' Set the detached content upon which the signature is based.
mySD.Content = sdContent

' Verify the detached signature.
On Error Resume Next
    mySD.Verify sdCheck, True
If Err.Number <> 0 Then
    MsgBox "Signature verification failed. " & Err.Description
Else
    MsgBox "Verification complete."
End If

' Release the SignedData object.
Set mySD = Nothing

Exit Sub
ErrorHandler:
    If Err.Number > 0 Then
        MsgBox "Visual Basic error found: " & Err.Description
    Else
        MsgBox "CAPICOM error found: " & Hex(Err.Number)
    End If
End Sub

```



 

 
