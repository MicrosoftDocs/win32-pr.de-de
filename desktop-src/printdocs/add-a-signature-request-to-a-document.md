---
description: In diesem Thema wird beschrieben, wie einem XPS-Dokument eine Signatur Anforderung hinzugefügt wird.
ms.assetid: 95eb1887-8754-43e0-8886-1f23653bff26
title: Hinzufügen einer Signatur Anforderung zu einem XPS-Dokument
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9db0d3a899dd49f141adf5cd23ea8c837c8b12d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368960"
---
# <a name="add-a-signature-request-to-an-xps-document"></a><span data-ttu-id="6d467-103">Hinzufügen einer Signatur Anforderung zu einem XPS-Dokument</span><span class="sxs-lookup"><span data-stu-id="6d467-103">Add a Signature Request to an XPS Document</span></span>

<span data-ttu-id="6d467-104">In diesem Thema wird beschrieben, wie einem XPS-Dokument eine Signatur Anforderung hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="6d467-104">This topic describes how to add a signature request to an XPS document.</span></span> <span data-ttu-id="6d467-105">Bei einer Signatur Anforderung wird ein Benutzer aufgefordert, ein Dokument zu signieren, wenn er mit der Signatur Absicht einverstanden ist.</span><span class="sxs-lookup"><span data-stu-id="6d467-105">A signature request prompts a user to sign a document if he or she agrees with the signature intent.</span></span>

