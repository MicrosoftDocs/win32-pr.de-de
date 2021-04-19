---
title: WINBIO_STORAGE_SCHEMA Struktur (winbio \_ types. h)
description: Beschreibt die Funktionen eines biometrischen Speicher Adapters.
ms.assetid: e4924803-5a1b-4e0a-b2cb-01d018d27ba1
keywords:
- WINBIO_STORAGE_SCHEMA Struktur Windows-Biometrieframework-API
- PWINBIO_STORAGE_SCHEMA Struktur Zeiger Windows-Biometrieframework API
topic_type:
- apiref
api_name:
- WINBIO_STORAGE_SCHEMA
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28db23d55a7b3e43caaae5a88ca4bbf32fdf1178
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346762"
---
# <a name="winbio_storage_schema-structure"></a><span data-ttu-id="ef79d-105">Struktur des winbio- \_ Speicher \_ Schemas</span><span class="sxs-lookup"><span data-stu-id="ef79d-105">WINBIO\_STORAGE\_SCHEMA structure</span></span>

<span data-ttu-id="ef79d-106">In der Struktur des **winbio- \_ Speicher \_ Schemas** werden die Funktionen eines biometrischen Speicher Adapters beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ef79d-106">The **WINBIO\_STORAGE\_SCHEMA** structure describes the capabilities of a biometric storage adapter.</span></span> <span data-ttu-id="ef79d-107">Diese Struktur wird von der Funktion [**winbioenumdatenbanken**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases) verwendet.</span><span class="sxs-lookup"><span data-stu-id="ef79d-107">This structure is used by the [**WinBioEnumDatabases**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef79d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef79d-108">Syntax</span></span>


```C++
typedef struct _WINBIO_STORAGE_SCHEMA {
  WINBIO_BIOMETRIC_TYPE BiometricFactor;
  WINBIO_UUID           DatabaseId;
  WINBIO_UUID           DataFormat;
  ULONG                 Attributes;
  WINBIO_STRING         FilePath;
  WINBIO_STRING         ConnectionString;
} WINBIO_STORAGE_SCHEMA, *PWINBIO_STORAGE_SCHEMA;
```



## <a name="members"></a><span data-ttu-id="ef79d-109">Member</span><span class="sxs-lookup"><span data-stu-id="ef79d-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="ef79d-110">**Biometricfactor**</span><span class="sxs-lookup"><span data-stu-id="ef79d-110">**BiometricFactor**</span></span>
</dt> <dd>

<span data-ttu-id="ef79d-111">Der Typ der in der Datenbank gespeicherten biometrischen Messung.</span><span class="sxs-lookup"><span data-stu-id="ef79d-111">The type of biometric measurement saved in the database.</span></span>

</dd> <dt>

<span data-ttu-id="ef79d-112">**DatabaseID**</span><span class="sxs-lookup"><span data-stu-id="ef79d-112">**DatabaseId**</span></span>
</dt> <dd>

<span data-ttu-id="ef79d-113">Eine GUID, die die Datenbank identifiziert.</span><span class="sxs-lookup"><span data-stu-id="ef79d-113">A GUID that identifies the database.</span></span>

</dd> <dt>

<span data-ttu-id="ef79d-114">**DataFormat**</span><span class="sxs-lookup"><span data-stu-id="ef79d-114">**DataFormat**</span></span>
</dt> <dd>

<span data-ttu-id="ef79d-115">Eine GUID, die das Format der Vorlagen in der Datenbank identifiziert.</span><span class="sxs-lookup"><span data-stu-id="ef79d-115">A GUID that identifies the format of the templates in the database.</span></span>

</dd> <dt>

<span data-ttu-id="ef79d-116">**Attribute**</span><span class="sxs-lookup"><span data-stu-id="ef79d-116">**Attributes**</span></span>
</dt> <dd>

<span data-ttu-id="ef79d-117">Informationen zu den Merkmalen der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="ef79d-117">Information about the characteristics of the database.</span></span> <span data-ttu-id="ef79d-118">Hierbei kann es sich um ein bitweises **or** der folgenden Konstanten handeln.</span><span class="sxs-lookup"><span data-stu-id="ef79d-118">This can be a bitwise **OR** of the following constants.</span></span>



