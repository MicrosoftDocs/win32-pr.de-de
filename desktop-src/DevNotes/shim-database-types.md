---
description: Stellt die Typen für die Haupt-und benutzerdefinierten Shimdatenbanken dar.
ms.assetid: e893963a-6130-4f65-b925-6f3d292fc86d
title: Shim-Datenbanktypen
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 789265ea945ce068d2b0b74e3358582d5e4ccd78
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747673"
---
# <a name="shim-database-types"></a><span data-ttu-id="58417-103">Shim-Datenbanktypen</span><span class="sxs-lookup"><span data-stu-id="58417-103">Shim Database Types</span></span>

<span data-ttu-id="58417-104">Stellt die Typen für die Haupt-und benutzerdefinierten Shimdatenbanken dar.</span><span class="sxs-lookup"><span data-stu-id="58417-104">Represent the types for main and custom shim databases.</span></span>



| <span data-ttu-id="58417-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="58417-105">Constant/value</span></span>                                                                                                                                                                                                                                                | <span data-ttu-id="58417-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="58417-106">Description</span></span>                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| <span id="SDB_DATABASE_MAIN"></span><span id="sdb_database_main"></span><dl> <span data-ttu-id="58417-107"><dt>**SDB \_ Datenbank- \_ Haupt**</dt> - <dt>0x80000000</dt></span><span class="sxs-lookup"><span data-stu-id="58417-107"><dt>**SDB\_DATABASE\_MAIN**</dt> <dt>0x80000000</dt></span></span> </dl>                    | <span data-ttu-id="58417-108">Die Hauptdatenbank.</span><span class="sxs-lookup"><span data-stu-id="58417-108">The main database.</span></span> <span data-ttu-id="58417-109">Wenn dieses Flag nicht vorhanden ist, handelt es sich bei der Datenbank um eine benutzerdefinierte Datenbank.</span><span class="sxs-lookup"><span data-stu-id="58417-109">If this flag is not present, the database is a custom database.</span></span><br/> |
| <span id="SDB_DATABASE_SHIM"></span><span id="sdb_database_shim"></span><dl> <span data-ttu-id="58417-110"><dt>**SDB \_ \_Datenbankshim**</dt> <dt>0x00010000 bis</dt></span><span class="sxs-lookup"><span data-stu-id="58417-110"><dt>**SDB\_DATABASE\_SHIM**</dt> <dt>0x00010000</dt></span></span> </dl>                    | <span data-ttu-id="58417-111">Die Datenbank enthält Anwendungs Einträge, für die eine shimmverbindung besteht.</span><span class="sxs-lookup"><span data-stu-id="58417-111">The database contains application entries to be shimmed.</span></span><br/>                           |
| <span id="SDB_DATABASE_MSI"></span><span id="sdb_database_msi"></span><dl> <span data-ttu-id="58417-112"><dt>**SDB \_ Datenbank- \_ MSI**</dt> <dt>0x00020000</dt></span><span class="sxs-lookup"><span data-stu-id="58417-112"><dt>**SDB\_DATABASE\_MSI**</dt> <dt>0x00020000</dt></span></span> </dl>                       | <span data-ttu-id="58417-113">Die Datenbank enthält MSI-Einträge.</span><span class="sxs-lookup"><span data-stu-id="58417-113">The database contains MSI entries.</span></span><br/>                                                 |
| <span id="SDB_DATABASE_DRIVERS"></span><span id="sdb_database_drivers"></span><dl> <span data-ttu-id="58417-114"><dt>**SDB \_ Daten Bank \_ Treiber**</dt> <dt>0x00040000</dt></span><span class="sxs-lookup"><span data-stu-id="58417-114"><dt>**SDB\_DATABASE\_DRIVERS**</dt> <dt>0x00040000</dt></span></span> </dl>           | <span data-ttu-id="58417-115">Die Datenbank enthält Treiber Blockeinträge.</span><span class="sxs-lookup"><span data-stu-id="58417-115">The database contains driver block entries.</span></span><br/>                                        |
| <span id="SDB_DATABASE_DETAILS"></span><span id="sdb_database_details"></span><dl> <span data-ttu-id="58417-116"><dt>**SDB \_ Daten Bank \_ Details**</dt> <dt>0x00080000</dt></span><span class="sxs-lookup"><span data-stu-id="58417-116"><dt>**SDB\_DATABASE\_DETAILS**</dt> <dt>0x00080000</dt></span></span> </dl>           | <span data-ttu-id="58417-117">Die Datenbank enthält AppHelp-Details.</span><span class="sxs-lookup"><span data-stu-id="58417-117">The database contains Apphelp details.</span></span><br/>                                             |
| <span id="SDB_DATABASE_SP_DETAILS"></span><span id="sdb_database_sp_details"></span><dl> <span data-ttu-id="58417-118"><dt>**SDB \_ Datenbank- \_ SP- \_ Details**</dt> <dt>0x00100000</dt></span><span class="sxs-lookup"><span data-stu-id="58417-118"><dt>**SDB\_DATABASE\_SP\_DETAILS**</dt> <dt>0x00100000</dt></span></span> </dl> | <span data-ttu-id="58417-119">Die Datenbank enthält die SP-AppHelp-Details.</span><span class="sxs-lookup"><span data-stu-id="58417-119">The database contains SP Apphelp details.</span></span><br/>                                          |
| <span id="SDB_DATABASE_RESOURCE"></span><span id="sdb_database_resource"></span><dl> <span data-ttu-id="58417-120"><dt>**SDB \_ Daten Bank \_ Ressource**</dt> <dt>0x00200000</dt></span><span class="sxs-lookup"><span data-stu-id="58417-120"><dt>**SDB\_DATABASE\_RESOURCE**</dt> <dt>0x00200000</dt></span></span> </dl>        | <span data-ttu-id="58417-121">Die Ressourcen-DLL enthält AppHelp-Details.</span><span class="sxs-lookup"><span data-stu-id="58417-121">The resource DLL contains Apphelp details.</span></span><br/>                                         |
| <span id="SDB_DATABASE_TYPE_MASK"></span><span id="sdb_database_type_mask"></span><dl> <span data-ttu-id="58417-122"><dt>**SDB \_ Datenbank \_ - \_ typmaske**</dt> <dt>0xF 02f 0000</dt></span><span class="sxs-lookup"><span data-stu-id="58417-122"><dt>**SDB\_DATABASE\_TYPE\_MASK**</dt> <dt>0xF02F0000</dt></span></span> </dl>    | <span data-ttu-id="58417-123">Eine Maske, die zum Extrahieren von Hauptdaten Bankinformationen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="58417-123">A mask used to extract main database information.</span></span><br/>                                  |
| <span id="SDB_DATABASE_MAIN_SHIM"></span><span id="sdb_database_main_shim"></span><dl> <span data-ttu-id="58417-124"><dt>**Haupt- \_ \_ \_ Shim der SDB-Datenbank**</dt></span><span class="sxs-lookup"><span data-stu-id="58417-124"><dt>**SDB\_DATABASE\_MAIN\_SHIM**</dt></span></span> </dl>                                                                    | <span data-ttu-id="58417-125">SDB- \_ Datenbank \_ Shim \| SDB- \_ Datenbank \_ MSI \| SDB- \_ Datenbank \_ Main</span><span class="sxs-lookup"><span data-stu-id="58417-125">SDB\_DATABASE\_SHIM \| SDB\_DATABASE\_MSI \| SDB\_DATABASE\_MAIN</span></span><br/>                   |
| <span id="SDB_DATABASE_MAIN_MSI"></span><span id="sdb_database_main_msi"></span><dl> <span data-ttu-id="58417-126"><dt>**SDB- \_ Datenbank- \_ Haupt- \_ MSI**</dt></span><span class="sxs-lookup"><span data-stu-id="58417-126"><dt>**SDB\_DATABASE\_MAIN\_MSI**</dt></span></span> </dl>                                                                       | <span data-ttu-id="58417-127">SDB- \_ Datenbank \_ MSI \| SDB- \_ Datenbank \_ Main</span><span class="sxs-lookup"><span data-stu-id="58417-127">SDB\_DATABASE\_MSI \| SDB\_DATABASE\_MAIN</span></span><br/>                                          |
| <span id="SDB_DATABASE_MAIN_DRIVERS"></span><span id="sdb_database_main_drivers"></span><dl> <span data-ttu-id="58417-128"><dt>**\_ \_ Haupt \_ Treiber der SDB-Datenbank**</dt></span><span class="sxs-lookup"><span data-stu-id="58417-128"><dt>**SDB\_DATABASE\_MAIN\_DRIVERS**</dt></span></span> </dl>                                                           | <span data-ttu-id="58417-129">SDB- \_ Daten Bank \_ Treiber \| SDB- \_ Datenbank \_ Main</span><span class="sxs-lookup"><span data-stu-id="58417-129">SDB\_DATABASE\_DRIVERS \| SDB\_DATABASE\_MAIN</span></span><br/>                                      |
| <span id="SDB_DATABASE_MAIN_DETAILS"></span><span id="sdb_database_main_details"></span><dl> <span data-ttu-id="58417-130"><dt>**\_ \_ Haupt \_ Details der SDB-Datenbank**</dt></span><span class="sxs-lookup"><span data-stu-id="58417-130"><dt>**SDB\_DATABASE\_MAIN\_DETAILS**</dt></span></span> </dl>                                                           | <span data-ttu-id="58417-131">SDB-Daten \_ Bank \_ Details \| SDB- \_ Datenbank \_ Main</span><span class="sxs-lookup"><span data-stu-id="58417-131">SDB\_DATABASE\_DETAILS \| SDB\_DATABASE\_MAIN</span></span><br/>                                      |
| <span id="SDB_DATABASE_MAIN_SP_DETAILS"></span><span id="sdb_database_main_sp_details"></span><dl> <span data-ttu-id="58417-132"><dt>**Haupt- \_ \_ SP- \_ \_ Details der SDB-Datenbank**</dt></span><span class="sxs-lookup"><span data-stu-id="58417-132"><dt>**SDB\_DATABASE\_MAIN\_SP\_DETAILS**</dt></span></span> </dl>                                                 | <span data-ttu-id="58417-133">SDB- \_ Datenbank \_ SP \_ Details \| SDB- \_ Datenbank \_ Main</span><span class="sxs-lookup"><span data-stu-id="58417-133">SDB\_DATABASE\_SP\_DETAILS \| SDB\_DATABASE\_MAIN</span></span><br/>                                  |
| <span id="SDB_DATABASE_MAIN_RESOURCE"></span><span id="sdb_database_main_resource"></span><dl> <span data-ttu-id="58417-134"><dt>**\_ \_ Haupt \_ Ressource der SDB-Datenbank**</dt></span><span class="sxs-lookup"><span data-stu-id="58417-134"><dt>**SDB\_DATABASE\_MAIN\_RESOURCE**</dt></span></span> </dl>                                                        | <span data-ttu-id="58417-135">SDB- \_ Daten Bank \_ Ressource \| SDB- \_ Datenbank \_ Main</span><span class="sxs-lookup"><span data-stu-id="58417-135">SDB\_DATABASE\_RESOURCE \| SDB\_DATABASE\_MAIN</span></span><br/>                                     |



## <a name="requirements"></a><span data-ttu-id="58417-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="58417-136">Requirements</span></span>



| <span data-ttu-id="58417-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="58417-137">Requirement</span></span> | <span data-ttu-id="58417-138">Wert</span><span class="sxs-lookup"><span data-stu-id="58417-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="58417-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="58417-139">Minimum supported client</span></span><br/> | <span data-ttu-id="58417-140">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="58417-140">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="58417-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="58417-141">Minimum supported server</span></span><br/> | <span data-ttu-id="58417-142">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="58417-142">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="58417-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="58417-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58417-144">**Sdbopendatabase**</span><span class="sxs-lookup"><span data-stu-id="58417-144">**SdbOpenDatabase**</span></span>](sdbopendatabase.md)
</dt> </dl>

 

 




