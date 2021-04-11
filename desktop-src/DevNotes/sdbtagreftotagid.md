---
description: Ruft die TagID und ein Handle für die Shimdatenbank für die angegebene tagref ab.
ms.assetid: 869c6af5-4c10-4358-9d6a-1a354be6f4e9
title: Sdbtagrebtotagid-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbTagRefToTagID
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: faff00adc25a741342e586adea2f645a62eca36d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126386"
---
# <a name="sdbtagreftotagid-function"></a><span data-ttu-id="2b6bf-103">Sdbtagrebtotagid-Funktion</span><span class="sxs-lookup"><span data-stu-id="2b6bf-103">SdbTagRefToTagID function</span></span>

<span data-ttu-id="2b6bf-104">Ruft die **TagID** und ein Handle für die Shimdatenbank für die angegebene [**tagref**](tagref.md)ab.</span><span class="sxs-lookup"><span data-stu-id="2b6bf-104">Retrieves the **TAGID** and a handle to the shim database for the specified [**TAGREF**](tagref.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2b6bf-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b6bf-105">Syntax</span></span>


```C++
BOOL WINAPI SdbTagRefToTagID(
  _In_  HSDB   hSDB,
  _In_  TAGREF trWhich,
  _Out_ PDB    *ppdb,
  _Out_ TAGID  *ptiWhich
);
```



## <a name="parameters"></a><span data-ttu-id="2b6bf-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2b6bf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b6bf-107">*hsdb* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2b6bf-107">*hSDB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b6bf-108">Ein Handle für die von der [**sdbinitdatabase**](sdbinitdatabase.md) -Funktion zurückgegebene Shimdatenbank.</span><span class="sxs-lookup"><span data-stu-id="2b6bf-108">A handle to the shim database returned by the [**SdbInitDatabase**](sdbinitdatabase.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="2b6bf-109">*trwem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2b6bf-109">*trWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b6bf-110">Die [**tagref**](tagref.md).</span><span class="sxs-lookup"><span data-stu-id="2b6bf-110">The [**TAGREF**](tagref.md).</span></span>

</dd> <dt>

<span data-ttu-id="2b6bf-111">*ppdb* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2b6bf-111">*ppdb* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b6bf-112">Das resultierende Handle der Shimdatenbank.</span><span class="sxs-lookup"><span data-stu-id="2b6bf-112">The resulting handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="2b6bf-113">*ptiwhat* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2b6bf-113">*ptiWhich* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b6bf-114">Die resultierende **TagID**.</span><span class="sxs-lookup"><span data-stu-id="2b6bf-114">The resulting **TAGID**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b6bf-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2b6bf-115">Return value</span></span>

<span data-ttu-id="2b6bf-116">Bei einem Fehler gibt die Funktion **true** oder **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="2b6bf-116">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b6bf-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2b6bf-117">Requirements</span></span>



| <span data-ttu-id="2b6bf-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2b6bf-118">Requirement</span></span> | <span data-ttu-id="2b6bf-119">Wert</span><span class="sxs-lookup"><span data-stu-id="2b6bf-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b6bf-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2b6bf-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2b6bf-121">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2b6bf-121">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="2b6bf-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2b6bf-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2b6bf-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2b6bf-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="2b6bf-124">DLL</span><span class="sxs-lookup"><span data-stu-id="2b6bf-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b6bf-125"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b6bf-125"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b6bf-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b6bf-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b6bf-127">**Sdbinitdatabase**</span><span class="sxs-lookup"><span data-stu-id="2b6bf-127">**SdbInitDatabase**</span></span>](sdbinitdatabase.md)
</dt> <dt>

[<span data-ttu-id="2b6bf-128">**TagID**</span><span class="sxs-lookup"><span data-stu-id="2b6bf-128">**TAGID**</span></span>](tagid.md)
</dt> <dt>

[<span data-ttu-id="2b6bf-129">**Tagref**</span><span class="sxs-lookup"><span data-stu-id="2b6bf-129">**TAGREF**</span></span>](tagref.md)
</dt> </dl>

 

 




