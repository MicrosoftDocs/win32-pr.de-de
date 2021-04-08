---
title: Erkennen des Betriebsmodus einer Domäne
description: In Windows 2000 kann eine Domäne in zwei Betriebsmodi gemischt und System eigen ausgeführt werden.
ms.assetid: c20dec14-50ad-4f63-bd5c-222c2f2c83e4
ms.tgt_platform: multiple
keywords:
- Erkennen des Betriebsmodus einer Domänen Anzeige
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7d871bd50c9a7462972992685d4226963a3eaff
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103858156"
---
# <a name="detecting-the-operation-mode-of-a-domain"></a><span data-ttu-id="f6223-104">Erkennen des Betriebsmodus einer Domäne</span><span class="sxs-lookup"><span data-stu-id="f6223-104">Detecting the Operation Mode of a Domain</span></span>

<span data-ttu-id="f6223-105">In Windows 2000 kann eine Domäne in zwei Betriebsmodi ausgeführt werden: gemischt und System eigen.</span><span class="sxs-lookup"><span data-stu-id="f6223-105">In Windows 2000, a domain can run in two operation modes: mixed and native.</span></span> <span data-ttu-id="f6223-106">Der gemischte Modus sollte verwendet werden, um Domänen Controller unter Windows NT 4,0 in einer Windows 2000-Domäne einzubinden.</span><span class="sxs-lookup"><span data-stu-id="f6223-106">Mixed mode should be used to include domain controllers running Windows NT 4.0 in a Windows 2000 domain.</span></span> <span data-ttu-id="f6223-107">Der gemischte Modus unterstützt keine universellen Gruppen oder schsted Groups.</span><span class="sxs-lookup"><span data-stu-id="f6223-107">Mixed mode does not support universal groups or nested groups.</span></span> <span data-ttu-id="f6223-108">Wenn auf allen Domänen Controllern in der Domäne Windows 2000 ausgeführt wird, können Sie den einheitlichen Modus verwenden.</span><span class="sxs-lookup"><span data-stu-id="f6223-108">If all domain controllers in the domain are running Windows 2000, you can use native mode.</span></span>

<span data-ttu-id="f6223-109">Wenn Sie den Betriebsmodus einer Windows 2000-Domäne Programm gesteuert erkennen möchten, lesen Sie die [**nTMixedDomain**](/windows/desktop/ADSchema/a-ntmixeddomain) -Eigenschaft des [**domainDns**](/windows/desktop/ADSchema/c-domaindns) -Objekts für diese Domäne.</span><span class="sxs-lookup"><span data-stu-id="f6223-109">To programmatically detect the operation mode of a Windows 2000 domain, read the [**ntMixedDomain**](/windows/desktop/ADSchema/a-ntmixeddomain) property of the [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) object for that domain.</span></span> <span data-ttu-id="f6223-110">Der Wert 0 (null) bedeutet, dass sich die Domäne im einheitlichen Modus befindet.</span><span class="sxs-lookup"><span data-stu-id="f6223-110">A value of zero (0) means that the domain is in native mode.</span></span> <span data-ttu-id="f6223-111">Der Wert eins (1) gibt an, dass sich die Domäne im gemischten Modus befindet.</span><span class="sxs-lookup"><span data-stu-id="f6223-111">A value of one (1) indicates that the domain is in mixed mode.</span></span> <span data-ttu-id="f6223-112">Sie können auch die [**DsRoleGetPrimaryDomainInformation**](/windows/desktop/api/Dsrole/nf-dsrole-dsrolegetprimarydomaininformation) -Funktion verwenden, um den Betriebsmodus sowie andere Daten über die Domäne und ihren Status zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f6223-112">You can also use the [**DsRoleGetPrimaryDomainInformation**](/windows/desktop/api/Dsrole/nf-dsrole-dsrolegetprimarydomaininformation) function to get the operation mode as well as other data about the domain and its state.</span></span>

<span data-ttu-id="f6223-113">Verwenden Sie zum Binden an das [**domainDns**](/windows/desktop/ADSchema/c-domaindns) -Objekt der Domäne des Benutzerkontos, unter dem die Anwendung ausgeführt wird, die Server lose Bindung und RootDSE, um den Distinguished Name für die Domäne zu erhalten, und verwenden Sie dann den Distinguished Name, um eine Bindung an das **domainDns** -Objekt herzustellen, das diese Domäne darstellt.</span><span class="sxs-lookup"><span data-stu-id="f6223-113">To bind to the [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) object of the domain of the user account under which your application is running, use serverless binding and rootDSE to get the distinguished name for the domain and then use that distinguished name to bind to the **domainDNS** object that represents that domain.</span></span> <span data-ttu-id="f6223-114">Weitere Informationen zu Server losen Bindungen und RootDSE finden Sie unter [Server lose Bindung und RootDSE](serverless-binding-and-rootdse.md).</span><span class="sxs-lookup"><span data-stu-id="f6223-114">For more information about serverless binding and rootDSE, see [Serverless Binding and RootDSE](serverless-binding-and-rootdse.md).</span></span>

<span data-ttu-id="f6223-115">Weitere Informationen und ein Codebeispiel, das zeigt, wie der Betriebsmodus einer Domäne Programm gesteuert erkannt wird, finden Sie unter [Beispielcode zum Bestimmen des Betriebsmodus](example-code-for-determining-the-operation-mode.md).</span><span class="sxs-lookup"><span data-stu-id="f6223-115">For more information and a code example that shows how to programmatically detect the operation mode of a domain, see [Example Code for Determining the Operation Mode](example-code-for-determining-the-operation-mode.md).</span></span>

 

 