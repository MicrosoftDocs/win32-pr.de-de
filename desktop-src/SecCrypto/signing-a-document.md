---
description: Eine Signatur wird standardmäßig verwendet, um einen Text zu signieren und den signierten Text in einer Datei zu speichern. Der signierte Text kann auch über das Internet gesendet werden. Die signierte Nachricht weist das PKCS \# 7-Format auf.
ms.assetid: 67a36123-4fce-4d40-83c3-b9668221276b
title: Signieren eines Dokuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ce1754cdfa1e89c23525474bae880dc2809c242
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106339726"
---
# <a name="signing-a-document"></a>Signieren eines Dokuments

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die .NET Framework, um Sicherheitsfunktionen zu implementieren. Weitere Informationen finden Sie unter [Alternativen zur Verwendung von CAPICOM](alternatives-to-using-capicom.md).\]

Eine Signatur wird standardmäßig verwendet, um einen Text zu signieren und den signierten Text in einer Datei zu speichern. Der signierte Text kann auch über das Internet gesendet werden. Die signierte Nachricht weist das PKCS \# 7-Format auf.

In diesem Beispiel wird die Signatur für getrennten Inhalt erstellt (wenn der Inhalt nicht in der Signatur enthalten ist). Eine getrennte Signatur wird am häufigsten verwendet, wenn der Empfänger der Signatur über eine Kopie des exakt signierten Texts verfügt. Im folgenden Beispiel werden die ursprüngliche Nachricht und die getrennte Signatur in separate Dateien geschrieben.

Bei einem beliebigen CAPICOM-Fehler wird der negative Dezimalwert **Err. Number** zurückgegeben. Weitere Informationen finden Sie unter [**CAPICOM- \_ Fehler \_ Code**](capicom-error-code.md). Informationen zu positiven Dezimalwerten von **Err. Number** finden Sie unter Winerror. h.

Beim Erstellen einer Signatur wird der [*private Schlüssel*](../secgloss/p-gly.md)des Signatur Gebers verwendet. Eine Signatur kann nur erstellt werden, wenn das Zertifikat des Signatur Gebers mit einem zugeordneten privaten Schlüssel verfügbar ist. In diesem Beispiel der **Sign** -Methode ist kein Signatur Geber angegeben. Wenn kein Signatur Geber angegeben ist und kein Zertifikat in **CAPICOM \_ meinem \_ Speicher** über einen zugeordneten privaten Schlüssel verfügt, **schlägt die** Signierungs Methode fehl. Wenn nur ein Zertifikat in **CAPICOM \_ meinem \_ Speicher** über einen zugeordneten privaten Schlüssel verfügt, wird dieses Zertifikat und der zugehörige private Schlüssel zum Erstellen der Signatur verwendet. Wenn mehr als ein Zertifikat im CAPICOM-Speicher " **\_ mein \_ Speicher** " über einen zugeordneten privaten Schlüssel verfügt, wird ein Dialogfeld angezeigt, und der Benutzer kann das Zertifikat auswählen, das zum Erstellen der Signatur verwendet werden soll.

Wenn eine webbasierte Anwendung die **Sign** -Methode verwendet, wird immer eine Eingabeaufforderung angezeigt, und die Berechtigung des Benutzers ist erforderlich, bevor eine Signatur erstellt wird, die den privaten Schlüssel des Signatur Gebers verwendet.


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

[**Store. Open**](store-open.md)
</dt> <dt>

[**Signatur Geber. Certificate**](signer-certificate.md)
</dt> <dt>

[**Versehen**](attribute.md)
</dt> <dt>

[**SignedData**](signeddata.md)
</dt> </dl>

 

 
