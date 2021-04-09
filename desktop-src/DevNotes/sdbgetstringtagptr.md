---
description: Ruft die Zeichen folgen Daten für die angegebene TagID ab.
ms.assetid: c558e0bb-7e35-4298-93fb-400db00a2972
title: Sdbgetstringtagptr-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetStringTagPtr
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 56c80c4000df95fe13486d95bb872bfc39274389
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958363"
---
# <a name="sdbgetstringtagptr-function"></a><span data-ttu-id="8ff30-103">Sdbgetstringtagptr-Funktion</span><span class="sxs-lookup"><span data-stu-id="8ff30-103">SdbGetStringTagPtr function</span></span>

<span data-ttu-id="8ff30-104">Ruft die Zeichen folgen Daten für die angegebene **TagID** ab.</span><span class="sxs-lookup"><span data-stu-id="8ff30-104">Retrieves the string data for the specified **TAGID**.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ff30-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ff30-105">Syntax</span></span>


```C++
LPTSTR WINAPI SdbGetStringTagPtr(
  _In_ PDB   pdb,
  _In_ TAGID tiWhich
);
```



## <a name="parameters"></a><span data-ttu-id="8ff30-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ff30-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ff30-107">*PDB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8ff30-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ff30-108">Ein Handle für die Shimdatenbank.</span><span class="sxs-lookup"><span data-stu-id="8ff30-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="8ff30-109">*tiwhat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8ff30-109">*tiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ff30-110">Die **TagID** , die den abzurufenden Zeichen folgen Daten entspricht.</span><span class="sxs-lookup"><span data-stu-id="8ff30-110">The **TAGID** that corresponds to the string data to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ff30-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8ff30-111">Return value</span></span>

<span data-ttu-id="8ff30-112">Die-Funktion gibt einen Zeiger auf die Zeichen folgen Daten oder **null** zurück, wenn die **TagID** ungültig ist oder nicht vom Typ " **Tag \_ Type \_ String** " oder vom **\_ Tagtyp " \_ uningref**" ist.</span><span class="sxs-lookup"><span data-stu-id="8ff30-112">The function returns a pointer to the string data or **NULL** if the **TAGID** is invalid or not of type **TAG\_TYPE\_STRING** or **TAG\_TYPE\_STRINGREF**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ff30-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8ff30-113">Requirements</span></span>



| <span data-ttu-id="8ff30-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8ff30-114">Requirement</span></span> | <span data-ttu-id="8ff30-115">Wert</span><span class="sxs-lookup"><span data-stu-id="8ff30-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ff30-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8ff30-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8ff30-117">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8ff30-117">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="8ff30-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8ff30-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8ff30-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8ff30-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="8ff30-120">DLL</span><span class="sxs-lookup"><span data-stu-id="8ff30-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ff30-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ff30-121"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ff30-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8ff30-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ff30-123">**Sdbgetbinarytagdata**</span><span class="sxs-lookup"><span data-stu-id="8ff30-123">**SdbGetBinaryTagData**</span></span>](sdbgetbinarytagdata.md)
</dt> <dt>

[<span data-ttu-id="8ff30-124">**Sdbreaddwordtag**</span><span class="sxs-lookup"><span data-stu-id="8ff30-124">**SdbReadDWORDTag**</span></span>](sdbreaddwordtag.md)
</dt> <dt>

[<span data-ttu-id="8ff30-125">**Sdbreadqwordtag**</span><span class="sxs-lookup"><span data-stu-id="8ff30-125">**SdbReadQWORDTag**</span></span>](sdbreadqwordtag.md)
</dt> <dt>

[<span data-ttu-id="8ff30-126">**Sdbreadstringtag**</span><span class="sxs-lookup"><span data-stu-id="8ff30-126">**SdbReadStringTag**</span></span>](sdbreadstringtag.md)
</dt> </dl>

 

 




