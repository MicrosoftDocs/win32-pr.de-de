---
description: Mit der Identity Manager-API können Sie eine Peer Identität erstellen, die in einem Peer Netzwerk verwendet werden kann.
ms.assetid: 44b85bbc-9594-4f68-b930-51a28422b571
title: Erstellen einer Peer Identität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ab240b9fa1265ba03bfb1ce584dabed92988620
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959789"
---
# <a name="creating-a-peer-identity"></a><span data-ttu-id="4bf98-103">Erstellen einer Peer Identität</span><span class="sxs-lookup"><span data-stu-id="4bf98-103">Creating a Peer Identity</span></span>

<span data-ttu-id="4bf98-104">Mit der Identity Manager-API können Sie eine Peer Identität erstellen, die in einem Peer Netzwerk verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="4bf98-104">The Identity Manager API allows you to create a peer identity to use in a peer network.</span></span>

<span data-ttu-id="4bf98-105">Wenn Sie eine Peer Identität erstellen, können Sie die folgenden optionalen Informationen bereitstellen:</span><span class="sxs-lookup"><span data-stu-id="4bf98-105">When you create a peer identity, you can provide the following optional information:</span></span>

-   [<span data-ttu-id="4bf98-106">Klassifizierung</span><span class="sxs-lookup"><span data-stu-id="4bf98-106">Classifier</span></span>](peer-names.md)
-   <span data-ttu-id="4bf98-107">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="4bf98-107">Friendly name</span></span>
-   <span data-ttu-id="4bf98-108">Kryptografiedienstanbieter</span><span class="sxs-lookup"><span data-stu-id="4bf98-108">Cryptographic service provider</span></span>

> [!Note]  
> <span data-ttu-id="4bf98-109">Verwenden Sie nach Möglichkeit eine Peer Identität erneut.</span><span class="sxs-lookup"><span data-stu-id="4bf98-109">Whenever possible, re-use a peer identity.</span></span>

 

## <a name="example-of-creating-and-deleting-a-peer-identity"></a><span data-ttu-id="4bf98-110">Beispiel für das Erstellen und Löschen einer Peer Identität</span><span class="sxs-lookup"><span data-stu-id="4bf98-110">Example of Creating and Deleting a Peer Identity</span></span>

<span data-ttu-id="4bf98-111">Der folgende Code Ausschnitt zeigt, wie Sie eine Peer Identität mit einem Klassifizierer und einem anzeigen Amen erstellen und löschen.</span><span class="sxs-lookup"><span data-stu-id="4bf98-111">The following code snippet shows you how to create and delete a peer identity by using a classifier and friendly name.</span></span>


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



 

 



