---
title: Festlegen von Rechten für bestimmte Objekttypen
description: Im folgenden Verfahren wird gezeigt, wie ein ACE festgelegt wird, der nur von einer bestimmten Objektklasse geerbt werden kann.
ms.assetid: 42712458-69c7-4fe1-bfb3-b3fb28092a56
ms.tgt_platform: multiple
keywords:
- Festlegen von Rechten auf Objekttypen
- Objekte AD, Festlegen von Rechten auf
- Active Directory, Verwendung von, Sicherheit, Festlegen von Rechten auf Objekttypen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6f44cfbe753e6f92787f8269eab1f4eab4c2e98
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103948544"
---
# <a name="setting-rights-to-specific-types-of-objects"></a><span data-ttu-id="397af-106">Festlegen von Rechten für bestimmte Objekttypen</span><span class="sxs-lookup"><span data-stu-id="397af-106">Setting Rights to Specific Types of Objects</span></span>

<span data-ttu-id="397af-107">Im folgenden Verfahren wird gezeigt, wie ein ACE festgelegt wird, der nur von einer bestimmten Objektklasse geerbt werden kann.</span><span class="sxs-lookup"><span data-stu-id="397af-107">The following procedure shows how to set an ACE that can be inherited only by a specific class of objects.</span></span>

 <span data-ttu-id="397af-108">**So legen Sie einen ACE fest, der nur von einer bestimmten Objektklasse geerbt werden kann**</span><span class="sxs-lookup"><span data-stu-id="397af-108">**To set an ACE that can be inherited only by a specific class of objects**</span></span>

1.  <span data-ttu-id="397af-109">Legen Sie die [**IADsAccessControlEntry. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) -Eigenschaft auf **ADS \_ AceType \_ Access \_ Allowed \_ Object** oder **ADS \_ AceType \_ Access \_ denied \_ Object** fest.</span><span class="sxs-lookup"><span data-stu-id="397af-109">Set the [**IADsAccessControlEntry.AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to **ADS\_ACETYPE\_ACCESS\_ALLOWED\_OBJECT** or **ADS\_ACETYPE\_ACCESS\_DENIED\_OBJECT**.</span></span>
2.  <span data-ttu-id="397af-110">Legen Sie die [**IADsAccessControlEntry. AceFlags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) -Eigenschaft so fest, dass Sie das \_ Flag ADS aceflag \_ erben-ACE einschließt \_ .</span><span class="sxs-lookup"><span data-stu-id="397af-110">Set the [**IADsAccessControlEntry.AceFlags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to include the ADS\_ACEFLAG\_INHERIT\_ACE flag.</span></span>
3.  <span data-ttu-id="397af-111">Legen Sie die [**IADsAccessControlEntry. eritedobjecttype**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) -Eigenschaft auf die **schemaIdGUID** der Objektklasse fest, die den ACE erben kann.</span><span class="sxs-lookup"><span data-stu-id="397af-111">Set the [**IADsAccessControlEntry.InheritedObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to the **schemaIDGUID** of the object class that can inherit the ACE.</span></span>
4.  <span data-ttu-id="397af-112">Legen Sie die [**IADsAccessControlEntry. Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) -Eigenschaft auf den angezeigten **\_ \_ \_ Objekttyp \_ ADS-Flag** fest.</span><span class="sxs-lookup"><span data-stu-id="397af-112">Set the [**IADsAccessControlEntry.Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to **ADS\_FLAG\_INHERITED OBJECT\_TYPE\_PRESENT**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="397af-113">Legen Sie fest, dass die ACE-Zugriffs Steuerungs Liste den ACE **\_ \_ erben \_** soll.</span><span class="sxs-lookup"><span data-stu-id="397af-113">Set **ADS\_ACEFLAG\_INHERIT\_ACE** to cause the ACE to be inherited.</span></span> <span data-ttu-id="397af-114">Außerdem müssen Sie **ADS \_ aceflag \_ \_ nur auf \_ ACE erben** , wenn der Objekttyp, für den dieser ACE gilt, nicht dem Objekttyp des Containers entspricht, in dem der ACE angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="397af-114">In addition, you must set **ADS\_ACEFLAG\_INHERIT\_ONLY\_ACE** if the object type this ACE applies to does not match the object type of the container where the ACE is specified.</span></span> <span data-ttu-id="397af-115">Wenn dies nicht der Fall ist, wird der ACE auch für den Container wirksam und kann unbeabsichtigte Rechte gewähren.</span><span class="sxs-lookup"><span data-stu-id="397af-115">If this is not done, the ACE will also become effective on the container and can grant unintended rights.</span></span>

 

<span data-ttu-id="397af-116">Weitere Informationen und Codebeispiele, die verwendet werden können, um diese Art von ACE festzulegen, finden Sie unter [Beispielcode für das Festlegen eines ACE für ein Verzeichnis Objekt](example-code-for-setting-an-ace-on-a-directory-object.md).</span><span class="sxs-lookup"><span data-stu-id="397af-116">For more information and code examples that can be used to set this type of ACE, see [Example Code for Setting an ACE on a Directory Object](example-code-for-setting-an-ace-on-a-directory-object.md).</span></span>

 

 