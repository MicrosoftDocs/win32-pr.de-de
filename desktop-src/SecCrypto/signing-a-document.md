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
# <a name="signing-a-document"></a><span data-ttu-id="47a21-105">Signieren eines Dokuments</span><span class="sxs-lookup"><span data-stu-id="47a21-105">Signing a Document</span></span>

<span data-ttu-id="47a21-106">\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="47a21-106">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="47a21-107">Verwenden Sie stattdessen die .NET Framework, um Sicherheitsfunktionen zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="47a21-107">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="47a21-108">Weitere Informationen finden Sie unter [Alternativen zur Verwendung von CAPICOM](alternatives-to-using-capicom.md).\]</span><span class="sxs-lookup"><span data-stu-id="47a21-108">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="47a21-109">Eine Signatur wird standardmäßig verwendet, um einen Text zu signieren und den signierten Text in einer Datei zu speichern.</span><span class="sxs-lookup"><span data-stu-id="47a21-109">A standard use of a signature is to sign a text and save that signed text to a file.</span></span> <span data-ttu-id="47a21-110">Der signierte Text kann auch über das Internet gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="47a21-110">The signed text could also be sent over the Internet.</span></span> <span data-ttu-id="47a21-111">Die signierte Nachricht weist das PKCS \# 7-Format auf.</span><span class="sxs-lookup"><span data-stu-id="47a21-111">The signed message is in PKCS \#7 format.</span></span>

<span data-ttu-id="47a21-112">In diesem Beispiel wird die Signatur für getrennten Inhalt erstellt (wenn der Inhalt nicht in der Signatur enthalten ist).</span><span class="sxs-lookup"><span data-stu-id="47a21-112">In this example, the signature is created for detached content (when the content is not included with the signature).</span></span> <span data-ttu-id="47a21-113">Eine getrennte Signatur wird am häufigsten verwendet, wenn der Empfänger der Signatur über eine Kopie des exakt signierten Texts verfügt.</span><span class="sxs-lookup"><span data-stu-id="47a21-113">A detached signature would most often be used if the recipient of the signature has a copy of the exact signed text.</span></span> <span data-ttu-id="47a21-114">Im folgenden Beispiel werden die ursprüngliche Nachricht und die getrennte Signatur in separate Dateien geschrieben.</span><span class="sxs-lookup"><span data-stu-id="47a21-114">In the example below, the original message and the detached signature are written to separate files.</span></span>

<span data-ttu-id="47a21-115">Bei einem beliebigen CAPICOM-Fehler wird der negative Dezimalwert **Err. Number** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="47a21-115">On any CAPICOM error, a negative decimal value of **Err.Number** is returned.</span></span> <span data-ttu-id="47a21-116">Weitere Informationen finden Sie unter [**CAPICOM- \_ Fehler \_ Code**](capicom-error-code.md).</span><span class="sxs-lookup"><span data-stu-id="47a21-116">For more information, see [**CAPICOM\_ERROR\_CODE**](capicom-error-code.md).</span></span> <span data-ttu-id="47a21-117">Informationen zu positiven Dezimalwerten von **Err. Number** finden Sie unter Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="47a21-117">For information about positive decimal values of **Err.Number**, see Winerror.h.</span></span>

<span data-ttu-id="47a21-118">Beim Erstellen einer Signatur wird der [*private Schlüssel*](../secgloss/p-gly.md)des Signatur Gebers verwendet.</span><span class="sxs-lookup"><span data-stu-id="47a21-118">Creating a signature uses the signer's [*private key*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="47a21-119">Eine Signatur kann nur erstellt werden, wenn das Zertifikat des Signatur Gebers mit einem zugeordneten privaten Schlüssel verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="47a21-119">A signature can only be created if the signer's certificate with an associated private key is available.</span></span> <span data-ttu-id="47a21-120">In diesem Beispiel der **Sign** -Methode ist kein Signatur Geber angegeben.</span><span class="sxs-lookup"><span data-stu-id="47a21-120">This example of the **Sign** method does not specify a signer.</span></span> <span data-ttu-id="47a21-121">Wenn kein Signatur Geber angegeben ist und kein Zertifikat in **CAPICOM \_ meinem \_ Speicher** über einen zugeordneten privaten Schlüssel verfügt, **schlägt die** Signierungs Methode fehl.</span><span class="sxs-lookup"><span data-stu-id="47a21-121">If a signer is not specified and no certificate in **CAPICOM\_MY\_STORE** has an associated private key, the **Sign** method fails.</span></span> <span data-ttu-id="47a21-122">Wenn nur ein Zertifikat in **CAPICOM \_ meinem \_ Speicher** über einen zugeordneten privaten Schlüssel verfügt, wird dieses Zertifikat und der zugehörige private Schlüssel zum Erstellen der Signatur verwendet.</span><span class="sxs-lookup"><span data-stu-id="47a21-122">If one and only one certificate in **CAPICOM\_MY\_STORE** has an associated private key, that certificate and its private key is used to create the signature.</span></span> <span data-ttu-id="47a21-123">Wenn mehr als ein Zertifikat im CAPICOM-Speicher " **\_ mein \_ Speicher** " über einen zugeordneten privaten Schlüssel verfügt, wird ein Dialogfeld angezeigt, und der Benutzer kann das Zertifikat auswählen, das zum Erstellen der Signatur verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="47a21-123">If more than one certificate in the **CAPICOM\_MY\_STORE** store has an associated private key, a dialog box appears and the user can choose the certificate to be used to create the signature.</span></span>

<span data-ttu-id="47a21-124">Wenn eine webbasierte Anwendung die **Sign** -Methode verwendet, wird immer eine Eingabeaufforderung angezeigt, und die Berechtigung des Benutzers ist erforderlich, bevor eine Signatur erstellt wird, die den privaten Schlüssel des Signatur Gebers verwendet.</span><span class="sxs-lookup"><span data-stu-id="47a21-124">When a web-based application uses the **Sign** method, a prompt is always displayed and the user's permission is required before a signature that uses that signer's private key is created.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="47a21-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="47a21-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47a21-126">**Store. Open**</span><span class="sxs-lookup"><span data-stu-id="47a21-126">**Store.Open**</span></span>](store-open.md)
</dt> <dt>

[<span data-ttu-id="47a21-127">**Signatur Geber. Certificate**</span><span class="sxs-lookup"><span data-stu-id="47a21-127">**Signer.Certificate**</span></span>](signer-certificate.md)
</dt> <dt>

[<span data-ttu-id="47a21-128">**Versehen**</span><span class="sxs-lookup"><span data-stu-id="47a21-128">**Attribute**</span></span>](attribute.md)
</dt> <dt>

[<span data-ttu-id="47a21-129">**SignedData**</span><span class="sxs-lookup"><span data-stu-id="47a21-129">**SignedData**</span></span>](signeddata.md)
</dt> </dl>

 

 
