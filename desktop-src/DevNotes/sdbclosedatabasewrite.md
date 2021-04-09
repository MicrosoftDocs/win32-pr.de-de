---
description: Schließt die angegebene Datenbank.
ms.assetid: 69546f03-9912-401a-9c1a-b7fdbe16dbf8
title: Sdbclosedatabasewrite-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbCloseDatabaseWrite
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 24df6f9ce2c4f0fae4dd1c1ef244e006ea00c047
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860984"
---
# <a name="sdbclosedatabasewrite-function"></a><span data-ttu-id="8a6d7-103">Sdbclosedatabasewrite-Funktion</span><span class="sxs-lookup"><span data-stu-id="8a6d7-103">SdbCloseDatabaseWrite function</span></span>

<span data-ttu-id="8a6d7-104">Schließt die angegebene Datenbank.</span><span class="sxs-lookup"><span data-stu-id="8a6d7-104">Closes the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a6d7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a6d7-105">Syntax</span></span>


```C++
void WINAPI SdbCloseDatabaseWrite(
  _Inout_ PDB pdb
);
```



## <a name="parameters"></a><span data-ttu-id="8a6d7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a6d7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a6d7-107">*PDB* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="8a6d7-107">*pdb* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a6d7-108">Ein Handle für die Shimdatenbank.</span><span class="sxs-lookup"><span data-stu-id="8a6d7-108">A handle to the shim database.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a6d7-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8a6d7-109">Return value</span></span>

<span data-ttu-id="8a6d7-110">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="8a6d7-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a6d7-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8a6d7-111">Remarks</span></span>

<span data-ttu-id="8a6d7-112">Diese Funktion ruft [**sdbclosedatabase**](sdbclosedatabase.md)auf. Daher sind diese beiden Funktionen Äquivalent.</span><span class="sxs-lookup"><span data-stu-id="8a6d7-112">This function calls [**SdbCloseDatabase**](sdbclosedatabase.md); therefore, these two functions are equivalent.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a6d7-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8a6d7-113">Requirements</span></span>



| <span data-ttu-id="8a6d7-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8a6d7-114">Requirement</span></span> | <span data-ttu-id="8a6d7-115">Wert</span><span class="sxs-lookup"><span data-stu-id="8a6d7-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a6d7-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8a6d7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8a6d7-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8a6d7-117">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8a6d7-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8a6d7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8a6d7-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8a6d7-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8a6d7-120">DLL</span><span class="sxs-lookup"><span data-stu-id="8a6d7-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a6d7-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a6d7-121"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a6d7-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8a6d7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a6d7-123">**Sdbbeginschreitelisttag**</span><span class="sxs-lookup"><span data-stu-id="8a6d7-123">**SdbBeginWriteListTag**</span></span>](sdbbeginwritelisttag.md)
</dt> <dt>

[<span data-ttu-id="8a6d7-124">**Sdbclosedatabase**</span><span class="sxs-lookup"><span data-stu-id="8a6d7-124">**SdbCloseDatabase**</span></span>](sdbclosedatabase.md)
</dt> <dt>

[<span data-ttu-id="8a6d7-125">**Sdbendschreitelisttag**</span><span class="sxs-lookup"><span data-stu-id="8a6d7-125">**SdbEndWriteListTag**</span></span>](sdbendwritelisttag.md)
</dt> </dl>

 

 




