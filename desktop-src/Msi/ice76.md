---
description: ICE76 überprüft die Verwendung des SFP (WFP)-Katalogs in Windows Installer Paketen für Windows Me. Dieses Eis überprüft auch, ob keine Dateien in der BindImage-Tabelle SFP-Kataloge referenzieren.
ms.assetid: e8b60b11-19ac-4ec4-aa36-a1f7a3ccd6f6
title: ICE76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5beb0157053e9bd3e4bf0d896f52af04a511ac24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343347"
---
# <a name="ice76"></a><span data-ttu-id="d729a-104">ICE76</span><span class="sxs-lookup"><span data-stu-id="d729a-104">ICE76</span></span>

<span data-ttu-id="d729a-105">ICE76 überprüft die Verwendung des SFP (WFP)-Katalogs in Windows Installer Paketen für Windows Me.</span><span class="sxs-lookup"><span data-stu-id="d729a-105">ICE76 verifies the use of the SFP (WFP) catalog within Windows Installer packages for Windows Me.</span></span> <span data-ttu-id="d729a-106">Dieses Eis überprüft auch, ob keine Dateien in der BindImage- [Tabelle](bindimage-table.md) SFP-Kataloge referenzieren.</span><span class="sxs-lookup"><span data-stu-id="d729a-106">This ICE also verifies that no files in the BindImage [table](bindimage-table.md) reference SFP catalogs.</span></span>

<span data-ttu-id="d729a-107">Der Windows-Datei Schutz erfordert eine genaue Entsprechung zwischen der Datei und der Signatur, die in die Katalog Datei eingebettet ist.</span><span class="sxs-lookup"><span data-stu-id="d729a-107">Windows File Protection requires an exact match between the file and the signature embedded in the catalog file.</span></span> <span data-ttu-id="d729a-108">Dateien, die auf einen SFP-Katalog verweisen, dürfen nicht in der Tabelle ' BindImage ' aufgeführt werden, da die Auswirkung der [BindImage-Aktion](bindimage-action.md) auf diese Dateien zwischen Computern abweicht.</span><span class="sxs-lookup"><span data-stu-id="d729a-108">Files that reference a SFP catalog must not be listed in the BindImage table because the effect of the [BindImage action](bindimage-action.md) on these files differs between computers.</span></span> <span data-ttu-id="d729a-109">Dateien, auf die von SFP-Katalogen verwiesen wird, müssen in Komponenten vorliegen, die permanent sind oder lokal installiert sind</span><span class="sxs-lookup"><span data-stu-id="d729a-109">Files referenced by SFP catalogs must be in components that are permanent or installed locally.</span></span>

## <a name="result"></a><span data-ttu-id="d729a-110">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="d729a-110">Result</span></span>

<span data-ttu-id="d729a-111">ICE76 gibt einen Fehler für jede Datei in der [Tabelle BindImage](bindimage-table.md) aus, die auch in der [Tabelle filesfpcatalog](filesfpcatalog-table.md)vorliegt.</span><span class="sxs-lookup"><span data-stu-id="d729a-111">ICE76 posts an error for each file in the [BindImage table](bindimage-table.md) that is also in the [FileSFPCatalog table](filesfpcatalog-table.md).</span></span>

<span data-ttu-id="d729a-112">ICE76 gibt einen Fehler aus, wenn eine Datei in der filesfpcatalog-Tabelle zu einer Komponente mit einer der folgenden true gehört:</span><span class="sxs-lookup"><span data-stu-id="d729a-112">ICE76 outputs an error if a file in the FileSFPCatalog table belongs to a component with any of the following true:</span></span>

-   <span data-ttu-id="d729a-113">**msidbcomponentattributespermanent** ist nicht in der Attribute-Spalte der [Component-Tabelle](component-table.md)festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d729a-113">**msidbComponentAttributesPermanent** is not set in the Attributes column of the [Component table](component-table.md).</span></span>
-   <span data-ttu-id="d729a-114">**msidbcomponentattributessourceonly** wird in der Spalte Attribute der Komponenten Tabelle festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d729a-114">**msidbComponentAttributesSourceOnly** is set in the Attributes column of the Component table.</span></span>
-   <span data-ttu-id="d729a-115">**msidbattributesoptional** wird in der Spalte Attribute der Komponenten Tabelle festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d729a-115">**msidbAttributesOptional** is set in the Attributes column of the Component table.</span></span>

## <a name="example"></a><span data-ttu-id="d729a-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d729a-116">Example</span></span>

<span data-ttu-id="d729a-117">ICE76 meldet den folgenden Fehler für das Beispiel:</span><span class="sxs-lookup"><span data-stu-id="d729a-117">ICE76 reports the following error for the example:</span></span>

``` syntax
File 'File1' references a SFP catalog. Therefore it cannot be in the BindImage table.
```

<span data-ttu-id="d729a-118">[Filesfpcatalog-Tabelle](filesfpcatalog-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="d729a-118">[FileSFPCatalog Table](filesfpcatalog-table.md) (partial)</span></span>



| <span data-ttu-id="d729a-119">Datei\_</span><span class="sxs-lookup"><span data-stu-id="d729a-119">File\_</span></span> | <span data-ttu-id="d729a-120">Sfpcatalog\_</span><span class="sxs-lookup"><span data-stu-id="d729a-120">SFPCatalog\_</span></span> |
|--------|--------------|
| <span data-ttu-id="d729a-121">Datei1</span><span class="sxs-lookup"><span data-stu-id="d729a-121">File1</span></span>  | <span data-ttu-id="d729a-122">Catalog1.Cat</span><span class="sxs-lookup"><span data-stu-id="d729a-122">Catalog1.Cat</span></span> |



 

<span data-ttu-id="d729a-123">[BindImage-Tabelle](bindimage-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="d729a-123">[BindImage Table](bindimage-table.md) (partial)</span></span>



| <span data-ttu-id="d729a-124">Datei\_</span><span class="sxs-lookup"><span data-stu-id="d729a-124">File\_</span></span> |
|--------|
| <span data-ttu-id="d729a-125">Datei1</span><span class="sxs-lookup"><span data-stu-id="d729a-125">File1</span></span>  |



 

<span data-ttu-id="d729a-126">Um dieses Problem zu beheben, geben Sie keine Dateien ein, die auf SFP-Kataloge in der BindImage-Tabelle verweisen.</span><span class="sxs-lookup"><span data-stu-id="d729a-126">To fix this do not enter any files that reference SFP catalogs into the BindImage table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d729a-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d729a-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d729a-128">BindImage-Tabelle</span><span class="sxs-lookup"><span data-stu-id="d729a-128">BindImage Table</span></span>](bindimage-table.md)
</dt> <dt>

[<span data-ttu-id="d729a-129">Komponenten Tabelle</span><span class="sxs-lookup"><span data-stu-id="d729a-129">Component Table</span></span>](component-table.md)
</dt> <dt>

[<span data-ttu-id="d729a-130">Filesfpcatalog-Tabelle</span><span class="sxs-lookup"><span data-stu-id="d729a-130">FileSFPCatalog Table</span></span>](filesfpcatalog-table.md)
</dt> <dt>

[<span data-ttu-id="d729a-131">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="d729a-131">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



