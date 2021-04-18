---
description: Ruft den Status des Offlinedateien Caches ab.
ms.assetid: a8cc0dbb-0005-4e74-892e-898e2ebe0465
title: Cscquerydatabasestatus-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCQueryDatabaseStatus
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: badd869306290609ccadeba80e6ea67ca3479be8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365601"
---
# <a name="cscquerydatabasestatus-function"></a><span data-ttu-id="9a86f-103">Cscquerydatabasestatus-Funktion</span><span class="sxs-lookup"><span data-stu-id="9a86f-103">CSCQueryDatabaseStatus function</span></span>

<span data-ttu-id="9a86f-104">\[Diese Funktion wird nicht unterstützt und sollte nicht verwendet werden.\]</span><span class="sxs-lookup"><span data-stu-id="9a86f-104">\[This function is not supported and should not be used.\]</span></span>

<span data-ttu-id="9a86f-105">Ruft den Status des Offlinedateien Caches ab.</span><span class="sxs-lookup"><span data-stu-id="9a86f-105">Retrieves the status of the Offline Files cache.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a86f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a86f-106">Syntax</span></span>


```C++
BOOL WINAPI CSCQueryDatabaseStatus(
   ULONG *pulStatus,
   ULONG *pulErrors
);
```



## <a name="parameters"></a><span data-ttu-id="9a86f-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a86f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a86f-108">*pulstatus*</span><span class="sxs-lookup"><span data-stu-id="9a86f-108">*pulStatus*</span></span> 
</dt> <dd>

<span data-ttu-id="9a86f-109">Der Status.</span><span class="sxs-lookup"><span data-stu-id="9a86f-109">The status.</span></span> <span data-ttu-id="9a86f-110">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="9a86f-110">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="9a86f-111">Wert</span><span class="sxs-lookup"><span data-stu-id="9a86f-111">Value</span></span>                                                                                                                                                                                                                                                                                                               | <span data-ttu-id="9a86f-112">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9a86f-112">Meaning</span></span>                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span id="FLAG_DATABASESTATUS_ENCRYPTED"></span><span id="flag_databasestatus_encrypted"></span><dl> <span data-ttu-id="9a86f-113"><dt>**Flag \_ Databasestatus \_ verschlüsselt**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="9a86f-113"><dt>**FLAG\_DATABASESTATUS\_ENCRYPTED**</dt> <dt>0x00000002</dt></span></span> </dl>                                      | <span data-ttu-id="9a86f-114">Der Cache ist für die Verschlüsselung markiert, und alle Dateien im Cache werden verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="9a86f-114">The cache is marked for encryption and all files in the cache are encrypted.</span></span><br/>                |
| <span id="FLAG_DATABASESTATUS_PARTIALLY_ENCRYPTED"></span><span id="flag_databasestatus_partially_encrypted"></span><dl> <span data-ttu-id="9a86f-115"><dt>**Flag \_ Databasestatus \_ teilweise \_ verschlüsselt**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="9a86f-115"><dt>**FLAG\_DATABASESTATUS\_PARTIALLY\_ENCRYPTED**</dt> <dt>0x00000004</dt></span></span> </dl>       | <span data-ttu-id="9a86f-116">Der Cache ist für die Verschlüsselung gekennzeichnet, einige Dateien im Cache werden jedoch nicht verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="9a86f-116">The cache is marked for encryption, but some files in the cache are not encrypted.</span></span><br/>          |
| <span id="FLAG_DATABASESTATUS_PARTIALLY_UNENCRYPTED"></span><span id="flag_databasestatus_partially_unencrypted"></span><dl> <span data-ttu-id="9a86f-117"><dt>**Flag \_ Databasestatus \_ teilweise \_ unverschlüsselt**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="9a86f-117"><dt>**FLAG\_DATABASESTATUS\_PARTIALLY\_UNENCRYPTED**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="9a86f-118">Der Cache ist nicht für die Verschlüsselung gekennzeichnet, aber nicht alle Dateien im Cache wurden entschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="9a86f-118">The cache is not marked for encryption, but not all files in the cache have been decrypted.</span></span><br/> |
| <span id="FLAG_DATABASESTATUS_UNENCRYPTED"></span><span id="flag_databasestatus_unencrypted"></span><dl> <span data-ttu-id="9a86f-119"><dt>**Flag \_ Databasestatus \_ unverschlüsselt**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="9a86f-119"><dt>**FLAG\_DATABASESTATUS\_UNENCRYPTED**</dt> <dt>0x00000000</dt></span></span> </dl>                                | <span data-ttu-id="9a86f-120">Der Cache ist nicht für die Verschlüsselung markiert, und alle Dateien im Cache wurden entschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="9a86f-120">The cache is not marked for encryption and all files in the cache have been decrypted.</span></span><br/>      |



 

</dd> <dt>

<span data-ttu-id="9a86f-121">*pulerrors*</span><span class="sxs-lookup"><span data-stu-id="9a86f-121">*pulErrors*</span></span> 
</dt> <dd>

<span data-ttu-id="9a86f-122">Dieser Parameter ist ein Wert ungleich 0 (null), wenn ein interner Datenbankfehler vorliegt oder andernfalls 0.</span><span class="sxs-lookup"><span data-stu-id="9a86f-122">This parameter is a nonzero value if there is an internal database error or 0 otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a86f-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9a86f-123">Return value</span></span>

<span data-ttu-id="9a86f-124">Diese Funktion gibt **true** zurück, wenn Sie erfolgreich ist. Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9a86f-124">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a86f-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9a86f-125">Remarks</span></span>

<span data-ttu-id="9a86f-126">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="9a86f-126">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a86f-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9a86f-127">Requirements</span></span>



| <span data-ttu-id="9a86f-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9a86f-128">Requirement</span></span> | <span data-ttu-id="9a86f-129">Wert</span><span class="sxs-lookup"><span data-stu-id="9a86f-129">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9a86f-130">DLL</span><span class="sxs-lookup"><span data-stu-id="9a86f-130">DLL</span></span><br/> | <dl> <span data-ttu-id="9a86f-131"><dt>Cscmig.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a86f-131"><dt>Cscmig.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a86f-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9a86f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a86f-133">**Csciscscenabled**</span><span class="sxs-lookup"><span data-stu-id="9a86f-133">**CSCIsCSCEnabled**</span></span>](csciscscenabled.md)
</dt> </dl>

 

 
