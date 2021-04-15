---
title: Aktivierungs Sicherheit
description: Aktivierungs Sicherheit
ms.assetid: 0c13d473-a9f9-40b5-951b-731eab736fe6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e5b01b918666e911d96ed16528ba5045103f445
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474405"
---
# <a name="activation-security"></a><span data-ttu-id="99d9d-103">Aktivierungs Sicherheit</span><span class="sxs-lookup"><span data-stu-id="99d9d-103">Activation Security</span></span>

<span data-ttu-id="99d9d-104">Die Aktivierungs Sicherheit (auch als Start Sicherheit bezeichnet) unterstützt die Steuerung der Benutzer, die einen Server starten können.</span><span class="sxs-lookup"><span data-stu-id="99d9d-104">Activation security (also called launch security) helps control who can launch a server.</span></span> <span data-ttu-id="99d9d-105">Die Aktivierungs Sicherheit wird automatisch durch den Dienststeuerungs-Manager (Service Control Manager, SCM) eines bestimmten Computers angewendet.</span><span class="sxs-lookup"><span data-stu-id="99d9d-105">Activation security is automatically applied by the service control manager (SCM) of a particular computer.</span></span> <span data-ttu-id="99d9d-106">Beim Empfang einer Anforderung von einem Client zum Aktivieren eines Objekts (wie in [Hilfsfunktionen](instance-creation-helper-functions.md)für die Instanzerstellung beschrieben) überprüft der SCM die Anforderung auf die in der Registrierung gespeicherten Aktivierungs Sicherheitsinformationen.</span><span class="sxs-lookup"><span data-stu-id="99d9d-106">Upon receipt of a request from a client to activate an object (as described in [Instance Creation Helper Functions](instance-creation-helper-functions.md)), the SCM checks the request against activation-security information stored within its registry.</span></span> <span data-ttu-id="99d9d-107">(Die Aktivierungs Sicherheit wird auch für dieselben Computer Aktivierungen geprüft.)</span><span class="sxs-lookup"><span data-stu-id="99d9d-107">(Activation security is also checked for same-computer activations.)</span></span>

<span data-ttu-id="99d9d-108">Beim Bestimmen der Identität des Clients prüft die Aktivierung das Cloaking-Flag, das im Client- [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)-Befehl festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="99d9d-108">When determining the identity of the client, activation examines the cloaking flag set in the client's call to [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="99d9d-109">Wenn das Cloaking-Flag festgelegt ist (für dynamisches oder statisches Cloaking), wird das Thread Token verwendet, falls vorhanden, um die Identität des Clients zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="99d9d-109">If the cloaking flag is set (for either dynamic or static cloaking), the thread token is used, if present, to determine the identity of the client.</span></span> <span data-ttu-id="99d9d-110">Wenn kein Cloaking festgelegt ist, wird das Prozess Token anstelle des Thread Tokens verwendet.</span><span class="sxs-lookup"><span data-stu-id="99d9d-110">If no cloaking is set, the process token is used instead of the thread token.</span></span>

<span data-ttu-id="99d9d-111">Weitere Informationen zur Aktivierungs Sicherheit finden Sie unter [**coauthinfo**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) und [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo).</span><span class="sxs-lookup"><span data-stu-id="99d9d-111">For more information about activation security, see [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) and [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo).</span></span>

## <a name="related-topics"></a><span data-ttu-id="99d9d-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="99d9d-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99d9d-113">Sicherheit in com</span><span class="sxs-lookup"><span data-stu-id="99d9d-113">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 