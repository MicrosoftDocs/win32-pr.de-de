---
description: Die OpenView-Methode des Database-Objekts gibt ein Ansichts Objekt zurück, das die durch eine SQL-Zeichenfolge angegebene Abfrage darstellt.
ms.assetid: 6afb2fdb-0e6a-468f-8faf-e48d8d1960b6
title: Database. OpenView-Methode (certview. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.OpenView
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8dc62ca38bfe28980da71ecf63eda8e6c39aaf0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359810"
---
# <a name="databaseopenview-method"></a><span data-ttu-id="0ff62-103">Database. OpenView-Methode</span><span class="sxs-lookup"><span data-stu-id="0ff62-103">Database.OpenView method</span></span>

<span data-ttu-id="0ff62-104">Die **OpenView** -Methode des [**Database**](database-object.md) -Objekts gibt ein [**Ansichts**](view-object.md) Objekt zurück, das die durch eine SQL-Zeichenfolge angegebene Abfrage darstellt.</span><span class="sxs-lookup"><span data-stu-id="0ff62-104">The **OpenView** method of the [**Database**](database-object.md) object returns a [**View**](view-object.md) object that represents the query specified by a SQL string.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ff62-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0ff62-105">Syntax</span></span>


```JScript
Database.OpenView(
  sql
)
```



## <a name="parameters"></a><span data-ttu-id="0ff62-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0ff62-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ff62-107">*sql*</span><span class="sxs-lookup"><span data-stu-id="0ff62-107">*sql*</span></span> 
</dt> <dd>

<span data-ttu-id="0ff62-108">Erforderliche SQL-Abfrage Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="0ff62-108">Required SQL query string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ff62-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0ff62-109">Return value</span></span>

<span data-ttu-id="0ff62-110">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="0ff62-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ff62-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0ff62-111">Remarks</span></span>

<span data-ttu-id="0ff62-112">Informationen zur SQL-Syntax, die im Installer implementiert ist, finden Sie unter [SQL-Syntax](sql-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="0ff62-112">For information about SQL syntax implemented in the installer, see [SQL Syntax](sql-syntax.md).</span></span>

<span data-ttu-id="0ff62-113">Wenn die Methode fehlschlägt, können Sie erweiterte Fehlerinformationen mithilfe der [**lasterrorrecord**](installer-lasterrorrecord.md) -Methode abrufen.</span><span class="sxs-lookup"><span data-stu-id="0ff62-113">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ff62-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0ff62-114">Requirements</span></span>



| <span data-ttu-id="0ff62-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0ff62-115">Requirement</span></span> | <span data-ttu-id="0ff62-116">Wert</span><span class="sxs-lookup"><span data-stu-id="0ff62-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ff62-117">Version</span><span class="sxs-lookup"><span data-stu-id="0ff62-117">Version</span></span><br/> | <span data-ttu-id="0ff62-118">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0ff62-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="0ff62-119">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0ff62-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="0ff62-120">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="0ff62-120">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="0ff62-121">Header</span><span class="sxs-lookup"><span data-stu-id="0ff62-121">Header</span></span><br/>  | <dl> <span data-ttu-id="0ff62-122"><dt>Certview. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ff62-122"><dt>Certview.h</dt></span></span> </dl>                                                                                                                                                                   |
| <span data-ttu-id="0ff62-123">DLL</span><span class="sxs-lookup"><span data-stu-id="0ff62-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="0ff62-124"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ff62-124"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="0ff62-125">IID</span><span class="sxs-lookup"><span data-stu-id="0ff62-125">IID</span></span><br/>     | <span data-ttu-id="0ff62-126">IID \_ idatabase ist definiert als 000c109d-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="0ff62-126">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="0ff62-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0ff62-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ff62-128">**Verbindung**</span><span class="sxs-lookup"><span data-stu-id="0ff62-128">**Database**</span></span>](database-object.md)
</dt> <dt>

[<span data-ttu-id="0ff62-129">SQL-Syntax</span><span class="sxs-lookup"><span data-stu-id="0ff62-129">SQL Syntax</span></span>](sql-syntax.md)
</dt> </dl>

 

 




