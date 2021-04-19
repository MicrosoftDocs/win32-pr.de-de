---
description: In diesem Beispiel kann der modulconsumer ein Bearbeitungs Steuerelement, das Prüfsumme-Attribut und das komprimierte Attribut unabhängig konfigurieren.
ms.assetid: f0500856-18d0-45e5-992a-57e01fb2cca5
title: Beispiel für konfigurierbare Komponente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 971b2a7c442acb96d7ba00a444c8c3a038c339f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350489"
---
# <a name="configurable-component-example"></a><span data-ttu-id="4acd7-103">Beispiel für konfigurierbare Komponente</span><span class="sxs-lookup"><span data-stu-id="4acd7-103">Configurable Component Example</span></span>

<span data-ttu-id="4acd7-104">In diesem Beispiel kann der modulconsumer mithilfe der folgenden ModuleConfiguration-und ModuleSubstitution-Tabellen das Kenn Wort Attribut für ein Bearbeitungs Steuerelement, das Prüfsumme-Attribut für eine Datei und das komprimierte Attribut für dieselbe Datei unabhängig konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="4acd7-104">In this example, the following ModuleConfiguration and ModuleSubstitution tables allows the module consumer to independently configure the Password attribute for an edit control, the checksum attribute for a file, and the compressed attribute for the same file.</span></span>

[<span data-ttu-id="4acd7-105">ModuleSubstitution-Tabelle</span><span class="sxs-lookup"><span data-stu-id="4acd7-105">ModuleSubstitution Table</span></span>](modulesubstitution-table.md)



| <span data-ttu-id="4acd7-106">Tabelle</span><span class="sxs-lookup"><span data-stu-id="4acd7-106">Table</span></span>   | <span data-ttu-id="4acd7-107">Zeile</span><span class="sxs-lookup"><span data-stu-id="4acd7-107">Row</span></span>           | <span data-ttu-id="4acd7-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="4acd7-108">Column</span></span>     | <span data-ttu-id="4acd7-109">Wert</span><span class="sxs-lookup"><span data-stu-id="4acd7-109">Value</span></span>                        |
|---------|---------------|------------|------------------------------|
| <span data-ttu-id="4acd7-110">Control</span><span class="sxs-lookup"><span data-stu-id="4acd7-110">Control</span></span> | <span data-ttu-id="4acd7-111">Dialog1; Edit1</span><span class="sxs-lookup"><span data-stu-id="4acd7-111">Dialog1;Edit1</span></span> | <span data-ttu-id="4acd7-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="4acd7-112">Attributes</span></span> | <span data-ttu-id="4acd7-113">\[= Kennwort\]</span><span class="sxs-lookup"><span data-stu-id="4acd7-113">\[=Password\]</span></span>                |
| <span data-ttu-id="4acd7-114">File</span><span class="sxs-lookup"><span data-stu-id="4acd7-114">File</span></span>    | <span data-ttu-id="4acd7-115">Datei1</span><span class="sxs-lookup"><span data-stu-id="4acd7-115">File1</span></span>         | <span data-ttu-id="4acd7-116">Attribute</span><span class="sxs-lookup"><span data-stu-id="4acd7-116">Attributes</span></span> | <span data-ttu-id="4acd7-117">\[= Prüfsumme \] \[ = komprimiert\]</span><span class="sxs-lookup"><span data-stu-id="4acd7-117">\[=Checksum\]\[=Compressed\]</span></span> |



 

[<span data-ttu-id="4acd7-118">ModuleConfiguration-Tabelle</span><span class="sxs-lookup"><span data-stu-id="4acd7-118">ModuleConfiguration Table</span></span>](moduleconfiguration-table.md)



| <span data-ttu-id="4acd7-119">Name</span><span class="sxs-lookup"><span data-stu-id="4acd7-119">Name</span></span>       | <span data-ttu-id="4acd7-120">Format</span><span class="sxs-lookup"><span data-stu-id="4acd7-120">Format</span></span>   | <span data-ttu-id="4acd7-121">type</span><span class="sxs-lookup"><span data-stu-id="4acd7-121">Type</span></span> | <span data-ttu-id="4acd7-122">ContextData</span><span class="sxs-lookup"><span data-stu-id="4acd7-122">ContextData</span></span>                              | <span data-ttu-id="4acd7-123">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="4acd7-123">DefaultValue</span></span> | <span data-ttu-id="4acd7-124">Attribute</span><span class="sxs-lookup"><span data-stu-id="4acd7-124">Attributes</span></span> | <span data-ttu-id="4acd7-125">DisplayName</span><span class="sxs-lookup"><span data-stu-id="4acd7-125">DisplayName</span></span> | <span data-ttu-id="4acd7-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4acd7-126">Description</span></span> |
|------------|----------|------|------------------------------------------|--------------|------------|-------------|-------------|
| <span data-ttu-id="4acd7-127">Kennwort</span><span class="sxs-lookup"><span data-stu-id="4acd7-127">Password</span></span>   | <span data-ttu-id="4acd7-128">Bitfeld</span><span class="sxs-lookup"><span data-stu-id="4acd7-128">Bitfield</span></span> |      | <span data-ttu-id="4acd7-129">2097152; True = 2097152; False = 0</span><span class="sxs-lookup"><span data-stu-id="4acd7-129">2097152;True=2097152;False=0</span></span>             | <span data-ttu-id="4acd7-130">0</span><span class="sxs-lookup"><span data-stu-id="4acd7-130">0</span></span>            | <span data-ttu-id="4acd7-131">0</span><span class="sxs-lookup"><span data-stu-id="4acd7-131">0</span></span>          |             |             |
| <span data-ttu-id="4acd7-132">Checksum</span><span class="sxs-lookup"><span data-stu-id="4acd7-132">Checksum</span></span>   | <span data-ttu-id="4acd7-133">Bitfeld</span><span class="sxs-lookup"><span data-stu-id="4acd7-133">Bitfield</span></span> |      | <span data-ttu-id="4acd7-134">1024; Prüfsumme = 1024; Keine Prüfsumme = 0</span><span class="sxs-lookup"><span data-stu-id="4acd7-134">1024;Checksum=1024;No Checksum=0</span></span>         | <span data-ttu-id="4acd7-135">0</span><span class="sxs-lookup"><span data-stu-id="4acd7-135">0</span></span>            | <span data-ttu-id="4acd7-136">0</span><span class="sxs-lookup"><span data-stu-id="4acd7-136">0</span></span>          |             |             |
| <span data-ttu-id="4acd7-137">Compressed</span><span class="sxs-lookup"><span data-stu-id="4acd7-137">Compressed</span></span> | <span data-ttu-id="4acd7-138">Bitfeld</span><span class="sxs-lookup"><span data-stu-id="4acd7-138">Bitfield</span></span> |      | <span data-ttu-id="4acd7-139">24576; Komprimiert = 16384; Unkomprimiert = 8192</span><span class="sxs-lookup"><span data-stu-id="4acd7-139">24576;Compressed=16384;Uncompressed=8192</span></span> | <span data-ttu-id="4acd7-140">8192</span><span class="sxs-lookup"><span data-stu-id="4acd7-140">8192</span></span>         | <span data-ttu-id="4acd7-141">0</span><span class="sxs-lookup"><span data-stu-id="4acd7-141">0</span></span>          |             |             |



 

 

 



