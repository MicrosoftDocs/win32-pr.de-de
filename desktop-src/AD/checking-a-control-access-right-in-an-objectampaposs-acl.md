---
title: Überprüfen des Zugriffs auf das Steuerungs Recht in der ACL eines Objekts
description: Verwenden Sie die accesscheckbytyperesultlist-Funktion, um ein Zugriffsrecht für das Steuerelement auf der ACL eines Objekts zu überprüfen.
ms.assetid: 5a609622-6a1a-46ae-a336-afec504225c7
ms.tgt_platform: multiple
keywords:
- Überprüfen des Zugriffs auf das Zugriffsrecht in einer Objekt-ACL-Werbung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10170bd496da14657356a2334015975da1cc02ff
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104038797"
---
# <a name="checking-a-control-access-right-in-an-objects-acl"></a><span data-ttu-id="8c577-104">Überprüfen des Zugriffs auf das Steuerungs Recht in der ACL eines Objekts</span><span class="sxs-lookup"><span data-stu-id="8c577-104">Checking a Control Access Right in an Object's ACL</span></span>

<span data-ttu-id="8c577-105">Verwenden Sie die [**accesscheckbytyperesultlist**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) -Funktion, um ein Zugriffsrecht für das Steuerelement auf der ACL eines Objekts zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="8c577-105">To check a control access right on an object's ACL, use the [**AccessCheckByTypeResultList**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) function.</span></span> <span data-ttu-id="8c577-106">Um diese Funktion verwenden zu können, benötigt eine Anwendung einen Zeiger auf die [**Sicherheits \_ Beschreibung**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) für das-Objekt anstelle einer [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) -Schnittstelle auf ein COM-Objekt des ADSI-Sicherheits Deskriptors.</span><span class="sxs-lookup"><span data-stu-id="8c577-106">To use this function, an application requires a pointer to the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) for the object instead of an [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) interface to an ADSI security descriptor COM object.</span></span>

<span data-ttu-id="8c577-107">Führen Sie die folgenden Schritte aus, um den Zugriff auf ein kontrolliertes Zugriffsrecht für ein Objekt zu überprüfen:</span><span class="sxs-lookup"><span data-stu-id="8c577-107">Use the following steps to check access for an controlled access right on an object:</span></span>

1.  <span data-ttu-id="8c577-108">Einen [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) -Schnittstellen Zeiger auf das-Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8c577-108">Get an [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) interface pointer to the object.</span></span>
2.  <span data-ttu-id="8c577-109">Verwenden Sie die [**IDirectoryObject:: getobjectattributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-getobjectattributes) -Methode, um die Sicherheits Beschreibung des-Objekts zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8c577-109">Use the [**IDirectoryObject::GetObjectAttributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-getobjectattributes) method to get the security descriptor of the object.</span></span> <span data-ttu-id="8c577-110">Der Name der Eigenschaft, die die Sicherheits Beschreibung enthält, ist [**ntSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor).</span><span class="sxs-lookup"><span data-stu-id="8c577-110">The name of the property containing the security descriptor is [**nTSecurityDescriptor**](/windows/desktop/ADSchema/a-ntsecuritydescriptor).</span></span> <span data-ttu-id="8c577-111">Die-Eigenschaft wird als Zeiger auf eine [**Sicherheits \_ deskriptorstruktur**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8c577-111">The property is returned as a pointer to a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure.</span></span>
3.  <span data-ttu-id="8c577-112">Verwenden Sie die [**Sicherheits \_ deskriptorstruktur**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) mit der [**accesscheckbytyperesultlist**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) -Funktion, um die Berechtigungen für das angegebene Zugriffsrecht für den angegebenen Client zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="8c577-112">Use the [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure with the [**AccessCheckByTypeResultList**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) function to check the permissions for the specified control access right for the specified client.</span></span>

<span data-ttu-id="8c577-113">Der Beispielcode im [Beispielcode zum Überprüfen eines Steuerungs Zugriffsrechts in der ACL eines Objekts](example-code-for-checking-a-control-access-right-in-an-objectampaposs-acl.md) zeigt im Detail, wie dies geschieht.</span><span class="sxs-lookup"><span data-stu-id="8c577-113">The example code in [Example Code for Checking a Control Access Right in an Object's ACL](example-code-for-checking-a-control-access-right-in-an-objectampaposs-acl.md) shows, in detail, how to do this.</span></span>

 

 