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
# <a name="initialize-the-signature-manager"></a><span data-ttu-id="af103-103">Initialisieren des Signatur-Managers</span><span class="sxs-lookup"><span data-stu-id="af103-103">Initialize the Signature Manager</span></span>

<span data-ttu-id="af103-104">In diesem Thema wird beschrieben, wie der Signatur-Manager für die Verwendung mit einem XPS-Dokument initialisiert wird.</span><span class="sxs-lookup"><span data-stu-id="af103-104">This topic describes how to initialize the signature manager for use with an XPS document.</span></span>

<span data-ttu-id="af103-105">Bevor Sie die folgenden Codebeispiele in Ihrem Programm verwenden, lesen Sie den Haftungsausschluss in [Common Digital Signature Programming Tasks](basic-digital-signature-programming-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="af103-105">Before using the following code examples in your program, read the disclaimer in [Common Digital Signature Programming Tasks](basic-digital-signature-programming-tasks.md).</span></span>

<span data-ttu-id="af103-106">Um die Windows 7-Funktionen der kryptografieapi zu verwenden, definieren Sie das Symbol " **crypt \_ OID \_ Info \_ has \_ extra \_ Fields** " wie folgt:</span><span class="sxs-lookup"><span data-stu-id="af103-106">To use the Windows 7 features of the Crypto API, define the **CRYPT\_OID\_INFO\_HAS\_EXTRA\_FIELDS** symbol as follows:</span></span>


```C++
#define CRYPT_OID_INFO_HAS_EXTRA_FIELDS
```



<span data-ttu-id="af103-107">Als nächstes instanziieren Sie eine [**ixpssignaturemanager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) -Schnittstelle, indem Sie [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)aufrufen, wie im folgenden Codebeispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="af103-107">Next, instantiate an [**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) interface by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance), as shown in the following code example.</span></span>


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



<span data-ttu-id="af103-108">Die von [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) instanziierte Schnittstelle kann nur von einem XPS-Dokument verwendet werden, das durch den Aufruf von [**loadpackagefile**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagefile) oder [**loadpackagestream**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagestream) geladen werden muss, bevor eine andere Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="af103-108">The interface instantiated by [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) can be used by only one XPS document, which must be loaded by calling [**LoadPackageFile**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagefile) or [**LoadPackageStream**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-loadpackagestream) before calling any other method.</span></span>

<span data-ttu-id="af103-109">Nachdem die [**ixpssignaturemanager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) -Schnittstelle instanziiert und ein XPS-Dokument geladen wurde, kann der Signatur-Manager verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="af103-109">After the [**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager) interface has been instantiated and an XPS document has been loaded, the signature manager is ready for use.</span></span>

## <a name="related-topics"></a><span data-ttu-id="af103-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="af103-110">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="af103-111">**Next Steps**</span><span class="sxs-lookup"><span data-stu-id="af103-111">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="af103-112">Signieren eines Dokuments</span><span class="sxs-lookup"><span data-stu-id="af103-112">Sign a Document</span></span>](sign-a-document.md)
</dt> <dt>

[<span data-ttu-id="af103-113">Hinzufügen einer Signatur Anforderung zu einem XPS-Dokument</span><span class="sxs-lookup"><span data-stu-id="af103-113">Add a Signature Request to an XPS Document</span></span>](add-a-signature-request-to-a-document.md)
</dt> <dt>

[<span data-ttu-id="af103-114">Überprüfen von Dokument Signaturen</span><span class="sxs-lookup"><span data-stu-id="af103-114">Verify Document Signatures</span></span>](verify-document-signatures.md)
</dt> <dt>

<span data-ttu-id="af103-115">**In diesem Abschnitt verwendet**</span><span class="sxs-lookup"><span data-stu-id="af103-115">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="af103-116">**CoCreateInstance**</span><span class="sxs-lookup"><span data-stu-id="af103-116">**CoCreateInstance**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

[<span data-ttu-id="af103-117">**Ixpssignaturemanager**</span><span class="sxs-lookup"><span data-stu-id="af103-117">**IXpsSignatureManager**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)
</dt> <dt>

<span data-ttu-id="af103-118">**Weitere Informationen**</span><span class="sxs-lookup"><span data-stu-id="af103-118">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="af103-119">XPS-Fehler bei der digitalen Signatur-API</span><span class="sxs-lookup"><span data-stu-id="af103-119">XPS Digital Signature API Errors</span></span>](xps-digital-signatures-errors.md)
</dt> <dt>

[<span data-ttu-id="af103-120">XPS-Dokument Fehler</span><span class="sxs-lookup"><span data-stu-id="af103-120">XPS Document Errors</span></span>](xps-document-errors.md)
</dt> <dt>

[<span data-ttu-id="af103-121">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="af103-121">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
