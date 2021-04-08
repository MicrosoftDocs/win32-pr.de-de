---
title: WINBIO_DATABASE_TYPE Konstanten (winbio \_ types. h)
description: Flags, die für den Attribute-Member der Struktur des winbio- \_ Speicher Schemas verwendet werden können \_ .
ms.assetid: 07e7e91c-3ca6-41cd-a2c7-ac43bb5156a6
topic_type:
- apiref
api_name:
- WINBIO_DATABASE_TYPE_MASK
- WINBIO_DATABASE_TYPE_FILE
- WINBIO_DATABASE_TYPE_DBMS
- WINBIO_DATABASE_TYPE_ONCHIP
- WINBIO_DATABASE_TYPE_SMARTCARD
- WINBIO_DATABASE_FLAG_MASK
- WINBIO_DATABASE_FLAG_REMOVABLE
- WINBIO_DATABASE_FLAG_REMOTE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acd67f49c5fa689fb4418789aae7c4d6c9a305a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741528"
---
# <a name="winbio_database_type-constants"></a><span data-ttu-id="6de5d-103">Winbio- \_ Daten \_ Banktyp Konstanten</span><span class="sxs-lookup"><span data-stu-id="6de5d-103">WINBIO\_DATABASE\_TYPE Constants</span></span>

<span data-ttu-id="6de5d-104">Die folgenden Flags können für den **Attribute** -Member der Struktur des [**winbio- \_ Speicher \_ Schemas**](winbio-storage-schema.md) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6de5d-104">The following flags can be used for the **Attributes** member of the [**WINBIO\_STORAGE\_SCHEMA**](winbio-storage-schema.md) structure.</span></span>



