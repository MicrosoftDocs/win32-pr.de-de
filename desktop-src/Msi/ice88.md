---
description: ICE88 überprüft, ob das Verzeichnis, auf das in der dirproperty-Spalte der IniFile-Tabelle verwiesen wird, im Windows Installer Paket vorhanden ist.
ms.assetid: 9bb253fd-e231-4016-807d-3b1068ecff68
title: ICE88
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f59197259f8e5e1831c055618a85854d9f7c427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867687"
---
# <a name="ice88"></a><span data-ttu-id="8de92-103">ICE88</span><span class="sxs-lookup"><span data-stu-id="8de92-103">ICE88</span></span>

<span data-ttu-id="8de92-104">ICE88 überprüft, ob das Verzeichnis, auf das in der dirproperty-Spalte der [IniFile-Tabelle](inifile-table.md) verwiesen wird, im Windows Installer Paket vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="8de92-104">ICE88 validates that the directory referenced in the DirProperty column of the [IniFile table](inifile-table.md) exists in the Windows Installer package.</span></span> <span data-ttu-id="8de92-105">ICE88 gibt eine Warnung aus, wenn der dirproperty-Wert keine Eigenschaft in den Verzeichnis-, AppSearch-oder Eigenschafts Tabellen, bestimmten [Systemordner Eigenschaften](property-reference.md)oder einer Eigenschaft darstellt, die durch eine benutzerdefinierte Aktion vom Typ 51 festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="8de92-105">ICE88 issues a warning if the DirProperty value does not represent a property in the Directory, AppSearch, or Property tables, certain [system folder properties](property-reference.md), or a property set by a type 51 custom action.</span></span>

<span data-ttu-id="8de92-106">ICE88 scannt die folgenden Tabellen und Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8de92-106">ICE88 scans the following tables and properties.</span></span>

-   [<span data-ttu-id="8de92-107">Verzeichnis Tabelle</span><span class="sxs-lookup"><span data-stu-id="8de92-107">Directory Table</span></span>](directory-table.md)
-   [<span data-ttu-id="8de92-108">AppSearch-Tabelle</span><span class="sxs-lookup"><span data-stu-id="8de92-108">AppSearch Table</span></span>](appsearch-table.md)
-   [<span data-ttu-id="8de92-109">Eigenschaften Tabelle</span><span class="sxs-lookup"><span data-stu-id="8de92-109">Property Table</span></span>](property-table.md)
-   <span data-ttu-id="8de92-110">[CustomAction-Tabelle](customaction-table.md) , in der die benutzerdefinierte Aktion ein [benutzerdefinierter Aktionstyp 51](custom-action-type-51.md) ist</span><span class="sxs-lookup"><span data-stu-id="8de92-110">[CustomAction Table](customaction-table.md) , where the custom action is a [Custom Action Type 51](custom-action-type-51.md)</span></span>
-   [<span data-ttu-id="8de92-111">**ProgramFilesFolder (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="8de92-111">**ProgramFilesFolder Property**</span></span>](programfilesfolder.md)
-   [<span data-ttu-id="8de92-112">**CommonFilesFolder (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="8de92-112">**CommonFilesFolder Property**</span></span>](commonfilesfolder.md)
-   [<span data-ttu-id="8de92-113">**SystemFolder-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="8de92-113">**SystemFolder Property**</span></span>](systemfolder.md)
-   [<span data-ttu-id="8de92-114">**ProgramFiles64Folder-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="8de92-114">**ProgramFiles64Folder Property**</span></span>](programfiles64folder.md)
-   [<span data-ttu-id="8de92-115">**CommonFiles64Folder-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="8de92-115">**CommonFiles64Folder Property**</span></span>](commonfiles64folder.md)
-   [<span data-ttu-id="8de92-116">**System64Folder-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="8de92-116">**System64Folder Property**</span></span>](system64folder.md)

## <a name="result"></a><span data-ttu-id="8de92-117">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="8de92-117">Result</span></span>

<span data-ttu-id="8de92-118">ICE88 gibt die folgende Warnung aus.</span><span class="sxs-lookup"><span data-stu-id="8de92-118">ICE88 posts the following warning.</span></span>



| <span data-ttu-id="8de92-119">ICE88-Warnung</span><span class="sxs-lookup"><span data-stu-id="8de92-119">ICE88 Warning</span></span>                                                                                                                                                                  | <span data-ttu-id="8de92-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8de92-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8de92-121">Im IniFile-Tabelleneintrag (iniFile =) \[ 3 wurde \] dirproperty = \[ 1 \] nicht in den Tabellen Directory/Property/AppSearch/ca-Type51 gefunden, und es handelt sich nicht um eine der Installer-Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8de92-121">In the IniFile table entry (IniFile=) \[3\] the DirProperty=\[1\] is not found in Directory/Property/AppSearch/CA-Type51 tables and it is not one of the installer properties.</span></span> | <span data-ttu-id="8de92-122">Für jeden Datensatz in der Tabelle "inifile" liest ICE88 den Wert in der dirproperty-Spalte.</span><span class="sxs-lookup"><span data-stu-id="8de92-122">For each record in the IniFile table, ICE88 reads the value in the DirProperty column.</span></span> <span data-ttu-id="8de92-123">ICE88 scannt den Wert in der [Verzeichnis Tabelle](directory-table.md), der [AppSearch-Tabelle](appsearch-table.md)und der Eigenschaften [Tabelle](property-table.md) und scannt außerdem die Liste der Eigenschaften, die vom Installationsprogramm festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="8de92-123">ICE88 scans for the value in the [Directory Table](directory-table.md), [AppSearch Table](appsearch-table.md), and [Property Table](property-table.md) and also scans the list of properties set by the installer.</span></span> <span data-ttu-id="8de92-124">ICE88 gibt diese Warnung aus, wenn der Wert im Scan nicht gefunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="8de92-124">ICE88 posts this warning if the value cannot be found in the scan.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="8de92-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8de92-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8de92-126">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="8de92-126">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



