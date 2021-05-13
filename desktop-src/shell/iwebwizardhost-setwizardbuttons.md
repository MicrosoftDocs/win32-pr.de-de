---
description: Aktualisiert die Schaltflächen Zurück, Weiter und Fertig stellen im Assistentenframe des Clients.
title: WebWizardHost.SetWizardButtons-Methode (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost.SetWizardButtons
api_type:
- COM
api_location:
- Shldisp.h
ms.assetid: 863aa667-454c-40cd-8091-9bb456047b6c
ms.openlocfilehash: a1b2a79c7ea323c36371e08d3519e71e4c537935
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842621"
---
# <a name="webwizardhostsetwizardbuttons-method"></a><span data-ttu-id="bfde5-103">WebWizardHost.SetWizardButtons-Methode</span><span class="sxs-lookup"><span data-stu-id="bfde5-103">WebWizardHost.SetWizardButtons method</span></span>

<span data-ttu-id="bfde5-104">Aktualisiert die Schaltflächen **Zurück,** **Weiter** und **Fertig stellen** im Assistentenframe des Clients.</span><span class="sxs-lookup"><span data-stu-id="bfde5-104">Updates the **Back**, **Next**, and **Finish** buttons in the client's wizard frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfde5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bfde5-105">Syntax</span></span>


```JScript
iRetVal = WebWizardHost.SetWizardButtons(
  vbEnableBack,
  vbEnableNext,
  vbLastPage
)
```



## <a name="parameters"></a><span data-ttu-id="bfde5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bfde5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfde5-107">*vbEnableBack* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="bfde5-107">*vbEnableBack* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfde5-108">Typ: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="bfde5-108">Type: **Boolean**</span></span>

<span data-ttu-id="bfde5-109">Aktiviert die Schaltfläche **Zurück.**</span><span class="sxs-lookup"><span data-stu-id="bfde5-109">Enables the **Back** button.</span></span>

</dd> <dt>

<span data-ttu-id="bfde5-110">*vbEnableNext* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="bfde5-110">*vbEnableNext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfde5-111">Typ: **Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="bfde5-111">Type: **Boolean**</span></span>

<span data-ttu-id="bfde5-112">Hiermit wird die Schaltfläche **Weiter** aktiviert.</span><span class="sxs-lookup"><span data-stu-id="bfde5-112">Enables the **Next** button.</span></span>

</dd> <dt>

<span data-ttu-id="bfde5-113">*vbLastPage* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="bfde5-113">*vbLastPage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bfde5-114">Typ: **Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="bfde5-114">Type: **Boolean**</span></span>

<span data-ttu-id="bfde5-115">Aktiviert die Schaltfläche **Fertig stellen.**</span><span class="sxs-lookup"><span data-stu-id="bfde5-115">Enables the **Finish** button.</span></span> <span data-ttu-id="bfde5-116">Gibt an, dass dies die letzte serverseitige Seite ist.</span><span class="sxs-lookup"><span data-stu-id="bfde5-116">States that this is the last server-side page.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bfde5-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bfde5-117">Remarks</span></span>

<span data-ttu-id="bfde5-118">Stellen Sie sicher, dass Sie Handlerfunktionen auf jeder serverseitigen Seite für OnBack() und OnNext() implementieren, die den Assistentenschaltflächen **Zurück** und **Weiter** entsprechen.</span><span class="sxs-lookup"><span data-stu-id="bfde5-118">Be sure to implement handler functions in each server-side page for OnBack() and OnNext(), corresponding to the wizard buttons **Back** and **Next**.</span></span> <span data-ttu-id="bfde5-119">Die Funktionen OnBack() und OnNext() reagieren auf **SetWizardButtons**.</span><span class="sxs-lookup"><span data-stu-id="bfde5-119">The OnBack() and OnNext() functions respond to **SetWizardButtons**.</span></span> <span data-ttu-id="bfde5-120">Zur entsprechenden Zeit ruft die OnNext()-Funktion **SetWizardButtons** mit *vbLastPage* = **true** auf, wodurch eine **Fertig stellen-Schaltfläche** aktiviert werden kann.</span><span class="sxs-lookup"><span data-stu-id="bfde5-120">At the appropriate time, the OnNext() function calls **SetWizardButtons** with *vbLastPage*=**true**, which can enable a **Finish** button.</span></span> <span data-ttu-id="bfde5-121">OnNext() ruft auch [**FinalNext**](iwebwizardhost-finalnext.md) auf, wenn ein Benutzer auf die Schaltfläche **Fertig stellen** klickt.</span><span class="sxs-lookup"><span data-stu-id="bfde5-121">OnNext() also calls [**FinalNext**](iwebwizardhost-finalnext.md) when a user clicks the **Finish** button.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfde5-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bfde5-122">Requirements</span></span>



| <span data-ttu-id="bfde5-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bfde5-123">Requirement</span></span> | <span data-ttu-id="bfde5-124">Wert</span><span class="sxs-lookup"><span data-stu-id="bfde5-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bfde5-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bfde5-125">Minimum supported client</span></span><br/> | <span data-ttu-id="bfde5-126">Nur Windows \[ XP-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bfde5-126">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="bfde5-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bfde5-127">Minimum supported server</span></span><br/> | <span data-ttu-id="bfde5-128">Nur Windows Server \[ 2003-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bfde5-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="bfde5-129">Header</span><span class="sxs-lookup"><span data-stu-id="bfde5-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfde5-130"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="bfde5-130"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="bfde5-131">Idl</span><span class="sxs-lookup"><span data-stu-id="bfde5-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bfde5-132"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="bfde5-132"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 




