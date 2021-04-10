---
description: ICE45 überprüft, ob die Bitfeld Spalten in der Datenbank reservierte Bits nicht auf 1 festlegen.
ms.assetid: 43fa5e9c-2059-4217-8f8e-c194e37f238a
title: ICE45
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0651d94c296ae14f66b562841c3c4e2bca7b8e32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215703"
---
# <a name="ice45"></a><span data-ttu-id="920ba-103">ICE45</span><span class="sxs-lookup"><span data-stu-id="920ba-103">ICE45</span></span>

<span data-ttu-id="920ba-104">ICE45 überprüft, ob die Bitfeld Spalten in der Datenbank reservierte Bits nicht auf 1 festlegen.</span><span class="sxs-lookup"><span data-stu-id="920ba-104">ICE45 validates that bit field columns in the database do not set any reserved bits to 1.</span></span>

<span data-ttu-id="920ba-105">Reservierte Bits bieten keine Funktionalität in den aktuellen Versionen des Installers, aber in zukünftigen Versionen.</span><span class="sxs-lookup"><span data-stu-id="920ba-105">Reserved bits provide no functionality in current versions of the installer, but might in future versions.</span></span> <span data-ttu-id="920ba-106">Sie sollten auf 0 festgelegt werden, um mit zukünftigen Versionen von Windows Installer kompatibel zu sein.</span><span class="sxs-lookup"><span data-stu-id="920ba-106">They should be set to 0 to be compatible with future versions of Windows Installer.</span></span>

## <a name="result"></a><span data-ttu-id="920ba-107">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="920ba-107">Result</span></span>

<span data-ttu-id="920ba-108">ICE45 gibt eine Fehlermeldung aus, wenn eine der folgenden Tabellen ein Bitfeld mit einem reservierten Bit enthält, das auf den Wert 1 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="920ba-108">ICE45 posts an error message if any of the following tables contains a bit field with a reserved bit set to a value of 1.</span></span>

-   [<span data-ttu-id="920ba-109">Bbcontrol-Tabelle</span><span class="sxs-lookup"><span data-stu-id="920ba-109">BBControl table</span></span>](bbcontrol-table.md)
-   [<span data-ttu-id="920ba-110">Dialog Feld Tabelle</span><span class="sxs-lookup"><span data-stu-id="920ba-110">Dialog table</span></span>](dialog-table.md)
-   [<span data-ttu-id="920ba-111">Funktions Tabelle</span><span class="sxs-lookup"><span data-stu-id="920ba-111">Feature table</span></span>](feature-table.md)
-   [<span data-ttu-id="920ba-112">Dateitabelle</span><span class="sxs-lookup"><span data-stu-id="920ba-112">File table</span></span>](file-table.md)
-   [<span data-ttu-id="920ba-113">"Muvefile"-Tabelle</span><span class="sxs-lookup"><span data-stu-id="920ba-113">MoveFile table</span></span>](movefile-table.md)
-   [<span data-ttu-id="920ba-114">ModuleConfiguration-Tabelle</span><span class="sxs-lookup"><span data-stu-id="920ba-114">ModuleConfiguration table</span></span>](moduleconfiguration-table.md)
-   [<span data-ttu-id="920ba-115">ODBCDatasource-Tabelle</span><span class="sxs-lookup"><span data-stu-id="920ba-115">ODBCDataSource table</span></span>](odbcdatasource-table.md)
-   [<span data-ttu-id="920ba-116">Patchtabelle</span><span class="sxs-lookup"><span data-stu-id="920ba-116">Patch table</span></span>](patch-table.md)
-   [<span data-ttu-id="920ba-117">RemoveFile-Tabelle</span><span class="sxs-lookup"><span data-stu-id="920ba-117">RemoveFile table</span></span>](removefile-table.md)
-   [<span data-ttu-id="920ba-118">ServiceControl-Tabelle</span><span class="sxs-lookup"><span data-stu-id="920ba-118">ServiceControl table</span></span>](servicecontrol-table.md)
-   [<span data-ttu-id="920ba-119">Servicabstall-Tabelle</span><span class="sxs-lookup"><span data-stu-id="920ba-119">ServiceInstall table</span></span>](serviceinstall-table.md)
-   [<span data-ttu-id="920ba-120">TextStyle-Tabelle</span><span class="sxs-lookup"><span data-stu-id="920ba-120">TextStyle table</span></span>](textstyle-table.md)

