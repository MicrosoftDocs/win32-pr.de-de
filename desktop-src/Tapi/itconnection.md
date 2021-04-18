---
description: Die Funktionalität der itconnection-Schnittstelle ist unten dargestellt.
ms.assetid: 44dc39cf-3222-41ed-b29c-df2d32615500
title: Itconnection-Schnittstelle (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a00da80631c0ef4e8186aa36425f18e4d2a62bfc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371779"
---
# <a name="itconnection-interface"></a><span data-ttu-id="e4472-103">Itconnection-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="e4472-103">ITConnection interface</span></span>

<span data-ttu-id="e4472-104">\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e4472-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e4472-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="e4472-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="e4472-106">Die **itconnection** -Schnittstelle bietet die folgenden Funktionen:</span><span class="sxs-lookup"><span data-stu-id="e4472-106">The **ITConnection** interface provides the following functionality:</span></span>

-   <span data-ttu-id="e4472-107">Bietet Zugriff auf die Informationen zu Adresse und Gültigkeitsdauer (Time to Live, TTL) für die Sitzung.</span><span class="sxs-lookup"><span data-stu-id="e4472-107">Provides access to the address and time to live (TTL) information for the session.</span></span>
-   <span data-ttu-id="e4472-108">Ermöglicht den Zugriff auf die Bandbreiten Informationen.</span><span class="sxs-lookup"><span data-stu-id="e4472-108">Provides access to the bandwidth information.</span></span>
-   <span data-ttu-id="e4472-109">Ermöglicht die Bearbeitung des Verschlüsselungsschlüssels.</span><span class="sxs-lookup"><span data-stu-id="e4472-109">Enables manipulation of the encryption key.</span></span>

<span data-ttu-id="e4472-110">Die **itconnection** -Schnittstelle wird durch Aufrufen von **QueryInterface** für [**itconferenceblob**](itconferenceblob.md)erstellt.</span><span class="sxs-lookup"><span data-stu-id="e4472-110">The **ITConnection** interface is created by calling **QueryInterface** on [**ITConferenceBlob**](itconferenceblob.md).</span></span>

## <a name="members"></a><span data-ttu-id="e4472-111">Member</span><span class="sxs-lookup"><span data-stu-id="e4472-111">Members</span></span>

<span data-ttu-id="e4472-112">Die **itconnection** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="e4472-112">The **ITConnection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="e4472-113">**Itconnection** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e4472-113">**ITConnection** also has these types of members:</span></span>

-   [<span data-ttu-id="e4472-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="e4472-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e4472-115">Methoden</span><span class="sxs-lookup"><span data-stu-id="e4472-115">Methods</span></span>

<span data-ttu-id="e4472-116">Die **itconnection** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="e4472-116">The **ITConnection** interface has these methods.</span></span>



| <span data-ttu-id="e4472-117">Methode</span><span class="sxs-lookup"><span data-stu-id="e4472-117">Method</span></span>                                                               | <span data-ttu-id="e4472-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e4472-118">Description</span></span>                                                                                                                                    |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e4472-119">**\_adressstypen erhalten**</span><span class="sxs-lookup"><span data-stu-id="e4472-119">**get\_AddressType**</span></span>](itconnection-get-addresstype.md)             | <span data-ttu-id="e4472-120">Ruft den Adresstyp ab.</span><span class="sxs-lookup"><span data-stu-id="e4472-120">Gets the address type.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="e4472-121">**\_Bandbreite erhalten**</span><span class="sxs-lookup"><span data-stu-id="e4472-121">**get\_Bandwidth**</span></span>](itconnection-get-bandwidth.md)                 | <span data-ttu-id="e4472-122">Ruft den Bandbreitenwert ab.</span><span class="sxs-lookup"><span data-stu-id="e4472-122">Gets bandwidth value.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="e4472-123">**get \_ bandwidthmodifier**</span><span class="sxs-lookup"><span data-stu-id="e4472-123">**get\_BandwidthModifier**</span></span>](itconnection-get-bandwidthmodifier.md) | <span data-ttu-id="e4472-124">Ruft den bandbreitmodifizierer ab.</span><span class="sxs-lookup"><span data-stu-id="e4472-124">Gets the bandwidth modifier.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="e4472-125">**\_NetworkType erhalten**</span><span class="sxs-lookup"><span data-stu-id="e4472-125">**get\_NetworkType**</span></span>](itconnection-get-networktype.md)             | <span data-ttu-id="e4472-126">Ruft den Netzwerktyp ab.</span><span class="sxs-lookup"><span data-stu-id="e4472-126">Gets the network type.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="e4472-127">**\_numadkleider erhalten**</span><span class="sxs-lookup"><span data-stu-id="e4472-127">**get\_NumAddresses**</span></span>](itconnection-get-numaddresses.md)           | <span data-ttu-id="e4472-128">Ruft die Anzahl der Adressen ab, die für die Sitzung verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e4472-128">Gets the number of addresses to be used for the session.</span></span><br/>                                                                            |
| [<span data-ttu-id="e4472-129">**\_STARTADDRESS erhalten**</span><span class="sxs-lookup"><span data-stu-id="e4472-129">**get\_StartAddress**</span></span>](itconnection-get-startaddress.md)           | <span data-ttu-id="e4472-130">Ruft die erste Adresse ab, die für die Sitzung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e4472-130">Gets the first address to be used for the session.</span></span><br/>                                                                                  |
| [<span data-ttu-id="e4472-131">**Gültigkeitsdauer \_**</span><span class="sxs-lookup"><span data-stu-id="e4472-131">**get\_Ttl**</span></span>](itconnection-get-ttl.md)                             | <span data-ttu-id="e4472-132">Ruft den Gültigkeitsbereich der Gültigkeits [*Dauer*](t-tapgloss.md) (TTL) für Übertragungen für die Adressen ab.</span><span class="sxs-lookup"><span data-stu-id="e4472-132">Gets the [*time to live*](t-tapgloss.md) (TTL) scope for transmissions on the addresses.</span></span><br/> |
| [<span data-ttu-id="e4472-133">**GetEncryptionKey**</span><span class="sxs-lookup"><span data-stu-id="e4472-133">**GetEncryptionKey**</span></span>](itconnection-getencryptionkey.md)            | <span data-ttu-id="e4472-134">Ruft den Verschlüsselungsschlüssel ab.</span><span class="sxs-lookup"><span data-stu-id="e4472-134">Gets the encryption key.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="e4472-135">**Put- \_ Adresstype**</span><span class="sxs-lookup"><span data-stu-id="e4472-135">**put\_AddressType**</span></span>](itconnection-put-addresstype.md)             | <span data-ttu-id="e4472-136">Legt den adrestyp fest.</span><span class="sxs-lookup"><span data-stu-id="e4472-136">Sets the address type.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="e4472-137">**\_NetworkType platzieren**</span><span class="sxs-lookup"><span data-stu-id="e4472-137">**put\_NetworkType**</span></span>](itconnection-put-networktype.md)             | <span data-ttu-id="e4472-138">Legt den Netzwerktyp fest.</span><span class="sxs-lookup"><span data-stu-id="e4472-138">Sets the network type.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="e4472-139">**Setaddressinfo**</span><span class="sxs-lookup"><span data-stu-id="e4472-139">**SetAddressInfo**</span></span>](itconnection-setaddressinfo.md)                | <span data-ttu-id="e4472-140">Legt Adressinformationen fest.</span><span class="sxs-lookup"><span data-stu-id="e4472-140">Sets address information.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="e4472-141">**Setbandwidthinfo**</span><span class="sxs-lookup"><span data-stu-id="e4472-141">**SetBandwidthInfo**</span></span>](itconnection-setbandwidthinfo.md)            | <span data-ttu-id="e4472-142">Legt den Bandbreitenwert fest.</span><span class="sxs-lookup"><span data-stu-id="e4472-142">Sets the bandwidth value.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="e4472-143">**SetEncryptionKey**</span><span class="sxs-lookup"><span data-stu-id="e4472-143">**SetEncryptionKey**</span></span>](itconnection-setencryptionkey.md)            | <span data-ttu-id="e4472-144">Legt den Verschlüsselungsschlüssel fest, der zum Entschlüsseln der Sitzung erforderlich ist, oder einen Indikator für einen Mechanismus, um einen verwendbaren Schlüssel auf externe Weise zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e4472-144">Sets the encryption key needed to decrypt the session or an indication to a mechanism to obtain a usable key by external means.</span></span><br/>     |



 

## <a name="requirements"></a><span data-ttu-id="e4472-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e4472-145">Requirements</span></span>



| <span data-ttu-id="e4472-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e4472-146">Requirement</span></span> | <span data-ttu-id="e4472-147">Wert</span><span class="sxs-lookup"><span data-stu-id="e4472-147">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e4472-148">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="e4472-148">TAPI version</span></span><br/> | <span data-ttu-id="e4472-149">Erfordert TAPI 3,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="e4472-149">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="e4472-150">Header</span><span class="sxs-lookup"><span data-stu-id="e4472-150">Header</span></span><br/>       | <dl> <span data-ttu-id="e4472-151"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4472-151"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="e4472-152">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e4472-152">Library</span></span><br/>      | <dl> <span data-ttu-id="e4472-153"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e4472-153"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="e4472-154">DLL</span><span class="sxs-lookup"><span data-stu-id="e4472-154">DLL</span></span><br/>          | <dl> <span data-ttu-id="e4472-155"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4472-155"><dt>Sdpblb.dll</dt></span></span> </dl> |



 

