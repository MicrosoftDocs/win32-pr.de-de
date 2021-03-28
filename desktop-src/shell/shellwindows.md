---
description: Stellt eine Auflistung der geöffneten Fenster dar, die zur Shell gehören. Mit diesen Objekten verknüpfte Methoden können Befehle in der Shell Steuern und ausführen sowie andere shellbezogene Objekte abrufen.
ms.assetid: cad1f961-7fb4-4ba1-be48-b664d3de2c60
title: Shellwindows-Objekt (Exdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellWindows
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 6a3a782dd4e29d56f5edc7a869004ac7b3fb7ccd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979809"
---
# <a name="shellwindows-object"></a><span data-ttu-id="1ca86-104">Shellwindows-Objekt</span><span class="sxs-lookup"><span data-stu-id="1ca86-104">ShellWindows object</span></span>

<span data-ttu-id="1ca86-105">Stellt eine Auflistung der geöffneten Fenster dar, die zur Shell gehören.</span><span class="sxs-lookup"><span data-stu-id="1ca86-105">Represents a collection of the open windows that belong to the Shell.</span></span> <span data-ttu-id="1ca86-106">Mit diesen Objekten verknüpfte Methoden können Befehle in der Shell Steuern und ausführen sowie andere shellbezogene Objekte abrufen.</span><span class="sxs-lookup"><span data-stu-id="1ca86-106">Methods associated with this objects can control and execute commands within the Shell, and obtain other Shell-related objects.</span></span>

## <a name="members"></a><span data-ttu-id="1ca86-107">Member</span><span class="sxs-lookup"><span data-stu-id="1ca86-107">Members</span></span>

<span data-ttu-id="1ca86-108">Das **shellwindows** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="1ca86-108">The **ShellWindows** object has these types of members:</span></span>

-   [<span data-ttu-id="1ca86-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="1ca86-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="1ca86-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1ca86-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1ca86-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="1ca86-111">Methods</span></span>

<span data-ttu-id="1ca86-112">Das **shellwindows** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="1ca86-112">The **ShellWindows** object has these methods.</span></span>



| <span data-ttu-id="1ca86-113">Methode</span><span class="sxs-lookup"><span data-stu-id="1ca86-113">Method</span></span>                                                 | <span data-ttu-id="1ca86-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1ca86-114">Description</span></span>                                                                                                         |
|:-------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1ca86-115">**\_"Netwenum"**</span><span class="sxs-lookup"><span data-stu-id="1ca86-115">**\_NewEnum**</span></span>](shellwindows--newenum-method-7ral.md) | <span data-ttu-id="1ca86-116">Erstellt ein neues **shellwindows** -Objekt, das eine Kopie dieses **shellwindows** -Objekts ist, und gibt es zurück.</span><span class="sxs-lookup"><span data-stu-id="1ca86-116">Creates and returns a new **ShellWindows** object that is a copy of this **ShellWindows** object.</span></span><br/>        |
| [<span data-ttu-id="1ca86-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="1ca86-117">**Item**</span></span>](shellwindows-item.md)                      | <span data-ttu-id="1ca86-118">Ruft ein [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) -Objekt ab, das das Shellfenster darstellt.</span><span class="sxs-lookup"><span data-stu-id="1ca86-118">Retrieves an [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) object that represents the Shell window.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="1ca86-119">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1ca86-119">Properties</span></span>

<span data-ttu-id="1ca86-120">Das **shellwindows** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1ca86-120">The **ShellWindows** object has these properties.</span></span>



| <span data-ttu-id="1ca86-121">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1ca86-121">Property</span></span>                                       | <span data-ttu-id="1ca86-122">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="1ca86-122">Access type</span></span>          | <span data-ttu-id="1ca86-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1ca86-123">Description</span></span>                                                |
|:-----------------------------------------------|:---------------------|:-----------------------------------------------------------|
| [<span data-ttu-id="1ca86-124">**Anzahl**</span><span class="sxs-lookup"><span data-stu-id="1ca86-124">**Count**</span></span>](shellwindows-count.md)<br/> | <span data-ttu-id="1ca86-125">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="1ca86-125">Read-only</span></span><br/> | <span data-ttu-id="1ca86-126">Enthält die Anzahl der Elemente in der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="1ca86-126">Contains the number of items in the collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1ca86-127">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="1ca86-127">Requirements</span></span>



| <span data-ttu-id="1ca86-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1ca86-128">Requirement</span></span> | <span data-ttu-id="1ca86-129">Wert</span><span class="sxs-lookup"><span data-stu-id="1ca86-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ca86-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1ca86-130">Minimum supported client</span></span><br/> | <span data-ttu-id="1ca86-131">Windows 2000 Professional, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1ca86-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="1ca86-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1ca86-132">Minimum supported server</span></span><br/> | <span data-ttu-id="1ca86-133">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1ca86-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1ca86-134">Header</span><span class="sxs-lookup"><span data-stu-id="1ca86-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ca86-135"><dt>Exdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ca86-135"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="1ca86-136">DLL</span><span class="sxs-lookup"><span data-stu-id="1ca86-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ca86-137"><dt>Shell32.dll (Version 4,71 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="1ca86-137"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
