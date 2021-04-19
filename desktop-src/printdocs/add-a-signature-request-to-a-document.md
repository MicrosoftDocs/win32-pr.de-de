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
# <a name="add-a-signature-request-to-an-xps-document"></a>Hinzufügen einer Signatur Anforderung zu einem XPS-Dokument

In diesem Thema wird beschrieben, wie einem XPS-Dokument eine Signatur Anforderung hinzugefügt wird. Bei einer Signatur Anforderung wird ein Benutzer aufgefordert, ein Dokument zu signieren, wenn er mit der Signatur Absicht einverstanden ist.

Bevor Sie die folgenden Codebeispiele in Ihrem Programm verwenden, lesen Sie den Haftungsausschluss in [Common Digital Signature Programming Tasks](basic-digital-signature-programming-tasks.md).

So fügen Sie einem XPS-Dokument eine Signatur Anforderung hinzu:

1.  Laden Sie das XPS-Dokument in einen Signatur-Manager, wie unter [Initialisieren des Signatur-Managers](initialize-the-signature-manager.md)beschrieben.
2.  Fügen Sie dem Signatur-Manager einen Signatur Block hinzu.
3.  Erstellen Sie eine Signatur Anforderung im neuen Signatur Block.
4.  Legen Sie die Eigenschaften der Signatur Anforderung fest:
    1.  Legen Sie die Signatur Absicht fest.
    2.  Legen Sie den Namen der Person fest, deren Signatur angefordert wird (der angeforderte Signatur Geber).
    3.  Legen Sie das Datum für die erforderliche Signatur fest.
    4.  Legen Sie andere Signatur Eigenschaften nach Bedarf fest.

Im folgenden Codebeispiel wird veranschaulicht, wie einem XPS-Dokument eine Signatur Anforderung hinzugefügt wird.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**In diesem Abschnitt verwendet**
</dt> <dt>

[**Ixpssignatureblock**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblock)
</dt> <dt>

[**Ixpssignatureblock:: samaterequest**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignatureblock-createrequest)
</dt> <dt>

[**Ixpssignaturemanager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)
</dt> <dt>

[**Ixpssignaturemanager:: addsignatureblock**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-addsignatureblock)
</dt> <dt>

[**Ixpssignaturerequest**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequest)
</dt> <dt>

[**Ixpssignaturerequest:: ssitintent**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-setintent)
</dt> <dt>

[**Ixpssignaturerequest:: Setup-questedsigner**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-setrequestedsigner)
</dt> <dt>

[**Ixpssignaturerequest:: Setup questsignbydate**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturerequest-setrequestsignbydate)
</dt> <dt>

**Weitere Informationen**
</dt> <dt>

[XPS-Fehler bei der digitalen Signatur-API](xps-digital-signatures-errors.md)
</dt> <dt>

[XPS-Dokument Fehler](xps-document-errors.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 



