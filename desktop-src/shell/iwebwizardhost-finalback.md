---
description: Navigiert zur Client seitigen Seite unmittelbar vor der Seite, auf der die serverseitigen HTML-Seiten gehostet werden.
title: Webwizardhost. finalback-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost.FinalBack
api_type:
- COM
api_location:
- Shldisp.h
ms.assetid: a0616388-cf94-4433-ae52-24f02f1d15ac
ms.openlocfilehash: 704efbd4aae5a98ec01d8bd900e226144d25833d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865840"
---
# <a name="webwizardhostfinalback-method"></a><span data-ttu-id="555bf-103">Webwizardhost. finalback-Methode</span><span class="sxs-lookup"><span data-stu-id="555bf-103">WebWizardHost.FinalBack method</span></span>

<span data-ttu-id="555bf-104">Navigiert zur Client seitigen Seite unmittelbar vor der Seite, auf der die serverseitigen HTML-Seiten gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="555bf-104">Navigates to the client-side page immediately preceding the page hosting the server-side HTML pages.</span></span>

## <a name="syntax"></a><span data-ttu-id="555bf-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="555bf-105">Syntax</span></span>


```JScript
iRetVal = WebWizardHost.FinalBack()
```



## <a name="parameters"></a><span data-ttu-id="555bf-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="555bf-106">Parameters</span></span>

<span data-ttu-id="555bf-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="555bf-107">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="555bf-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="555bf-108">Remarks</span></span>

<span data-ttu-id="555bf-109">Wenn der Assistent die erste serverseitige Seite anzeigt und der Benutzer auf die Schaltfläche " **zurück** " klickt, ruft der Server **finalback** auf, wenn er über dieses Ereignis über den Ereignishandler des Clients benachrichtigt wird.</span><span class="sxs-lookup"><span data-stu-id="555bf-109">When the wizard displays the first server-side page and the user clicks the **Back** button, the server invokes **FinalBack** when notified of that event by the client's event handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="555bf-110">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="555bf-110">Requirements</span></span>



| <span data-ttu-id="555bf-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="555bf-111">Requirement</span></span> | <span data-ttu-id="555bf-112">Wert</span><span class="sxs-lookup"><span data-stu-id="555bf-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="555bf-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="555bf-113">Minimum supported client</span></span><br/> | <span data-ttu-id="555bf-114">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="555bf-114">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="555bf-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="555bf-115">Minimum supported server</span></span><br/> | <span data-ttu-id="555bf-116">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="555bf-116">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="555bf-117">Header</span><span class="sxs-lookup"><span data-stu-id="555bf-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="555bf-118"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="555bf-118"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="555bf-119">IDL</span><span class="sxs-lookup"><span data-stu-id="555bf-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="555bf-120"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="555bf-120"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 




