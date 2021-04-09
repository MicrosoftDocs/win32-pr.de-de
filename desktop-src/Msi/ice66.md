---
description: ICE66 verwendet die Tabellen in der-Datenbank, um zu bestimmen, welches Schema von der Datenbank verwendet werden soll.
ms.assetid: 7cf929a0-2c4c-40ca-a902-dfd9dcd203b8
title: ICE66
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea1436ad791941c96c0484a02f40a60fc9939e73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753016"
---
# <a name="ice66"></a><span data-ttu-id="419d2-103">ICE66</span><span class="sxs-lookup"><span data-stu-id="419d2-103">ICE66</span></span>

<span data-ttu-id="419d2-104">ICE66 verwendet die Tabellen in der-Datenbank, um zu bestimmen, welches Schema von der Datenbank verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="419d2-104">ICE66 uses the tables in the database to determine which schema your database should use.</span></span>

<span data-ttu-id="419d2-105">Einige Funktionen sind möglicherweise nur verfügbar, wenn das Paket auf einem System mit einer aktuellen Windows Installer Version installiert ist.</span><span class="sxs-lookup"><span data-stu-id="419d2-105">Some functionality may only be available if the package is installed on a system with a current Windows Installer version.</span></span>

## <a name="result"></a><span data-ttu-id="419d2-106">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="419d2-106">Result</span></span>

<span data-ttu-id="419d2-107">ICE66 gibt eine Warnung aus, wenn die Datenbank das falsche Schema verwendet.</span><span class="sxs-lookup"><span data-stu-id="419d2-107">ICE66 posts a warning if your database is using the wrong schema.</span></span>

## <a name="example"></a><span data-ttu-id="419d2-108">Beispiel</span><span class="sxs-lookup"><span data-stu-id="419d2-108">Example</span></span>

<span data-ttu-id="419d2-109">ICE66 meldet die folgende Warnung für das gezeigte Beispiel.</span><span class="sxs-lookup"><span data-stu-id="419d2-109">ICE66 reports the following warning for the example shown.</span></span>

``` syntax
WARNING: Complete functionality of the IsolatedComponents table is only available with Windows Installer versions 1.1 or greater. Your schema is 100.
```

<span data-ttu-id="419d2-110">Diese Warnung kann ignoriert werden, wenn das Paket mit einer aktuellen Windows Installer Version installiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="419d2-110">This warning can be ignored if you want your package to be installed using a current Windows Installer version.</span></span> <span data-ttu-id="419d2-111">Wenn Sie z. b. möchten, dass das Paket nur in Version 2,0 oder höher installiert werden kann, ändern Sie das Paket Schema (PID \_ Page count) in 200.</span><span class="sxs-lookup"><span data-stu-id="419d2-111">For example, if you want your package to be installable only on version 2.0 or later, change your package schema (PID\_PAGECOUNT) to 200.</span></span>

[<span data-ttu-id="419d2-112">Isolatedcomponent-Tabelle</span><span class="sxs-lookup"><span data-stu-id="419d2-112">IsolatedComponent Table</span></span>](isolatedcomponent-table.md)



| <span data-ttu-id="419d2-113">Frei \_ gegebene Komponente</span><span class="sxs-lookup"><span data-stu-id="419d2-113">Component\_Shared</span></span> | <span data-ttu-id="419d2-114">Komponenten \_ Anwendung</span><span class="sxs-lookup"><span data-stu-id="419d2-114">Component\_Application</span></span> |
|-------------------|------------------------|
| <span data-ttu-id="419d2-115">Component1</span><span class="sxs-lookup"><span data-stu-id="419d2-115">Component1</span></span>        | <span data-ttu-id="419d2-116">Component2</span><span class="sxs-lookup"><span data-stu-id="419d2-116">Component2</span></span>             |



 

[<span data-ttu-id="419d2-117">Zusammenfassungs Informationsdaten Strom</span><span class="sxs-lookup"><span data-stu-id="419d2-117">Summary Information Stream</span></span>](summary-information-stream.md)



| <span data-ttu-id="419d2-118">Pidt</span><span class="sxs-lookup"><span data-stu-id="419d2-118">PIDt</span></span>           | <span data-ttu-id="419d2-119">Wert</span><span class="sxs-lookup"><span data-stu-id="419d2-119">Value</span></span> |
|----------------|-------|
| <span data-ttu-id="419d2-120">PID- \_ PageCount</span><span class="sxs-lookup"><span data-stu-id="419d2-120">PID\_PAGECOUNT</span></span> | <span data-ttu-id="419d2-121">100</span><span class="sxs-lookup"><span data-stu-id="419d2-121">100</span></span>   |



 

## <a name="table-used-during-execution"></a><span data-ttu-id="419d2-122">Während der Ausführung verwendete Tabelle:</span><span class="sxs-lookup"><span data-stu-id="419d2-122">Table used during execution:</span></span>

[<span data-ttu-id="419d2-123">\_Columns-Tabelle</span><span class="sxs-lookup"><span data-stu-id="419d2-123">\_Columns table</span></span>](-columns-table.md)

## <a name="related-topics"></a><span data-ttu-id="419d2-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="419d2-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="419d2-125">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="419d2-125">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



