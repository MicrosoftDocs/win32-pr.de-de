---
description: Navigiert zur clientseitigen Assistentenseite, die auf die Seite folgt, die die serverseitigen HTML-Seiten hostet, oder beendet den Assistenten, wenn keine weiteren clientseitigen Seiten verfügbar sind.
title: WebWizardHost.FinalNext-Methode (Shldisp.h)
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
ms.openlocfilehash: fa59a70c04e7f78a315955aeabb9477c6f28c80d
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841841"
---
# <a name="webwizardhostfinalnext-method"></a><span data-ttu-id="45348-103">WebWizardHost.FinalNext-Methode</span><span class="sxs-lookup"><span data-stu-id="45348-103">WebWizardHost.FinalNext method</span></span>

<span data-ttu-id="45348-104">Navigiert zur clientseitigen Assistentenseite, die auf die Seite folgt, die die serverseitigen HTML-Seiten hostet, oder beendet den Assistenten, wenn keine weiteren clientseitigen Seiten verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="45348-104">Navigates to the client-side wizard page that follows the page that hosts the server-side HTML pages, or finishes the wizard if there are no further client-side pages.</span></span>

## <a name="syntax"></a><span data-ttu-id="45348-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="45348-105">Syntax</span></span>


```JScript
iRetVal = WebWizardHost.FinalNext()
```



## <a name="parameters"></a><span data-ttu-id="45348-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="45348-106">Parameters</span></span>

<span data-ttu-id="45348-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="45348-107">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="45348-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="45348-108">Remarks</span></span>

<span data-ttu-id="45348-109">Wenn der Assistent die letzte serverseitige HTML-Seite zeigt  und  der Benutzer auf die Schaltfläche Weiter oder Fertig stellen klickt, ruft der Server **FinalNext** im Ereignishandler dieser Schaltfläche auf.</span><span class="sxs-lookup"><span data-stu-id="45348-109">When the wizard is displaying the last server-side HTML page and the user clicks the **Next** or **Finish** button, the server invokes **FinalNext** in that button's event handler.</span></span>

## <a name="requirements"></a><span data-ttu-id="45348-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="45348-110">Requirements</span></span>



| <span data-ttu-id="45348-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="45348-111">Requirement</span></span> | <span data-ttu-id="45348-112">Wert</span><span class="sxs-lookup"><span data-stu-id="45348-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="45348-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="45348-113">Minimum supported client</span></span><br/> | <span data-ttu-id="45348-114">Nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="45348-114">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="45348-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="45348-115">Minimum supported server</span></span><br/> | <span data-ttu-id="45348-116">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="45348-116">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="45348-117">Header</span><span class="sxs-lookup"><span data-stu-id="45348-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="45348-118"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="45348-118"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="45348-119">Idl</span><span class="sxs-lookup"><span data-stu-id="45348-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="45348-120"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="45348-120"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 




