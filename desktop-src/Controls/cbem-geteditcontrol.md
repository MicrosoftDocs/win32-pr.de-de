---
title: CBEM_GETEDITCONTROL Meldung (kommstrg. h)
description: Ruft das Handle für den Bearbeitungs Steuerelement Teil eines ComboBoxEx-Steuer Elements ab. Ein ComboBoxEx-Steuerelement verwendet ein Bearbeitungsfeld, wenn es auf den CBS- \_ Dropdown Stil festgelegt ist.
ms.assetid: def91949-cadc-4297-a504-0680d7d9b815
keywords:
- Windows-Steuerelemente für CBEM_GETEDITCONTROL Meldung
topic_type:
- apiref
api_name:
- CBEM_GETEDITCONTROL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 412d1183b29c8c89b5977d5f7f2a1b962d54dc01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105597"
---
# <a name="cbem_geteditcontrol-message"></a><span data-ttu-id="8376a-105">CBEM \_ geteditcontrol-Meldung</span><span class="sxs-lookup"><span data-stu-id="8376a-105">CBEM\_GETEDITCONTROL message</span></span>

<span data-ttu-id="8376a-106">Ruft das Handle für den Bearbeitungs Steuerelement Teil eines ComboBoxEx-Steuer Elements ab.</span><span class="sxs-lookup"><span data-stu-id="8376a-106">Gets the handle to the edit control portion of a ComboBoxEx control.</span></span> <span data-ttu-id="8376a-107">Ein ComboBoxEx-Steuerelement verwendet ein Bearbeitungsfeld, wenn es auf den [**CBS- \_ Dropdown**](combo-box-styles.md) Stil festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="8376a-107">A ComboBoxEx control uses an edit box when it is set to the [**CBS\_DROPDOWN**](combo-box-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="8376a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8376a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8376a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8376a-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="8376a-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="8376a-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="8376a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8376a-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="8376a-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="8376a-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8376a-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8376a-113">Return value</span></span>

<span data-ttu-id="8376a-114">Gibt das Handle für das Bearbeitungs Steuerelement im ComboBoxEx-Steuerelement zurück, wenn es die [**CBS- \_ Dropdown**](combo-box-styles.md) -Formatvorlage verwendet.</span><span class="sxs-lookup"><span data-stu-id="8376a-114">Returns the handle to the edit control within the ComboBoxEx control if it uses the [**CBS\_DROPDOWN**](combo-box-styles.md) style.</span></span> <span data-ttu-id="8376a-115">Andernfalls gibt die Meldung **null** zurück.</span><span class="sxs-lookup"><span data-stu-id="8376a-115">Otherwise, the message returns **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8376a-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8376a-116">Requirements</span></span>



| <span data-ttu-id="8376a-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8376a-117">Requirement</span></span> | <span data-ttu-id="8376a-118">Wert</span><span class="sxs-lookup"><span data-stu-id="8376a-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8376a-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8376a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8376a-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8376a-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8376a-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8376a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8376a-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8376a-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8376a-123">Header</span><span class="sxs-lookup"><span data-stu-id="8376a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8376a-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="8376a-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





