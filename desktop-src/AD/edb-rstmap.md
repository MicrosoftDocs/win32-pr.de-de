---
title: EDB_RSTMAP Struktur (ntdsbcli. h)
description: Wird mit der dsrestoreregiester-Funktion verwendet, um eine gesicherte Datenbank einer neuen Datenbank zuzuordnen.
ms.assetid: b2c5d30a-3617-4807-82e8-57f7179b817c
ms.tgt_platform: multiple
keywords:
- EDB_RSTMAP Struktur Active Directory
- PEDB_RSTMAP Struktur Zeiger Active Directory
topic_type:
- apiref
api_name:
- EDB_RSTMAP
- EDB_RSTMAPA
- EDB_RSTMAPW
api_location:
- Ntdsbcli.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be2c960ab7ebc687508131deac6cd8e7b99bbe81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040725"
---
# <a name="edb_rstmap-structure"></a><span data-ttu-id="528e7-105">EDB- \_ rstmap-Struktur</span><span class="sxs-lookup"><span data-stu-id="528e7-105">EDB\_RSTMAP structure</span></span>

<span data-ttu-id="528e7-106">Die **EDB- \_ rstmap** -Struktur wird mit der [**dsrestoreregiester**](dsrestoreregister.md) -Funktion verwendet, um eine gesicherte Datenbank einer neuen Datenbank zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="528e7-106">The **EDB\_RSTMAP** structure is used with the [**DsRestoreRegister**](dsrestoreregister.md) function to map a backed up database to a new database.</span></span>

## <a name="syntax"></a><span data-ttu-id="528e7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="528e7-107">Syntax</span></span>


```C++
typedef struct {
  LPTSTR szDatabaseName;
  LPTSTR szNewDatabaseName;
} EDB_RSTMAP, *PEDB_RSTMAP;
```



## <a name="members"></a><span data-ttu-id="528e7-108">Member</span><span class="sxs-lookup"><span data-stu-id="528e7-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="528e7-109">**szdatabasename**</span><span class="sxs-lookup"><span data-stu-id="528e7-109">**szDatabaseName**</span></span>
</dt> <dd>

<span data-ttu-id="528e7-110">Zeiger auf eine mit NULL endenden Zeichenfolge, die den Namen der Datenbank enthält, als Sie gesichert wurde.</span><span class="sxs-lookup"><span data-stu-id="528e7-110">Pointer to a null-terminated string that contains the name of the database when it was backed up.</span></span>

</dd> <dt>

<span data-ttu-id="528e7-111">**sznewdatabasename**</span><span class="sxs-lookup"><span data-stu-id="528e7-111">**szNewDatabaseName**</span></span>
</dt> <dd>

<span data-ttu-id="528e7-112">Zeiger auf eine auf NULL endende Zeichenfolge, die den neuen Namen der Datenbank enthält, einschließlich des neuen Speicher Orts, falls zutreffend.</span><span class="sxs-lookup"><span data-stu-id="528e7-112">Pointer to a null-terminated string that contains the new name of the database, including its new location, when applicable.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="528e7-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="528e7-113">Requirements</span></span>



| <span data-ttu-id="528e7-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="528e7-114">Requirement</span></span> | <span data-ttu-id="528e7-115">Wert</span><span class="sxs-lookup"><span data-stu-id="528e7-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="528e7-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="528e7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="528e7-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="528e7-117">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="528e7-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="528e7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="528e7-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="528e7-119">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="528e7-120">Header</span><span class="sxs-lookup"><span data-stu-id="528e7-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="528e7-121"><dt>Ntdsbcli. h</dt></span><span class="sxs-lookup"><span data-stu-id="528e7-121"><dt>Ntdsbcli.h</dt></span></span> </dl> |
| <span data-ttu-id="528e7-122">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="528e7-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="528e7-123">**EDB \_ Rstmapw** (Unicode) und **EDB \_ rstmapa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="528e7-123">**EDB\_RSTMAPW** (Unicode) and **EDB\_RSTMAPA** (ANSI)</span></span><br/>                     |



## <a name="see-also"></a><span data-ttu-id="528e7-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="528e7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="528e7-125">**Dsrestoreregiester**</span><span class="sxs-lookup"><span data-stu-id="528e7-125">**DsRestoreRegister**</span></span>](dsrestoreregister.md)
</dt> <dt>

[<span data-ttu-id="528e7-126">Struktur der Verzeichnis Sicherung</span><span class="sxs-lookup"><span data-stu-id="528e7-126">Directory Backup Structures</span></span>](directory-backup-structures.md)
</dt> </dl>

 

 





