---
description: Die ittime-Schnittstelle ist eine anbieterspezifische Schnittstelle für ein Sitzungs Deskriptor Protocol (SDP)-Konferenz-BLOB-Objekt.
ms.assetid: 24d33259-dcbe-47e4-9c71-fcc25f6e9a76
title: Ittime-Schnittstelle (sdpblb. h)
ms.topic: interface
ms.date: 05/31/2018
ms.openlocfilehash: 964fa197318d8cbe9614beb97c5bea0db94f242b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354104"
---
# <a name="ittime-interface"></a><span data-ttu-id="0c9f6-103">Ittime-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="0c9f6-103">ITTime interface</span></span>

<span data-ttu-id="0c9f6-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0c9f6-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0c9f6-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="0c9f6-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="0c9f6-106">Die **ittime** -Schnittstelle ist eine anbieterspezifische Schnittstelle für ein Sitzungs Deskriptor Protocol (SDP)-Konferenz-BLOB-Objekt.</span><span class="sxs-lookup"><span data-stu-id="0c9f6-106">The **ITTime** interface is a provider-specific interface for a Session Descriptor Protocol (SDP) conference blob object.</span></span> <span data-ttu-id="0c9f6-107">Sie ermöglicht den Zugriff auf einen Satz von Aktivierungs Zeiten für die Sitzung.</span><span class="sxs-lookup"><span data-stu-id="0c9f6-107">It provides access to a set of activation times for the session.</span></span> <span data-ttu-id="0c9f6-108">Die [**ienumtime:: Next**](ienumtime-next.md) -Methode und die [**ittimecollection:: Create**](ittimecollection-create.md) -Methode erstellen die **ittime** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="0c9f6-108">The [**IEnumTime::Next**](ienumtime-next.md) and [**ITTimeCollection::Create**](ittimecollection-create.md) methods create the **ITTime** interface.</span></span>

## <a name="members"></a><span data-ttu-id="0c9f6-109">Member</span><span class="sxs-lookup"><span data-stu-id="0c9f6-109">Members</span></span>

<span data-ttu-id="0c9f6-110">Die **ittime** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="0c9f6-110">The **ITTime** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="0c9f6-111">**Ittime** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="0c9f6-111">**ITTime** also has these types of members:</span></span>

-   [<span data-ttu-id="0c9f6-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="0c9f6-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0c9f6-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="0c9f6-113">Methods</span></span>

<span data-ttu-id="0c9f6-114">Die **ittime** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="0c9f6-114">The **ITTime** interface has these methods.</span></span>



| <span data-ttu-id="0c9f6-115">Methode</span><span class="sxs-lookup"><span data-stu-id="0c9f6-115">Method</span></span>                                         | <span data-ttu-id="0c9f6-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0c9f6-116">Description</span></span>                                                                 |
|:-----------------------------------------------|:----------------------------------------------------------------------------|
| [<span data-ttu-id="0c9f6-117">**\_StartTime aufrufen**</span><span class="sxs-lookup"><span data-stu-id="0c9f6-117">**get\_StartTime**</span></span>](ittime-get-starttime.md) | <span data-ttu-id="0c9f6-118">Ruft den Start Zeitwert der 32-Bit-NTP (Netzwerk Zeitprotokoll) ab.</span><span class="sxs-lookup"><span data-stu-id="0c9f6-118">Gets the 32-bit NTP (Network Time Protocol) starting time value.</span></span><br/> |
| [<span data-ttu-id="0c9f6-119">**\_Stopp Zeit erhalten**</span><span class="sxs-lookup"><span data-stu-id="0c9f6-119">**get\_StopTime**</span></span>](ittime-get-stoptime.md)   | <span data-ttu-id="0c9f6-120">Ruft den NTP-Endzeit Wert ab.</span><span class="sxs-lookup"><span data-stu-id="0c9f6-120">Gets the NTP ending time value.</span></span><br/>                                  |
| [<span data-ttu-id="0c9f6-121">**\_StartTime ablegen**</span><span class="sxs-lookup"><span data-stu-id="0c9f6-121">**put\_StartTime**</span></span>](ittime-put-starttime.md) | <span data-ttu-id="0c9f6-122">Legt den Wert von 32-Bit-NTP-Start Zeitwert fest.</span><span class="sxs-lookup"><span data-stu-id="0c9f6-122">Sets the 32-bit NTP starting time value.</span></span><br/>                         |
| [<span data-ttu-id="0c9f6-123">**\_Stopp Zeit einfügen**</span><span class="sxs-lookup"><span data-stu-id="0c9f6-123">**put\_StopTime**</span></span>](ittime-put-stoptime.md)   | <span data-ttu-id="0c9f6-124">Legt den NTP-Endzeit Wert fest.</span><span class="sxs-lookup"><span data-stu-id="0c9f6-124">Sets the NTP ending time value.</span></span><br/>                                  |



 

## <a name="requirements"></a><span data-ttu-id="0c9f6-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0c9f6-125">Requirements</span></span>



| <span data-ttu-id="0c9f6-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0c9f6-126">Requirement</span></span> | <span data-ttu-id="0c9f6-127">Wert</span><span class="sxs-lookup"><span data-stu-id="0c9f6-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0c9f6-128">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="0c9f6-128">TAPI version</span></span><br/> | <span data-ttu-id="0c9f6-129">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="0c9f6-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="0c9f6-130">Header</span><span class="sxs-lookup"><span data-stu-id="0c9f6-130">Header</span></span><br/>       | <dl> <span data-ttu-id="0c9f6-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c9f6-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="0c9f6-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0c9f6-132">Library</span></span><br/>      | <dl> <span data-ttu-id="0c9f6-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0c9f6-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="0c9f6-134">DLL</span><span class="sxs-lookup"><span data-stu-id="0c9f6-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="0c9f6-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0c9f6-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



 

