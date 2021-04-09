---
title: TB_GETBITMAP Meldung (kommstrg. h)
description: Ruft den Index der Bitmap ab, die einer Schaltfläche in einer Symbolleiste zugeordnet ist.
ms.assetid: 64878cca-7d71-48ad-b2ed-d2bdc3067592
keywords:
- Windows-Steuerelemente für TB_GETBITMAP Meldung
topic_type:
- apiref
api_name:
- TB_GETBITMAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 771073b67b1421a5d9bda9d162bc234400c85885
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957250"
---
# <a name="tb_getbitmap-message"></a><span data-ttu-id="86570-104">TB \_ getbitmap-Meldung</span><span class="sxs-lookup"><span data-stu-id="86570-104">TB\_GETBITMAP message</span></span>

<span data-ttu-id="86570-105">Ruft den Index der Bitmap ab, die einer Schaltfläche in einer Symbolleiste zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="86570-105">Retrieves the index of the bitmap associated with a button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="86570-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="86570-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86570-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="86570-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="86570-108">Befehls Bezeichner der Schaltfläche, deren Bitmapindex abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="86570-108">Command identifier of the button whose bitmap index is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="86570-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="86570-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="86570-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="86570-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86570-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="86570-111">Return value</span></span>

<span data-ttu-id="86570-112">Gibt den Index der Bitmap zurück, wenn erfolgreich, andernfalls 0 (null).</span><span class="sxs-lookup"><span data-stu-id="86570-112">Returns the index of the bitmap if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="86570-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="86570-113">Requirements</span></span>



| <span data-ttu-id="86570-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="86570-114">Requirement</span></span> | <span data-ttu-id="86570-115">Wert</span><span class="sxs-lookup"><span data-stu-id="86570-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="86570-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="86570-116">Minimum supported client</span></span><br/> | <span data-ttu-id="86570-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="86570-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="86570-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="86570-118">Minimum supported server</span></span><br/> | <span data-ttu-id="86570-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="86570-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="86570-120">Header</span><span class="sxs-lookup"><span data-stu-id="86570-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="86570-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="86570-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





