---
description: Konvertiert die angegebenen Attributdaten in das XML-Format.
ms.assetid: 7a75726d-f1ec-4137-89c1-eccb4a78fc22
title: Sdbformatattribute-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFormatAttribute
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: e06bbaa288c7ecb0e85cd8a779100d547c33d687
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860558"
---
# <a name="sdbformatattribute-function"></a><span data-ttu-id="4a089-103">Sdbformatattribute-Funktion</span><span class="sxs-lookup"><span data-stu-id="4a089-103">SdbFormatAttribute function</span></span>

<span data-ttu-id="4a089-104">Konvertiert die angegebenen Attributdaten in das XML-Format.</span><span class="sxs-lookup"><span data-stu-id="4a089-104">Converts the specified attribute data to XML format.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a089-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a089-105">Syntax</span></span>


```C++
BOOL WINAPI SdbFormatAttribute(
  _In_  PATTRINFO pAttrInfo,
  _Out_ LPTSTR    pchBuffer,
  _In_  DWORD     dwBufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="4a089-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4a089-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a089-107">*pattrinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4a089-107">*pAttrInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a089-108">Eine [**attrinfo**](attrinfo.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="4a089-108">An [**ATTRINFO**](attrinfo.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="4a089-109">*pchBuffer* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4a089-109">*pchBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4a089-110">Der Ausgabepuffer.</span><span class="sxs-lookup"><span data-stu-id="4a089-110">The output buffer.</span></span>

</dd> <dt>

<span data-ttu-id="4a089-111">*dwbuffersize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4a089-111">*dwBufferSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a089-112">Die Größe des *pchBuffer* -Puffers in Zeichen.</span><span class="sxs-lookup"><span data-stu-id="4a089-112">The size of the *pchBuffer* buffer, in characters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a089-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4a089-113">Return value</span></span>

<span data-ttu-id="4a089-114">Die Funktion gibt bei Erfolg **true** oder **false** zurück, wenn der Puffer zu klein ist oder das Attribut nicht gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="4a089-114">The function returns **TRUE** on success or **FALSE** if the buffer is too small or the attribute is not found.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a089-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4a089-115">Requirements</span></span>



| <span data-ttu-id="4a089-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4a089-116">Requirement</span></span> | <span data-ttu-id="4a089-117">Wert</span><span class="sxs-lookup"><span data-stu-id="4a089-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a089-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4a089-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4a089-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4a089-119">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="4a089-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4a089-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4a089-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4a089-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4a089-122">DLL</span><span class="sxs-lookup"><span data-stu-id="4a089-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a089-123"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a089-123"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a089-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4a089-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a089-125">**Sdbgetfileattribute**</span><span class="sxs-lookup"><span data-stu-id="4a089-125">**SdbGetFileAttributes**</span></span>](sdbgetfileattributes.md)
</dt> </dl>

 

 




