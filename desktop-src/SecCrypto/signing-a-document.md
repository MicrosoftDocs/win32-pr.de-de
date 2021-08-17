---
description: Eine Standardverwendung einer Signatur besteht darin, einen Text zu signieren und diesen signierten Text in einer Datei zu speichern. Der signierte Text kann auch über das Internet gesendet werden. Die signierte Nachricht hat das PKCS \# 7-Format.
ms.assetid: 67a36123-4fce-4d40-83c3-b9668221276b
title: Signieren eines Dokuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 526bc4cd98d6cab40efc884a2377f3720c9849dbb7f6c1d4e8da5d49898bfa64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898164"
---
# <a name="signing-a-document"></a>Signieren eines Dokuments

\[CAPICOM ist eine nur 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die .NET Framework, um Sicherheitsfeatures zu implementieren. Weitere Informationen finden Sie unter [Alternativen zur Verwendung von CAPICOM.](alternatives-to-using-capicom.md)\]

Eine Standardverwendung einer Signatur besteht darin, einen Text zu signieren und diesen signierten Text in einer Datei zu speichern. Der signierte Text kann auch über das Internet gesendet werden. Die signierte Nachricht hat das PKCS \# 7-Format.

In diesem Beispiel wird die Signatur für getrennten Inhalt erstellt (wenn der Inhalt nicht in der Signatur enthalten ist). Eine getrennte Signatur wird am häufigsten verwendet, wenn der Empfänger der Signatur über eine Kopie des genau signierten Texts verfügt. Im folgenden Beispiel werden die ursprüngliche Nachricht und die getrennte Signatur in separate Dateien geschrieben.

Bei einem CAPICOM-Fehler wird ein negativer Dezimalwert von **Err.Number** zurückgegeben. Weitere Informationen finden Sie unter [**CAPICOM \_ ERROR \_ CODE**](capicom-error-code.md). Informationen zu positiven Dezimalwerten von **Err.Number** finden Sie unter Winerror.h.

Beim Erstellen einer Signatur wird der private Schlüssel des Signaturgebers [*verwendet.*](../secgloss/p-gly.md) Eine Signatur kann nur erstellt werden, wenn das Zertifikat des Signaturgebers mit einem zugeordneten privaten Schlüssel verfügbar ist. In diesem Beispiel der **Sign-Methode** wird kein Signer angegeben. Wenn kein Signierer angegeben ist und kein Zertifikat in **CAPICOM \_ MY \_ STORE** über einen zugeordneten privaten Schlüssel verfügt, schlägt die **Sign-Methode** fehl. Wenn einem und nur einem Zertifikat in **CAPICOM \_ MY \_ STORE** ein privater Schlüssel zugeordnet ist, werden dieses Zertifikat und sein privater Schlüssel zum Erstellen der Signatur verwendet. Wenn mehr als ein Zertifikat im **CAPICOM \_ MY \_ STORE-Speicher** über einen zugeordneten privaten Schlüssel verfügt, wird ein Dialogfeld angezeigt, und der Benutzer kann das Zertifikat auswählen, das zum Erstellen der Signatur verwendet werden soll.

Wenn eine webbasierte Anwendung die **Sign-Methode** verwendet, wird immer eine Eingabeaufforderung angezeigt, und die Berechtigung des Benutzers ist erforderlich, bevor eine Signatur erstellt wird, die den privaten Schlüssel des Signaturgebers verwendet.


```VB
Sub Signfile(ByVal InputFileName As String, _
    ByVal OutputFileName As String)
    
    On Error GoTo ErrorHandler
    Dim c As String
    Dim s As String
    Dim MyStore As New Store
    Dim Signobj As New SignedData
    Dim Signer As New Signer

    ' NOTE: the name 'Attribute' is not a unique name
    ' and must be preceded by 'CAPICOM.'
    Dim SigningTime As New CAPICOM.Attribute

    ' Open the MY store and retrieve the first certificate from the
    ' Store. The signing operation will only work if this
    ' certificate is valid and has access to the signer's private key.
    MyStore.Open CAPICOM_CURRENT_USER_STORE, "MY", _
        CAPICOM_STORE_OPEN_READ_ONLY
    Signer.Certificate = MyStore.Certificates.Item(1)

    ' Open the input file and read the content to be signed from
    ' the file.
    Open App.Path & "\" & InputFileName For Input As #1
    Input #1, c
    Close #1
    
    ' Set the content to be signed.
    Signobj.Content = c

    ' Save the time the data was signed as a signer attribute.
    SigningTime.Name = CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME
    SigningTime.Value = Now
    Signer.AuthenticatedAttributes.Add SigningTime

    ' Sign the content using the signer's private key.
    ' The 'True' parameter indicates that the content signed is not
    ' included in the signature string.
    s = Signobj.Sign(Signer, True)

    Open App.Path & "\" & OutputFileName For Output As #2
    Write #2, s
    Close #2

    MsgBox ("Signature done - Saved to file" & OutputFileName)
    Set Signobj = Nothing
    Set MyStore = Nothing
    Set Signer = Nothing
    Set SigningTime = Nothing

    Exit Sub

ErrorHandler:
    If Err.Number > 0 Then
        MsgBox ("Visual Basic error found:" & Err.Description)
    Else
        MsgBox ("CAPICOM error found : " & Err.Number)
    End If
End Sub
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Store. Öffnen**](store-open.md)
</dt> <dt>

[**Signer.Certificate**](signer-certificate.md)
</dt> <dt>

[**attribute**](attribute.md)
</dt> <dt>

[**SignedData**](signeddata.md)
</dt> </dl>

 

 
