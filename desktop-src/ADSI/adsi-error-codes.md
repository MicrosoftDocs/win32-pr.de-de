---
title: ADSI-Fehler Codes
description: Alle ADSI-Fehlercodes werden als com HRESULT-Werte zurückgegeben.
ms.assetid: 573889e4-37af-4aca-afd7-ef06bcf8aa0d
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, Referenz, Fehlercodes
- Fehlercodes ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24d9383998429b2ec64dd16fbed0d0df314f0d72
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855363"
---
# <a name="adsi-error-codes"></a><span data-ttu-id="23524-105">ADSI-Fehler Codes</span><span class="sxs-lookup"><span data-stu-id="23524-105">ADSI Error Codes</span></span>

<span data-ttu-id="23524-106">Alle ADSI-Fehlercodes werden als com **HRESULT** -Werte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="23524-106">All ADSI error codes are returned as COM **HRESULT** values.</span></span> <span data-ttu-id="23524-107">Sie können in die folgenden vier Typen gruppiert werden:</span><span class="sxs-lookup"><span data-stu-id="23524-107">They can be grouped into the following four types:</span></span>

-   [<span data-ttu-id="23524-108">Generische com-Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="23524-108">Generic COM error codes</span></span>](generic-com-error-codes.md)
-   [<span data-ttu-id="23524-109">Generische ADSI-Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="23524-109">Generic ADSI error codes</span></span>](generic-adsi-error-codes.md)
-   [<span data-ttu-id="23524-110">Win32-Fehlercodes für ADSI</span><span class="sxs-lookup"><span data-stu-id="23524-110">Win32 error codes for ADSI</span></span>](win32-error-codes-for-adsi.md)
-   [<span data-ttu-id="23524-111">LDAP-Fehlercodes für ADSI</span><span class="sxs-lookup"><span data-stu-id="23524-111">LDAP error codes for ADSI</span></span>](ldap-error-codes-for-adsi.md)

<span data-ttu-id="23524-112">Außerdem bieten bestimmte Schnittstellen zusätzliche Fehlerinformationen, die als erweiterte ADSI-Fehlermeldungen bezeichnet werden, die mithilfe der [**adsgetlasterror**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetlasterror) -Funktion abgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="23524-112">In addition, certain interfaces provide additional error information, known as ADSI extended error messages, which can be obtained using the [**ADsGetLastError**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetlasterror) function.</span></span>

<span data-ttu-id="23524-113">Der C++- [Beispielcode](code-example-for-working-with-adsi-error-messages.md) in diesem Abschnitt zeigt, wie ADSI-Fehlermeldungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="23524-113">Finally, the C++ [example code](code-example-for-working-with-adsi-error-messages.md) shown in this section shows how to work ADSI error messages.</span></span>

 

 




