---
title: TB_COMMANDTOINDEX Meldung (kommstrg. h)
description: Ruft den NULL basierten Index für die Schaltfläche ab, die dem angegebenen Befehls Bezeichner zugeordnet ist.
ms.assetid: vs|controls|~\controls\toolbar\messages\tb_commandtoindex.htm
keywords:
- Windows-Steuerelemente für TB_COMMANDTOINDEX Meldung
topic_type:
- apiref
api_name:
- TB_COMMANDTOINDEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0257f55e01db59f1d23d59583f1ef78f44b1dac1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106605"
---
# <a name="tb_commandtoindex-message"></a><span data-ttu-id="9327a-104">TB \_ commanddeindex-Meldung</span><span class="sxs-lookup"><span data-stu-id="9327a-104">TB\_COMMANDTOINDEX message</span></span>

<span data-ttu-id="9327a-105">Ruft den NULL basierten Index für die Schaltfläche ab, die dem angegebenen Befehls Bezeichner zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="9327a-105">Retrieves the zero-based index for the button associated with the specified command identifier.</span></span>

## <a name="parameters"></a><span data-ttu-id="9327a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9327a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9327a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9327a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9327a-108">Der Befehls Bezeichner, der der Schaltfläche zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="9327a-108">Command identifier associated with the button.</span></span>

</dd> <dt>

<span data-ttu-id="9327a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9327a-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9327a-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="9327a-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9327a-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9327a-111">Return value</span></span>

<span data-ttu-id="9327a-112">Gibt den NULL basierten Index für die Schaltfläche oder-1 zurück, wenn der angegebene Befehls Bezeichner ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="9327a-112">Returns the zero-based index for the button or -1 if the specified command identifier is invalid.</span></span>

## <a name="requirements"></a><span data-ttu-id="9327a-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9327a-113">Requirements</span></span>



| <span data-ttu-id="9327a-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9327a-114">Requirement</span></span> | <span data-ttu-id="9327a-115">Wert</span><span class="sxs-lookup"><span data-stu-id="9327a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9327a-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9327a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9327a-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9327a-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9327a-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9327a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9327a-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9327a-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9327a-120">Header</span><span class="sxs-lookup"><span data-stu-id="9327a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9327a-121"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="9327a-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





