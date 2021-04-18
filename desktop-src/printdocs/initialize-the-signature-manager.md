---
description: In diesem Thema wird beschrieben, wie der Signatur-Manager für die Verwendung mit einem XPS-Dokument initialisiert wird.
ms.assetid: 4c4c6e8f-4ee0-4089-a283-1082baee5054
title: Initialisieren des Signatur-Managers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2796838a9cd041859f0eb47bf4aeafb2a8d5356
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351087"
---
# <a name="initialize-the-signature-manager"></a>Initialisieren des Signatur-Managers

In diesem Thema wird beschrieben, wie der Signatur-Manager für die Verwendung mit einem XPS-Dokument initialisiert wird.

Bevor Sie die folgenden Codebeispiele in Ihrem Programm verwenden, lesen Sie den Haftungsausschluss in [Common Digital Signature Programming Tasks](basic-digital-signature-programming-tasks.md).

Um die Windows 7-Funktionen der kryptografieapi zu verwenden, definieren Sie das Symbol " **crypt \_ OID \_ Info \_ has \_ extra \_ Fields** " wie folgt:


```C++
#define CRYPT_OID_INFO_HAS_EXTRA_FIELDS
```



Als nächstes instanziieren Sie eine [**ixpssignaturemanager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) -Schnittstelle, indem Sie [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)aufrufen, wie im folgenden Codebeispiel gezeigt.


```C++
IXpsSignatureManager    *newInterface;

// Note the implicit requirement that CoInitializeEx 
//  has previously been called from this thread.

hr = CoCreateInstance(
    __uuidof(XpsSignatureManager),
    NULL, 
    CLSCTX_INPROC_SERVER,
    __uuidof(IXpsSignatureManager),
    reinterpret_cast<LPVOID*>(&newInterface));

// make sure that you got a pointer 
// to the interface
if (SUCCEEDED(hr)) {
    // Load document into signature manager from file.
    //  xpsDocument is initialized with the file name
    //  of the document to load outside of this example.
    hr = newInterface->LoadPackageFile (xpsDocument);

    // Use newInterface

    // Release interface pointers when finished with them 
    newInterface->Release();
}    
```



Die von [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) instanziierte Schnittstelle kann nur von einem XPS-Dokument verwendet werden, das durch den Aufruf von [**loadpackagefile**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagefile) oder [**loadpackagestream**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagestream) geladen werden muss, bevor eine andere Methode aufgerufen wird.

Nachdem die [**ixpssignaturemanager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) -Schnittstelle instanziiert und ein XPS-Dokument geladen wurde, kann der Signatur-Manager verwendet werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Next Steps**
</dt> <dt>

[Signieren eines Dokuments](sign-a-document.md)
</dt> <dt>

[Hinzufügen einer Signatur Anforderung zu einem XPS-Dokument](add-a-signature-request-to-a-document.md)
</dt> <dt>

[Überprüfen von Dokument Signaturen](verify-document-signatures.md)
</dt> <dt>

**In diesem Abschnitt verwendet**
</dt> <dt>

[**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

[**Ixpssignaturemanager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)
</dt> <dt>

**Weitere Informationen**
</dt> <dt>

[XPS-Fehler bei der digitalen Signatur-API](xps-digital-signatures-errors.md)
</dt> <dt>

[XPS-Dokument Fehler](xps-document-errors.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
