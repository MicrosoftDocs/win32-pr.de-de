---
description: Die removefromblob-Funktion löscht eine beliebige Ebene des BLOB-Eintrags (Besitzer, Kategorie oder Tag).
ms.assetid: b8bb01e0-8b97-4c95-96f5-f2a30c8700e9
title: Removefromblob-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RemoveFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: a23e4e7e6e6d5c85b1284f8aaba49c1f8eae728d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346297"
---
# <a name="removefromblob-function"></a><span data-ttu-id="a06a7-103">Removefromblob-Funktion</span><span class="sxs-lookup"><span data-stu-id="a06a7-103">RemoveFromBlob function</span></span>

<span data-ttu-id="a06a7-104">Die **removefromblob** -Funktion löscht eine beliebige Ebene des BLOB-Eintrags (**Besitzer**, **Kategorie** oder **Tag**).</span><span class="sxs-lookup"><span data-stu-id="a06a7-104">The **RemoveFromBlob** function deletes any level of BLOB entry (**Owner**, **Category**, or **Tag**).</span></span>

## <a name="syntax"></a><span data-ttu-id="a06a7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a06a7-105">Syntax</span></span>


```C++
DWORD RemoveFromBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName
);
```



## <a name="parameters"></a><span data-ttu-id="a06a7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a06a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a06a7-107">*hblob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a06a7-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a06a7-108">Handle für das BLOB, aus dem ein Eintrag gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="a06a7-108">Handle to the BLOB from which an entry is deleted.</span></span>

</dd> <dt>

<span data-ttu-id="a06a7-109">*pownername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a06a7-109">*pOwnerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a06a7-110">Zeiger auf den Namen des **Besitzers** .</span><span class="sxs-lookup"><span data-stu-id="a06a7-110">Pointer to the **Owner** name.</span></span>

</dd> <dt>

<span data-ttu-id="a06a7-111">*pcategoryname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a06a7-111">*pCategoryName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a06a7-112">Zeiger auf den **Kategorienamen** .</span><span class="sxs-lookup"><span data-stu-id="a06a7-112">Pointer to the **Category** name.</span></span> <span data-ttu-id="a06a7-113">Ein **null** -Parameterwert gibt an, dass der Aufrufer versucht, die angegebenen **Besitzer** Informationen und alle zugehörigen untergeordneten Einträge zu löschen.</span><span class="sxs-lookup"><span data-stu-id="a06a7-113">A **NULL** parameter value indicates the caller is attempting to delete the given **Owner** information and all of its child entries.</span></span> <span data-ttu-id="a06a7-114">Beachten Sie, dass der *ptagname* -Parameter ebenfalls **null** sein muss, wenn der *pcategoryname* -Parameter den Wert **null** hat.</span><span class="sxs-lookup"><span data-stu-id="a06a7-114">Note that if the *pCategoryName* parameter value is **NULL**, the *pTagName* parameter must also be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a06a7-115">*ptagname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a06a7-115">*pTagName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a06a7-116">Zeiger auf den **Tagnamen** .</span><span class="sxs-lookup"><span data-stu-id="a06a7-116">Pointer to the **Tag** name.</span></span> <span data-ttu-id="a06a7-117">Ein _ptagname_ -Wert von NULL gibt an, dass der Aufrufer versucht, die angegebene **Kategorie** und alle zugehörigen untergeordneten Einträge zu löschen.</span><span class="sxs-lookup"><span data-stu-id="a06a7-117">A **NULL**_pTagName_ value indicates the caller is attempting to delete the given **Category** and all of its child entries.</span></span> <span data-ttu-id="a06a7-118">Wenn der Parameterwert nicht **null** ist, fragt der Aufrufer nur, dass die angegebenen **tageinträge** gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="a06a7-118">If the parameter value is not **NULL**, the caller is asking that only that the specified **Tag** entries be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a06a7-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a06a7-119">Return value</span></span>

<span data-ttu-id="a06a7-120">Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="a06a7-120">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="a06a7-121">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein nmerr-Wert, der den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="a06a7-121">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="a06a7-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a06a7-122">Requirements</span></span>



| <span data-ttu-id="a06a7-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a06a7-123">Requirement</span></span> | <span data-ttu-id="a06a7-124">Wert</span><span class="sxs-lookup"><span data-stu-id="a06a7-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a06a7-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a06a7-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a06a7-126">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a06a7-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a06a7-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a06a7-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a06a7-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a06a7-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a06a7-129">Header</span><span class="sxs-lookup"><span data-stu-id="a06a7-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="a06a7-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="a06a7-130"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="a06a7-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a06a7-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="a06a7-132"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a06a7-132"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="a06a7-133">DLL</span><span class="sxs-lookup"><span data-stu-id="a06a7-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a06a7-134"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a06a7-134"><dt>Npptools.dll</dt></span></span> </dl> |



 

 




