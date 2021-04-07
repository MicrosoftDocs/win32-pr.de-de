---
title: Lesen von defaultSecurityDescriptor für eine Objektklasse
description: Mithilfe von ADSI können Sie das defaultSecurityDescriptor-Attribut für eine Objektklasse mit der IADs-Schnittstelle abrufen.
ms.assetid: 12d1e77a-bd70-4c64-9b4f-ac5caaf5fe40
ms.tgt_platform: multiple
keywords:
- Active Directory Beispiele Active Directory, Lesen von defaultSecurityDescriptor für eine Objektklasse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e217ae42214c2c07867c2a57427d74fb7636736
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104038738"
---
# <a name="reading-the-defaultsecuritydescriptor-for-an-object-class"></a><span data-ttu-id="d499c-104">Lesen von defaultSecurityDescriptor für eine Objektklasse</span><span class="sxs-lookup"><span data-stu-id="d499c-104">Reading the defaultSecurityDescriptor for an Object Class</span></span>

<span data-ttu-id="d499c-105">Mithilfe von ADSI können Sie das **defaultSecurityDescriptor** -Attribut für eine Objektklasse mit der [**IADs**](/windows/desktop/api/iads/nn-iads-iads) -Schnittstelle abrufen.</span><span class="sxs-lookup"><span data-stu-id="d499c-105">Using ADSI, you can obtain the **defaultSecurityDescriptor** attribute for an object class with the [**IADs**](/windows/desktop/api/iads/nn-iads-iads) interface.</span></span> <span data-ttu-id="d499c-106">Um das **defaultSecurityDescriptor** -Attribut für eine Objektklasse zu erhalten, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="d499c-106">To obtain the **defaultSecurityDescriptor** attribute for an object class, perform the following steps.</span></span>

1.  <span data-ttu-id="d499c-107">Einen [**IADs**](/windows/desktop/api/iads/nn-iads-iads) -Schnittstellen Zeiger auf das **classSchema** -Objekt für die Objektklasse erhalten.</span><span class="sxs-lookup"><span data-stu-id="d499c-107">Get an [**IADs**](/windows/desktop/api/iads/nn-iads-iads) interface pointer to the **classSchema** object for the object class.</span></span>
2.  <span data-ttu-id="d499c-108">Verwenden Sie die [**IADs. Get**](/windows/desktop/api/iads/nf-iads-iads-get) -Methode, um die Standard Sicherheits Beschreibung des-Objekts zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d499c-108">Use the [**IADs.Get**](/windows/desktop/api/iads/nf-iads-iads-get) method to get the default security descriptor of the object.</span></span> <span data-ttu-id="d499c-109">Der Name der Eigenschaft, die die Sicherheits Beschreibung enthält, ist "defaultSecurityDescriptor".</span><span class="sxs-lookup"><span data-stu-id="d499c-109">The name of the property that contains the security descriptor is "defaultSecurityDescriptor".</span></span> <span data-ttu-id="d499c-110">Die-Eigenschaft wird als [**Variante**](/windows/win32/api/oaidl/ns-oaidl-variant) zurückgegeben, die ein BSTR mit der Standard Sicherheits Beschreibung im SDDL-Zeichen folgen Format enthält.</span><span class="sxs-lookup"><span data-stu-id="d499c-110">The property will be returned as a [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) containing a BSTR with the default security descriptor in SDDL string format.</span></span>
3.  <span data-ttu-id="d499c-111">Verwenden Sie die [**convertstringsecuritydescriptortosecuritydescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) -Funktion, um die SDDL-Zeichen folgen Form in eine Sicherheits Beschreibung zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="d499c-111">Use the [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) function to convert the SDDL string form to a security descriptor.</span></span>
4.  <span data-ttu-id="d499c-112">Verwenden Sie die Sicherheits-APIs [**GetSecurityDescriptorDacl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl), [**getsecuritydescriptorsacl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl), [**GetSecurityDescriptorOwner**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorowner)und [**getsecuritydescriptorcontrol**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) , um die Teile der Sicherheits Beschreibung zu lesen.</span><span class="sxs-lookup"><span data-stu-id="d499c-112">Use the [**GetSecurityDescriptorDacl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl), [**GetSecurityDescriptorSacl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl), [**GetSecurityDescriptorOwner**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorowner), and [**GetSecurityDescriptorControl**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) Security APIs to read the parts of the security descriptor.</span></span>

<span data-ttu-id="d499c-113">Ein Codebeispiel, in dem veranschaulicht wird, wie Sie dies tun, finden Sie unter [Beispielcode zum Lesen von defaultSecurityDescriptor](example-code-for-reading-defaultsecuritydescriptor.md).</span><span class="sxs-lookup"><span data-stu-id="d499c-113">For a code example that demonstrates how to do this, see [Example Code for Reading defaultSecurityDescriptor](example-code-for-reading-defaultsecuritydescriptor.md).</span></span>

 

 