---
description: Die authzfreecentralaccesspolicycallback-Funktion ist eine Anwendungs definierte Funktion, die von der authzgetcentralaccesspolicycallback-Funktion zugeordnete Arbeitsspeicher freigibt.
ms.assetid: F0859A67-4D20-4189-8F35-A78034E41E6A
title: Authzfreecentralaccesspolicycallback-Rückruffunktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthzFreeCentralAccessPolicyCallback
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: d2139c9fa106b6070a3c043d417bdbf23379084b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218834"
---
# <a name="authzfreecentralaccesspolicycallback-callback-function"></a><span data-ttu-id="1fbc7-103">Authzfreecentralaccesspolicycallback-Rückruffunktion</span><span class="sxs-lookup"><span data-stu-id="1fbc7-103">AuthzFreeCentralAccessPolicyCallback callback function</span></span>

<span data-ttu-id="1fbc7-104">Die *authzfreecentralaccesspolicycallback* -Funktion ist eine Anwendungs definierte Funktion, die von der [*authzgetcentralaccesspolicycallback*](authzgetcentralaccesspolicycallback-.md) -Funktion zugeordnete Arbeitsspeicher freigibt.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-104">The *AuthzFreeCentralAccessPolicyCallback* function is an application-defined function that frees memory allocated by the [*AuthzGetCentralAccessPolicyCallback*](authzgetcentralaccesspolicycallback-.md) function.</span></span> <span data-ttu-id="1fbc7-105">*Authzfreecentralaccesspolicycallback* ist ein Platzhalter für den Namen der Anwendungs definierten Funktion.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-105">*AuthzFreeCentralAccessPolicyCallback* is a placeholder for the application-defined function name.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fbc7-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1fbc7-106">Syntax</span></span>


```C++
BOOL CALLBACK AuthzFreeCentralAccessPolicyCallback(
  _In_ PVOID pCentralAccessPolicy
);
```



## <a name="parameters"></a><span data-ttu-id="1fbc7-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="1fbc7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fbc7-108">*pcentralaccesspolicy* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1fbc7-108">*pCentralAccessPolicy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fbc7-109">Ein Zeiger auf die zentrale Zugriffs Richtlinie, die freigegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-109">Pointer to the central access policy to be freed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fbc7-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1fbc7-110">Return value</span></span>

<span data-ttu-id="1fbc7-111">Wenn die Funktion erfolgreich ausgeführt wird, gibt die Funktion **true** zurück.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-111">If the function succeeds, the function returns **TRUE**.</span></span>

<span data-ttu-id="1fbc7-112">Wenn die Funktion die Auswertung nicht ausführen kann, wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-112">If the function is unable to perform the evaluation, it returns **FALSE**.</span></span> <span data-ttu-id="1fbc7-113">Verwenden Sie [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) , um einen Fehler an die Access Check-Funktion zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="1fbc7-113">Use [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) to return an error to the access check function.</span></span>

## <a name="see-also"></a><span data-ttu-id="1fbc7-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1fbc7-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fbc7-115">**Authz- \_ Init- \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="1fbc7-115">**AUTHZ\_INIT\_INFO**</span></span>](/windows/desktop/api/Authz/ns-authz-authz_init_info)
</dt> <dt>

[<span data-ttu-id="1fbc7-116">*Authzgetcentralaccesspolicycallback*</span><span class="sxs-lookup"><span data-stu-id="1fbc7-116">*AuthzGetCentralAccessPolicyCallback*</span></span>](authzgetcentralaccesspolicycallback-.md)
</dt> </dl>

 

 
