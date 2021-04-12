---
description: Öffnet die Shimdatenbank.
ms.assetid: ece1bd39-20a1-42e6-8e2b-1d38f7223d42
title: Sdbinitdatabase-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbInitDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 7a3c63fa712aec988dbf13c4fb7f9fddbf159fdd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104482894"
---
# <a name="sdbinitdatabase-function"></a><span data-ttu-id="8a646-103">Sdbinitdatabase-Funktion</span><span class="sxs-lookup"><span data-stu-id="8a646-103">SdbInitDatabase function</span></span>

<span data-ttu-id="8a646-104">Öffnet die Shimdatenbank.</span><span class="sxs-lookup"><span data-stu-id="8a646-104">Opens the shim database.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a646-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a646-105">Syntax</span></span>


```C++
HSDB WINAPI SdbInitDatabase(
  _In_ DWORD   dwFlags,
  _In_ LPCTSTR pszDatabasePath
);
```



## <a name="parameters"></a><span data-ttu-id="8a646-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a646-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a646-107">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8a646-107">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a646-108">Dieser Parameter gibt das Format des Pfads im *pszdatabasepath* -Parameter an.</span><span class="sxs-lookup"><span data-stu-id="8a646-108">This parameter specifies the format of the path in the *pszDatabasePath* parameter.</span></span> <span data-ttu-id="8a646-109">Dieses Argument einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="8a646-109">It can be one of the following values.</span></span>



| <span data-ttu-id="8a646-110">Wert</span><span class="sxs-lookup"><span data-stu-id="8a646-110">Value</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="8a646-111">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="8a646-111">Meaning</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span id="HID_DOS_PATHS"></span><span id="hid_dos_paths"></span><dl> <span data-ttu-id="8a646-112"><dt>**Versteckt \_ DOS- \_ Pfade**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="8a646-112"><dt>**HID\_DOS\_PATHS**</dt> <dt>0x00000001</dt></span></span> </dl>                             | <span data-ttu-id="8a646-113">Ein MS-DOS-stilpfad.</span><span class="sxs-lookup"><span data-stu-id="8a646-113">An MS-DOS style path.</span></span><br/>                                                                       |
| <span id="HID_DATABASE_FULLPATH"></span><span id="hid_database_fullpath"></span><dl> <span data-ttu-id="8a646-114"><dt>**Versteckt \_ Daten Bank \_ Vollständiger Pfad**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="8a646-114"><dt>**HID\_DATABASE\_FULLPATH**</dt> <dt>0x00000002</dt></span></span> </dl>     | <span data-ttu-id="8a646-115">Ein vollständiger Pfad.</span><span class="sxs-lookup"><span data-stu-id="8a646-115">A full path.</span></span><br/>                                                                                |
| <span id="HID_NO_DATABASE"></span><span id="hid_no_database"></span><dl> <span data-ttu-id="8a646-116"><dt>**Versteckt \_ Keine \_ Datenbank**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="8a646-116"><dt>**HID\_NO\_DATABASE**</dt> <dt>0x00000004</dt></span></span> </dl>                       | <span data-ttu-id="8a646-117">Der *pszdatabasepath* -Parameter wird ignoriert, und es wird keine Datenbank geöffnet.</span><span class="sxs-lookup"><span data-stu-id="8a646-117">The *pszDatabasePath* parameter is ignored and no database is opened.</span></span><br/>                       |
| <span id="HID_DATABASE_TYPE_MASK"></span><span id="hid_database_type_mask"></span><dl> <span data-ttu-id="8a646-118"><dt>**Versteckt \_ Datenbank \_ - \_ typmaske**</dt> <dt>0xF 00F 0000</dt></span><span class="sxs-lookup"><span data-stu-id="8a646-118"><dt>**HID\_DATABASE\_TYPE\_MASK**</dt> <dt>0xF00F0000</dt></span></span> </dl> | <span data-ttu-id="8a646-119">Dieser Parameter gibt eine vordefinierte Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="8a646-119">This parameter specifies a predefined database.</span></span> <span data-ttu-id="8a646-120">Der *pszdatabasepath* -Parameter wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="8a646-120">The *pszDatabasePath* parameter is ignored.</span></span><br/> |



 

<span data-ttu-id="8a646-121">Wenn *dwFlags* eine **versteckte \_ \_ Datentyp \_ Maske** enthält, kann dieser Parameter auch einen der folgenden Werte enthalten.</span><span class="sxs-lookup"><span data-stu-id="8a646-121">If *dwFlags* contains **HID\_DATA\_TYPE\_MASK**, this parameter can also include one of the following values.</span></span>



