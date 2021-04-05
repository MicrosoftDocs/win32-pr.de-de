---
title: TB_CHANGEBITMAP Meldung (kommstrg. h)
description: Ändert die Bitmap für eine Schaltfläche in einer Symbolleiste.
ms.assetid: 112b6f4e-6034-4e13-8b2f-b8411a351fbd
keywords:
- Windows-Steuerelemente für TB_CHANGEBITMAP Meldung
topic_type:
- apiref
api_name:
- TB_CHANGEBITMAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1367a2a1b4e35d6f52bf1e7a0be42f1e75daa7ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859335"
---
# <a name="tb_changebitmap-message"></a><span data-ttu-id="f9e2f-104">TB \_ changebitmap-Meldung</span><span class="sxs-lookup"><span data-stu-id="f9e2f-104">TB\_CHANGEBITMAP message</span></span>

<span data-ttu-id="f9e2f-105">Ändert die Bitmap für eine Schaltfläche in einer Symbolleiste.</span><span class="sxs-lookup"><span data-stu-id="f9e2f-105">Changes the bitmap for a button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="f9e2f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9e2f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9e2f-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f9e2f-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f9e2f-108">Der Befehls Bezeichner der Schaltfläche, mit der eine neue Bitmap empfangen werden soll.</span><span class="sxs-lookup"><span data-stu-id="f9e2f-108">Command identifier of the button that is to receive a new bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="f9e2f-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f9e2f-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f9e2f-110">NULL basierter Index eines Bilds in der Bildliste der Symbolleiste.</span><span class="sxs-lookup"><span data-stu-id="f9e2f-110">Zero-based index of an image in the toolbar's image list.</span></span> <span data-ttu-id="f9e2f-111">Das System zeigt das angegebene Bild in der Schaltfläche an.</span><span class="sxs-lookup"><span data-stu-id="f9e2f-111">The system displays the specified image in the button.</span></span> <span data-ttu-id="f9e2f-112">Legen Sie diesen Parameter auf " \_ imagecallback" fest, und die Symbolleiste sendet die [**TBN- \_ getdispinfo**](tbn-getdispinfo.md) -Benachrichtigung, um den Abbild Index bei Bedarf abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f9e2f-112">Set this parameter to I\_IMAGECALLBACK, and the toolbar will send the [**TBN\_GETDISPINFO**](tbn-getdispinfo.md) notification to retrieve the image index when it is needed.</span></span>

<span data-ttu-id="f9e2f-113">[Version 5,81](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="f9e2f-113">[Version 5.81](common-control-versions.md).</span></span> <span data-ttu-id="f9e2f-114">Legen Sie diesen Parameter auf " \_ imagenone" fest, um anzugeben, dass die Schaltfläche kein Bild hat.</span><span class="sxs-lookup"><span data-stu-id="f9e2f-114">Set this parameter to I\_IMAGENONE to indicate that the button does not have an image.</span></span> <span data-ttu-id="f9e2f-115">Das Layout der Schaltfläche enthält keinen Platz für eine Bitmap, sondern nur Text.</span><span class="sxs-lookup"><span data-stu-id="f9e2f-115">The button layout will not include any space for a bitmap, only text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9e2f-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f9e2f-116">Return value</span></span>

<span data-ttu-id="f9e2f-117">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="f9e2f-117">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9e2f-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f9e2f-118">Requirements</span></span>



| <span data-ttu-id="f9e2f-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f9e2f-119">Requirement</span></span> | <span data-ttu-id="f9e2f-120">Wert</span><span class="sxs-lookup"><span data-stu-id="f9e2f-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f9e2f-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f9e2f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f9e2f-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f9e2f-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f9e2f-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f9e2f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f9e2f-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f9e2f-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f9e2f-125">Header</span><span class="sxs-lookup"><span data-stu-id="f9e2f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9e2f-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9e2f-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





