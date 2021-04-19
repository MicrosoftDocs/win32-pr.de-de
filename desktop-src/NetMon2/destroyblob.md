---
description: Die destroyblob-Funktion gibt den gesamten Arbeitsspeicher frei, der dem BLOB zugeordnet ist, und zerstört dann das BLOB.
ms.assetid: 46cde0b7-1b59-426e-b19b-3c73af3d461a
title: Destroyblob-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: e90630981c16f38d601d4e06d04f9326174ef721
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362931"
---
# <a name="destroyblob-function"></a><span data-ttu-id="c4dce-103">Destroyblob-Funktion</span><span class="sxs-lookup"><span data-stu-id="c4dce-103">DestroyBlob function</span></span>

<span data-ttu-id="c4dce-104">Die **destroyblob** -Funktion gibt den gesamten Arbeitsspeicher frei, der dem BLOB zugeordnet ist, und zerstört dann das BLOB.</span><span class="sxs-lookup"><span data-stu-id="c4dce-104">The **DestroyBlob** function frees all memory associated with the BLOB and then destroys the BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4dce-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4dce-105">Syntax</span></span>


```C++
DWORD DestroyBlob(
  _In_ HBLOB hBlob
);
```



## <a name="parameters"></a><span data-ttu-id="c4dce-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4dce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4dce-107">*hblob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4dce-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4dce-108">Handle für das-BLOB, das zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="c4dce-108">Handle to the to the BLOB that is destroyed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4dce-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c4dce-109">Return value</span></span>

<span data-ttu-id="c4dce-110">Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="c4dce-110">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="c4dce-111">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein nmerr-Wert, der den Fehler beschreibt.</span><span class="sxs-lookup"><span data-stu-id="c4dce-111">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4dce-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c4dce-112">Requirements</span></span>



| <span data-ttu-id="c4dce-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c4dce-113">Requirement</span></span> | <span data-ttu-id="c4dce-114">Wert</span><span class="sxs-lookup"><span data-stu-id="c4dce-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4dce-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c4dce-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c4dce-116">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c4dce-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c4dce-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c4dce-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c4dce-118">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c4dce-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c4dce-119">Header</span><span class="sxs-lookup"><span data-stu-id="c4dce-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4dce-120"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4dce-120"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="c4dce-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c4dce-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="c4dce-122"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c4dce-122"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="c4dce-123">DLL</span><span class="sxs-lookup"><span data-stu-id="c4dce-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4dce-124"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4dce-124"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4dce-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c4dce-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4dce-126">CreateBlob</span><span class="sxs-lookup"><span data-stu-id="c4dce-126">CreateBlob</span></span>](createblob.md)
</dt> </dl>

 

 




