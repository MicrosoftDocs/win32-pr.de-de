---
description: Die regopenblobkey-Funktion Ruft ein BLOB ab, das am angegebenen Registrierungsschlüssel gespeichert ist.
ms.assetid: f6b16c07-c705-47f1-a21c-6155368551c7
title: Regopenblobkey-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RegOpenBlobKey
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 24d788c8c4b69525d6c0be374845b44f804982bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362764"
---
# <a name="regopenblobkey-function"></a><span data-ttu-id="2eaa1-103">Regopenblobkey-Funktion</span><span class="sxs-lookup"><span data-stu-id="2eaa1-103">RegOpenBlobKey function</span></span>

<span data-ttu-id="2eaa1-104">Die **regopenblobkey** -Funktion Ruft ein BLOB ab, das am angegebenen Registrierungsschlüssel gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="2eaa1-104">The **RegOpenBlobKey** function retrieves a BLOB stored at the given registry key.</span></span>

## <a name="syntax"></a><span data-ttu-id="2eaa1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2eaa1-105">Syntax</span></span>


```C++
DWORD RegOpenBlobKey(
  _In_        HKEY  hkey,
  _In_  const char  *szBlobName,
  _Out_       HBLOB *phBlob
);
```



## <a name="parameters"></a><span data-ttu-id="2eaa1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2eaa1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2eaa1-107">*HKEY* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2eaa1-107">*hkey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2eaa1-108">Handle für den Registrierungsschlüssel, der das BLOB enthält.</span><span class="sxs-lookup"><span data-stu-id="2eaa1-108">Handle to the registry key that contains the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="2eaa1-109">*szblobname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2eaa1-109">*szBlobName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2eaa1-110">Der Name, der das angegebene BLOB in der Registrierung identifiziert.</span><span class="sxs-lookup"><span data-stu-id="2eaa1-110">Name that identifies the given BLOB in the registry.</span></span>

</dd> <dt>

<span data-ttu-id="2eaa1-111">*phblob* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2eaa1-111">*phBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2eaa1-112">Zeiger auf das BLOB, das abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="2eaa1-112">Pointer to the BLOB that is retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2eaa1-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2eaa1-113">Return value</span></span>

<span data-ttu-id="2eaa1-114">Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="2eaa1-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="2eaa1-115">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein nmerr-Wert, der den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="2eaa1-115">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="2eaa1-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2eaa1-116">Requirements</span></span>



| <span data-ttu-id="2eaa1-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2eaa1-117">Requirement</span></span> | <span data-ttu-id="2eaa1-118">Wert</span><span class="sxs-lookup"><span data-stu-id="2eaa1-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2eaa1-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2eaa1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2eaa1-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2eaa1-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="2eaa1-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2eaa1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2eaa1-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2eaa1-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2eaa1-123">Header</span><span class="sxs-lookup"><span data-stu-id="2eaa1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2eaa1-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="2eaa1-124"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="2eaa1-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2eaa1-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="2eaa1-126"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2eaa1-126"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="2eaa1-127">DLL</span><span class="sxs-lookup"><span data-stu-id="2eaa1-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2eaa1-128"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2eaa1-128"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2eaa1-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2eaa1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2eaa1-130">Regkreateblobkey</span><span class="sxs-lookup"><span data-stu-id="2eaa1-130">RegCreateBlobKey</span></span>](regcreateblobkey.md)
</dt> </dl>

 

 




