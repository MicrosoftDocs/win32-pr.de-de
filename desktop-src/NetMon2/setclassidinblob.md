---
description: Die setclassidinblob-Funktion legt den Wert der benannten Klassen Kennung eines BLOBs fest.
ms.assetid: d17dd48b-2e35-4c57-ba33-688180910b63
title: Setclassidinblob-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetClassIDInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: b617c39767038bac51d749a640ebcf2301e0c63f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106351617"
---
# <a name="setclassidinblob-function"></a><span data-ttu-id="44786-103">Setclassidinblob-Funktion</span><span class="sxs-lookup"><span data-stu-id="44786-103">SetClassIDInBlob function</span></span>

<span data-ttu-id="44786-104">Die **setclassidinblob** -Funktion legt den Wert der benannten Klassen Kennung eines BLOBs fest.</span><span class="sxs-lookup"><span data-stu-id="44786-104">The **SetClassIDInBlob** function sets the named class identifier value of a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="44786-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="44786-105">Syntax</span></span>


```C++
DWORD SetClassIDInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_ const CLSID *pClsID
);
```



## <a name="parameters"></a><span data-ttu-id="44786-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="44786-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44786-107">*hblob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="44786-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44786-108">Handle für ein BLOB.</span><span class="sxs-lookup"><span data-stu-id="44786-108">Handle to a BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="44786-109">*pownername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="44786-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44786-110">Zeiger auf den Namen des BLOB- **Besitzers** , der festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="44786-110">Pointer to the BLOB **Owner** name that is set.</span></span>

</dd> <dt>

<span data-ttu-id="44786-111">*pcategoryname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="44786-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44786-112">Zeiger auf den Namen der BLOB- **Kategorie** , die festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="44786-112">Pointer to the BLOB **Category** name that is set.</span></span>

</dd> <dt>

<span data-ttu-id="44786-113">*ptagname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="44786-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44786-114">Zeiger auf den Namen des BLOB- **Tags** , der festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="44786-114">Pointer to the BLOB **Tag** name that is set.</span></span>

</dd> <dt>

<span data-ttu-id="44786-115">*pclsid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="44786-115">*pClsID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44786-116">Zeiger auf den Klassen Bezeichner des festgelegten BLOBs.</span><span class="sxs-lookup"><span data-stu-id="44786-116">Pointer to the class identifier of the BLOB that is set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44786-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="44786-117">Return value</span></span>

<span data-ttu-id="44786-118">Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="44786-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="44786-119">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein nmerr-Wert, der den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="44786-119">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="44786-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="44786-120">Requirements</span></span>



| <span data-ttu-id="44786-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="44786-121">Requirement</span></span> | <span data-ttu-id="44786-122">Wert</span><span class="sxs-lookup"><span data-stu-id="44786-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="44786-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="44786-123">Minimum supported client</span></span><br/> | <span data-ttu-id="44786-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="44786-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="44786-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="44786-125">Minimum supported server</span></span><br/> | <span data-ttu-id="44786-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="44786-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="44786-127">Header</span><span class="sxs-lookup"><span data-stu-id="44786-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="44786-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="44786-128"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="44786-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="44786-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="44786-130"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="44786-130"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="44786-131">DLL</span><span class="sxs-lookup"><span data-stu-id="44786-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44786-132"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44786-132"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44786-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="44786-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44786-134">Getclassidfromblob</span><span class="sxs-lookup"><span data-stu-id="44786-134">GetClassIDFromBlob</span></span>](getclassidfromblob.md)
</dt> <dt>

[<span data-ttu-id="44786-135">Setboolinblob</span><span class="sxs-lookup"><span data-stu-id="44786-135">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="44786-136">Setdwordinblob</span><span class="sxs-lookup"><span data-stu-id="44786-136">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="44786-137">Setmacaddressinblob</span><span class="sxs-lookup"><span data-stu-id="44786-137">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="44786-138">Setnetworkinfoinblob</span><span class="sxs-lookup"><span data-stu-id="44786-138">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="44786-139">Setnppaddressfilterinblob</span><span class="sxs-lookup"><span data-stu-id="44786-139">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="44786-140">Setnpppatternfilterinblob</span><span class="sxs-lookup"><span data-stu-id="44786-140">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="44786-141">Setnpptriggerinblob</span><span class="sxs-lookup"><span data-stu-id="44786-141">SetNPPTriggerInBlob</span></span>](setnpptriggerinblob.md)
</dt> <dt>

[<span data-ttu-id="44786-142">Setstringinblob</span><span class="sxs-lookup"><span data-stu-id="44786-142">SetStringInBlob</span></span>](setstringinblob.md)
</dt> </dl>

 

 




