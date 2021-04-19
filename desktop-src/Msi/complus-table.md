---
description: Die complus-Tabelle enthält Informationen, die zum Installieren von com+-Anwendungen erforderlich sind.
ms.assetid: 0c9a7469-5959-45ad-b84d-6cfd3e169ff6
title: ComPlus-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a2ad5b7b96044025b78bfc774ee0767c2756aa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369045"
---
# <a name="complus-table"></a><span data-ttu-id="f132c-103">ComPlus-Tabelle</span><span class="sxs-lookup"><span data-stu-id="f132c-103">Complus Table</span></span>

<span data-ttu-id="f132c-104">Die complus-Tabelle enthält Informationen, die zum Installieren von com+-Anwendungen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="f132c-104">The Complus table contains information needed to install COM+ applications.</span></span>

<span data-ttu-id="f132c-105">Die complus-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="f132c-105">The Complus table has the following columns.</span></span>



| <span data-ttu-id="f132c-106">Spalte</span><span class="sxs-lookup"><span data-stu-id="f132c-106">Column</span></span>      | <span data-ttu-id="f132c-107">Typ</span><span class="sxs-lookup"><span data-stu-id="f132c-107">Type</span></span>                         | <span data-ttu-id="f132c-108">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="f132c-108">Key</span></span> | <span data-ttu-id="f132c-109">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="f132c-109">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="f132c-110">Komponente\_</span><span class="sxs-lookup"><span data-stu-id="f132c-110">Component\_</span></span> | [<span data-ttu-id="f132c-111">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="f132c-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="f132c-112">J</span><span class="sxs-lookup"><span data-stu-id="f132c-112">Y</span></span>   | <span data-ttu-id="f132c-113">N</span><span class="sxs-lookup"><span data-stu-id="f132c-113">N</span></span>        |
| <span data-ttu-id="f132c-114">EXPTYPE</span><span class="sxs-lookup"><span data-stu-id="f132c-114">ExpType</span></span>     | [<span data-ttu-id="f132c-115">Integer</span><span class="sxs-lookup"><span data-stu-id="f132c-115">Integer</span></span>](integer.md)       | <span data-ttu-id="f132c-116">N</span><span class="sxs-lookup"><span data-stu-id="f132c-116">N</span></span>   | <span data-ttu-id="f132c-117">J</span><span class="sxs-lookup"><span data-stu-id="f132c-117">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="f132c-118">Spalten</span><span class="sxs-lookup"><span data-stu-id="f132c-118">Columns</span></span>

<dl> <dt>

<span data-ttu-id="f132c-119"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Zulieferern\_</span><span class="sxs-lookup"><span data-stu-id="f132c-119"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="f132c-120">Ein externer Schlüssel in die erste Spalte der [Komponenten Tabelle](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="f132c-120">An external key into the first column of the [Component table](component-table.md).</span></span> <span data-ttu-id="f132c-121">Dies ist die Komponente, die die COM+-Anwendung enthält.</span><span class="sxs-lookup"><span data-stu-id="f132c-121">This is the component that contains the COM+ application.</span></span>

</dd> <dt>

<span data-ttu-id="f132c-122"><span id="ExpType"></span><span id="exptype"></span><span id="EXPTYPE"></span>EXPTYPE</span><span class="sxs-lookup"><span data-stu-id="f132c-122"><span id="ExpType"></span><span id="exptype"></span><span id="EXPTYPE"></span>ExpType</span></span>
</dt> <dd>

<span data-ttu-id="f132c-123">Exportiererungsflags, die während der Generierung der MSI-Datei verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f132c-123">Export flags used during the generation of the .msi file.</span></span> <span data-ttu-id="f132c-124">Weitere Informationen finden Sie in der com+-Dokumentation im Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="f132c-124">For more information see the COM+ documentation in the Microsoft Windows Software Development Kit (SDK).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f132c-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f132c-125">Remarks</span></span>

<span data-ttu-id="f132c-126">Weitere Informationen finden Sie in der [registercomplus-Aktion](registercomplus-action.md) und der [unregistercomplus-Aktion](unregistercomplus-action.md).</span><span class="sxs-lookup"><span data-stu-id="f132c-126">See the [RegisterComPlus action](registercomplus-action.md) and [UnregisterComPlus action](unregistercomplus-action.md).</span></span>

<span data-ttu-id="f132c-127">Weitere Informationen finden Sie unter [Installieren einer COM+-Anwendung mit dem Windows Installer](installing-a-com--application-with-the-windows-installer.md).</span><span class="sxs-lookup"><span data-stu-id="f132c-127">See [Installing a COM+ Application with the Windows Installer](installing-a-com--application-with-the-windows-installer.md).</span></span>

## <a name="validation"></a><span data-ttu-id="f132c-128">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="f132c-128">Validation</span></span>

<dl>

[<span data-ttu-id="f132c-129">ICE03</span><span class="sxs-lookup"><span data-stu-id="f132c-129">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="f132c-130">ICE06</span><span class="sxs-lookup"><span data-stu-id="f132c-130">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="f132c-131">ICE32</span><span class="sxs-lookup"><span data-stu-id="f132c-131">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="f132c-132">ICE66</span><span class="sxs-lookup"><span data-stu-id="f132c-132">ICE66</span></span>](ice66.md)  
</dl>

 

 



