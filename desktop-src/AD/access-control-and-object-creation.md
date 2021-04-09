---
title: Access Control und Objekt Erstellung
description: Der Active Directory Server kann ein untergeordnetes Objekt nicht erstellen, wenn der Aufrufer nicht über die ADS \_ right \_ DS \_ Create \_ Child für diesen Objekttyp für den übergeordneten Container verfügt.
ms.assetid: 52f56e2a-580c-44b5-ba97-21388f6258bc
ms.tgt_platform: multiple
keywords:
- AD-Access Control und Objekt Erstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71ac54c1fe71a1821d3a02db383ca95606ae360d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104101399"
---
# <a name="access-control-and-object-creation"></a><span data-ttu-id="8153d-104">Access Control und Objekt Erstellung</span><span class="sxs-lookup"><span data-stu-id="8153d-104">Access Control and Object Creation</span></span>

<span data-ttu-id="8153d-105">Der Active Directory Server kann ein untergeordnetes Objekt nicht erstellen, wenn der Aufrufer nicht über die **ADS \_ right \_ DS \_ Create \_ Child** für diesen Objekttyp für den übergeordneten Container verfügt.</span><span class="sxs-lookup"><span data-stu-id="8153d-105">The Active Directory server will fail to create a child object if the caller does not have the **ADS\_RIGHT\_DS\_CREATE\_CHILD** for that object type on the parent container.</span></span> <span data-ttu-id="8153d-106">Um die Typen von untergeordneten Objekten zu bestimmen, die der Aufrufer in einem Verzeichnis Objekt erstellen kann, lesen Sie das Attribut " **attribuwedchildclasseseffective** " des Objekts.</span><span class="sxs-lookup"><span data-stu-id="8153d-106">To determine the types of child objects that the caller can create in a directory object, read the object's **allowedChildClassesEffective** attribute.</span></span>

<span data-ttu-id="8153d-107">Wenn Sie die [**IADsContainer:: Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) -Methode zum Erstellen eines untergeordneten Objekts verwenden, wird das Objekt erst dann persistent gemacht, wenn [**IADs:: SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) für das neue Objekt aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="8153d-107">When you use the [**IADsContainer::Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) method to create a child object, the object is not made persistent until [**IADs::SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) is called on the new object.</span></span> <span data-ttu-id="8153d-108">Zwischen den **Create** -und **SetInfo** -aufrufen kann der Erstellungs Thread Werte in die Eigenschaften des neuen Objekts einfügen.</span><span class="sxs-lookup"><span data-stu-id="8153d-108">Between the **Create** and **SetInfo** calls, the creating thread can put values into any of the new object's properties.</span></span> <span data-ttu-id="8153d-109">Nachdem der **SetInfo-Befehl** aufgerufen wurde, verfügt der erstellende Thread nicht unbedingt über die Zugriffsrechte, um die Eigenschaften des neuen Objekts festzulegen.</span><span class="sxs-lookup"><span data-stu-id="8153d-109">After the **SetInfo** call, the creating thread does not necessarily have the access rights to set the new object's properties.</span></span> <span data-ttu-id="8153d-110">Um sicherzustellen, dass der Aufrufer über diese Rechte verfügt, müssen Sie während der Erstellung eine explizite Sicherheits Beschreibung angeben.</span><span class="sxs-lookup"><span data-stu-id="8153d-110">To ensure that the caller has these rights, specify an explicit security descriptor during creation.</span></span> <span data-ttu-id="8153d-111">Die DACL sollte über einen ACE verfügen, der dem Aufrufer die erforderlichen Zugriffsrechte für das Objekt übergibt.</span><span class="sxs-lookup"><span data-stu-id="8153d-111">The DACL should have an ACE that gives the caller the necessary access rights on the object.</span></span>

<span data-ttu-id="8153d-112">Weitere Informationen zur Zugriffs Steuerung und Objekt Erstellung finden Sie unter [Festlegen von Sicherheits Deskriptoren für neue Verzeichnisobjekte](how-security-descriptors-are-set-on-new-directory-objects.md).</span><span class="sxs-lookup"><span data-stu-id="8153d-112">For more information about access control and object creation, see [How Security Descriptors are Set on New Directory Objects](how-security-descriptors-are-set-on-new-directory-objects.md).</span></span>

 

 