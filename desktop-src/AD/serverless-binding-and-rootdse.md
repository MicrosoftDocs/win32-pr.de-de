---
title: Server lose Bindung und RootDSE
description: Wenn möglich, sollten Sie einen Servernamen nicht hart codieren.
ms.assetid: 24cfd8ce-18e6-42f1-8bc5-2c6dee82d133
ms.tgt_platform: multiple
keywords:
- Server lose Bindung und RootDSE-AD
- Server lose Bindungs Anzeige
- RootDSE-AD
- Active Directory, verwenden, Bindung, Server lose Bindung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 492a1ed115c4b0d9160305eb54b08c24db86abb8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104472484"
---
# <a name="serverless-binding-and-rootdse"></a><span data-ttu-id="43b82-107">Server lose Bindung und RootDSE</span><span class="sxs-lookup"><span data-stu-id="43b82-107">Serverless Binding and RootDSE</span></span>

<span data-ttu-id="43b82-108">Wenn möglich, sollten Sie einen Servernamen nicht hart codieren.</span><span class="sxs-lookup"><span data-stu-id="43b82-108">If possible, do not hard-code a server name.</span></span> <span data-ttu-id="43b82-109">Außerdem sollte die Bindung unter den meisten Umständen nicht unnötig an einen einzelnen Server gebunden werden.</span><span class="sxs-lookup"><span data-stu-id="43b82-109">Furthermore, under most circumstances, binding should not be unnecessarily tied to a single server.</span></span> <span data-ttu-id="43b82-110">Active Directory Domain Services unterstützen die Server lose Bindung, was bedeutet, dass Active Directory an die Standard Domäne gebunden werden kann, ohne den Namen eines Domänen Controllers anzugeben.</span><span class="sxs-lookup"><span data-stu-id="43b82-110">Active Directory Domain Services support serverless binding, which means that Active Directory can be bound to on the default domain without specifying the name of a domain controller.</span></span> <span data-ttu-id="43b82-111">Für normale Anwendungen ist dies in der Regel die Domäne des angemeldeten Benutzers.</span><span class="sxs-lookup"><span data-stu-id="43b82-111">For ordinary applications, this is typically the domain of the logged-on user.</span></span> <span data-ttu-id="43b82-112">Bei Dienst Anwendungen ist dies entweder die Domäne des Dienst Anmelde Kontos oder die des Clients, dessen Identität der Dienst annimmt.</span><span class="sxs-lookup"><span data-stu-id="43b82-112">For service applications, this is either the domain of the service logon account or that of the client that the service impersonates.</span></span>

<span data-ttu-id="43b82-113">In LDAP 3,0 ist RootDSE als Stammverzeichnis der Verzeichnis Datenstruktur auf einem Verzeichnisserver definiert.</span><span class="sxs-lookup"><span data-stu-id="43b82-113">In LDAP 3.0, rootDSE is defined as the root of the directory data tree on a directory server.</span></span> <span data-ttu-id="43b82-114">RootDSE ist nicht Teil eines Namespace.</span><span class="sxs-lookup"><span data-stu-id="43b82-114">The rootDSE is not part of any namespace.</span></span> <span data-ttu-id="43b82-115">Der Zweck von RootDSE besteht darin, Daten zum Verzeichnisserver bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="43b82-115">The purpose of the rootDSE is to provide data about the directory server.</span></span> <span data-ttu-id="43b82-116">Im folgenden finden Sie die Bindungs Zeichenfolge, die verwendet wird, um eine Bindung an RootDSE herzustellen.</span><span class="sxs-lookup"><span data-stu-id="43b82-116">The following is the binding string that is used to bind to rootDSE.</span></span>


```C++
LDAP://<servername>/rootDSE
```



<span data-ttu-id="43b82-117">Der <servername> ist der DNS-Name eines Servers.</span><span class="sxs-lookup"><span data-stu-id="43b82-117">The <servername> is the DNS name of a server.</span></span> <span data-ttu-id="43b82-118">Der <servername> ist optional, wie im folgenden Format dargestellt.</span><span class="sxs-lookup"><span data-stu-id="43b82-118">The <servername> is optional, as shown in the following format.</span></span>


```C++
LDAP://rootDSE
```



<span data-ttu-id="43b82-119">In diesem Fall wird ein Standard Domänen Controller aus der Domäne verwendet, in der der Sicherheitskontext des aufrufenden Threads verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="43b82-119">In this case, a default domain controller from the domain that the security context of the calling thread is in will be used.</span></span> <span data-ttu-id="43b82-120">Wenn innerhalb des Standorts nicht auf einen Domänen Controller zugegriffen werden kann, wird der erste Domänen Controller verwendet, der gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="43b82-120">If a domain controller cannot be accessed within the site, the first domain controller that can be found will be used.</span></span>

<span data-ttu-id="43b82-121">RootDSE ist ein bekannter und zuverlässiger Speicherort auf jedem Verzeichnisserver, um Distinguished Names der Domäne, des Schemas und der Konfigurations Container sowie anderer Daten zum Server und zum Inhalt der Verzeichnis Datenstruktur zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="43b82-121">The rootDSE is a well-known and reliable location on every directory server to get distinguished names of the domain, schema, and configuration containers, and other data about the server and the contents of its directory data tree.</span></span> <span data-ttu-id="43b82-122">Diese Eigenschaften ändern sich nur selten auf einem bestimmten Server.</span><span class="sxs-lookup"><span data-stu-id="43b82-122">These properties rarely change on a particular server.</span></span> <span data-ttu-id="43b82-123">Eine Anwendung kann diese Eigenschaften beim Start Lesen und in der gesamten Sitzung verwenden.</span><span class="sxs-lookup"><span data-stu-id="43b82-123">An application can read these properties at startup and use them throughout the session.</span></span>

<span data-ttu-id="43b82-124">Zusammenfassend sollte eine Anwendung eine Server lose Bindung verwenden, um Sie an das Verzeichnis in der aktuellen Domäne zu binden, mithilfe von RootDSE den Distinguished Name für einen Namespace zu erhalten und den Distinguished Name für die Bindung an Objekte im Namespace zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="43b82-124">In summary, an application should use serverless binding to bind to the directory on the current domain, use rootDSE to get the distinguished name for a namespace, and use that distinguished name to bind to objects in the namespace.</span></span>

<span data-ttu-id="43b82-125">Weitere Informationen zu Attributen, die von RootDSE unterstützt werden, finden Sie in der Active Directory-Schema Dokumentation unter [rootDSE](/windows/desktop/ADSchema/rootdse) .</span><span class="sxs-lookup"><span data-stu-id="43b82-125">For more information about attributes supported by rootDSE, see [RootDSE](/windows/desktop/ADSchema/rootdse) in the Active Directory Schema documentation.</span></span>

<span data-ttu-id="43b82-126">Weitere Informationen und ein Codebeispiel, in dem gezeigt wird, wie Sie die Server lose Bindung und RootDSE verwenden, finden Sie unter [Beispielcode zum Ermitteln des Distinguished Name der Domäne](example-code-for-getting-the-distinguished-name-of-the-domain.md).</span><span class="sxs-lookup"><span data-stu-id="43b82-126">For more information and a code example that shows how to use serverless binding and rootDSE, see [Example Code for Getting the Distinguished Name of the Domain](example-code-for-getting-the-distinguished-name-of-the-domain.md).</span></span>

 

 