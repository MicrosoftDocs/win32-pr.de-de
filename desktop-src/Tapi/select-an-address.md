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
# <a name="select-an-address"></a>Adresse auswählen

Im folgenden Codebeispiel wird die Verwendung des TAPI-Objekts zum Untersuchen der verfügbaren Telefonieressourcen für eine Adresse veranschaulicht, die einen angegebenen Satz von Medientyp Anforderungen verarbeiten kann. In diesem Beispiel sind Audiodaten und Videos die erforderlichen Medien.

Bevor Sie dieses Codebeispiel verwenden, müssen Sie die Vorgänge in [Initialize TAPI](initialize-tapi.md)ausführen.

> [!NOTE]  
> Dieses Beispiel enthält nicht die Fehlerüberprüfung und die Releases, die für Produktionscode geeignet sind.

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

## <a name="related-topics"></a>Zugehörige Themen

[Ittapi:: enumerateadressen](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-enumerateaddresses)

[Itmediasupport](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport)

[Tapimediatype- \_ Konstanten](tapimediatype--constants.md)
