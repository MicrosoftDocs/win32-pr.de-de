---
title: Credential Guard und Drittanbieter-apps
description: Credential Guard erlaubt Drittanbieter-SSPs nicht, Kennworthashes von LSA abzufragen.
ms.assetid: DA518005-C603-41CF-BBB9-2B46414653A5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a036ba5db5b86ab7c186b25e4d858b1badc60bd0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473140"
---
# <a name="third-party-security-support-providers-with-credential-guard"></a><span data-ttu-id="5e883-103">Security Support Provider von Drittanbietern mit Credential Guard</span><span class="sxs-lookup"><span data-stu-id="5e883-103">Third party Security Support Providers with Credential Guard</span></span>

<span data-ttu-id="5e883-104">Credential Guard erlaubt Drittanbieter-SSPs nicht, Kennworthashes von LSA abzufragen.</span><span class="sxs-lookup"><span data-stu-id="5e883-104">Credential Guard does not allow 3rd party SSPs to ask for password hashes from LSA.</span></span> <span data-ttu-id="5e883-105">SSPs und Zugriffspunkte werden aber weiterhin über das Kennwort informiert, wenn sich ein Benutzer anmeldet bzw. sein Kennwort ändert.</span><span class="sxs-lookup"><span data-stu-id="5e883-105">However, SSPs and APs still get notified of the password when a user logs on and/or changes their password.</span></span> <span data-ttu-id="5e883-106">Die Verwendung von undokumentierten APIs in benutzerdefinierten SSPs und Zugriffspunkten wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5e883-106">Any use of undocumented APIs within custom SSPs and APs are not supported.</span></span>

<span data-ttu-id="5e883-107">Da die Tiefe und der Umfang der Schutzmaßnahmen, die Credential Guard bereitstellt, erweitert werden, können nachfolgende Versionen von Windows 10 mit Credential Guard Szenarien beeinträchtigen, die in der Vergangenheit funktioniert haben.</span><span class="sxs-lookup"><span data-stu-id="5e883-107">As the depth and breadth of protections provided by Credential Guard are increased, subsequent releases of Windows 10 with Credential Guard running may impact scenarios that were working in the past.</span></span> <span data-ttu-id="5e883-108">Beispielsweise kann Anmelde Informationen Guard die Verwendung eines bestimmten Typs von Anmelde Informationen oder einer bestimmten Komponente blockieren, um zu verhindern, dass Schadsoftware von Sicherheitsrisiken ausgenutzt wird.</span><span class="sxs-lookup"><span data-stu-id="5e883-108">For example, Credential Guard may block the use of a particular type of credential or a particular component to prevent malware from taking advantage of vulnerabilities.</span></span> <span data-ttu-id="5e883-109">Daher sollten Sie Szenarien, die für Vorgänge in einer Organisation wichtig sind, vor dem Upgrade eines Geräts testen, auf dem Credential Guard ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5e883-109">Therefore, we recommend that scenarios required for operations in an organization are tested before upgrading a device that has Credential Guard running.</span></span>

<span data-ttu-id="5e883-110">Die vollständige Beschreibung und empfohlene entschärfungen finden Sie in [diesem Artikel](/windows/security/identity-protection/credential-guard/credential-guard) .</span><span class="sxs-lookup"><span data-stu-id="5e883-110">Please refer to [this article](/windows/security/identity-protection/credential-guard/credential-guard) for the full description and recommended mitigations.</span></span>

 

 