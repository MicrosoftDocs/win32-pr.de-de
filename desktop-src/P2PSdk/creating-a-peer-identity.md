---
description: Mit der Identity Manager-API können Sie eine Peeridentität für die Verwendung in einem Peernetzwerk erstellen.
ms.assetid: 44b85bbc-9594-4f68-b930-51a28422b571
title: Erstellen einer Peeridentität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7d7e2a1bfba386ede4bf3f10e8b009794c3e17676abc65d797d42e203f214f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887820"
---
# <a name="creating-a-peer-identity"></a>Erstellen einer Peeridentität

Mit der Identity Manager-API können Sie eine Peeridentität für die Verwendung in einem Peernetzwerk erstellen.

Wenn Sie eine Peeridentität erstellen, können Sie die folgenden optionalen Informationen bereitstellen:

-   [Klassifizierung](peer-names.md)
-   Anzeigename
-   Kryptografiedienstanbieter

> [!Note]  
> Verwenden Sie nach Möglichkeit eine Peeridentität erneut.

 

## <a name="example-of-creating-and-deleting-a-peer-identity"></a>Beispiel für das Erstellen und Löschen einer Peeridentität

Im folgenden Codeausschnitt wird veranschaulicht, wie Sie eine Peeridentität mithilfe eines Klassifizierers und eines Bezeichnernamens erstellen und löschen.


```C++
#define UNICODE
#include <p2p.h>
#include <stdio.h>

#pragma comment(lib, "p2p.lib")

//-----------------------------------------------------------------------------
// Function: CreateIdentity
//
// Purpose:  Creates a new Identity.
//
// Returns:  HRESULT
//
HRESULT CreateIdentity(PWSTR pwzFriendlyName)
{
    HRESULT     hr              = S_OK;   
    PWSTR       pwzClassifier   = L"GroupMember";
    PWSTR       pwzIdentity     = NULL;

    hr = PeerIdentityCreate(pwzClassifier, pwzFriendlyName, 0, &pwzIdentity);
    if (FAILED(hr))
    {            
        printf("Failed to create identity.");
    }
    else
    {
        printf("Identity: %s", pwzFriendlyName);
    }
       
    PeerFreeData(pwzIdentity);    

    return hr;
}


//-----------------------------------------------------------------------------
// Function: DeleteIdentity
//
// Purpose:  Delete the identity created by CreateIdentity
//
// Returns:  HRESULT
//
HRESULT DeleteIdentity()
{
    HRESULT hr = S_OK;

    if (g_pwzIdentity)
    {
        hr = PeerIdentityDelete(g_pwzIdentity);
        g_pwzIdentity = NULL;
    }

    return hr;
}
```



 

 



