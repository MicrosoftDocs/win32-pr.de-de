---
title: Festlegen von Berechtigungen für untergeordnete Objekt Vorgänge
description: Berechtigungen, z. b. untergeordnete Elemente erstellen und untergeordnete Elemente löschen, können auch für Vorgänge für alle untergeordneten Objekte oder unter Objekte einer bestimmten Klasse erteilt oder verweigert werden.
ms.assetid: fe2f8939-7562-4c03-a7a9-3ac5fc3e81bb
ms.tgt_platform: multiple
keywords:
- Festlegen von Berechtigungen für untergeordnete Objekt Vorgänge
- Objekte AD, Child, Setting-Berechtigungen für untergeordnete Objekt Vorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d407e9b0db865c5df8d5dab53bd97f9f1afa1497
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104101419"
---
# <a name="setting-permissions-on-child-object-operations"></a><span data-ttu-id="46396-105">Festlegen von Berechtigungen für untergeordnete Objekt Vorgänge</span><span class="sxs-lookup"><span data-stu-id="46396-105">Setting Permissions on Child Object Operations</span></span>

<span data-ttu-id="46396-106">Berechtigungen, z. b. untergeordnete Elemente erstellen und untergeordnete Elemente löschen, können auch für Vorgänge für alle untergeordneten Objekte oder unter Objekte einer bestimmten Klasse erteilt oder verweigert werden.</span><span class="sxs-lookup"><span data-stu-id="46396-106">Permissions, such as Create Child and Delete Child, can also be granted or denied for operations on all subobjects or subobjects of a specific class.</span></span>

<span data-ttu-id="46396-107">Das folgende Verfahren kann verwendet werden, um Berechtigungen für einen bestimmten untergeordneten Typ festzulegen.</span><span class="sxs-lookup"><span data-stu-id="46396-107">The following procedure can be used to set permissions for a specific subobject type.</span></span>

<span data-ttu-id="46396-108">**So legen Sie Berechtigungen für einen bestimmten untergeordneten Typ fest**</span><span class="sxs-lookup"><span data-stu-id="46396-108">**To set permissions for a specific subobject type**</span></span>

1.  <span data-ttu-id="46396-109">Legen Sie die [**IADsAccessControlEntry. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) -Eigenschaft auf **ADS \_ AceType \_ Access \_ Allowed \_ Object** oder **ADS \_ AceType \_ Access \_ denied \_ Object** fest.</span><span class="sxs-lookup"><span data-stu-id="46396-109">Set the [**IADsAccessControlEntry.AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to **ADS\_ACETYPE\_ACCESS\_ALLOWED\_OBJECT** or **ADS\_ACETYPE\_ACCESS\_DENIED\_OBJECT**.</span></span>
2.  <span data-ttu-id="46396-110">Legen Sie die [**IADsAccessControlEntry. ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) -Eigenschaft auf die GUID für die Objektklasse fest.</span><span class="sxs-lookup"><span data-stu-id="46396-110">Set the [**IADsAccessControlEntry.ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to the GUID for object class.</span></span> <span data-ttu-id="46396-111">Dies ist die **schemaIdGUID** -Eigenschaft des classSchema-Objekts, das die Objektklasse definiert.</span><span class="sxs-lookup"><span data-stu-id="46396-111">This is the **schemaIDGUID** property of the classSchema object that defines the object class.</span></span> <span data-ttu-id="46396-112">Wenn die **ObjectType** -Eigenschaft **null** ist, gilt der ACE für ein untergeordnetes Element einer beliebigen Klasse.</span><span class="sxs-lookup"><span data-stu-id="46396-112">If the **ObjectType** property is **NULL**, the ACE applies to subobjects of any class.</span></span>
3.  <span data-ttu-id="46396-113">Legen Sie die [**IADsAccessControlEntry. Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) -Eigenschaft auf den **AD-Flag- \_ \_ \_ Objekttyp \_ vorhanden** fest.</span><span class="sxs-lookup"><span data-stu-id="46396-113">Set the [**IADsAccessControlEntry.Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to **ADS\_FLAG\_OBJECT\_TYPE\_PRESENT**.</span></span>

<span data-ttu-id="46396-114">Weitere Informationen und eine Vorgehensweise zum Erstellen eines ACE finden Sie unter [Festlegen von Zugriffsrechten für ein Objekt](setting-access-rights-on-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="46396-114">For more information and a procedure for creating an ACE, see [Setting Access Rights on an Object](setting-access-rights-on-an-object.md).</span></span>

<span data-ttu-id="46396-115">Weitere Informationen und ein Codebeispiel, das verwendet werden kann, um einen ACE festzulegen, der Vorgänge für untergeordnete Objekte steuert, finden Sie unter [Beispielcode für das Festlegen eines ACE für ein Verzeichnis Objekt](example-code-for-setting-an-ace-on-a-directory-object.md).</span><span class="sxs-lookup"><span data-stu-id="46396-115">For more information and a code example that can be used to set an ACE that controls child object operations, see [Example Code for Setting an ACE on a Directory Object](example-code-for-setting-an-ace-on-a-directory-object.md).</span></span>

 

 