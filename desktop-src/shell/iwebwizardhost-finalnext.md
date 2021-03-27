---
description: Navigiert zur Client seitigen Assistenten Seite, die der Seite folgt, auf der die serverseitigen HTML-Seiten gehostet werden, oder schließt den Assistenten ab, wenn keine weiteren Client seitigen Seiten vorhanden sind.
title: Webwizardhost. finalnext-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost.FinalNext
api_type:
- COM
api_location:
- Shldisp.h
ms.assetid: 0699eb16-d6ef-46e3-bd02-d35512536275
ms.openlocfilehash: 5693de342b03a9ee4b7ed04cf24d8cfa9ee8b784
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216989"
---
# <a name="webwizardhostfinalnext-method"></a><span data-ttu-id="dc234-103">Webwizardhost. finalnext-Methode</span><span class="sxs-lookup"><span data-stu-id="dc234-103">WebWizardHost.FinalNext method</span></span>

<span data-ttu-id="dc234-104">Navigiert zur Client seitigen Assistenten Seite, die der Seite folgt, auf der die serverseitigen HTML-Seiten gehostet werden, oder schließt den Assistenten ab, wenn keine weiteren Client seitigen Seiten vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="dc234-104">Navigates to the client-side wizard page that follows the page that hosts the server-side HTML pages, or finishes the wizard if there are no further client-side pages.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc234-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc234-105">Syntax</span></span>


```JScript
iRetVal = WebWizardHost.FinalNext()
```



## <a name="parameters"></a><span data-ttu-id="dc234-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc234-106">Parameters</span></span>

<span data-ttu-id="dc234-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="dc234-107">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc234-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dc234-108">Remarks</span></span>

<span data-ttu-id="dc234-109">Wenn der Assistent die letzte serverseitige HTML-Seite anzeigt und der Benutzer auf die Schaltfläche " **weiter** " oder " **Fertig** stellen" klickt, ruft der Server **finalnext** im-Ereignishandler der Schaltfläche auf.</span><span class="sxs-lookup"><span data-stu-id="dc234-109">When the wizard is displaying the last server-side HTML page and the user clicks the **Next** or **Finish** button, the server invokes **FinalNext** in that button's event handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc234-110">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="dc234-110">Requirements</span></span>



| <span data-ttu-id="dc234-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dc234-111">Requirement</span></span> | <span data-ttu-id="dc234-112">Wert</span><span class="sxs-lookup"><span data-stu-id="dc234-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc234-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dc234-113">Minimum supported client</span></span><br/> | <span data-ttu-id="dc234-114">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dc234-114">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="dc234-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dc234-115">Minimum supported server</span></span><br/> | <span data-ttu-id="dc234-116">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dc234-116">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="dc234-117">Header</span><span class="sxs-lookup"><span data-stu-id="dc234-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc234-118"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc234-118"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="dc234-119">IDL</span><span class="sxs-lookup"><span data-stu-id="dc234-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dc234-120"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dc234-120"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 




