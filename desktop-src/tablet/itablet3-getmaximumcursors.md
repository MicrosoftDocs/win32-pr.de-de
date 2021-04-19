---
description: Die getmaximumcursors-Methode ruft die maximale Anzahl von Cursorn ab, die ein Tablet-Gerät unterstützt.
ms.assetid: 5a43d792-e64c-4506-9792-31efe0885959
title: 'ITablet3:: getmaximumcursors-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet3.GetMaximumCursors
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 7c40184d35ac1d42cb5f5e845396b40efc2d928e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362551"
---
# <a name="itablet3getmaximumcursors-method"></a><span data-ttu-id="0fb36-103">ITablet3:: getmaximumcursors-Methode</span><span class="sxs-lookup"><span data-stu-id="0fb36-103">ITablet3::GetMaximumCursors method</span></span>

<span data-ttu-id="0fb36-104">Die **getmaximumcursors** -Methode ruft die maximale Anzahl von Cursorn ab, die ein Tablet-Gerät unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0fb36-104">The **GetMaximumCursors** method retrieves the maximum number of cursors that a tablet device supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fb36-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0fb36-105">Syntax</span></span>


```C++
HRESULT GetMaximumCursors(
   ULONG *pMaximumCursors
);
```



## <a name="parameters"></a><span data-ttu-id="0fb36-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0fb36-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fb36-107">*pmaximumcursors*</span><span class="sxs-lookup"><span data-stu-id="0fb36-107">*pMaximumCursors*</span></span> 
</dt> <dd>

<span data-ttu-id="0fb36-108">Die maximale Anzahl von Eingaben, die das Gerät unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0fb36-108">The maximum number of inputs that the device supports.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fb36-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0fb36-109">Return value</span></span>

<span data-ttu-id="0fb36-110">Gibt \_ bei Erfolg S OK zurück; andernfalls wird ein Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0fb36-110">Returns S\_OK on success; otherwise, returns an error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fb36-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0fb36-111">Requirements</span></span>



| <span data-ttu-id="0fb36-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0fb36-112">Requirement</span></span> | <span data-ttu-id="0fb36-113">Wert</span><span class="sxs-lookup"><span data-stu-id="0fb36-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0fb36-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0fb36-114">Minimum supported client</span></span><br/> | <span data-ttu-id="0fb36-115">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0fb36-115">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="0fb36-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0fb36-116">Minimum supported server</span></span><br/> | <span data-ttu-id="0fb36-117">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0fb36-117">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0fb36-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0fb36-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="0fb36-119"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0fb36-119"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fb36-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0fb36-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fb36-121">**ITablet3**</span><span class="sxs-lookup"><span data-stu-id="0fb36-121">**ITablet3**</span></span>](itablet3.md)
</dt> </dl>

 

 




