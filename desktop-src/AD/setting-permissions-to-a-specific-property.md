---
title: Festlegen von Berechtigungen für eine bestimmte Eigenschaft
description: Berechtigungen können so festgelegt werden, dass Sie auf eine bestimmte Eigenschaft eines Objekts angewendet werden.
ms.assetid: 7bafba5a-a437-4777-98a0-f478b738a8ca
ms.tgt_platform: multiple
keywords:
- Festlegen von Berechtigungen für eine bestimmte Eigenschaften Anzeige
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99dbfc3dc682103166b41957a3f52206d84fe671
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104038729"
---
# <a name="setting-permissions-to-a-specific-property"></a><span data-ttu-id="eed48-104">Festlegen von Berechtigungen für eine bestimmte Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="eed48-104">Setting Permissions to a Specific Property</span></span>

<span data-ttu-id="eed48-105">Berechtigungen können so festgelegt werden, dass Sie auf eine bestimmte Eigenschaft eines Objekts angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="eed48-105">Permissions can be set to apply to a specific property of an object.</span></span>

<span data-ttu-id="eed48-106">**So legen Sie Berechtigungen fest, die für eine bestimmte Eigenschaft eines Objekts gelten**</span><span class="sxs-lookup"><span data-stu-id="eed48-106">**To set permissions that apply to a specific property of an object**</span></span>

1.  <span data-ttu-id="eed48-107">Legen Sie die Eigenschaft [**IADsAccessControlEntry. AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) auf **ADS \_ right \_ DS \_ Read \_ Prop** und/oder **ADS \_ right \_ DS \_ Write \_ Prop** fest.</span><span class="sxs-lookup"><span data-stu-id="eed48-107">Set the [**IADsAccessControlEntry.AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to **ADS\_RIGHT\_DS\_READ\_PROP** and/or **ADS\_RIGHT\_DS\_WRITE\_PROP**.</span></span>
2.  <span data-ttu-id="eed48-108">Legen Sie die [**IADsAccessControlEntry. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) -Eigenschaft auf **ADS \_ AceType \_ Access \_ Allowed \_ Object** oder **ADS \_ AceType \_ Access \_ denied \_ Object** fest.</span><span class="sxs-lookup"><span data-stu-id="eed48-108">Set the [**IADsAccessControlEntry.AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to **ADS\_ACETYPE\_ACCESS\_ALLOWED\_OBJECT** or **ADS\_ACETYPE\_ACCESS\_DENIED\_OBJECT**.</span></span>
3.  <span data-ttu-id="eed48-109">Legen Sie die [**IADsAccessControlEntry. ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) -Eigenschaft auf die **schemaIdGUID** der Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="eed48-109">Set the [**IADsAccessControlEntry.ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to the **schemaIDGUID** of the property.</span></span> <span data-ttu-id="eed48-110">Dies ist die **schemaIdGUID** des **attributeSchema** -Objekts, das die Eigenschaft im Schema definiert.</span><span class="sxs-lookup"><span data-stu-id="eed48-110">This is the **schemaIDGUID** of the **attributeSchema** object that defines the property in the schema.</span></span> <span data-ttu-id="eed48-111">Die GUID muss als Zeichenfolge der Form angegeben werden, die von der [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) -Funktion in der com-Bibliothek erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="eed48-111">The GUID must be specified as a string of the form produced by the [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) function in the COM library.</span></span>
4.  <span data-ttu-id="eed48-112">Legen Sie [**IADsAccessControlEntry. Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) auf **ADS-Flag- \_ \_ \_ Objekttyp \_ vorhanden** fest.</span><span class="sxs-lookup"><span data-stu-id="eed48-112">Set [**IADsAccessControlEntry.Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) to **ADS\_FLAG\_OBJECT\_TYPE\_PRESENT**.</span></span>

<span data-ttu-id="eed48-113">Weitere Informationen über die **schemaIdGUID** eines vordefinierten Attributs finden Sie unter [Active Directory Domain Services Reference](active-directory-domain-services-reference.md).</span><span class="sxs-lookup"><span data-stu-id="eed48-113">For more information about the **schemaIDGUID** of a predefined attribute, see [Active Directory Domain Services Reference](active-directory-domain-services-reference.md).</span></span>

<span data-ttu-id="eed48-114">Weitere Informationen und ein Codebeispiel, das zum Abrufen einer schemaIDGUID verwendet werden kann, finden Sie unter [Lesen von attributeSchema-und classSchema-Objekten](reading-attributeschema-and-classschema-objects.md).</span><span class="sxs-lookup"><span data-stu-id="eed48-114">For more information and a code example that can be used to retrieve a schemaIDGUID, see [Reading attributeSchema and classSchema Objects](reading-attributeschema-and-classschema-objects.md).</span></span>

<span data-ttu-id="eed48-115">Weitere Informationen zum Erstellen eines ACE finden Sie unter [Festlegen von Zugriffsrechten für ein Objekt](setting-access-rights-on-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="eed48-115">For more information about how to create an ACE, see [Setting Access Rights on an Object](setting-access-rights-on-an-object.md).</span></span>

<span data-ttu-id="eed48-116">Weitere Informationen und ein Codebeispiel, das verwendet werden kann, um einen Eigenschafts spezifischen ACE festzulegen, finden Sie unter [Beispielcode für das Festlegen eines ACE für ein Verzeichnis Objekt](example-code-for-setting-an-ace-on-a-directory-object.md).</span><span class="sxs-lookup"><span data-stu-id="eed48-116">For more information and a code example that can be used to set a property-specific ACE, see [Example Code for Setting an ACE on a Directory Object](example-code-for-setting-an-ace-on-a-directory-object.md).</span></span>

 

 