---
description: Die ITmedia-Schnittstelle ist eine Darstellung von Medien in einem Sitzungs Deskriptor-Protokoll (SDP, siehe RFC 2327).
ms.assetid: f5cd7971-3456-4e2f-8808-deb16678099a
title: ITmedia-Schnittstelle (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dd00d7eab685fe99b089556bcdb0ed2bf6329df
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354233"
---
# <a name="itmedia-interface"></a><span data-ttu-id="5a004-103">ITmedia-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="5a004-103">ITMedia interface</span></span>

<span data-ttu-id="5a004-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5a004-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="5a004-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="5a004-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="5a004-106">Die **ITmedia** -Schnittstelle ist eine Darstellung von Medien in einem Sitzungs Deskriptor-Protokoll (SDP, siehe RFC 2327).</span><span class="sxs-lookup"><span data-stu-id="5a004-106">The **ITMedia** interface is a representation of media in a Session Descriptor Protocol (SDP, see RFC 2327).</span></span> <span data-ttu-id="5a004-107">Diese Schnittstelle exportiert Methoden zum erhalten und Festlegen grundlegender Medien Eigenschaften, z. b. Typ.</span><span class="sxs-lookup"><span data-stu-id="5a004-107">This interface exports methods to get and set basic media properties, such as type.</span></span> <span data-ttu-id="5a004-108">Das [**itmediacollection:: get- \_ Element**](itmediacollection-get-item.md) und die [**itmediacollection:: Create**](itmediacollection-create.md) -Methode erstellen die **ITmedia** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="5a004-108">The [**ITMediaCollection::get\_Item**](itmediacollection-get-item.md) and [**ITMediaCollection::Create**](itmediacollection-create.md) methods create the **ITMedia** interface.</span></span>

## <a name="members"></a><span data-ttu-id="5a004-109">Member</span><span class="sxs-lookup"><span data-stu-id="5a004-109">Members</span></span>

<span data-ttu-id="5a004-110">Die **ITmedia** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="5a004-110">The **ITMedia** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="5a004-111">**ITmedia** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="5a004-111">**ITMedia** also has these types of members:</span></span>

-   [<span data-ttu-id="5a004-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="5a004-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5a004-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="5a004-113">Methods</span></span>

<span data-ttu-id="5a004-114">Die **ITmedia** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="5a004-114">The **ITMedia** interface has these methods.</span></span>



| <span data-ttu-id="5a004-115">Methode</span><span class="sxs-lookup"><span data-stu-id="5a004-115">Method</span></span>                                                          | <span data-ttu-id="5a004-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5a004-116">Description</span></span>                                                                                      |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5a004-117">**\_Formatcodes erhalten**</span><span class="sxs-lookup"><span data-stu-id="5a004-117">**get\_FormatCodes**</span></span>](itmedia-get-formatcodes.md)             | <span data-ttu-id="5a004-118">Ruft die Liste der Formatcodes der Medien Nutzlast ab.</span><span class="sxs-lookup"><span data-stu-id="5a004-118">Gets the list of media payload format codes.</span></span><br/>                                          |
| [<span data-ttu-id="5a004-119">**" \_ MEDIANAME" erhalten**</span><span class="sxs-lookup"><span data-stu-id="5a004-119">**get\_MediaName**</span></span>](itmedia-get-medianame.md)                 | <span data-ttu-id="5a004-120">Ruft den Mediennamen ab.</span><span class="sxs-lookup"><span data-stu-id="5a004-120">Gets the media name.</span></span><br/>                                                                  |
| [<span data-ttu-id="5a004-121">**\_mediatitle erhalten**</span><span class="sxs-lookup"><span data-stu-id="5a004-121">**get\_MediaTitle**</span></span>](itmedia-get-mediatitle.md)               | <span data-ttu-id="5a004-122">Ruft den Medien Titel ab.</span><span class="sxs-lookup"><span data-stu-id="5a004-122">Gets the media title.</span></span><br/>                                                                 |
| [<span data-ttu-id="5a004-123">**\_numports erhalten**</span><span class="sxs-lookup"><span data-stu-id="5a004-123">**get\_NumPorts**</span></span>](itmedia-get-numports.md)                   | <span data-ttu-id="5a004-124">Ruft die Anzahl der für die Sitzung benötigten Ports ab.</span><span class="sxs-lookup"><span data-stu-id="5a004-124">Gets the number of ports needed for the session.</span></span><br/>                                      |
| [<span data-ttu-id="5a004-125">**\_startport starten**</span><span class="sxs-lookup"><span data-stu-id="5a004-125">**get\_StartPort**</span></span>](itmedia-get-startport.md)                 | <span data-ttu-id="5a004-126">Ruft den 16-Bit-Portwert für den ersten Port ab.</span><span class="sxs-lookup"><span data-stu-id="5a004-126">Gets the 16-bit port value for the first port.</span></span><br/>                                        |
| [<span data-ttu-id="5a004-127">**\_transportprotocol-Protokoll**</span><span class="sxs-lookup"><span data-stu-id="5a004-127">**get\_TransportProtocol**</span></span>](itmedia-get-transportprotocol.md) | <span data-ttu-id="5a004-128">Ruft das Transportprotokoll ab.</span><span class="sxs-lookup"><span data-stu-id="5a004-128">Gets the transport protocol.</span></span><br/>                                                          |
| [<span data-ttu-id="5a004-129">**Put- \_ Formatcodes**</span><span class="sxs-lookup"><span data-stu-id="5a004-129">**put\_FormatCodes**</span></span>](itmedia-put-formatcodes.md)             | <span data-ttu-id="5a004-130">Legt die Liste der Medien Nutzlast-Formatcodes fest.</span><span class="sxs-lookup"><span data-stu-id="5a004-130">Sets the list of media payload format codes.</span></span><br/>                                          |
| [<span data-ttu-id="5a004-131">**\_MEDIANAME platzieren**</span><span class="sxs-lookup"><span data-stu-id="5a004-131">**put\_MediaName**</span></span>](itmedia-put-medianame.md)                 | <span data-ttu-id="5a004-132">Legt den Mediennamen fest.</span><span class="sxs-lookup"><span data-stu-id="5a004-132">Sets the media name.</span></span><br/>                                                                  |
| [<span data-ttu-id="5a004-133">**\_mediatitle platzieren**</span><span class="sxs-lookup"><span data-stu-id="5a004-133">**put\_MediaTitle**</span></span>](itmedia-put-mediatitle.md)               | <span data-ttu-id="5a004-134">Legt den Medien Titel fest.</span><span class="sxs-lookup"><span data-stu-id="5a004-134">Sets the media title.</span></span><br/>                                                                 |
| [<span data-ttu-id="5a004-135">**\_transportprotocol ablegen**</span><span class="sxs-lookup"><span data-stu-id="5a004-135">**put\_TransportProtocol**</span></span>](itmedia-put-transportprotocol.md) | <span data-ttu-id="5a004-136">Legt das Transportprotokoll fest.</span><span class="sxs-lookup"><span data-stu-id="5a004-136">Sets the transport protocol.</span></span><br/>                                                          |
| [<span data-ttu-id="5a004-137">**Setportinfo**</span><span class="sxs-lookup"><span data-stu-id="5a004-137">**SetPortInfo**</span></span>](itmedia-setportinfo.md)                      | <span data-ttu-id="5a004-138">Legt den Wert für den 16-Bit-Port für den ersten Port und die Anzahl der für die Sitzung benötigten Ports fest.</span><span class="sxs-lookup"><span data-stu-id="5a004-138">Sets the 16-bit port value for the first port and number of ports needed for session.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5a004-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5a004-139">Requirements</span></span>



| <span data-ttu-id="5a004-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5a004-140">Requirement</span></span> | <span data-ttu-id="5a004-141">Wert</span><span class="sxs-lookup"><span data-stu-id="5a004-141">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5a004-142">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="5a004-142">TAPI version</span></span><br/> | <span data-ttu-id="5a004-143">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="5a004-143">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="5a004-144">Header</span><span class="sxs-lookup"><span data-stu-id="5a004-144">Header</span></span><br/>       | <dl> <span data-ttu-id="5a004-145"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a004-145"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="5a004-146">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5a004-146">Library</span></span><br/>      | <dl> <span data-ttu-id="5a004-147"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5a004-147"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="5a004-148">DLL</span><span class="sxs-lookup"><span data-stu-id="5a004-148">DLL</span></span><br/>          | <dl> <span data-ttu-id="5a004-149"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a004-149"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a004-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5a004-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a004-151">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="5a004-151">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="5a004-152">**Itmediacollection**</span><span class="sxs-lookup"><span data-stu-id="5a004-152">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> <dt>

[<span data-ttu-id="5a004-153">**Itsdp**</span><span class="sxs-lookup"><span data-stu-id="5a004-153">**ITSDP**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="5a004-154">**Ittime**</span><span class="sxs-lookup"><span data-stu-id="5a004-154">**ITTime**</span></span>](ittime.md)
</dt> </dl>

 