| <span data-ttu-id="ef79d-119">Wert</span><span class="sxs-lookup"><span data-stu-id="ef79d-119">Value</span></span>                                                                                                                                                                                                                                                                              | <span data-ttu-id="ef79d-120">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ef79d-120">Meaning</span></span>                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="WINBIO_DATABASE_FLAG_MASK"></span><span id="winbio_database_flag_mask"></span><dl> <span data-ttu-id="ef79d-121"><dt>**Winbio \_ \_Datenbankflag- \_ Maske**</dt> <dt>0xFFFF0000</dt></span><span class="sxs-lookup"><span data-stu-id="ef79d-121"><dt>**WINBIO\_DATABASE\_FLAG\_MASK**</dt> <dt>0xFFFF0000</dt></span></span> </dl>                | <span data-ttu-id="ef79d-122">Stellt eine Maske für die Flagbits dar.</span><span class="sxs-lookup"><span data-stu-id="ef79d-122">Represents a mask for the flag bits.</span></span><br/>                     |
| <span id="WINBIO_DATABASE_FLAG_REMOTE"></span><span id="winbio_database_flag_remote"></span><dl> <span data-ttu-id="ef79d-123"><dt>**Winbio \_ \_Datenbankflag \_ Remote**</dt> <dt>0x00020000</dt></span><span class="sxs-lookup"><span data-stu-id="ef79d-123"><dt>**WINBIO\_DATABASE\_FLAG\_REMOTE**</dt> <dt>0x00020000</dt></span></span> </dl>          | <span data-ttu-id="ef79d-124">Die Datenbank befindet sich auf einem Remote Computer.</span><span class="sxs-lookup"><span data-stu-id="ef79d-124">The database resides on a remote computer.</span></span><br/>               |
| <span id="WINBIO_DATABASE_FLAG_REMOVABLE"></span><span id="winbio_database_flag_removable"></span><dl> <span data-ttu-id="ef79d-125"><dt>**Winbio \_ \_Datenbankflag \_**</dt> -Wechsel <dt>0x00010000 bis</dt></span><span class="sxs-lookup"><span data-stu-id="ef79d-125"><dt>**WINBIO\_DATABASE\_FLAG\_REMOVABLE**</dt> <dt>0x00010000</dt></span></span> </dl> | <span data-ttu-id="ef79d-126">Die Datenbank befindet sich auf einem Wechsel Datenträger.</span><span class="sxs-lookup"><span data-stu-id="ef79d-126">The database resides on a removable drive.</span></span><br/>               |
| <span id="WINBIO_DATABASE_TYPE_DBMS"></span><span id="winbio_database_type_dbms"></span><dl> <span data-ttu-id="ef79d-127"><dt>**Winbio \_ Database \_ Type \_ DBMS**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="ef79d-127"><dt>**WINBIO\_DATABASE\_TYPE\_DBMS**</dt> <dt>0x00000002</dt></span></span> </dl>                | <span data-ttu-id="ef79d-128">Die Datenbank wird von einem Datenbankverwaltungssystem verwaltet.</span><span class="sxs-lookup"><span data-stu-id="ef79d-128">The database is managed by a database management system.</span></span><br/> |
| <span id="WINBIO_DATABASE_TYPE_FILE"></span><span id="winbio_database_type_file"></span><dl> <span data-ttu-id="ef79d-129"><dt>**Winbio \_ \_ \_ Dateityp Datei**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="ef79d-129"><dt>**WINBIO\_DATABASE\_TYPE\_FILE**</dt> <dt>0x00000001</dt></span></span> </dl>                | <span data-ttu-id="ef79d-130">Die Datenbank ist in einer Datei enthalten.</span><span class="sxs-lookup"><span data-stu-id="ef79d-130">The database is contained in a file.</span></span><br/>                     |
| <span id="WINBIO_DATABASE_TYPE_MASK"></span><span id="winbio_database_type_mask"></span><dl> <span data-ttu-id="ef79d-131"><dt>**Winbio \_ Daten \_ Bank \_ typmaske**</dt> <dt>0X0000FFFF</dt></span><span class="sxs-lookup"><span data-stu-id="ef79d-131"><dt>**WINBIO\_DATABASE\_TYPE\_MASK**</dt> <dt>0x0000FFFF</dt></span></span> </dl>                | <span data-ttu-id="ef79d-132">Stellt eine Maske für die typbits dar.</span><span class="sxs-lookup"><span data-stu-id="ef79d-132">Represents a mask for the type bits.</span></span><br/>                     |
| <span id="WINBIO_DATABASE_TYPE_ONCHIP"></span><span id="winbio_database_type_onchip"></span><dl> <span data-ttu-id="ef79d-133"><dt>**Winbio \_ Database \_ Type \_ Onchip**</dt> <dt>0x00000003</dt></span><span class="sxs-lookup"><span data-stu-id="ef79d-133"><dt>**WINBIO\_DATABASE\_TYPE\_ONCHIP**</dt> <dt>0x00000003</dt></span></span> </dl>          | <span data-ttu-id="ef79d-134">Die Datenbank befindet sich auf dem biometrischen Sensor.</span><span class="sxs-lookup"><span data-stu-id="ef79d-134">The database resides on the biometric sensor.</span></span><br/>            |
| <span id="WINBIO_DATABASE_TYPE_SMARTCARD"></span><span id="winbio_database_type_smartcard"></span><dl> <span data-ttu-id="ef79d-135"><dt>**Winbio \_ Database \_ Type \_ Smartcard**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="ef79d-135"><dt>**WINBIO\_DATABASE\_TYPE\_SMARTCARD**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="ef79d-136">Die Datenbank befindet sich auf einer Smartcard.</span><span class="sxs-lookup"><span data-stu-id="ef79d-136">The database resides on a smart card.</span></span><br/>                    |



 

