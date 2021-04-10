---
description: Legt eine Zeichenfolge an einer angegebenen Position innerhalb eines BLOBs fest.
ms.assetid: 645e6b8b-aaaf-429f-ad2f-bf4364ef4e80
title: Setstringinblob-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetStringInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 37278b9111818957e6d5fb3032f1bf33ad3a6ec3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214742"
---
# <a name="setstringinblob-function"></a><span data-ttu-id="671f6-103">Setstringinblob-Funktion</span><span class="sxs-lookup"><span data-stu-id="671f6-103">SetStringInBlob function</span></span>

<span data-ttu-id="671f6-104">Die **setstringinblob** -Funktion legt eine Zeichenfolge an einer bestimmten Position innerhalb eines BLOBs fest.</span><span class="sxs-lookup"><span data-stu-id="671f6-104">The **SetStringInBlob** function sets a string at a given location within a BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="671f6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="671f6-105">Syntax</span></span>


```C++
DWORD SetStringInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_ const char  *pString
);
```



## <a name="parameters"></a><span data-ttu-id="671f6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="671f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="671f6-107">*hblob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="671f6-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="671f6-108">Ein Handle für das BLOB.</span><span class="sxs-lookup"><span data-stu-id="671f6-108">A handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="671f6-109">*pownername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="671f6-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="671f6-110">Ein Zeiger auf den **Besitzer** Abschnitt des BLOBs, in dem die Zeichenfolge festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="671f6-110">A pointer to the **Owner** section of the BLOB, where the string is set.</span></span>

</dd> <dt>

<span data-ttu-id="671f6-111">*pcategoryname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="671f6-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="671f6-112">Ein Zeiger auf den **Kategorieabschnitt** des BLOBs, in dem die Zeichenfolge festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="671f6-112">A pointer to the **Category** section of the BLOB, where the string is set.</span></span>

</dd> <dt>

<span data-ttu-id="671f6-113">*ptagname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="671f6-113">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="671f6-114">Ein Zeiger auf das **Tag** der angeforderten Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="671f6-114">A pointer to the **Tag** of the requested string.</span></span>

</dd> <dt>

<span data-ttu-id="671f6-115">*pstring* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="671f6-115">*pString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="671f6-116">Ein Zeiger auf die Variable, in der ein Zeiger auf die Zeichenfolge zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="671f6-116">A pointer to the variable where a pointer to the string will be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="671f6-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="671f6-117">Return value</span></span>

<span data-ttu-id="671f6-118">Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="671f6-118">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="671f6-119">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein nmerr-Wert, der das Problem angibt.</span><span class="sxs-lookup"><span data-stu-id="671f6-119">If the function is unsuccessful, the return value is a NMERR value that indicates the problem.</span></span>

<span data-ttu-id="671f6-120">Wenn die angegebenen **Besitzer**-, **Kategorie**-oder **Taginformationen** nicht vorhanden sind, ist der Rückgabewert nmerr \_ BLOB \_ Entry \_ \_ nicht \_ vorhanden.</span><span class="sxs-lookup"><span data-stu-id="671f6-120">If the specified **Owner**, **Category**, or **Tag** information does not exist, the return value is NMERR\_BLOB\_ENTRY\_DOES\_NOT\_EXIST.</span></span>

## <a name="requirements"></a><span data-ttu-id="671f6-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="671f6-121">Requirements</span></span>



| <span data-ttu-id="671f6-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="671f6-122">Requirement</span></span> | <span data-ttu-id="671f6-123">Wert</span><span class="sxs-lookup"><span data-stu-id="671f6-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="671f6-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="671f6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="671f6-125">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="671f6-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="671f6-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="671f6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="671f6-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="671f6-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="671f6-128">Header</span><span class="sxs-lookup"><span data-stu-id="671f6-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="671f6-129"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="671f6-129"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="671f6-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="671f6-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="671f6-131"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="671f6-131"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="671f6-132">DLL</span><span class="sxs-lookup"><span data-stu-id="671f6-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="671f6-133"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="671f6-133"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="671f6-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="671f6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="671f6-135">Getstringfromblob</span><span class="sxs-lookup"><span data-stu-id="671f6-135">GetStringFromBlob</span></span>](getstringfromblob.md)
</dt> <dt>

[<span data-ttu-id="671f6-136">Setboolinblob</span><span class="sxs-lookup"><span data-stu-id="671f6-136">SetBoolInBlob</span></span>](setboolinblob.md)
</dt> <dt>

[<span data-ttu-id="671f6-137">Setclassidinblob</span><span class="sxs-lookup"><span data-stu-id="671f6-137">SetClassIDInBlob</span></span>](setclassidinblob.md)
</dt> <dt>

[<span data-ttu-id="671f6-138">Setdwordinblob</span><span class="sxs-lookup"><span data-stu-id="671f6-138">SetDwordInBlob</span></span>](setdwordinblob.md)
</dt> <dt>

[<span data-ttu-id="671f6-139">Setmacaddressinblob</span><span class="sxs-lookup"><span data-stu-id="671f6-139">SetMacAddressInBlob</span></span>](setmacaddressinblob.md)
</dt> <dt>

[<span data-ttu-id="671f6-140">Setnetworkinfoinblob</span><span class="sxs-lookup"><span data-stu-id="671f6-140">SetNetworkInfoInBlob</span></span>](setnetworkinfoinblob.md)
</dt> <dt>

[<span data-ttu-id="671f6-141">Setnppaddressfilterinblob</span><span class="sxs-lookup"><span data-stu-id="671f6-141">SetNPPAddressFilterInBlob</span></span>](setnppaddressfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="671f6-142">Setnpppatternfilterinblob</span><span class="sxs-lookup"><span data-stu-id="671f6-142">SetNPPPatternFilterInBlob</span></span>](setnpppatternfilterinblob.md)
</dt> <dt>

[<span data-ttu-id="671f6-143">Setnpptriggerinblob</span><span class="sxs-lookup"><span data-stu-id="671f6-143">SetNPPTriggerInBlob</span></span>](setnpptriggerinblob.md)
</dt> </dl>

 

 




