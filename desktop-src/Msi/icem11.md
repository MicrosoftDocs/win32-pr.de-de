---
description: ICEM11 überprüft, ob ein konfigurierbares Mergemodul die ModuleConfiguration-Tabelle und die ModuleSubstitution-Tabelle in der moduleignoretable-Tabelle des Moduls auflistet.
ms.assetid: f0199137-0a40-40ca-b3cf-ff8eef4309cc
title: ICEM11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 403a36435ce2367fc356934740e6d022f5457698
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216940"
---
# <a name="icem11"></a><span data-ttu-id="cd760-103">ICEM11</span><span class="sxs-lookup"><span data-stu-id="cd760-103">ICEM11</span></span>

<span data-ttu-id="cd760-104">ICEM11 überprüft, ob ein konfigurierbares Mergemodul die [ModuleConfiguration-Tabelle](moduleconfiguration-table.md) und die [ModuleSubstitution](modulesubstitution-table.md) -Tabelle in der [moduleignoretable-Tabelle](moduleignoretable-table.md) des Moduls auflistet.</span><span class="sxs-lookup"><span data-stu-id="cd760-104">ICEM11 verifies that a Configurable Merge Module lists the [ModuleConfiguration table](moduleconfiguration-table.md) and [ModuleSubstitution table](modulesubstitution-table.md) in the [ModuleIgnoreTable table](moduleignoretable-table.md) of the module.</span></span> <span data-ttu-id="cd760-105">Dadurch wird sichergestellt, dass Merge-Tools, die konfigurierbare Mergemodule nicht erkennen (weniger als Version 2,0) diese Tabellen nicht in die Zieldatenbank kopieren.</span><span class="sxs-lookup"><span data-stu-id="cd760-105">This ensures that merge tools that do not recognize configurable merge modules(less than version 2.0) do not copy these tables into the target database.</span></span>

