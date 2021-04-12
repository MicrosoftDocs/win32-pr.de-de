---
description: Listet die Schritte auf, die zum Initialisieren eines Sicherheitspakets erforderlich sind, und erläutert diese.
ms.assetid: 60c11519-f7ca-4002-b3f6-d74f50310730
title: Initialisieren des Sicherheitspakets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bed981c7a209c8f76be9e58f970d84b0aa184371
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131181"
---
# <a name="initializing-the-security-package"></a><span data-ttu-id="905dc-103">Initialisieren des Sicherheitspakets</span><span class="sxs-lookup"><span data-stu-id="905dc-103">Initializing the Security Package</span></span>

<span data-ttu-id="905dc-104">Diese Schritte sind vor der Verwendung von SSPI erforderlich:</span><span class="sxs-lookup"><span data-stu-id="905dc-104">These steps are necessary before using SSPI:</span></span>

1.  <span data-ttu-id="905dc-105">Die Initialisierungsfunktion muss aufgerufen werden, um die Adresse der Sicherheits Funktions Tabelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="905dc-105">The initialization function must be called to obtain the address of the security function table.</span></span>

    <span data-ttu-id="905dc-106">Der Client und der Server aufrufen [**initsecurityinterface**](/windows/desktop/api/Sspi/nf-sspi-initsecurityinterfacea) für einen Zeiger auf eine [**securityfunctiontable**](/windows/win32/api/sspi/ns-sspi-securityfunctiontablea) Dispatch-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="905dc-106">The client and server call [**InitSecurityInterface**](/windows/desktop/api/Sspi/nf-sspi-initsecurityinterfacea) for a pointer to a [**SecurityFunctionTable**](/windows/win32/api/sspi/ns-sspi-securityfunctiontablea) dispatch table.</span></span> <span data-ttu-id="905dc-107">Diese Tabelle enthält Zeiger auf Rückruf Funktionen, die in SSPI. h deklariert werden.</span><span class="sxs-lookup"><span data-stu-id="905dc-107">This table contains pointers to callback functions declared in Sspi.h.</span></span> <span data-ttu-id="905dc-108">Diese Zeiger ermöglichen den Zugriff auf die dll-Implementierungen der verschiedenen SSPI-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="905dc-108">These pointers provide access to the DLL's implementations of the various SSPI functions.</span></span>

2.  <span data-ttu-id="905dc-109">Informationen zu den unterstützten Sicherheitspaketen finden Sie hier.</span><span class="sxs-lookup"><span data-stu-id="905dc-109">Information must be obtained about the supported security packages.</span></span>

    <span data-ttu-id="905dc-110">Wenngleich die meisten Anwendungen Sicherheitspakete verwenden, die standardmäßige oder allgemeine Funktionen unterstützen, können Sicherheitspakete über einzigartige Funktionen für die Anwendung verfügen.</span><span class="sxs-lookup"><span data-stu-id="905dc-110">While most applications use security packages that support default or common capabilities, security packages can have unique capabilities of interest to the application.</span></span> <span data-ttu-id="905dc-111">Eine Anwendung, die besondere Funktionen benötigt, kann ein Paket verwenden, das diese Funktionen bietet.</span><span class="sxs-lookup"><span data-stu-id="905dc-111">An application needing special capabilities can use a package that offers those capabilities.</span></span> <span data-ttu-id="905dc-112">Weitere Informationen finden Sie unter [Informationen zu Sicherheitspaketen](getting-information-about-security-packages.md).</span><span class="sxs-lookup"><span data-stu-id="905dc-112">For more information, see [Getting Information About Security Packages](getting-information-about-security-packages.md).</span></span>

<span data-ttu-id="905dc-113">An diesem Punkt hat die Anwendung einen SSP erfolgreich initialisiert und ein Sicherheitspaket mit ausreichenden Funktionen ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="905dc-113">At this point, the application has successfully initialized an SSP and chosen a security package with sufficient capabilities.</span></span>

<span data-ttu-id="905dc-114">Das [*Aushandlungs*](../secgloss/n-gly.md) Paket kann verwendet werden, wenn eine Vereinbarung zwischen Client und Server verwendet wird, um zu erfahren, welches [*Sicherheitspaket*](../secgloss/s-gly.md) verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="905dc-114">The [*Negotiate*](../secgloss/n-gly.md) package can be used where agreement between client and server about which [*security package*](../secgloss/s-gly.md) to use is done behind the scenes.</span></span> <span data-ttu-id="905dc-115">Wenn das Aushandlungs Paket nicht verwendet wird, müssen der Client und der Server dem spezifischen Sicherheitspaket zustimmen, das verwendet werden soll, bevor die obigen Setup Schritte ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="905dc-115">If the Negotiate package is not used, the client and server must agree on the specific security package to use before performing the setup steps above.</span></span>

 

 
