---
title: RootDSE (ADSI)
description: Jeder Verzeichnisserver verfügt über einen eindeutigen Eintrag mit dem Namen RootDSE. Es werden Daten zum Server bereitstellt, z. b. die Funktionen, die unterstützte LDAP-Version und die verwendeten Namenskontexte.
ms.assetid: bb6b7676-7042-453f-83f9-b0dd2e377a13
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f241f2b8bb08248c0579c5c23d461b8c0acf1e01
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730241"
---
# <a name="rootdse-adsi"></a><span data-ttu-id="d944d-104">RootDSE (ADSI)</span><span class="sxs-lookup"><span data-stu-id="d944d-104">RootDSE (ADSI)</span></span>

<span data-ttu-id="d944d-105">Jeder Verzeichnisserver verfügt über einen eindeutigen Eintrag mit dem Namen **rootDSE**.</span><span class="sxs-lookup"><span data-stu-id="d944d-105">Each directory server has a unique entry called **RootDSE**.</span></span> <span data-ttu-id="d944d-106">Es werden Daten zum Server bereitstellt, z. b. die Funktionen, die unterstützte LDAP-Version und die verwendeten Namenskontexte.</span><span class="sxs-lookup"><span data-stu-id="d944d-106">It provides data about the server, such as its capabilities, the LDAP version it supports, and the naming contexts it uses.</span></span>

<span data-ttu-id="d944d-107">Beispielsweise zum Erstellen eines Skripts oder einer Anwendung, das in einer beliebigen Windows-Domänen Umgebung ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="d944d-107">For example, to create a script, or application, that can run on any Windows domain environment.</span></span> <span data-ttu-id="d944d-108">Beim Herstellen einer Verbindung mit Active Directory können Sie entweder den Distinguished Name, den Servernamen oder den Domänen Namen angeben.</span><span class="sxs-lookup"><span data-stu-id="d944d-108">You can specify either the distinguished name, server name, or domain name when connecting to Active Directory.</span></span> <span data-ttu-id="d944d-109">Wenn Sie nicht über diese Informationen verfügen, können Sie das **rootDSE** -Objekt verwenden, um eine Verbindung herzustellen.</span><span class="sxs-lookup"><span data-stu-id="d944d-109">If you do not have this information, you can then use the **RootDSE** object to establish a connection.</span></span> <span data-ttu-id="d944d-110">Im folgenden Codebeispiel wird die Domänen Beschreibung in einer beliebigen Domäne geändert.</span><span class="sxs-lookup"><span data-stu-id="d944d-110">The following code example changes the domain description in any domain.</span></span>


```VB
Set rootDSE = GetObject("LDAP://RootDSE")
Set dom = GetObject( "LDAP://" & rootDSE.Get("defaultNamingContext"))
dom.Put "description", "My domain"
dom.SetInfo
```



<span data-ttu-id="d944d-111">Wenn Sie das **defaultNamingContext** -Attribut von **rootDSE** erhalten, können Sie eine Bindung an die aktuelle Domäne durchführen, z. b. ist der Fabrikam **defaultNamingContext** DC = fabrikam, DC = com.</span><span class="sxs-lookup"><span data-stu-id="d944d-111">By getting the **defaultNamingContext** attribute from **RootDSE**, you can bind to the current domain, for example, the Fabrikam **defaultNamingContext** is DC=Fabrikam, DC=COM.</span></span>

<span data-ttu-id="d944d-112">Um die Eigenschaften von **rootDSE** aufzulisten, verwenden Sie die [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d944d-112">To enumerate the properties of the **RootDSE**, use the [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) interface.</span></span> <span data-ttu-id="d944d-113">[**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) kann für diesen Task nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d944d-113">[**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) cannot be used for this task.</span></span>

<span data-ttu-id="d944d-114">Weitere Informationen finden Sie unter [Server lose Bindung und RootDSE](/windows/desktop/AD/serverless-binding-and-rootdse).</span><span class="sxs-lookup"><span data-stu-id="d944d-114">For more information, see [Serverless Binding and RootDSE](/windows/desktop/AD/serverless-binding-and-rootdse).</span></span>

 

 