<span data-ttu-id="cd760-106">Dieses ICEM ist in der Datei "Mergemod. Cub" verfügbar, die im SDK für Windows Installer 2,0 und höher bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="cd760-106">This ICEM is available in the Mergemod.cub file provided in the Windows Installer 2.0 SDK and later.</span></span> <span data-ttu-id="cd760-107">Weitere Informationen finden Sie unter [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="cd760-107">For details, see [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="result"></a><span data-ttu-id="cd760-108">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="cd760-108">Result</span></span>

<span data-ttu-id="cd760-109">ICEM11 gibt einen Fehler aus, wenn das Modul eine ModuleConfiguration-oder ModuleSubstitution-Tabelle enthält, die nicht in der moduleignoretable-Tabelle aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="cd760-109">ICEM11 posts an error if the module contains a ModuleConfiguration or ModuleSubstitution table not listed in the ModuleIgnoreTable table.</span></span>

## <a name="example"></a><span data-ttu-id="cd760-110">Beispiel</span><span class="sxs-lookup"><span data-stu-id="cd760-110">Example</span></span>

<span data-ttu-id="cd760-111">ICEM11 gibt die folgenden Fehlermeldungen für ein Modul mit den unten gezeigten Datenbankeinträgen aus.</span><span class="sxs-lookup"><span data-stu-id="cd760-111">ICEM11 posts the following error messages for a module containing the database entries shown below.</span></span>

``` syntax
Error The module contains a ModuleConfiguration or ModuleSubstitution 
table. These tables must be listed in the ModuleIgnoreTable table.
```

<span data-ttu-id="cd760-112">[ModuleConfiguration](moduleconfiguration-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="cd760-112">[ModuleConfiguration](moduleconfiguration-table.md) (partial)</span></span>



| <span data-ttu-id="cd760-113">Name</span><span class="sxs-lookup"><span data-stu-id="cd760-113">Name</span></span>     | <span data-ttu-id="cd760-114">Format</span><span class="sxs-lookup"><span data-stu-id="cd760-114">Format</span></span> | <span data-ttu-id="cd760-115">type</span><span class="sxs-lookup"><span data-stu-id="cd760-115">Type</span></span>   | <span data-ttu-id="cd760-116">ContextData</span><span class="sxs-lookup"><span data-stu-id="cd760-116">ContextData</span></span> | <span data-ttu-id="cd760-117">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="cd760-117">DefaultValue</span></span> |
|----------|--------|--------|-------------|--------------|
| <span data-ttu-id="cd760-118">IconKey1</span><span class="sxs-lookup"><span data-stu-id="cd760-118">IconKey1</span></span> | <span data-ttu-id="cd760-119">1</span><span class="sxs-lookup"><span data-stu-id="cd760-119">1</span></span>      | <span data-ttu-id="cd760-120">Binary</span><span class="sxs-lookup"><span data-stu-id="cd760-120">Binary</span></span> | <span data-ttu-id="cd760-121">Symbol</span><span class="sxs-lookup"><span data-stu-id="cd760-121">Icon</span></span>        | <span data-ttu-id="cd760-122">DefaultIcon</span><span class="sxs-lookup"><span data-stu-id="cd760-122">DefaultIcon</span></span>  |



 

[<span data-ttu-id="cd760-123">ModuleSubstitution</span><span class="sxs-lookup"><span data-stu-id="cd760-123">ModuleSubstitution</span></span>](modulesubstitution-table.md)



| <span data-ttu-id="cd760-124">Tabelle</span><span class="sxs-lookup"><span data-stu-id="cd760-124">Table</span></span>   | <span data-ttu-id="cd760-125">Zeile</span><span class="sxs-lookup"><span data-stu-id="cd760-125">Row</span></span>              | <span data-ttu-id="cd760-126">Spalte</span><span class="sxs-lookup"><span data-stu-id="cd760-126">Column</span></span> | <span data-ttu-id="cd760-127">Wert</span><span class="sxs-lookup"><span data-stu-id="cd760-127">Value</span></span>        |
|---------|------------------|--------|--------------|
| <span data-ttu-id="cd760-128">Control</span><span class="sxs-lookup"><span data-stu-id="cd760-128">Control</span></span> | <span data-ttu-id="cd760-129">Dialog1; Control1</span><span class="sxs-lookup"><span data-stu-id="cd760-129">Dialog1;Control1</span></span> | <span data-ttu-id="cd760-130">Text</span><span class="sxs-lookup"><span data-stu-id="cd760-130">Text</span></span>   | <span data-ttu-id="cd760-131">\[IconKey1\]</span><span class="sxs-lookup"><span data-stu-id="cd760-131">\[IconKey1\]</span></span> |



 

[<span data-ttu-id="cd760-132">Moduleignoretable</span><span class="sxs-lookup"><span data-stu-id="cd760-132">ModuleIgnoreTable</span></span>](moduleignoretable-table.md)



| <span data-ttu-id="cd760-133">Tabelle</span><span class="sxs-lookup"><span data-stu-id="cd760-133">Table</span></span>               |
|---------------------|
| <span data-ttu-id="cd760-134">ModuleConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd760-134">ModuleConfiguration</span></span> |



 

<span data-ttu-id="cd760-135">Um diesen Fehler zu beheben, schließen Sie die Tabellen ModuleSubstitution und ModuleConfiguration in der Tabelle moduleignoretable ein.</span><span class="sxs-lookup"><span data-stu-id="cd760-135">To fix this error include both the ModuleSubstitution and ModuleConfiguration tables in the ModuleIgnoreTable table.</span></span>

## <a name="table-used-during-execution"></a><span data-ttu-id="cd760-136">Während der Ausführung verwendete Tabelle</span><span class="sxs-lookup"><span data-stu-id="cd760-136">Table Used During Execution</span></span>

[<span data-ttu-id="cd760-137">ModuleSubstitution</span><span class="sxs-lookup"><span data-stu-id="cd760-137">ModuleSubstitution</span></span>](modulesubstitution-table.md)

[<span data-ttu-id="cd760-138">ModuleConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd760-138">ModuleConfiguration</span></span>](moduleconfiguration-table.md)

[<span data-ttu-id="cd760-139">Moduleignoretable</span><span class="sxs-lookup"><span data-stu-id="cd760-139">ModuleIgnoreTable</span></span>](moduleignoretable-table.md)

## <a name="related-topics"></a><span data-ttu-id="cd760-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cd760-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd760-141">Eisverweis für Mergemodul</span><span class="sxs-lookup"><span data-stu-id="cd760-141">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



