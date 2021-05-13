---
description: Navigiert zur clientseitigen Seite unmittelbar vor der Seite, die die serverseitigen HTML-Seiten hosten.
title: WebWizardHost.FinalBack-Methode (Shldisp.h)
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
ms.openlocfilehash: f131050bb5dd4cfc4b8533857c306f566f12ec2d
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841871"
---
# <a name="webwizardhostfinalback-method"></a><span data-ttu-id="b770d-103">WebWizardHost.FinalBack-Methode</span><span class="sxs-lookup"><span data-stu-id="b770d-103">WebWizardHost.FinalBack method</span></span>

<span data-ttu-id="b770d-104">Navigiert zur clientseitigen Seite unmittelbar vor der Seite, die die serverseitigen HTML-Seiten hosten.</span><span class="sxs-lookup"><span data-stu-id="b770d-104">Navigates to the client-side page immediately preceding the page hosting the server-side HTML pages.</span></span>

## <a name="syntax"></a><span data-ttu-id="b770d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b770d-105">Syntax</span></span>


```JScript
iRetVal = WebWizardHost.FinalBack()
```



## <a name="parameters"></a><span data-ttu-id="b770d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b770d-106">Parameters</span></span>

<span data-ttu-id="b770d-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="b770d-107">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="b770d-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b770d-108">Remarks</span></span>

<span data-ttu-id="b770d-109">Wenn der Assistent die erste serverseitige Seite anzeigt  und der Benutzer auf die Schaltfläche Zurück klickt, ruft der Server **FinalBack** auf, wenn er vom Ereignishandler des Clients über dieses Ereignis benachrichtigt wird.</span><span class="sxs-lookup"><span data-stu-id="b770d-109">When the wizard displays the first server-side page and the user clicks the **Back** button, the server invokes **FinalBack** when notified of that event by the client's event handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="b770d-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b770d-110">Requirements</span></span>



| <span data-ttu-id="b770d-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b770d-111">Requirement</span></span> | <span data-ttu-id="b770d-112">Wert</span><span class="sxs-lookup"><span data-stu-id="b770d-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b770d-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b770d-113">Minimum supported client</span></span><br/> | <span data-ttu-id="b770d-114">Nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b770d-114">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="b770d-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b770d-115">Minimum supported server</span></span><br/> | <span data-ttu-id="b770d-116">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b770d-116">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b770d-117">Header</span><span class="sxs-lookup"><span data-stu-id="b770d-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="b770d-118"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="b770d-118"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b770d-119">Idl</span><span class="sxs-lookup"><span data-stu-id="b770d-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b770d-120"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="b770d-120"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 




