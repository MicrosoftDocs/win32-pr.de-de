---
description: Ein Dokument kann von mehreren Signatur Bezeichnerzeichen signiert werden.
ms.assetid: f81cbf7b-317d-4fab-9b30-88b6c6576db8
title: Cosignieren eines Dokuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa06cbbc95dc0fe558c6e704bd18102e80221dbc
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106370360"
---
# <a name="cosigning-a-document"></a>Cosignieren eines Dokuments

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die .NET Framework, um Sicherheitsfunktionen zu implementieren. Weitere Informationen finden Sie unter [Alternativen zur Verwendung von CAPICOM](alternatives-to-using-capicom.md).\]

Ein Dokument kann von mehreren Signatur Bezeichnerzeichen signiert werden. Dies ist der Fall, wenn zwei oder mehr Parteien einen Vertrag oder einen Spesen Bericht signieren. Im folgenden Beispiel wird ein Dokument, das bereits signiert wurde, von einem zweiten Signatur Geber empfangen. Dieser Signatur Geber verwendet die [**cosign**](signeddata-cosign.md) -Methode, um dem Dokument eine zusätzliche Signatur anzufügen.

Wenn ein CAPICOM-Fehler auftritt, wird in der **Err. Number** -Eigenschaft ein negativer Wert zurückgegeben. Weitere Informationen zu CAPICOM-Fehlercodes finden Sie unter [**CAPICOM- \_ Fehler \_ Code**](capicom-error-code.md). Wenn der Fehlercode in der **Err. Number** -Eigenschaft ein positiver Wert ist, handelt es sich bei dem Fehler um einen Windows-Fehler. Informationen zu Windows-Fehlercodes finden Sie unter Winerror. h.

> [!Note]
> Für das cosignieren eines Dokuments ist es auch erforderlich, dass der kosigner über ein verfügbares [*Zertifikat*](../secgloss/c-gly.md) mit einem [*privaten Schlüssel*](../secgloss/p-gly.md) zum Erstellen der Signatur verfügt. Wenn ein Signatur Geber im-Befehl der [**Sign**](signeddata-sign.md) -Methode nicht angegeben ist und kein Zertifikat im CAPICOM- \_ \_ Speicher mit einem zugeordneten privaten Schlüssel vorhanden ist, schlägt die Methode fehl. Wenn in CAPICOM \_ mein \_ Speicher mit einem zugeordneten privaten Schlüssel nur ein Zertifikat vorhanden ist, werden dieser Schlüssel und dieses Zertifikat verwendet. Wenn mehrere verwendbare Zertifikate vorhanden sind, wird eine Eingabeaufforderung angezeigt, die es dem Benutzer ermöglicht, das gewünschte Zertifikat auszuwählen.
> 
> Wenn die [**cosign**](signeddata-cosign.md) -Methode in einer webbasierten Anwendung verwendet wird, wird immer eine Eingabeaufforderung angezeigt, um die Berechtigung des Benutzers zu erhalten, bevor eine Signatur mit dem privaten Schlüssel des Signatur Gebers erstellt wird.

 

Im folgenden Beispiel werden Dateien, die das zu Signier Ende Dokument enthalten, und die aktuellen Signaturen in diesem Dokument gelesen, die Signatur cosigniert, und die neue Signatur wird in eine Datei geschrieben. Im Beispiel wird eine getrennte Signatur mit den signierten Daten und der Signatur in separaten Dateien verwendet.


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



 

 