| <span data-ttu-id="8a646-122">Wert</span><span class="sxs-lookup"><span data-stu-id="8a646-122">Value</span></span>                                                                                                                                                                                                                                                               | <span data-ttu-id="8a646-123">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="8a646-123">Meaning</span></span>                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <span id="SDB_DATABASE_MAIN_SHIM"></span><span id="sdb_database_main_shim"></span><dl> <span data-ttu-id="8a646-124"><dt>**SDB \_ Datenbank- \_ Haupt- \_ Shim**</dt> <dt>0x80030000</dt></span><span class="sxs-lookup"><span data-stu-id="8a646-124"><dt>**SDB\_DATABASE\_MAIN\_SHIM**</dt> <dt>0x80030000</dt></span></span> </dl>          | <span data-ttu-id="8a646-125">Anwendungsshimdatenbank.</span><span class="sxs-lookup"><span data-stu-id="8a646-125">Application shim database.</span></span><br/>         |
| <span id="SDB_DATABASE_MAIN_MSI"></span><span id="sdb_database_main_msi"></span><dl> <span data-ttu-id="8a646-126"><dt>**SDB \_ Datenbank- \_ Haupt- \_ MSI**</dt> <dt>0x80020000</dt></span><span class="sxs-lookup"><span data-stu-id="8a646-126"><dt>**SDB\_DATABASE\_MAIN\_MSI**</dt> <dt>0x80020000</dt></span></span> </dl>             | <span data-ttu-id="8a646-127">MSI-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="8a646-127">MSI database.</span></span><br/>                      |
| <span id="SDB_DATABASE_MAIN_DRIVERS"></span><span id="sdb_database_main_drivers"></span><dl> <span data-ttu-id="8a646-128"><dt>**SDB \_ \_Haupt \_ Treiber der Datenbank**</dt> <dt>0x80040000</dt></span><span class="sxs-lookup"><span data-stu-id="8a646-128"><dt>**SDB\_DATABASE\_MAIN\_DRIVERS**</dt> <dt>0x80040000</dt></span></span> </dl> | <span data-ttu-id="8a646-129">Die Datenbank der zu blockierenden Treiber.</span><span class="sxs-lookup"><span data-stu-id="8a646-129">Database of drivers to be blocked.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="8a646-130">*pszdatabasepath* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8a646-130">*pszDatabasePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a646-131">Der Pfad zur Datenbank.</span><span class="sxs-lookup"><span data-stu-id="8a646-131">The path to the database.</span></span> <span data-ttu-id="8a646-132">Dieser Parameter kann **null** sein, wenn der *dwFlags* -Parameter eine vordefinierte Datenbank angibt.</span><span class="sxs-lookup"><span data-stu-id="8a646-132">This parameter can be **NULL** if the *dwFlags* parameter specifies a predefined database.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a646-133">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8a646-133">Return value</span></span>

<span data-ttu-id="8a646-134">Die-Funktion gibt ein Handle für die geöffnete Datenbank zurück.</span><span class="sxs-lookup"><span data-stu-id="8a646-134">The function returns a handle to the opened database.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a646-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8a646-135">Requirements</span></span>



| <span data-ttu-id="8a646-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8a646-136">Requirement</span></span> | <span data-ttu-id="8a646-137">Wert</span><span class="sxs-lookup"><span data-stu-id="8a646-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a646-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8a646-138">Minimum supported client</span></span><br/> | <span data-ttu-id="8a646-139">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8a646-139">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="8a646-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8a646-140">Minimum supported server</span></span><br/> | <span data-ttu-id="8a646-141">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8a646-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8a646-142">DLL</span><span class="sxs-lookup"><span data-stu-id="8a646-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a646-143"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a646-143"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a646-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8a646-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a646-145">**Sdbgetapppatchdir**</span><span class="sxs-lookup"><span data-stu-id="8a646-145">**SdbGetAppPatchDir**</span></span>](sdbgetapppatchdir.md)
</dt> <dt>

[<span data-ttu-id="8a646-146">**Sdbgetmatchingexe**</span><span class="sxs-lookup"><span data-stu-id="8a646-146">**SdbGetMatchingExe**</span></span>](sdbgetmatchingexe.md)
</dt> <dt>

[<span data-ttu-id="8a646-147">**Sdbreleasematchingexe**</span><span class="sxs-lookup"><span data-stu-id="8a646-147">**SdbReleaseMatchingExe**</span></span>](sdbreleasematchingexe.md)
</dt> <dt>

[<span data-ttu-id="8a646-148">**Sdbtagrebtotagid**</span><span class="sxs-lookup"><span data-stu-id="8a646-148">**SdbTagRefToTagID**</span></span>](sdbtagreftotagid.md)
</dt> </dl>

 

 




