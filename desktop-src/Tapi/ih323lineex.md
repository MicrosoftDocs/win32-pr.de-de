---
description: Die IH323LineEx-Schnittstelle wird vom h323 MSP implementiert und ist nur für H. 323 Address-Objekte verfügbar. Diese Schnittstelle macht Methoden verfügbar, die das Erstellen und manipulieren von Terminals ermöglichen, die zwischen h323-und SDP-Clients kommunizieren können.
ms.assetid: 2ab57343-8cf5-4af2-91f7-46926cfce6dd
title: IH323LineEx-Schnittstelle (H323priv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41888b16f645a3af1eefd9df61623cb28684bfdd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360905"
---
# <a name="ih323lineex-interface"></a><span data-ttu-id="adcee-104">IH323LineEx-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="adcee-104">IH323LineEx interface</span></span>

<span data-ttu-id="adcee-105">\[**IH323LineEx** ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="adcee-105">\[**IH323LineEx** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="adcee-106">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="adcee-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="adcee-107">Die **IH323LineEx** -Schnittstelle wird vom [h323 MSP](h323-msp.md) implementiert und ist nur für H. 323 Address-Objekte verfügbar.</span><span class="sxs-lookup"><span data-stu-id="adcee-107">The **IH323LineEx** interface is implemented by the [H323 MSP](h323-msp.md) and is available only on H.323 address objects.</span></span> <span data-ttu-id="adcee-108">Diese Schnittstelle macht Methoden verfügbar, die das Erstellen und manipulieren von Terminals ermöglichen, die zwischen h323-und SDP-Clients kommunizieren können.</span><span class="sxs-lookup"><span data-stu-id="adcee-108">This interface exposes methods that enable creation and manipulation of terminals that can communicate between H323 and SDP clients.</span></span>

> [!Note]  
> <span data-ttu-id="adcee-109">Alle Methoden in dieser Schnittstelle sollten erst nach der Registrierung für eingehende Aufrufe für diese Adresse aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="adcee-109">All methods in this interface should be called only after registering for incoming calls on this address.</span></span>

 

## <a name="members"></a><span data-ttu-id="adcee-110">Member</span><span class="sxs-lookup"><span data-stu-id="adcee-110">Members</span></span>

<span data-ttu-id="adcee-111">Die **IH323LineEx** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="adcee-111">The **IH323LineEx** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="adcee-112">**IH323LineEx** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="adcee-112">**IH323LineEx** also has these types of members:</span></span>

-   [<span data-ttu-id="adcee-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="adcee-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="adcee-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="adcee-114">Methods</span></span>

<span data-ttu-id="adcee-115">Die **IH323LineEx** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="adcee-115">The **IH323LineEx** interface has these methods.</span></span>



| <span data-ttu-id="adcee-116">Methode</span><span class="sxs-lookup"><span data-stu-id="adcee-116">Method</span></span>                                                                                 | <span data-ttu-id="adcee-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="adcee-117">Description</span></span>                                                              |
|:---------------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [<span data-ttu-id="adcee-118">**Nach dem Festlegen**</span><span class="sxs-lookup"><span data-stu-id="adcee-118">**SetAlias**</span></span>](ih323lineex-setalias.md)                                               | <span data-ttu-id="adcee-119">Konfiguriert einen standardmäßigen H. 323-Alias für die Adresse.</span><span class="sxs-lookup"><span data-stu-id="adcee-119">Configures a default H.323 alias for the address.</span></span><br/>             |
| [<span data-ttu-id="adcee-120">**Setdefaultcapabilityprefergenz**</span><span class="sxs-lookup"><span data-stu-id="adcee-120">**SetDefaultCapabilityPreferrence**</span></span>](ih323lineex-setdefaultcapabilitypreferrence.md) | <span data-ttu-id="adcee-121">Konfiguriert die bevorzugte Gewichtung für Standardfunktionen.</span><span class="sxs-lookup"><span data-stu-id="adcee-121">Configures the preference weighting for default capabilities.</span></span><br/> |
| [<span data-ttu-id="adcee-122">**SetExternalT120Address**</span><span class="sxs-lookup"><span data-stu-id="adcee-122">**SetExternalT120Address**</span></span>](ih323lineex-setexternalt120address.md)                   | <span data-ttu-id="adcee-123">Konfiguriert eine externe T. 120-Adresse für den Datenaustausch.</span><span class="sxs-lookup"><span data-stu-id="adcee-123">Configures an external T.120 address for data exchange.</span></span><br/>       |



 

## <a name="requirements"></a><span data-ttu-id="adcee-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="adcee-124">Requirements</span></span>



| <span data-ttu-id="adcee-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="adcee-125">Requirement</span></span> | <span data-ttu-id="adcee-126">Wert</span><span class="sxs-lookup"><span data-stu-id="adcee-126">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="adcee-127">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="adcee-127">TAPI version</span></span><br/> | <span data-ttu-id="adcee-128">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="adcee-128">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="adcee-129">Header</span><span class="sxs-lookup"><span data-stu-id="adcee-129">Header</span></span><br/>       | <dl> <span data-ttu-id="adcee-130"><dt>H323priv. h</dt></span><span class="sxs-lookup"><span data-stu-id="adcee-130"><dt>H323priv.h</dt></span></span> </dl> |
| <span data-ttu-id="adcee-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="adcee-131">Library</span></span><br/>      | <dl> <span data-ttu-id="adcee-132"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="adcee-132"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="adcee-133">DLL</span><span class="sxs-lookup"><span data-stu-id="adcee-133">DLL</span></span><br/>          | <dl> <span data-ttu-id="adcee-134"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="adcee-134"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="adcee-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="adcee-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adcee-136">H323-msp</span><span class="sxs-lookup"><span data-stu-id="adcee-136">H323 MSP</span></span>](h323-msp.md)
</dt> </dl>

 

