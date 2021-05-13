---
description: Legt den Titel und Untertitel fest, die im Assistentenheader angezeigt werden. Im Allgemeinen zeigt der Client den Header über dem HTML-Code und unterhalb der Titelleiste an.
title: WebWizardHost.SetHeaderText-Methode (Shldisp.h)
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
ms.openlocfilehash: d524f9ae6d1031d518e237d393bbb1dc0d35b2bd
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841831"
---
# <a name="webwizardhostsetheadertext-method"></a><span data-ttu-id="69b15-104">WebWizardHost.SetHeaderText-Methode</span><span class="sxs-lookup"><span data-stu-id="69b15-104">WebWizardHost.SetHeaderText method</span></span>

<span data-ttu-id="69b15-105">Legt den Titel und Untertitel fest, die im Assistentenheader angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="69b15-105">Sets the title and subtitle that appear in the wizard header.</span></span> <span data-ttu-id="69b15-106">Im Allgemeinen zeigt der Client den Header über dem HTML-Code und unterhalb der Titelleiste an.</span><span class="sxs-lookup"><span data-stu-id="69b15-106">In general, the client will display the header above the HTML and below the title bar.</span></span>

## <a name="syntax"></a><span data-ttu-id="69b15-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="69b15-107">Syntax</span></span>


```JScript
iRetVal = WebWizardHost.SetHeaderText(
  bstrHeaderTitle,
  bstrHeaderSubtitle
)
```



## <a name="parameters"></a><span data-ttu-id="69b15-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="69b15-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69b15-109">*bstrHeaderTitle* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="69b15-109">*bstrHeaderTitle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69b15-110">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="69b15-110">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="69b15-111">Eine Zeichenfolge, die den Titel enthält.</span><span class="sxs-lookup"><span data-stu-id="69b15-111">String containing the title.</span></span>

</dd> <dt>

<span data-ttu-id="69b15-112">*bstrHeaderSubtitle* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="69b15-112">*bstrHeaderSubtitle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69b15-113">Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="69b15-113">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="69b15-114">Eine Zeichenfolge, die den Untertitel enthält.</span><span class="sxs-lookup"><span data-stu-id="69b15-114">String containing the subtitle.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="69b15-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="69b15-115">Requirements</span></span>



| <span data-ttu-id="69b15-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="69b15-116">Requirement</span></span> | <span data-ttu-id="69b15-117">Wert</span><span class="sxs-lookup"><span data-stu-id="69b15-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="69b15-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="69b15-118">Minimum supported client</span></span><br/> | <span data-ttu-id="69b15-119">Nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="69b15-119">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="69b15-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="69b15-120">Minimum supported server</span></span><br/> | <span data-ttu-id="69b15-121">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="69b15-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="69b15-122">Header</span><span class="sxs-lookup"><span data-stu-id="69b15-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="69b15-123"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="69b15-123"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="69b15-124">Idl</span><span class="sxs-lookup"><span data-stu-id="69b15-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="69b15-125"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="69b15-125"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 
