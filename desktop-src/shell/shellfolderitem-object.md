---
description: Erweitert das FolderItem-Objekt. Zusätzlich zu den Eigenschaften und Methoden, die von FolderItem unterstützt werden, verfügt ShellFolderItem über zwei zusätzliche Methoden.
title: ShellFolderItem-Objekt (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderItem
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 0e2f4c91-f9f9-4daa-a801-9c7fea8af738
ms.openlocfilehash: a9e6d6b3f954f0c8ee4b13fb651a9ea04274deb6
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840771"
---
# <a name="shellfolderitem-object"></a><span data-ttu-id="f68fd-104">ShellFolderItem-Objekt</span><span class="sxs-lookup"><span data-stu-id="f68fd-104">ShellFolderItem object</span></span>

<span data-ttu-id="f68fd-105">Erweitert das [**FolderItem-Objekt.**](folderitem.md)</span><span class="sxs-lookup"><span data-stu-id="f68fd-105">Extends the [**FolderItem**](folderitem.md) object.</span></span> <span data-ttu-id="f68fd-106">Zusätzlich zu den Eigenschaften und Methoden, die von **FolderItem** unterstützt werden, verfügt **ShellFolderItem** über zwei zusätzliche Methoden.</span><span class="sxs-lookup"><span data-stu-id="f68fd-106">In addition to the properties and methods supported by **FolderItem**, **ShellFolderItem** has two additional methods.</span></span>

## <a name="members"></a><span data-ttu-id="f68fd-107">Member</span><span class="sxs-lookup"><span data-stu-id="f68fd-107">Members</span></span>

<span data-ttu-id="f68fd-108">Das **ShellFolderItem-Objekt** verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="f68fd-108">The **ShellFolderItem** object has these types of members:</span></span>

-   [<span data-ttu-id="f68fd-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="f68fd-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f68fd-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="f68fd-110">Methods</span></span>

<span data-ttu-id="f68fd-111">Das **ShellFolderItem-Objekt** verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="f68fd-111">The **ShellFolderItem** object has these methods.</span></span>



| <span data-ttu-id="f68fd-112">Methode</span><span class="sxs-lookup"><span data-stu-id="f68fd-112">Method</span></span>                                                       | <span data-ttu-id="f68fd-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f68fd-113">Description</span></span>                                                                                                                                                                                         |
|:-------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f68fd-114">**Extendedproperty**</span><span class="sxs-lookup"><span data-stu-id="f68fd-114">**ExtendedProperty**</span></span>](shellfolderitem-extendedproperty.md) | <span data-ttu-id="f68fd-115">Ruft den Wert einer Eigenschaft aus dem Eigenschaftensatz eines Elements ab.</span><span class="sxs-lookup"><span data-stu-id="f68fd-115">Gets the value of a property from an item's property set.</span></span> <span data-ttu-id="f68fd-116">Die Eigenschaft kann entweder anhand des Namens oder des Formatbezeichners (FMTID) und des Eigenschaftenbezeichners (PID) des Eigenschaftensatzes angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f68fd-116">The property can be specified either by name or by the property set's format identifier (FMTID) and property identifier (PID).</span></span><br/> |
| [<span data-ttu-id="f68fd-117">**InvokeVerbEx**</span><span class="sxs-lookup"><span data-stu-id="f68fd-117">**InvokeVerbEx**</span></span>](invokeverbex.md)                         | <span data-ttu-id="f68fd-118">Führt ein Verb für ein Shellelement aus.</span><span class="sxs-lookup"><span data-stu-id="f68fd-118">Executes a verb on a Shell item.</span></span><br/>                                                                                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="f68fd-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f68fd-119">Requirements</span></span>



| <span data-ttu-id="f68fd-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f68fd-120">Requirement</span></span> | <span data-ttu-id="f68fd-121">Wert</span><span class="sxs-lookup"><span data-stu-id="f68fd-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f68fd-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f68fd-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f68fd-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f68fd-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f68fd-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f68fd-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f68fd-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f68fd-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="f68fd-126">Header</span><span class="sxs-lookup"><span data-stu-id="f68fd-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f68fd-127"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="f68fd-127"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="f68fd-128">Idl</span><span class="sxs-lookup"><span data-stu-id="f68fd-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f68fd-129"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="f68fd-129"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="f68fd-130">DLL</span><span class="sxs-lookup"><span data-stu-id="f68fd-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f68fd-131"><dt>Shell32.dll (Version 5.0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="f68fd-131"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




