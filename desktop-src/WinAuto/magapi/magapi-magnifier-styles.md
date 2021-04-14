---
title: Bildschirm Stile
description: In diesem Thema werden die Stile beschrieben, die mit dem Bildschirm Steuerelement verwendet werden.
ms.assetid: B3C575AC-B8D3-40CF-AF09-BAC73E6C7B45
topic_type:
- apiref
api_name:
- MS_CLIPAROUNDCURSOR
- MS_INVERTCOLORS
- MS_SHOWMAGNIFIEDCURSOR
api_location:
- Magnification.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/07/2020
ms.openlocfilehash: 212e079a59db9a85b6d232d1c11ac9f46eceb314
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391929"
---
# <a name="magnifier-styles"></a><span data-ttu-id="e17ce-103">Bildschirm Stile</span><span class="sxs-lookup"><span data-stu-id="e17ce-103">Magnifier Styles</span></span>

<span data-ttu-id="e17ce-104">In diesem Thema werden die Stile beschrieben, die mit dem Bildschirm Steuerelement verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e17ce-104">This topic describes the styles used with the magnifier control.</span></span> <span data-ttu-id="e17ce-105">Um ein Bildschirm Steuerelement zu erstellen, verwenden Sie die Funktion "die Funktion" ", und geben [**Sie die WC_MAGNIFIER**](/windows/win32/api/winuser/nf-winuser-createwindowexa) Window-Klasse zusammen mit einer Kombination der folgenden Bildschirm Stile an.</span><span class="sxs-lookup"><span data-stu-id="e17ce-105">To create a magnifier control, use the [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) function and specify the WC_MAGNIFIER window class, along with a combination of the following magnifier styles.</span></span>

| <span data-ttu-id="e17ce-106">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e17ce-106">Requirement</span></span> | <span data-ttu-id="e17ce-107">Wert</span><span class="sxs-lookup"><span data-stu-id="e17ce-107">Value</span></span> |
|:---|:---|
| <span data-ttu-id="e17ce-108">MS_CLIPAROUNDCURSOR 0x0002l</span><span class="sxs-lookup"><span data-stu-id="e17ce-108">MS_CLIPAROUNDCURSOR 0x0002L</span></span> | <span data-ttu-id="e17ce-109">Schneidet den Bereich des Vergrößerungs Fensters ab, der den System Cursor umgibt.</span><span class="sxs-lookup"><span data-stu-id="e17ce-109">Clips the area of the magnifier window that surrounds the system cursor.</span></span> <span data-ttu-id="e17ce-110">Dieser Stil ermöglicht dem Benutzer das Anzeigen von Bildschirminhalt, der sich hinter dem Fenster "Bildschirmlupe" befindet.</span><span class="sxs-lookup"><span data-stu-id="e17ce-110">This style enables the user to see screen content that is behind the magnifier window.</span></span> |
| <span data-ttu-id="e17ce-111">MS_INVERTCOLORS 0x0004l</span><span class="sxs-lookup"><span data-stu-id="e17ce-111">MS_INVERTCOLORS 0x0004L</span></span> | <span data-ttu-id="e17ce-112">Zeigt den vergrößerten Bildschirminhalt mithilfe von umgekehrten Farben an.</span><span class="sxs-lookup"><span data-stu-id="e17ce-112">Displays the magnified screen content using inverted colors.</span></span> |
| <span data-ttu-id="e17ce-113">MS_SHOWMAGNIFIEDCURSOR 0x0001l</span><span class="sxs-lookup"><span data-stu-id="e17ce-113">MS_SHOWMAGNIFIEDCURSOR 0x0001L</span></span> | <span data-ttu-id="e17ce-114">Zeigt den vergrößerten System Cursor zusammen mit den vergrößerten Bildschirm Inhalten an.</span><span class="sxs-lookup"><span data-stu-id="e17ce-114">Displays the magnified system cursor along with the magnified screen content.</span></span> |

## <a name="requirements"></a><span data-ttu-id="e17ce-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e17ce-115">Requirements</span></span>

| <span data-ttu-id="e17ce-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e17ce-116">Requirement</span></span> | <span data-ttu-id="e17ce-117">Wert</span><span class="sxs-lookup"><span data-stu-id="e17ce-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="e17ce-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e17ce-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e17ce-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e17ce-119">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e17ce-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e17ce-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e17ce-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e17ce-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="e17ce-122">Header</span><span class="sxs-lookup"><span data-stu-id="e17ce-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e17ce-123"><dt>Vergrößerung. h</dt></span><span class="sxs-lookup"><span data-stu-id="e17ce-123"><dt>Magnification.h</dt></span></span> </dl> |

## <a name="see-also"></a><span data-ttu-id="e17ce-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e17ce-124">See also</span></span>

[<span data-ttu-id="e17ce-125">Konstanten</span><span class="sxs-lookup"><span data-stu-id="e17ce-125">Constants</span></span>](entry-magapi-constants.md)