<span data-ttu-id="6d467-106">Bevor Sie die folgenden Codebeispiele in Ihrem Programm verwenden, lesen Sie den Haftungsausschluss in [Common Digital Signature Programming Tasks](basic-digital-signature-programming-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="6d467-106">Before using the following code examples in your program, read the disclaimer in [Common Digital Signature Programming Tasks](basic-digital-signature-programming-tasks.md).</span></span>

<span data-ttu-id="6d467-107">So fügen Sie einem XPS-Dokument eine Signatur Anforderung hinzu:</span><span class="sxs-lookup"><span data-stu-id="6d467-107">To add a signature request to an XPS Document:</span></span>

1.  <span data-ttu-id="6d467-108">Laden Sie das XPS-Dokument in einen Signatur-Manager, wie unter [Initialisieren des Signatur-Managers](initialize-the-signature-manager.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6d467-108">Load the XPS document into a signature manager, as described in [Initialize the Signature Manager](initialize-the-signature-manager.md).</span></span>
2.  <span data-ttu-id="6d467-109">Fügen Sie dem Signatur-Manager einen Signatur Block hinzu.</span><span class="sxs-lookup"><span data-stu-id="6d467-109">Add a signature block to the signature manager.</span></span>
3.  <span data-ttu-id="6d467-110">Erstellen Sie eine Signatur Anforderung im neuen Signatur Block.</span><span class="sxs-lookup"><span data-stu-id="6d467-110">Create a signature request in the new signature block.</span></span>
4.  <span data-ttu-id="6d467-111">Legen Sie die Eigenschaften der Signatur Anforderung fest:</span><span class="sxs-lookup"><span data-stu-id="6d467-111">Set the properties of the signature request:</span></span>
    1.  <span data-ttu-id="6d467-112">Legen Sie die Signatur Absicht fest.</span><span class="sxs-lookup"><span data-stu-id="6d467-112">Set the signature intent.</span></span>
    2.  <span data-ttu-id="6d467-113">Legen Sie den Namen der Person fest, deren Signatur angefordert wird (der angeforderte Signatur Geber).</span><span class="sxs-lookup"><span data-stu-id="6d467-113">Set the name of the person whose signature is requested (the requested signer).</span></span>
    3.  <span data-ttu-id="6d467-114">Legen Sie das Datum für die erforderliche Signatur fest.</span><span class="sxs-lookup"><span data-stu-id="6d467-114">Set the date the signature is required.</span></span>
    4.  <span data-ttu-id="6d467-115">Legen Sie andere Signatur Eigenschaften nach Bedarf fest.</span><span class="sxs-lookup"><span data-stu-id="6d467-115">Set other signature properties as required.</span></span>

<span data-ttu-id="6d467-116">Im folgenden Codebeispiel wird veranschaulicht, wie einem XPS-Dokument eine Signatur Anforderung hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="6d467-116">The following code example illustrates how to add a signature request to an XPS document.</span></span>


```C++
HRESULT 
AddSignatureRequestToDocument (
    __in IXpsSignatureManager    *signatureManager,
    __in LPCWSTR                reasonForSignatureRequest,
    __in LPCWSTR                nameOfRequestedSigner,
    __in LPCWSTR                requestSignByDate
)
{
    HRESULT                  hr = S_OK;
    IXpsSignatureBlock       *signatureDefinition = NULL;
    IXpsSignatureRequest     *signatureRequest = NULL;
    
    // Create a new signature block and get a pointer to it
    hr = signatureManager->AddSignatureBlock (NULL, 0, &signatureDefinition);
    
    if (SUCCEEDED(hr)) {
        // Create a new signature request to use for this signature block
        hr = signatureDefinition->CreateRequest(NULL, &signatureRequest);
    }

    if (SUCCEEDED(hr)) {
        // Initialize the properties of the signature request

        //  Set the string that describes the purpose of the signature
        //  to the person who will sign the document.
        hr = signatureRequest->SetIntent(reasonForSignatureRequest);
    }

    if (SUCCEEDED(hr)) {
        //  Set the name of the person whose signature is requested.
        hr = signatureRequest->SetRequestedSigner(nameOfRequestedSigner);
    }

    if (SUCCEEDED(hr)) {
        //  Set the date that the person should sign the document.
        //  The person is requested to sign the document on or before
        //   the date specified in this field. Refer to the help text
        //   for the correct format of this string.
        hr = signatureRequest->SetRequestSignByDate(requestSignByDate);
    }

    if (NULL != signatureDefinition) signatureDefinition->Release();
    if (NULL != signatureRequest) signatureRequest->Release();

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="6d467-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6d467-117">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="6d467-118">**In diesem Abschnitt verwendet**</span><span class="sxs-lookup"><span data-stu-id="6d467-118">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="6d467-119">**Ixpssignatureblock**</span><span class="sxs-lookup"><span data-stu-id="6d467-119">**IXpsSignatureBlock**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock)
</dt> <dt>

[<span data-ttu-id="6d467-120">**Ixpssignatureblock:: samaterequest**</span><span class="sxs-lookup"><span data-stu-id="6d467-120">**IXpsSignatureBlock::CreateRequest**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignatureblock-createrequest)
</dt> <dt>

[<span data-ttu-id="6d467-121">**Ixpssignaturemanager**</span><span class="sxs-lookup"><span data-stu-id="6d467-121">**IXpsSignatureManager**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)
</dt> <dt>

[<span data-ttu-id="6d467-122">**Ixpssignaturemanager:: addsignatureblock**</span><span class="sxs-lookup"><span data-stu-id="6d467-122">**IXpsSignatureManager::AddSignatureBlock**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-addsignatureblock)
</dt> <dt>

[<span data-ttu-id="6d467-123">**Ixpssignaturerequest**</span><span class="sxs-lookup"><span data-stu-id="6d467-123">**IXpsSignatureRequest**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest)
</dt> <dt>

[<span data-ttu-id="6d467-124">**Ixpssignaturerequest:: ssitintent**</span><span class="sxs-lookup"><span data-stu-id="6d467-124">**IXpsSignatureRequest::SetIntent**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-setintent)
</dt> <dt>

[<span data-ttu-id="6d467-125">**Ixpssignaturerequest:: Setup-questedsigner**</span><span class="sxs-lookup"><span data-stu-id="6d467-125">**IXpsSignatureRequest::SetRequestedSigner**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-setrequestedsigner)
</dt> <dt>

[<span data-ttu-id="6d467-126">**Ixpssignaturerequest:: Setup questsignbydate**</span><span class="sxs-lookup"><span data-stu-id="6d467-126">**IXpsSignatureRequest::SetRequestSignByDate**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-setrequestsignbydate)
</dt> <dt>

<span data-ttu-id="6d467-127">**Weitere Informationen**</span><span class="sxs-lookup"><span data-stu-id="6d467-127">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="6d467-128">XPS-Fehler bei der digitalen Signatur-API</span><span class="sxs-lookup"><span data-stu-id="6d467-128">XPS Digital Signature API Errors</span></span>](xps-digital-signatures-errors.md)
</dt> <dt>

[<span data-ttu-id="6d467-129">XPS-Dokument Fehler</span><span class="sxs-lookup"><span data-stu-id="6d467-129">XPS Document Errors</span></span>](xps-document-errors.md)
</dt> <dt>

[<span data-ttu-id="6d467-130">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="6d467-130">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 



