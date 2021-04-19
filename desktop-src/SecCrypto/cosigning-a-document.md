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
# <a name="cosigning-a-document"></a><span data-ttu-id="ca329-103">Cosignieren eines Dokuments</span><span class="sxs-lookup"><span data-stu-id="ca329-103">Cosigning a Document</span></span>

<span data-ttu-id="ca329-104">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ca329-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="ca329-105">Verwenden Sie stattdessen die .NET Framework, um Sicherheitsfunktionen zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="ca329-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="ca329-106">Weitere Informationen finden Sie unter [Alternativen zur Verwendung von CAPICOM](alternatives-to-using-capicom.md).\]</span><span class="sxs-lookup"><span data-stu-id="ca329-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="ca329-107">Ein Dokument kann von mehreren Signatur Bezeichnerzeichen signiert werden.</span><span class="sxs-lookup"><span data-stu-id="ca329-107">A document can be signed by more than one signer.</span></span> <span data-ttu-id="ca329-108">Dies ist der Fall, wenn zwei oder mehr Parteien einen Vertrag oder einen Spesen Bericht signieren.</span><span class="sxs-lookup"><span data-stu-id="ca329-108">This happens when, for instance, two or more parties sign a contract or an expense report.</span></span> <span data-ttu-id="ca329-109">Im folgenden Beispiel wird ein Dokument, das bereits signiert wurde, von einem zweiten Signatur Geber empfangen.</span><span class="sxs-lookup"><span data-stu-id="ca329-109">In the following example, a document already signed is received by a second signer.</span></span> <span data-ttu-id="ca329-110">Dieser Signatur Geber verwendet die [**cosign**](signeddata-cosign.md) -Methode, um dem Dokument eine zusätzliche Signatur anzufügen.</span><span class="sxs-lookup"><span data-stu-id="ca329-110">This signer uses the [**CoSign**](signeddata-cosign.md) method to attach an additional signature to the document.</span></span>

<span data-ttu-id="ca329-111">Wenn ein CAPICOM-Fehler auftritt, wird in der **Err. Number** -Eigenschaft ein negativer Wert zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ca329-111">If any CAPICOM error occurs, a negative value is returned in the **Err.Number** property.</span></span> <span data-ttu-id="ca329-112">Weitere Informationen zu CAPICOM-Fehlercodes finden Sie unter [**CAPICOM- \_ Fehler \_ Code**](capicom-error-code.md).</span><span class="sxs-lookup"><span data-stu-id="ca329-112">For more information about CAPICOM error codes, see [**CAPICOM\_ERROR\_CODE**](capicom-error-code.md).</span></span> <span data-ttu-id="ca329-113">Wenn der Fehlercode in der **Err. Number** -Eigenschaft ein positiver Wert ist, handelt es sich bei dem Fehler um einen Windows-Fehler.</span><span class="sxs-lookup"><span data-stu-id="ca329-113">If the error code in the **Err.Number** property is a positive value, then the error is a Windows error.</span></span> <span data-ttu-id="ca329-114">Informationen zu Windows-Fehlercodes finden Sie unter Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="ca329-114">For information about Windows error codes, see Winerror.h.</span></span>

> [!Note]
> <span data-ttu-id="ca329-115">Für das cosignieren eines Dokuments ist es auch erforderlich, dass der kosigner über ein verfügbares [*Zertifikat*](../secgloss/c-gly.md) mit einem [*privaten Schlüssel*](../secgloss/p-gly.md) zum Erstellen der Signatur verfügt.</span><span class="sxs-lookup"><span data-stu-id="ca329-115">Cosigning a document also requires that the cosigner have an available [*certificate*](../secgloss/c-gly.md) with a [*private key*](../secgloss/p-gly.md) to create the signature.</span></span> <span data-ttu-id="ca329-116">Wenn ein Signatur Geber im-Befehl der [**Sign**](signeddata-sign.md) -Methode nicht angegeben ist und kein Zertifikat im CAPICOM- \_ \_ Speicher mit einem zugeordneten privaten Schlüssel vorhanden ist, schlägt die Methode fehl.</span><span class="sxs-lookup"><span data-stu-id="ca329-116">If a signer is not specified in the call of the [**Sign**](signeddata-sign.md) method and there is no certificate in CAPICOM\_MY\_STORE with an associated private key, the method fails.</span></span> <span data-ttu-id="ca329-117">Wenn in CAPICOM \_ mein \_ Speicher mit einem zugeordneten privaten Schlüssel nur ein Zertifikat vorhanden ist, werden dieser Schlüssel und dieses Zertifikat verwendet.</span><span class="sxs-lookup"><span data-stu-id="ca329-117">If there is one and only one certificate in CAPICOM\_MY\_STORE with an associated private key, that key and certificate are used.</span></span> <span data-ttu-id="ca329-118">Wenn mehrere verwendbare Zertifikate vorhanden sind, wird eine Eingabeaufforderung angezeigt, die es dem Benutzer ermöglicht, das gewünschte Zertifikat auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="ca329-118">If there is more than one usable certificate, a prompt is displayed to allow the user to choose the desired certificate.</span></span>
> 
> <span data-ttu-id="ca329-119">Wenn die [**cosign**](signeddata-cosign.md) -Methode in einer webbasierten Anwendung verwendet wird, wird immer eine Eingabeaufforderung angezeigt, um die Berechtigung des Benutzers zu erhalten, bevor eine Signatur mit dem privaten Schlüssel des Signatur Gebers erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="ca329-119">If the [**CoSign**](signeddata-cosign.md) method is used in a web-based application, a prompt is always displayed to get the user's permission before a signature is created by using that signer's private key.</span></span>

 

<span data-ttu-id="ca329-120">Im folgenden Beispiel werden Dateien, die das zu Signier Ende Dokument enthalten, und die aktuellen Signaturen in diesem Dokument gelesen, die Signatur cosigniert, und die neue Signatur wird in eine Datei geschrieben.</span><span class="sxs-lookup"><span data-stu-id="ca329-120">In the following example, files that contain the document to be signed and the current signatures on that document are read, the signature is cosigned, and the new signature is written to a file.</span></span> <span data-ttu-id="ca329-121">Im Beispiel wird eine getrennte Signatur mit den signierten Daten und der Signatur in separaten Dateien verwendet.</span><span class="sxs-lookup"><span data-stu-id="ca329-121">The example uses a detached signature with the data signed and the signature in separate files.</span></span>


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



 

 
