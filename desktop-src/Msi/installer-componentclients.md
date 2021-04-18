---
description: Die schreibgeschützte componentclients-Eigenschaft gibt ein stringlist-Objekt zurück, das den Satz von Clients einer angegebenen Komponente auflistet.
ms.assetid: 47553360-298f-4be8-819d-18f4df96667c
title: Installer. componentclients (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentClients
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 2241babae283f367a15c8f742b51af280ed1a3b1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371154"
---
# <a name="installercomponentclients-property"></a><span data-ttu-id="08e05-103">Installer. componentclients (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="08e05-103">Installer.ComponentClients property</span></span>

<span data-ttu-id="08e05-104">Die schreibgeschützte **componentclients** -Eigenschaft gibt ein [**stringlist**](stringlist-object.md) -Objekt zurück, das den Satz von Clients einer angegebenen Komponente auflistet.</span><span class="sxs-lookup"><span data-stu-id="08e05-104">The read-only **ComponentClients** property returns a [**StringList**](stringlist-object.md) object enumerating the set of clients of a specified component.</span></span>

<span data-ttu-id="08e05-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="08e05-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="08e05-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="08e05-106">Syntax</span></span>


```JScript
propVal = Installer.ComponentClients
```



## <a name="property-value"></a><span data-ttu-id="08e05-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="08e05-107">Property value</span></span>

<span data-ttu-id="08e05-108">Eine Zeichen folgen-GUID, die den Komponenten Code der Komponente darstellt.</span><span class="sxs-lookup"><span data-stu-id="08e05-108">A string GUID that represents the component code of the component.</span></span> <span data-ttu-id="08e05-109">Die Komponenten Codes werden in der ComponentID-Spalte der [Component-Tabelle](component-table.md)angegeben.</span><span class="sxs-lookup"><span data-stu-id="08e05-109">The component codes are specified in the ComponentId column of the [Component table](component-table.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="08e05-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="08e05-110">Remarks</span></span>

<span data-ttu-id="08e05-111">Um die Komponenten Clients aufzulisten, kann eine Anwendung das [**stringlist**](stringlist-object.md) -Objekt durchlaufen, indem ein-Objekt für jedes Konstrukt verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="08e05-111">To enumerate the component clients, an application may iterate through the [**StringList**](stringlist-object.md) object using a For Each construct.</span></span> <span data-ttu-id="08e05-112">Da Clients nicht geordnet sind, haben alle neuen Komponenten einen beliebigen Index.</span><span class="sxs-lookup"><span data-stu-id="08e05-112">Because clients are not ordered, any new components has an arbitrary index.</span></span> <span data-ttu-id="08e05-113">Dies bedeutet, dass die Funktion Clients in beliebiger Reihenfolge zurückgeben kann.</span><span class="sxs-lookup"><span data-stu-id="08e05-113">This means that the function may return clients in any order.</span></span>

## <a name="requirements"></a><span data-ttu-id="08e05-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="08e05-114">Requirements</span></span>



| <span data-ttu-id="08e05-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="08e05-115">Requirement</span></span> | <span data-ttu-id="08e05-116">Wert</span><span class="sxs-lookup"><span data-stu-id="08e05-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08e05-117">Version</span><span class="sxs-lookup"><span data-stu-id="08e05-117">Version</span></span><br/> | <span data-ttu-id="08e05-118">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="08e05-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="08e05-119">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="08e05-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="08e05-120">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="08e05-120">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="08e05-121">DLL</span><span class="sxs-lookup"><span data-stu-id="08e05-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="08e05-122"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08e05-122"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="08e05-123">IID</span><span class="sxs-lookup"><span data-stu-id="08e05-123">IID</span></span><br/>     | <span data-ttu-id="08e05-124">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="08e05-124">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="08e05-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="08e05-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08e05-126">**Msienumschlag Clients**</span><span class="sxs-lookup"><span data-stu-id="08e05-126">**MsiEnumClients**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumclientsa)
</dt> </dl>

 

 




