---
description: Ein Dokument kann von mehr als einem Signator signiert werden.
ms.assetid: f81cbf7b-317d-4fab-9b30-88b6c6576db8
title: Cosignieren eines Dokuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb384ef47001f1df85810ac37595988da96a356ff3b36b1b140d1a6f54d0d698
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769385"
---
# <a name="cosigning-a-document"></a>Cosignieren eines Dokuments

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die .NET Framework, um Sicherheitsfeatures zu implementieren. Weitere Informationen finden Sie unter [Alternativen zur Verwendung von CAPICOM](alternatives-to-using-capicom.md).\]

Ein Dokument kann von mehr als einem Signator signiert werden. Dies geschieht beispielsweise, wenn zwei oder mehr Parteien einen Vertrag oder eine Spesenabrechnung unterzeichnen. Im folgenden Beispiel wird ein bereits signiertes Dokument von einem zweiten Signator empfangen. Dieser Signaturer verwendet die [**CoSign-Methode,**](signeddata-cosign.md) um dem Dokument eine zusätzliche Signatur anfügen.

Wenn ein CAPICOM-Fehler auftritt, wird in der **Err.Number-Eigenschaft** ein negativer Wert zurückgegeben. Weitere Informationen zu CAPICOM-Fehlercodes finden Sie unter [**CAPICOM \_ ERROR \_ CODE**](capicom-error-code.md). Wenn der Fehlercode in der **Err.Number-Eigenschaft** ein positiver Wert ist, ist der Fehler ein Windows Fehler. Informationen zu Windows Fehlercodes finden Sie unter Winerror.h.

> [!Note]
> Das Cosignieren eines Dokuments erfordert auch, [](../secgloss/c-gly.md) dass der Cosigner über ein verfügbares Zertifikat mit einem [*privaten*](../secgloss/p-gly.md) Schlüssel zum Erstellen der Signatur verfügen muss. Wenn ein Signator im Aufruf der [**Sign-Methode**](signeddata-sign.md) nicht angegeben ist und kein Zertifikat in CAPICOM MY STORE mit einem zugeordneten privaten Schlüssel verfügbar ist, schlägt die \_ Methode \_ fehl. Wenn es in CAPICOM MY STORE nur ein Zertifikat mit einem zugeordneten privaten Schlüssel gibt, werden dieser Schlüssel \_ \_ und das Zertifikat verwendet. Wenn es mehrere nutzbare Zertifikate gibt, wird eine Eingabeaufforderung angezeigt, damit der Benutzer das gewünschte Zertifikat auswählen kann.
> 
> Wenn die [**CoSign-Methode**](signeddata-cosign.md) in einer webbasierten Anwendung verwendet wird, wird immer eine Eingabeaufforderung angezeigt, um die Berechtigung des Benutzers zu erhalten, bevor eine Signatur mit dem privaten Schlüssel dieses Signaturers erstellt wird.

 

Im folgenden Beispiel werden Dateien gelesen, die das zu unterschreibende Dokument und die aktuellen Signaturen für dieses Dokument enthalten, die Signatur wird cosigniert, und die neue Signatur wird in eine Datei geschrieben. Im Beispiel wird eine getrennte Signatur mit den signierten Daten und die Signatur in separaten Dateien verwendet.


```VB
Sub CoSignContent(ByVal InputFile1Name As String, ByVal _
    InputFile2Name As String, ByVal OutputFileName As String)

    On Error GoTo ErrorHandler
    Dim c As String
    Dim s As String
    Dim CS As String
    Dim Signobj As New SignedData
    Open InputFile1Name for Input as #1
    Input #1, s
    Close #1
    Open InputFileName2 for input as #2
    Input #2, c 
    Close #2

    Signobj.Content = c
    Signobj.Verify(s)
    CS = Signobj.CoSign
    Open OutputFileName for output as #3
    Write #3, CS
    Close # 3
    Signobj = Nothing
    MsgBox("Cosign finished. Cosignature saved to a file.")
    Exit Sub
ErrorHandler:
    If err.number > 0 Then
        MsgBox("Visual Basic error found:" & err.description)
    Else
        MsgBox("CAPICOM error found : " & err.number)
    End If
End Sub
```



 

 