| <span data-ttu-id="6de5d-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="6de5d-105">Constant/value</span></span>                                                                                                                                                                                                                                                                     | <span data-ttu-id="6de5d-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6de5d-106">Description</span></span>                                                                                                                  |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATABASE_TYPE_MASK"></span><span id="winbio_database_type_mask"></span><dl> <span data-ttu-id="6de5d-107"><dt>**Winbio \_ Daten \_ Bank \_ typmaske**</dt> <dt>0X0000FFFF</dt></span><span class="sxs-lookup"><span data-stu-id="6de5d-107"><dt>**WINBIO\_DATABASE\_TYPE\_MASK**</dt> <dt>0x0000FFFF</dt></span></span> </dl>                | <span data-ttu-id="6de5d-108">Stellt eine Maske für alle \_ \_ typbits dar.</span><span class="sxs-lookup"><span data-stu-id="6de5d-108">Represents a mask for all of the \_TYPE\_ bits.</span></span><br/>                                                                   |
| <span id="WINBIO_DATABASE_TYPE_FILE"></span><span id="winbio_database_type_file"></span><dl> <span data-ttu-id="6de5d-109"><dt>**Winbio \_ \_ \_ Dateityp Datei**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="6de5d-109"><dt>**WINBIO\_DATABASE\_TYPE\_FILE**</dt> <dt>0x00000001</dt></span></span> </dl>                | <span data-ttu-id="6de5d-110">Die Datenbank ist in einer Datei enthalten.</span><span class="sxs-lookup"><span data-stu-id="6de5d-110">The database is contained in a file.</span></span><br/>                                                                              |
| <span id="WINBIO_DATABASE_TYPE_DBMS"></span><span id="winbio_database_type_dbms"></span><dl> <span data-ttu-id="6de5d-111"><dt>**Winbio \_ Database \_ Type \_ DBMS**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="6de5d-111"><dt>**WINBIO\_DATABASE\_TYPE\_DBMS**</dt> <dt>0x00000002</dt></span></span> </dl>                | <span data-ttu-id="6de5d-112">Die Datenbank wird von einer externen DBMS-Komponente (Database Management System) verwaltet, z. b. Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="6de5d-112">The database is managed by an external database management system (DBMS) component, such as Microsoft SQL Server.</span></span><br/> |
| <span id="WINBIO_DATABASE_TYPE_ONCHIP"></span><span id="winbio_database_type_onchip"></span><dl> <span data-ttu-id="6de5d-113"><dt>**Winbio \_ Database \_ Type \_ Onchip**</dt> <dt>0x00000003</dt></span><span class="sxs-lookup"><span data-stu-id="6de5d-113"><dt>**WINBIO\_DATABASE\_TYPE\_ONCHIP**</dt> <dt>0x00000003</dt></span></span> </dl>          | <span data-ttu-id="6de5d-114">Die Datenbank befindet sich auf dem biometrischen Sensor.</span><span class="sxs-lookup"><span data-stu-id="6de5d-114">The database resides on the biometric sensor.</span></span><br/>                                                                     |
| <span id="WINBIO_DATABASE_TYPE_SMARTCARD"></span><span id="winbio_database_type_smartcard"></span><dl> <span data-ttu-id="6de5d-115"><dt>**Winbio \_ Database \_ Type \_ Smartcard**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="6de5d-115"><dt>**WINBIO\_DATABASE\_TYPE\_SMARTCARD**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="6de5d-116">Die Datenbank befindet sich auf einer Smartcard.</span><span class="sxs-lookup"><span data-stu-id="6de5d-116">The database resides on a smart card.</span></span><br/>                                                                             |
| <span id="WINBIO_DATABASE_FLAG_MASK"></span><span id="winbio_database_flag_mask"></span><dl> <span data-ttu-id="6de5d-117"><dt>**Winbio \_ \_Datenbankflag- \_ Maske**</dt> <dt>0xFFFF0000</dt></span><span class="sxs-lookup"><span data-stu-id="6de5d-117"><dt>**WINBIO\_DATABASE\_FLAG\_MASK**</dt> <dt>0xFFFF0000</dt></span></span> </dl>                | <span data-ttu-id="6de5d-118">Stellt eine Maske für alle \_ \_ Flagbits dar.</span><span class="sxs-lookup"><span data-stu-id="6de5d-118">Represents a mask for all of the \_FLAG\_ bits.</span></span><br/>                                                                   |
| <span id="WINBIO_DATABASE_FLAG_REMOVABLE"></span><span id="winbio_database_flag_removable"></span><dl> <span data-ttu-id="6de5d-119"><dt>**Winbio \_ \_Datenbankflag \_**</dt> -Wechsel <dt>0x00010000 bis</dt></span><span class="sxs-lookup"><span data-stu-id="6de5d-119"><dt>**WINBIO\_DATABASE\_FLAG\_REMOVABLE**</dt> <dt>0x00010000</dt></span></span> </dl> | <span data-ttu-id="6de5d-120">Das Speichermedium mit der Datenbank kann physisch vom Computer entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="6de5d-120">The storage medium containing the database can be physically removed from the computer.</span></span><br/>                           |
| <span id="WINBIO_DATABASE_FLAG_REMOTE"></span><span id="winbio_database_flag_remote"></span><dl> <span data-ttu-id="6de5d-121"><dt>**Winbio \_ \_Datenbankflag \_ Remote**</dt> <dt>0x00020000</dt></span><span class="sxs-lookup"><span data-stu-id="6de5d-121"><dt>**WINBIO\_DATABASE\_FLAG\_REMOTE**</dt> <dt>0x00020000</dt></span></span> </dl>          | <span data-ttu-id="6de5d-122">Die Datenbank befindet sich auf einem Remote Computer.</span><span class="sxs-lookup"><span data-stu-id="6de5d-122">The database resides on a remote computer.</span></span><br/>                                                                        |



## <a name="requirements"></a><span data-ttu-id="6de5d-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6de5d-123">Requirements</span></span>



| <span data-ttu-id="6de5d-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6de5d-124">Requirement</span></span> | <span data-ttu-id="6de5d-125">Wert</span><span class="sxs-lookup"><span data-stu-id="6de5d-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6de5d-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6de5d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="6de5d-127">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6de5d-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="6de5d-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6de5d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="6de5d-129">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6de5d-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="6de5d-130">Header</span><span class="sxs-lookup"><span data-stu-id="6de5d-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="6de5d-131"><dt>Winbio \_ types. h (Include winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6de5d-131"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6de5d-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6de5d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6de5d-133">Client Anwendungs Konstanten</span><span class="sxs-lookup"><span data-stu-id="6de5d-133">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





