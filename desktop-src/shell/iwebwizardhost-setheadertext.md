---
description: Legt den Titel und den Untertitel fest, die im Assistenten Header angezeigt werden. Im Allgemeinen zeigt der Client den Header oberhalb von HTML und unterhalb der Titelleiste an.
title: Webwizardhost. abadertext-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost.SetHeaderText
api_type:
- COM
api_location:
- Shldisp.h
ms.assetid: e627de44-9929-4e08-9fd9-ca22743f434a
ms.openlocfilehash: 92e23fab94cfedd8bbc62e31086759af48238a95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980256"
---
# <a name="webwizardhostsetheadertext-method"></a><span data-ttu-id="cd36a-104">Webwizardhost. abadertext-Methode</span><span class="sxs-lookup"><span data-stu-id="cd36a-104">WebWizardHost.SetHeaderText method</span></span>

<span data-ttu-id="cd36a-105">Legt den Titel und den Untertitel fest, die im Assistenten Header angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="cd36a-105">Sets the title and subtitle that appear in the wizard header.</span></span> <span data-ttu-id="cd36a-106">Im Allgemeinen zeigt der Client den Header oberhalb von HTML und unterhalb der Titelleiste an.</span><span class="sxs-lookup"><span data-stu-id="cd36a-106">In general, the client will display the header above the HTML and below the title bar.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd36a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd36a-107">Syntax</span></span>


```JScript
iRetVal = WebWizardHost.SetHeaderText(
  bstrHeaderTitle,
  bstrHeaderSubtitle
)
```



## <a name="parameters"></a><span data-ttu-id="cd36a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="cd36a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd36a-109">*bstrinheadertitle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cd36a-109">*bstrHeaderTitle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd36a-110">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="cd36a-110">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="cd36a-111">Zeichenfolge, die den Titel enthält.</span><span class="sxs-lookup"><span data-stu-id="cd36a-111">String containing the title.</span></span>

</dd> <dt>

<span data-ttu-id="cd36a-112">*bstrinheaderuntertitel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cd36a-112">*bstrHeaderSubtitle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd36a-113">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="cd36a-113">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="cd36a-114">Zeichenfolge, die Untertitel enthält.</span><span class="sxs-lookup"><span data-stu-id="cd36a-114">String containing the subtitle.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cd36a-115">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="cd36a-115">Requirements</span></span>



| <span data-ttu-id="cd36a-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cd36a-116">Requirement</span></span> | <span data-ttu-id="cd36a-117">Wert</span><span class="sxs-lookup"><span data-stu-id="cd36a-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd36a-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cd36a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="cd36a-119">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cd36a-119">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="cd36a-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cd36a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="cd36a-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cd36a-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="cd36a-122">Header</span><span class="sxs-lookup"><span data-stu-id="cd36a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd36a-123"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd36a-123"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="cd36a-124">IDL</span><span class="sxs-lookup"><span data-stu-id="cd36a-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cd36a-125"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cd36a-125"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 
