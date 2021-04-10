---
title: TDN_HYPERLINK_CLICKED Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Aufgaben Dialogfeld gesendet, wenn der Benutzer auf einen Link im Inhalt des Aufgaben Dialogfelds klickt. Dieser Benachrichtigungs Code wird nur über die Task Dialog-Rückruffunktion empfangen, die mit der TaskDialogIndirect-Methode registriert werden kann.
ms.assetid: b769af31-32d0-463e-be15-6abf5dcb425c
keywords:
- Windows-Steuerelemente für TDN_HYPERLINK_CLICKED Benachrichtigungs
topic_type:
- apiref
api_name:
- TDN_HYPERLINK_CLICKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edd79406eb59f9bafd93269f8982db6213ef882c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106233"
---
# <a name="tdn_hyperlink_clicked-notification-code"></a><span data-ttu-id="4446b-105">Von TDN \_ \_ angeklickte Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="4446b-105">TDN\_HYPERLINK\_CLICKED notification code</span></span>

<span data-ttu-id="4446b-106">Wird von einem Aufgaben Dialogfeld gesendet, wenn der Benutzer auf einen Link im Inhalt des Aufgaben Dialogfelds klickt.</span><span class="sxs-lookup"><span data-stu-id="4446b-106">Sent by a task dialog when the user clicks a hyperlink in the task dialog content.</span></span> <span data-ttu-id="4446b-107">Dieser Benachrichtigungs Code wird nur über die Task Dialog-Rückruffunktion empfangen, die mit der [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) -Methode registriert werden kann.</span><span class="sxs-lookup"><span data-stu-id="4446b-107">This notification code is received only through the task dialog callback function, which can be registered using the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) method.</span></span>


```C++
TDN_HYPERLINK_CLICKED

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="4446b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4446b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4446b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4446b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4446b-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="4446b-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="4446b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4446b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4446b-112">Zeiger auf eine breit Zeichen-Zeichenfolge, die die URL des Links enthält.</span><span class="sxs-lookup"><span data-stu-id="4446b-112">Pointer to a wide-character string containing the URL of the hyperlink.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4446b-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4446b-113">Return value</span></span>

<span data-ttu-id="4446b-114">Der Rückgabewert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="4446b-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="4446b-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4446b-115">Requirements</span></span>



| <span data-ttu-id="4446b-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4446b-116">Requirement</span></span> | <span data-ttu-id="4446b-117">Wert</span><span class="sxs-lookup"><span data-stu-id="4446b-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4446b-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4446b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4446b-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4446b-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4446b-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4446b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4446b-121">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4446b-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4446b-122">Header</span><span class="sxs-lookup"><span data-stu-id="4446b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4446b-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="4446b-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





