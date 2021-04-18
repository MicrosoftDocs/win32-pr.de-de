---
description: Im folgenden Codebeispiel wird die Verwendung des TAPI-Objekts zum Untersuchen der verfügbaren Telefonieressourcen für eine Adresse veranschaulicht, die einen angegebenen Satz von Medientyp Anforderungen verarbeiten kann. In diesem Beispiel sind Audiodaten und Videos die erforderlichen Medien.
ms.assetid: 8be40a87-931d-4cda-9ef7-f9c0489e0b7b
title: Adresse auswählen
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: da41059c38328ff00271e4fa561561eecf83e1cb
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/20/2021
ms.locfileid: "106365145"
---
# <a name="select-an-address"></a><span data-ttu-id="328da-104">Adresse auswählen</span><span class="sxs-lookup"><span data-stu-id="328da-104">Select an Address</span></span>

<span data-ttu-id="328da-105">Im folgenden Codebeispiel wird die Verwendung des TAPI-Objekts zum Untersuchen der verfügbaren Telefonieressourcen für eine Adresse veranschaulicht, die einen angegebenen Satz von Medientyp Anforderungen verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="328da-105">The following code example demonstrates use of the TAPI object to examine available telephony resources for an address that can handle a specified set of media type requirements.</span></span> <span data-ttu-id="328da-106">In diesem Beispiel sind Audiodaten und Videos die erforderlichen Medien.</span><span class="sxs-lookup"><span data-stu-id="328da-106">In this example, audio and video are the required media.</span></span>

<span data-ttu-id="328da-107">Bevor Sie dieses Codebeispiel verwenden, müssen Sie die Vorgänge in [Initialize TAPI](initialize-tapi.md)ausführen.</span><span class="sxs-lookup"><span data-stu-id="328da-107">Before using this code example, you must perform the operations in [Initialize TAPI](initialize-tapi.md).</span></span>

> [!NOTE]  
> <span data-ttu-id="328da-108">Dieses Beispiel enthält nicht die Fehlerüberprüfung und die Releases, die für Produktionscode geeignet sind.</span><span class="sxs-lookup"><span data-stu-id="328da-108">This example doesn't have the error checking and releases appropriate for production code.</span></span>

```cpp
// Declare the interfaces used to select an address.
IEnumAddress * pIEnumAddress;
ITAddress * pAddress;
ITMediaSupport * pMediaSupport;

// Use the TAPI object to enumerate available addresses.
hr = gpTapi->EnumerateAddresses( &pIEnumAddress );
// If (hr != S_OK) process the error here. 

// Locate an address that can support the media type the application needs.
while ( S_OK == pIEnumAddress->Next(1, &pAddress, NULL) )
{
    // Determine the media support.
    hr = pAddress->QueryInterface(
         IID_ITMediaSupport,
         (void **)&pMediaSupport
         );
    // If (hr != S_OK) process the error here. 

    // In this example, the required media type is already known.
    // The application can also use the address object to
    // enumerate the media supported, then choose from there.
    hr = pMediaSupport->QueryMediaType(
         TAPIMEDIATYPE_AUDIO|TAPIMEDIATYPE_VIDEO,
         &bSupport
         );
    // If (hr != S_OK) process the error here. 

    if (bSupport)
    {
        break;
    }
}
// pAddress is now a usable address.
```

## <a name="related-topics"></a><span data-ttu-id="328da-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="328da-109">Related topics</span></span>

[<span data-ttu-id="328da-110">Ittapi:: enumerateadressen</span><span class="sxs-lookup"><span data-stu-id="328da-110">ITTAPI::EnumerateAddresses</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-enumerateaddresses)

[<span data-ttu-id="328da-111">Itmediasupport</span><span class="sxs-lookup"><span data-stu-id="328da-111">ITMediaSupport</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport)

[<span data-ttu-id="328da-112">Tapimediatype- \_ Konstanten</span><span class="sxs-lookup"><span data-stu-id="328da-112">TAPIMEDIATYPE\_ Constants</span></span>](tapimediatype--constants.md)
