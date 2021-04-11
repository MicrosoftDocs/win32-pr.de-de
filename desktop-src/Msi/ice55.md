---
description: ICE55 überprüft, ob alle lockberechtigungsobjekte vorhanden sind und gültige Berechtigungs Werte aufweisen.
ms.assetid: e23e43ce-942f-4f6b-b5fd-cf366f7a7fe5
title: ICE55
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 239093e3502a1731c3248918750c18aa1b3e1f18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217352"
---
# <a name="ice55"></a><span data-ttu-id="239cd-103">ICE55</span><span class="sxs-lookup"><span data-stu-id="239cd-103">ICE55</span></span>

<span data-ttu-id="239cd-104">ICE55 überprüft, ob alle lockberechtigungsobjekte vorhanden sind und gültige Berechtigungs Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="239cd-104">ICE55 validates that all LockPermission objects exist and have valid permission values.</span></span>

## <a name="result"></a><span data-ttu-id="239cd-105">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="239cd-105">Result</span></span>

<span data-ttu-id="239cd-106">ICE55 Posten Sie einen Fehler, wenn ein in der [lockberechtigungstabelle](lockpermissions-table.md) aufgelistetes lockobject-Objekt nicht vorhanden ist oder wenn keine Berechtigungsebene in der Berechtigungs Spalte angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="239cd-106">ICE55 post an error if a LockObject listed in the [LockPermissions table](lockpermissions-table.md) does not exist or if no privilege level is specified in the Permission column.</span></span>

## <a name="example"></a><span data-ttu-id="239cd-107">Beispiel</span><span class="sxs-lookup"><span data-stu-id="239cd-107">Example</span></span>

<span data-ttu-id="239cd-108">ICE55 würde die folgenden Fehler für das Beispiel melden.</span><span class="sxs-lookup"><span data-stu-id="239cd-108">ICE55 would report the following errors for the example.</span></span>

``` syntax
LockObject 'File1'.'File'.''.'guest' in the LockPermissions table 
    has a null Permission value. 
Could not find item 'File3' in table 'File' which is referenced 
    in the LockPermissions table.
```

<span data-ttu-id="239cd-109">[Lockberechtigungs Tabelle](lockpermissions-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="239cd-109">[LockPermissions Table](lockpermissions-table.md) (partial)</span></span>



| <span data-ttu-id="239cd-110">LockObject</span><span class="sxs-lookup"><span data-stu-id="239cd-110">LockObject</span></span> | <span data-ttu-id="239cd-111">Tabelle</span><span class="sxs-lookup"><span data-stu-id="239cd-111">Table</span></span> | <span data-ttu-id="239cd-112">Domain</span><span class="sxs-lookup"><span data-stu-id="239cd-112">Domain</span></span> | <span data-ttu-id="239cd-113">Benutzer</span><span class="sxs-lookup"><span data-stu-id="239cd-113">User</span></span>  | <span data-ttu-id="239cd-114">Berechtigung</span><span class="sxs-lookup"><span data-stu-id="239cd-114">Permission</span></span> |
|------------|-------|--------|-------|------------|
| <span data-ttu-id="239cd-115">Datei1</span><span class="sxs-lookup"><span data-stu-id="239cd-115">File1</span></span>      | <span data-ttu-id="239cd-116">File</span><span class="sxs-lookup"><span data-stu-id="239cd-116">File</span></span>  |        | <span data-ttu-id="239cd-117">guest</span><span class="sxs-lookup"><span data-stu-id="239cd-117">guest</span></span> |            |
| <span data-ttu-id="239cd-118">Datei3</span><span class="sxs-lookup"><span data-stu-id="239cd-118">File3</span></span>      | <span data-ttu-id="239cd-119">File</span><span class="sxs-lookup"><span data-stu-id="239cd-119">File</span></span>  |        | <span data-ttu-id="239cd-120">guest</span><span class="sxs-lookup"><span data-stu-id="239cd-120">guest</span></span> | <span data-ttu-id="239cd-121">1</span><span class="sxs-lookup"><span data-stu-id="239cd-121">1</span></span>          |



 

<span data-ttu-id="239cd-122">[Dateitabelle](file-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="239cd-122">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="239cd-123">File</span><span class="sxs-lookup"><span data-stu-id="239cd-123">File</span></span>  | <span data-ttu-id="239cd-124">Version</span><span class="sxs-lookup"><span data-stu-id="239cd-124">Version</span></span> | <span data-ttu-id="239cd-125">Sprache</span><span class="sxs-lookup"><span data-stu-id="239cd-125">Language</span></span> |
|-------|---------|----------|
| <span data-ttu-id="239cd-126">Datei1</span><span class="sxs-lookup"><span data-stu-id="239cd-126">File1</span></span> | <span data-ttu-id="239cd-127">Datei2</span><span class="sxs-lookup"><span data-stu-id="239cd-127">File2</span></span>   |          |
| <span data-ttu-id="239cd-128">Datei2</span><span class="sxs-lookup"><span data-stu-id="239cd-128">File2</span></span> | <span data-ttu-id="239cd-129">1.0.0.0</span><span class="sxs-lookup"><span data-stu-id="239cd-129">1.0.0.0</span></span> | <span data-ttu-id="239cd-130">1033</span><span class="sxs-lookup"><span data-stu-id="239cd-130">1033</span></span>     |



 

<span data-ttu-id="239cd-131">Das Objekt file1 weist in der Berechtigungs Spalte den Wert NULL auf.</span><span class="sxs-lookup"><span data-stu-id="239cd-131">The object File1 has a null in the Permission column.</span></span> <span data-ttu-id="239cd-132">Jede Zeile muss über einen Wert in der Spalte "Berechtigungen" verfügen.</span><span class="sxs-lookup"><span data-stu-id="239cd-132">Each row must have a value in the Permissions column.</span></span> <span data-ttu-id="239cd-133">Um diesen Fehler zu beheben, geben Sie einen numerischen Wert in dieser Spalte an.</span><span class="sxs-lookup"><span data-stu-id="239cd-133">To fix this error specify a numeric value in this column.</span></span> <span data-ttu-id="239cd-134">Wenn für dieses Objekt keine Berechtigungen erforderlich sind, sollten Sie die Zeile entfernen.</span><span class="sxs-lookup"><span data-stu-id="239cd-134">If no privileges are needed for this object then you should remove the row.</span></span>

<span data-ttu-id="239cd-135">Das in der lockberechtigungs-Tabelle beschriebene Objekt datei3 ist in der Dateitabelle nicht aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="239cd-135">The object File3 described in the LockPermissions table is not listed in the File table.</span></span> <span data-ttu-id="239cd-136">Um diesen Fehler zu beheben, verweisen Sie auf ein gültiges-Objekt.</span><span class="sxs-lookup"><span data-stu-id="239cd-136">To fix this error refer to a valid object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="239cd-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="239cd-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="239cd-138">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="239cd-138">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



