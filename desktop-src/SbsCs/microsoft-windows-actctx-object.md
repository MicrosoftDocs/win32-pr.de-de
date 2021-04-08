---
description: Das Microsoft. Windows. ActCtx-Objekt verweist auf Manifeste und bietet eine Möglichkeit für Skript-Engines, auf parallele Assemblys zuzugreifen. Das Microsoft. Windows. ActCtx-Objekt kann verwendet werden, um eine Instanz einer parallelen Assembly mit COM-Komponenten zu erstellen.
ms.assetid: 818e175e-2c58-4c44-87ce-4e97352fc3f3
title: Microsoft. Windows. ActCtx-Objekt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Microsoft.Windows.ActCtx
api_type:
- COM
api_location: ''
ms.openlocfilehash: 58290ec9d36d8e8428000422d0e1014335870149
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864212"
---
# <a name="microsoftwindowsactctx-object"></a><span data-ttu-id="9dcfb-104">Microsoft. Windows. ActCtx-Objekt</span><span class="sxs-lookup"><span data-stu-id="9dcfb-104">Microsoft.Windows.ActCtx object</span></span>

<span data-ttu-id="9dcfb-105">Das **Microsoft. Windows. ActCtx** -Objekt verweist auf Manifeste und bietet eine Möglichkeit für Skript-Engines, auf parallele Assemblys zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="9dcfb-105">The **Microsoft.Windows.ActCtx** object references manifests and provides a way for scripting engines to access side-by-side assemblies.</span></span> <span data-ttu-id="9dcfb-106">Das **Microsoft. Windows. ActCtx** -Objekt kann verwendet werden, um eine Instanz einer parallelen Assembly mit COM-Komponenten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9dcfb-106">The **Microsoft.Windows.ActCtx** object can be used to create an instance of a side-by-side assembly with COM components.</span></span>

<span data-ttu-id="9dcfb-107">Das **Microsoft. Windows. ActCtx** -Objekt ist als Assembly in Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9dcfb-107">The **Microsoft.Windows.ActCtx** object comes as an assembly in Windows Server 2003.</span></span> <span data-ttu-id="9dcfb-108">Sie kann auch von Anwendungen installiert werden, die die Windows Installer für Setup verwenden, und Sie als Mergemodul in das Installationspaket einschließen.</span><span class="sxs-lookup"><span data-stu-id="9dcfb-108">It can also be installed by applications that use the Windows Installer for setup and include it as a merge module in their installation package.</span></span>

## <a name="members"></a><span data-ttu-id="9dcfb-109">Member</span><span class="sxs-lookup"><span data-stu-id="9dcfb-109">Members</span></span>

<span data-ttu-id="9dcfb-110">Das **Microsoft. Windows. ActCtx** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="9dcfb-110">The **Microsoft.Windows.ActCtx** object has these types of members:</span></span>

-   [<span data-ttu-id="9dcfb-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="9dcfb-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="9dcfb-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9dcfb-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9dcfb-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="9dcfb-113">Methods</span></span>

<span data-ttu-id="9dcfb-114">Das **Microsoft. Windows. ActCtx** -Objekt verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="9dcfb-114">The **Microsoft.Windows.ActCtx** object has these methods.</span></span>



| <span data-ttu-id="9dcfb-115">Methode</span><span class="sxs-lookup"><span data-stu-id="9dcfb-115">Method</span></span>                               | <span data-ttu-id="9dcfb-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9dcfb-116">Description</span></span>                                                                     |
|:-------------------------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="9dcfb-117">**CreateObject**</span><span class="sxs-lookup"><span data-stu-id="9dcfb-117">**CreateObject**</span></span>](createobject.md) | <span data-ttu-id="9dcfb-118">Erstellt ein-Objekt im Kontext des aktuellen Manifests.</span><span class="sxs-lookup"><span data-stu-id="9dcfb-118">Creates an object in the context of the current manifest.</span></span><br/>            |
| [<span data-ttu-id="9dcfb-119">**GetObject**</span><span class="sxs-lookup"><span data-stu-id="9dcfb-119">**GetObject**</span></span>](getobject.md)       | <span data-ttu-id="9dcfb-120">Ruft eine Instanz eines vorhandenen **Microsoft. Windows. ActCtx** -Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="9dcfb-120">Gets an instance of an existing **Microsoft.Windows.ActCtx** object.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="9dcfb-121">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="9dcfb-121">Properties</span></span>

<span data-ttu-id="9dcfb-122">Das **Microsoft. Windows. ActCtx** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9dcfb-122">The **Microsoft.Windows.ActCtx** object has these properties.</span></span>



| <span data-ttu-id="9dcfb-123">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="9dcfb-123">Property</span></span>                                | <span data-ttu-id="9dcfb-124">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="9dcfb-124">Access type</span></span>          | <span data-ttu-id="9dcfb-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9dcfb-125">Description</span></span>                                    |
|:----------------------------------------|:---------------------|:-----------------------------------------------|
| [<span data-ttu-id="9dcfb-126">**Kundiger**</span><span class="sxs-lookup"><span data-stu-id="9dcfb-126">**Manifest**</span></span>](manifest.md)<br/> | <span data-ttu-id="9dcfb-127">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="9dcfb-127">Read-only</span></span><br/> | <span data-ttu-id="9dcfb-128">Ruft den aktiven Aktivierungs Kontext ab.</span><span class="sxs-lookup"><span data-stu-id="9dcfb-128">Gets the active activation context.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9dcfb-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9dcfb-129">Requirements</span></span>



| <span data-ttu-id="9dcfb-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9dcfb-130">Requirement</span></span> | <span data-ttu-id="9dcfb-131">Wert</span><span class="sxs-lookup"><span data-stu-id="9dcfb-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9dcfb-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9dcfb-132">Minimum supported client</span></span><br/> | <span data-ttu-id="9dcfb-133">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9dcfb-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="9dcfb-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9dcfb-134">Minimum supported server</span></span><br/> | <span data-ttu-id="9dcfb-135">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9dcfb-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 




