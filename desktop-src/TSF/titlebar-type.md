---
title: TITLEBAR_TYPE-Enumeration (Software-Domänen Controller. h)
description: Elemente der Titlebar- \_ Typenumeration werden verwendet, um die Typen von titlebars anzugeben, die für ein weiches Tastatur Fenster verfügbar sind.
ms.assetid: 10d9b1c0-fd52-4f62-9268-cb8903a4c2db
keywords:
- TITLEBAR_TYPE Enumeration Text Services-Framework
topic_type:
- apiref
api_name:
- TITLEBAR_TYPE
api_location:
- Softkbdc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97ae1af1aba106a9f319cee080d0963992034a75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342016"
---
# <a name="titlebar_type-enumeration"></a><span data-ttu-id="3c805-104">TitleBar- \_ Typenumeration</span><span class="sxs-lookup"><span data-stu-id="3c805-104">TITLEBAR\_TYPE enumeration</span></span>

<span data-ttu-id="3c805-105">Elemente der **TitleBar- \_ Typenumeration** werden verwendet, um die Typen von titlebars anzugeben, die für ein weiches Tastatur Fenster verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="3c805-105">Elements of the **TITLEBAR\_TYPE** enumeration are used to specify types of titlebars that are available for a soft keyboard window.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c805-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3c805-106">Syntax</span></span>


```C++
typedef enum tagTITLEBAR_TYPE { 
  TITLEBAR_NONE                = 0,
  TITLEBAR_GRIPPER_HORIZ_ONLY  = 1,
  TITLEBAR_GRIPPER_VERTI_ONLY  = 2,
  TITLEBAR_GRIPPER_BUTTON      = 3
} TITLEBAR_TYPE;
```



## <a name="constants"></a><span data-ttu-id="3c805-107">Konstanten</span><span class="sxs-lookup"><span data-stu-id="3c805-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="3c805-108"><span id="TITLEBAR_NONE"></span><span id="titlebar_none"></span>**TitleBar \_ None**</span><span class="sxs-lookup"><span data-stu-id="3c805-108"><span id="TITLEBAR_NONE"></span><span id="titlebar_none"></span>**TITLEBAR\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="3c805-109">Das weiche Tastatur Fenster verwendet keine Titlebar.</span><span class="sxs-lookup"><span data-stu-id="3c805-109">The soft keyboard window uses no titlebar.</span></span>

</dd> <dt>

<span data-ttu-id="3c805-110"><span id="TITLEBAR_GRIPPER_HORIZ_ONLY"></span><span id="titlebar_gripper_horiz_only"></span>**nur Titlebar- \_ \_ gripperhoriz \_**</span><span class="sxs-lookup"><span data-stu-id="3c805-110"><span id="TITLEBAR_GRIPPER_HORIZ_ONLY"></span><span id="titlebar_gripper_horiz_only"></span>**TITLEBAR\_GRIPPER\_HORIZ\_ONLY**</span></span>
</dt> <dd>

<span data-ttu-id="3c805-111">Das weiche Tastatur Fenster verwendet nur eine horizontale Zieh Punkt Leiste.</span><span class="sxs-lookup"><span data-stu-id="3c805-111">The soft keyboard window uses a horizontal gripper bar only.</span></span>

</dd> <dt>

<span data-ttu-id="3c805-112"><span id="TITLEBAR_GRIPPER_VERTI_ONLY"></span><span id="titlebar_gripper_verti_only"></span>**TitleBar-Zieh Punkt \_ \_ nur Verti \_**</span><span class="sxs-lookup"><span data-stu-id="3c805-112"><span id="TITLEBAR_GRIPPER_VERTI_ONLY"></span><span id="titlebar_gripper_verti_only"></span>**TITLEBAR\_GRIPPER\_VERTI\_ONLY**</span></span>
</dt> <dd>

<span data-ttu-id="3c805-113">Das weiche Tastatur Fenster verwendet nur eine vertikale Zieh Punkt Leiste.</span><span class="sxs-lookup"><span data-stu-id="3c805-113">The soft keyboard window uses a vertical gripper bar only.</span></span>

</dd> <dt>

<span data-ttu-id="3c805-114"><span id="TITLEBAR_GRIPPER_BUTTON"></span><span id="titlebar_gripper_button"></span>**TitleBar- \_ gripperschaltfläche \_**</span><span class="sxs-lookup"><span data-stu-id="3c805-114"><span id="TITLEBAR_GRIPPER_BUTTON"></span><span id="titlebar_gripper_button"></span>**TITLEBAR\_GRIPPER\_BUTTON**</span></span>
</dt> <dd>

<span data-ttu-id="3c805-115">Das weiche Tastatur Fenster verwendet nur eine Zieh Punkt Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="3c805-115">The soft keyboard window uses a gripper button only.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3c805-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3c805-116">Requirements</span></span>



| <span data-ttu-id="3c805-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3c805-117">Requirement</span></span> | <span data-ttu-id="3c805-118">Wert</span><span class="sxs-lookup"><span data-stu-id="3c805-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c805-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3c805-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3c805-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3c805-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3c805-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3c805-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3c805-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3c805-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="3c805-123">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="3c805-123">Redistributable</span></span><br/>          | <span data-ttu-id="3c805-124">TSF 1,0 unter Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="3c805-124">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="3c805-125">Header</span><span class="sxs-lookup"><span data-stu-id="3c805-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c805-126"><dt>Software-Domänen Controller. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c805-126"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="3c805-127">IDL</span><span class="sxs-lookup"><span data-stu-id="3c805-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3c805-128"><dt>Software. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3c805-128"><dt>Softkbd.idl</dt></span></span> </dl> |



 

 





