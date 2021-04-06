---
title: Herstellen einer Verbindung mit Active Directory
description: Für den Zugriff auf Active Directory werden mehrere Methoden verwendet.
ms.assetid: ef5720ff-6c66-466c-967e-f9c72a7bc0fa
ms.tgt_platform: multiple
keywords:
- Herstellen einer Verbindung mit Active Directory ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7626f01b644a0bb1a3acb39c5ef5ead70434e21e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947353"
---
# <a name="connecting-to-active-directory"></a><span data-ttu-id="b1162-104">Herstellen einer Verbindung mit Active Directory</span><span class="sxs-lookup"><span data-stu-id="b1162-104">Connecting to Active Directory</span></span>

<span data-ttu-id="b1162-105">Für den Zugriff auf Active Directory werden mehrere Methoden verwendet.</span><span class="sxs-lookup"><span data-stu-id="b1162-105">There are several methods used to access Active Directory.</span></span> <span data-ttu-id="b1162-106">Es wird empfohlen, dass Sie die ADSI-API verwenden, um auf Active Directory zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="b1162-106">It is recommended that you use the ADSI API to access Active Directory.</span></span> <span data-ttu-id="b1162-107">ADSI implementiert das LDAP-Protokoll für die Kommunikation mit Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b1162-107">ADSI implements the LDAP protocol to communicate with Active Directory.</span></span> <span data-ttu-id="b1162-108">In den folgenden Codebeispielen wird gezeigt, wie Sie auf Active Directory zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="b1162-108">The following code examples show how to access Active Directory.</span></span>


```VB
Set ns = GetObject("LDAP:")
```



<span data-ttu-id="b1162-109">Dadurch wird der LDAP-Anbieter geöffnet und zum Abrufen von Daten vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="b1162-109">This opens the LDAP provider and prepares it to retrieve data.</span></span> <span data-ttu-id="b1162-110">Es wird keine Verbindung hergestellt, bis Daten angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="b1162-110">No connection is established until data is requested.</span></span> <span data-ttu-id="b1162-111">Wenn Daten angefordert werden, versucht ADSI mithilfe des Serverlocatorpunkt-Dienstanbieter, den besten Domänen Controller (DC) für die Verbindung zu finden und stellt eine Verbindung mit dem Server her.</span><span class="sxs-lookup"><span data-stu-id="b1162-111">When data is requested, ADSI, with the help of the locator service, attempts to find the best domain controller (DC) for the connection and will establish a connection to the server.</span></span> <span data-ttu-id="b1162-112">Dieser Prozess wird als Server lose Bindung bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="b1162-112">This process is known as serverless binding.</span></span>

<span data-ttu-id="b1162-113">Mit ADSI können Sie auch den Servernamen angeben, der für die Verbindung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b1162-113">ADSI also enables you to specify the server name to use for the connection.</span></span>


```VB
Set obj = GetObject("LDAP://mysrv01")
```



<span data-ttu-id="b1162-114">In einem anderen Szenario kennen Sie möglicherweise nur den Domänen Namen, jedoch nicht den Namen des jeweiligen Servers.</span><span class="sxs-lookup"><span data-stu-id="b1162-114">In another scenario, you may only know the domain name but not the specific server name.</span></span> <span data-ttu-id="b1162-115">Auch hier können Sie mit ADSI den Domänen Namen angeben.</span><span class="sxs-lookup"><span data-stu-id="b1162-115">Again, ADSI enables you to specify the domain name.</span></span> <span data-ttu-id="b1162-116">In Windows 2000 wird der Domänen Name als DNS-Name dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b1162-116">In Windows 2000, the domain name is represented as a DNS name.</span></span> <span data-ttu-id="b1162-117">Wenn beispielsweise Joe de, der Netzwerkadministrator, eine Verbindung mit dem Domänen Namen herstellt, könnte er das folgende Codebeispiel verwenden.</span><span class="sxs-lookup"><span data-stu-id="b1162-117">For example, if Joe Worden, the network administrator, chooses to connect using the domain name, he could use the following code example.</span></span>


```VB
Set obj = GetObject("LDAP://fabrikam.com")
```



<span data-ttu-id="b1162-118">ADSI stellt eine Verbindung mit einem der Domänen Controller in der Fabrikam.com-Domäne her.</span><span class="sxs-lookup"><span data-stu-id="b1162-118">ADSI will connect to one of the domain controllers in the fabrikam.com domain.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b1162-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b1162-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1162-120">Binden an Active Directory Objekte</span><span class="sxs-lookup"><span data-stu-id="b1162-120">Binding to Active Directory Objects</span></span>](binding-to-active-directory-objects.md)
</dt> </dl>

 

 