<span data-ttu-id="920ba-121">ICE45 sendet eine von zwei Warnmeldungen, wenn die [Steuerelement Tabelle](control-table.md) ein Bitfeld mit einem reservierten Bit enthält, das auf den Wert 1 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="920ba-121">ICE45 posts one of two warning messages if the [Control Table](control-table.md) contains a bit field with a reserved bit set to a value of 1.</span></span>

## <a name="example"></a><span data-ttu-id="920ba-122">Beispiel</span><span class="sxs-lookup"><span data-stu-id="920ba-122">Example</span></span>

<span data-ttu-id="920ba-123">ICE45 meldet den folgenden Fehler für das gezeigte Beispiel.</span><span class="sxs-lookup"><span data-stu-id="920ba-123">ICE45 reports the following error for the example shown.</span></span>

``` syntax
Row 'File1' in table 'File' has bits set in the 'Attributes' 
    column that are reserved. They must be 0 to ensure 
    compatibility with future installer versions.
```

<span data-ttu-id="920ba-124">ICE45 meldet die folgende Warnung für das gezeigte Beispiel.</span><span class="sxs-lookup"><span data-stu-id="920ba-124">ICE45 reports the following warning for the example shown.</span></span>

``` syntax
Row 'Dialog1.Edit2' in table 'Control' has bits set in the 'Attribute' 
    column that are reserved. They should be 0 to ensure compatibility 
    with future installer versions.
```

<span data-ttu-id="920ba-125">[Dateitabelle](file-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="920ba-125">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="920ba-126">File</span><span class="sxs-lookup"><span data-stu-id="920ba-126">File</span></span>  | <span data-ttu-id="920ba-127">Attribute</span><span class="sxs-lookup"><span data-stu-id="920ba-127">Attributes</span></span> |
|-------|------------|
| <span data-ttu-id="920ba-128">Datei1</span><span class="sxs-lookup"><span data-stu-id="920ba-128">File1</span></span> | <span data-ttu-id="920ba-129">128</span><span class="sxs-lookup"><span data-stu-id="920ba-129">128</span></span>        |



 

<span data-ttu-id="920ba-130">[Control-Tabelle](control-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="920ba-130">[Control Table](control-table.md) (partial)</span></span>



| <span data-ttu-id="920ba-131">Dialog</span><span class="sxs-lookup"><span data-stu-id="920ba-131">Dialog</span></span>  | <span data-ttu-id="920ba-132">Control</span><span class="sxs-lookup"><span data-stu-id="920ba-132">Control</span></span> | <span data-ttu-id="920ba-133">Attribute</span><span class="sxs-lookup"><span data-stu-id="920ba-133">Attributes</span></span> |
|---------|---------|------------|
| <span data-ttu-id="920ba-134">Dialog1</span><span class="sxs-lookup"><span data-stu-id="920ba-134">Dialog1</span></span> | <span data-ttu-id="920ba-135">Edit1</span><span class="sxs-lookup"><span data-stu-id="920ba-135">Edit1</span></span>   | <span data-ttu-id="920ba-136">2097152</span><span class="sxs-lookup"><span data-stu-id="920ba-136">2097152</span></span>    |
| <span data-ttu-id="920ba-137">Dialog1</span><span class="sxs-lookup"><span data-stu-id="920ba-137">Dialog1</span></span> | <span data-ttu-id="920ba-138">Edit2</span><span class="sxs-lookup"><span data-stu-id="920ba-138">Edit2</span></span>   | <span data-ttu-id="920ba-139">1048576</span><span class="sxs-lookup"><span data-stu-id="920ba-139">1048576</span></span>    |



 

## <a name="related-topics"></a><span data-ttu-id="920ba-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="920ba-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="920ba-141">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="920ba-141">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



