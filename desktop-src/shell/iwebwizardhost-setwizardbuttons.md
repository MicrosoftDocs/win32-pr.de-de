---
description: Aktualisiert die Schaltflächen zurück, weiter und Fertigstellen im Assistenten Rahmen des Clients.
title: Webwizardhost. * twizardbuttons-Methode (Shldisp. h)
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
ms.openlocfilehash: 18af31eac1042e84a41e5651c517279869f03697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980249"
---
# <a name="webwizardhostsetwizardbuttons-method"></a><span data-ttu-id="d4d70-103">Webwizardhost. \* twizardbuttons-Methode</span><span class="sxs-lookup"><span data-stu-id="d4d70-103">WebWizardHost.SetWizardButtons method</span></span>

<span data-ttu-id="d4d70-104">Aktualisiert die Schaltflächen **zurück**, **weiter** und **Fertig** stellen im Assistenten Rahmen des Clients.</span><span class="sxs-lookup"><span data-stu-id="d4d70-104">Updates the **Back**, **Next**, and **Finish** buttons in the client's wizard frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4d70-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4d70-105">Syntax</span></span>


```JScript
iRetVal = WebWizardHost.SetWizardButtons(
  vbEnableBack,
  vbEnableNext,
  vbLastPage
)
```



## <a name="parameters"></a><span data-ttu-id="d4d70-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d4d70-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4d70-107">*vbenableback* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d4d70-107">*vbEnableBack* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4d70-108">Typ: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d4d70-108">Type: **Boolean**</span></span>

<span data-ttu-id="d4d70-109">Aktiviert die Schaltfläche " **zurück** ".</span><span class="sxs-lookup"><span data-stu-id="d4d70-109">Enables the **Back** button.</span></span>

</dd> <dt>

<span data-ttu-id="d4d70-110">*vbenablenext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d4d70-110">*vbEnableNext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4d70-111">Typ: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d4d70-111">Type: **Boolean**</span></span>

<span data-ttu-id="d4d70-112">Hiermit wird die Schaltfläche **Weiter** aktiviert.</span><span class="sxs-lookup"><span data-stu-id="d4d70-112">Enables the **Next** button.</span></span>

</dd> <dt>

<span data-ttu-id="d4d70-113">*vblastpage* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d4d70-113">*vbLastPage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4d70-114">Typ: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="d4d70-114">Type: **Boolean**</span></span>

<span data-ttu-id="d4d70-115">Aktiviert die Schaltfläche **Fertig** stellen.</span><span class="sxs-lookup"><span data-stu-id="d4d70-115">Enables the **Finish** button.</span></span> <span data-ttu-id="d4d70-116">Gibt an, dass dies die letzte serverseitige Seite ist.</span><span class="sxs-lookup"><span data-stu-id="d4d70-116">States that this is the last server-side page.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d4d70-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d4d70-117">Remarks</span></span>

<span data-ttu-id="d4d70-118">Stellen Sie sicher, dass Sie Handlerfunktionen auf jeder serverseitigen Seite für onback () und OnNext () implementieren, die den Assistenten-Schaltflächen **zurück** und **weiter** entspricht.</span><span class="sxs-lookup"><span data-stu-id="d4d70-118">Be sure to implement handler functions in each server-side page for OnBack() and OnNext(), corresponding to the wizard buttons **Back** and **Next**.</span></span> <span data-ttu-id="d4d70-119">Die onback ()-Funktion und die OnNext ()-Funktion Antworten auf " **".**</span><span class="sxs-lookup"><span data-stu-id="d4d70-119">The OnBack() and OnNext() functions respond to **SetWizardButtons**.</span></span> <span data-ttu-id="d4d70-120">Zum entsprechenden **Zeitpunkt Ruft die** OnNext ()-Funktion "" mit " *vblastpage* = **true**" auf, wodurch eine Schaltfläche **Fertig** stellen aktiviert werden kann.</span><span class="sxs-lookup"><span data-stu-id="d4d70-120">At the appropriate time, the OnNext() function calls **SetWizardButtons** with *vbLastPage*=**true**, which can enable a **Finish** button.</span></span> <span data-ttu-id="d4d70-121">OnNext () ruft auch [**finalnext**](iwebwizardhost-finalnext.md) auf, wenn ein Benutzer auf die Schaltfläche **Fertig** stellen klickt.</span><span class="sxs-lookup"><span data-stu-id="d4d70-121">OnNext() also calls [**FinalNext**](iwebwizardhost-finalnext.md) when a user clicks the **Finish** button.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4d70-122">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="d4d70-122">Requirements</span></span>



| <span data-ttu-id="d4d70-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d4d70-123">Requirement</span></span> | <span data-ttu-id="d4d70-124">Wert</span><span class="sxs-lookup"><span data-stu-id="d4d70-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4d70-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d4d70-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d4d70-126">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d4d70-126">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="d4d70-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d4d70-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d4d70-128">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d4d70-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d4d70-129">Header</span><span class="sxs-lookup"><span data-stu-id="d4d70-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4d70-130"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4d70-130"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d4d70-131">IDL</span><span class="sxs-lookup"><span data-stu-id="d4d70-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d4d70-132"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d4d70-132"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 