</dd> <dt>

<span data-ttu-id="ef79d-137">**FilePath**</span><span class="sxs-lookup"><span data-stu-id="ef79d-137">**FilePath**</span></span>
</dt> <dd>

<span data-ttu-id="ef79d-138">Der Pfad und der Dateiname der Datenbank, wenn Sie sich auf dem Computer Datenträger befindet.</span><span class="sxs-lookup"><span data-stu-id="ef79d-138">The path and file name of the database if it resides on the computer disk.</span></span>

</dd> <dt>

<span data-ttu-id="ef79d-139">**ConnectionString**</span><span class="sxs-lookup"><span data-stu-id="ef79d-139">**ConnectionString**</span></span>
</dt> <dd>

<span data-ttu-id="ef79d-140">Ein Zeichen folgen Wert, der an einen Datenbankserver gesendet werden kann, um die Datenbank zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="ef79d-140">A string value that can be sent to a database server to identify the database.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ef79d-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ef79d-141">Requirements</span></span>



| <span data-ttu-id="ef79d-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ef79d-142">Requirement</span></span> | <span data-ttu-id="ef79d-143">Wert</span><span class="sxs-lookup"><span data-stu-id="ef79d-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef79d-144">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ef79d-144">Minimum supported client</span></span><br/> | <span data-ttu-id="ef79d-145">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ef79d-145">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="ef79d-146">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ef79d-146">Minimum supported server</span></span><br/> | <span data-ttu-id="ef79d-147">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ef79d-147">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="ef79d-148">Header</span><span class="sxs-lookup"><span data-stu-id="ef79d-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef79d-149"><dt>Winbio \_ types. h (Include winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ef79d-149"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef79d-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ef79d-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef79d-151">Client Anwendungs Strukturen</span><span class="sxs-lookup"><span data-stu-id="ef79d-151">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="ef79d-152">**Winbioenumdatenbanken**</span><span class="sxs-lookup"><span data-stu-id="ef79d-152">**WinBioEnumDatabases**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases)
</dt> </dl>

 

 





