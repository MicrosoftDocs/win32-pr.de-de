---
description: Erweitert das folderItem-Objekt. Zusätzlich zu den Eigenschaften und Methoden, die von folderItem unterstützt werden, verfügt shellfolderitem über zwei zusätzliche Methoden.
title: Shellfolderitem-Objekt (Shldisp. h)
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
ms.openlocfilehash: 84e230e295a956f3f83833a577b47be1e46873a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980433"
---
# <a name="shellfolderitem-object"></a><span data-ttu-id="d3e32-104">Shellfolderitem-Objekt</span><span class="sxs-lookup"><span data-stu-id="d3e32-104">ShellFolderItem object</span></span>

<span data-ttu-id="d3e32-105">Erweitert das [**folderItem**](folderitem.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="d3e32-105">Extends the [**FolderItem**](folderitem.md) object.</span></span> <span data-ttu-id="d3e32-106">Zusätzlich zu den Eigenschaften und Methoden, die von **folderItem** unterstützt werden, verfügt **shellfolderitem** über zwei zusätzliche Methoden.</span><span class="sxs-lookup"><span data-stu-id="d3e32-106">In addition to the properties and methods supported by **FolderItem**, **ShellFolderItem** has two additional methods.</span></span>

## <a name="members"></a><span data-ttu-id="d3e32-107">Member</span><span class="sxs-lookup"><span data-stu-id="d3e32-107">Members</span></span>

<span data-ttu-id="d3e32-108">Das **shellfolderitem** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="d3e32-108">The **ShellFolderItem** object has these types of members:</span></span>

-   [<span data-ttu-id="d3e32-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="d3e32-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d3e32-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="d3e32-110">Methods</span></span>

<span data-ttu-id="d3e32-111">Das **shellfolderitem** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="d3e32-111">The **ShellFolderItem** object has these methods.</span></span>



| <span data-ttu-id="d3e32-112">Methode</span><span class="sxs-lookup"><span data-stu-id="d3e32-112">Method</span></span>                                                       | <span data-ttu-id="d3e32-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d3e32-113">Description</span></span>                                                                                                                                                                                         |
|:-------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d3e32-114">**ExtendedProperty**</span><span class="sxs-lookup"><span data-stu-id="d3e32-114">**ExtendedProperty**</span></span>](shellfolderitem-extendedproperty.md) | <span data-ttu-id="d3e32-115">Ruft den Wert einer Eigenschaft aus dem Eigenschaften Satz eines Elements ab.</span><span class="sxs-lookup"><span data-stu-id="d3e32-115">Gets the value of a property from an item's property set.</span></span> <span data-ttu-id="d3e32-116">Die-Eigenschaft kann entweder anhand des Namens oder anhand des Format Bezeichners (fmtid) und des Eigenschafts Bezeichners (PID) des Eigenschaften Satzes angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d3e32-116">The property can be specified either by name or by the property set's format identifier (FMTID) and property identifier (PID).</span></span><br/> |
| [<span data-ttu-id="d3e32-117">**Invokeverbex**</span><span class="sxs-lookup"><span data-stu-id="d3e32-117">**InvokeVerbEx**</span></span>](invokeverbex.md)                         | <span data-ttu-id="d3e32-118">Führt ein Verb für ein shellelement aus.</span><span class="sxs-lookup"><span data-stu-id="d3e32-118">Executes a verb on a Shell item.</span></span><br/>                                                                                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="d3e32-119">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="d3e32-119">Requirements</span></span>



| <span data-ttu-id="d3e32-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d3e32-120">Requirement</span></span> | <span data-ttu-id="d3e32-121">Wert</span><span class="sxs-lookup"><span data-stu-id="d3e32-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3e32-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d3e32-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d3e32-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d3e32-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d3e32-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d3e32-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d3e32-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d3e32-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="d3e32-126">Header</span><span class="sxs-lookup"><span data-stu-id="d3e32-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3e32-127"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3e32-127"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="d3e32-128">IDL</span><span class="sxs-lookup"><span data-stu-id="d3e32-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d3e32-129"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d3e32-129"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="d3e32-130">DLL</span><span class="sxs-lookup"><span data-stu-id="d3e32-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3e32-131"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="d3e32-131"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




