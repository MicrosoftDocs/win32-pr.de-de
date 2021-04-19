---
description: Die regkreateblobkey-Funktion speichert ein BLOB mit dem angegebenen Registrierungsschlüssel.
ms.assetid: 14f3763e-aa04-4d51-b388-81ebf0d3952c
title: Regkreateblobkey-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RegCreateBlobKey
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: fc46b38919b37dc004c1065b0cc8d5f80e65984c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355448"
---
# <a name="regcreateblobkey-function"></a><span data-ttu-id="56b41-103">Regkreateblobkey-Funktion</span><span class="sxs-lookup"><span data-stu-id="56b41-103">RegCreateBlobKey function</span></span>

<span data-ttu-id="56b41-104">Die **regkreateblobkey** -Funktion speichert ein BLOB mit dem angegebenen Registrierungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="56b41-104">The **RegCreateBlobKey** function stores a BLOB at the given registry key.</span></span>

## <a name="syntax"></a><span data-ttu-id="56b41-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="56b41-105">Syntax</span></span>


```C++
DWORD RegCreateBlobKey(
  _Out_       HKEY  hkey,
  _In_  const char  *szBlobName,
  _In_        HBLOB hBlob
);
```



## <a name="parameters"></a><span data-ttu-id="56b41-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="56b41-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56b41-107">*HKEY* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="56b41-107">*hkey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="56b41-108">Handle für den Registrierungsschlüssel, in dem das BLOB gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="56b41-108">Handle to the registry key where the BLOB will be stored.</span></span>

</dd> <dt>

<span data-ttu-id="56b41-109">*szblobname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="56b41-109">*szBlobName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56b41-110">Name (Anwendung definiert), der das BLOB in der Registrierung darstellt.</span><span class="sxs-lookup"><span data-stu-id="56b41-110">Name (application defined) that represents the BLOB in the registry.</span></span>

</dd> <dt>

<span data-ttu-id="56b41-111">*hblob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="56b41-111">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56b41-112">Handle für das BLOB, das gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="56b41-112">Handle to the BLOB that is saved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56b41-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="56b41-113">Return value</span></span>

<span data-ttu-id="56b41-114">Wenn die Funktion erfolgreich ist, ist der Rückgabewert nmerr \_ Success.</span><span class="sxs-lookup"><span data-stu-id="56b41-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="56b41-115">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert ein nmerr-Wert, der den Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="56b41-115">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="56b41-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="56b41-116">Requirements</span></span>



| <span data-ttu-id="56b41-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="56b41-117">Requirement</span></span> | <span data-ttu-id="56b41-118">Wert</span><span class="sxs-lookup"><span data-stu-id="56b41-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="56b41-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="56b41-119">Minimum supported client</span></span><br/> | <span data-ttu-id="56b41-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="56b41-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="56b41-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="56b41-121">Minimum supported server</span></span><br/> | <span data-ttu-id="56b41-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="56b41-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="56b41-123">Header</span><span class="sxs-lookup"><span data-stu-id="56b41-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="56b41-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="56b41-124"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="56b41-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="56b41-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="56b41-126"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="56b41-126"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="56b41-127">DLL</span><span class="sxs-lookup"><span data-stu-id="56b41-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56b41-128"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56b41-128"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56b41-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="56b41-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56b41-130">Regopenblobkey</span><span class="sxs-lookup"><span data-stu-id="56b41-130">RegOpenBlobKey</span></span>](regopenblobkey.md)
</dt> </dl>

 

 




