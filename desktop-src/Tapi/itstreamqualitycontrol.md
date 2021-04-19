---
description: Das itstreamqualitycontrol-Steuerelement macht Methoden verfügbar, mit denen eine Anwendung Parameter für die streamqualitätskontrolle erhalten und festlegen kann.
ms.assetid: b9ecf24a-c87e-44a6-9e20-aa7bf7619314
title: Itstreamqualitycontrol-Schnittstelle (ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98a85eccc907ef2c8f4c0b67c2a32244004dbdca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370172"
---
# <a name="itstreamqualitycontrol-interface"></a><span data-ttu-id="5d269-103">Itstreamqualitycontrol-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="5d269-103">ITStreamQualityControl interface</span></span>

<span data-ttu-id="5d269-104">\[ Diese Schnittstelle ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5d269-104">\[ This interface is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="5d269-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="5d269-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="5d269-106">Das **itstreamqualitycontrol-Steuer** Element macht Methoden verfügbar, mit denen eine Anwendung Parameter für die streamqualitätskontrolle erhalten und festlegen kann.</span><span class="sxs-lookup"><span data-stu-id="5d269-106">The **ITStreamQualityControl** exposes methods that allow an application to get and set parameters for stream quality control.</span></span>

<span data-ttu-id="5d269-107">Diese Schnittstelle wird von [ipconf MSP](ipconf-msp.md) und [h323 MSP](h323-msp.md)implementiert.</span><span class="sxs-lookup"><span data-stu-id="5d269-107">This interface is implemented by the [IPConf MSP](ipconf-msp.md) and the [H323 MSP](h323-msp.md).</span></span> <span data-ttu-id="5d269-108">Sie wird nur verfügbar gemacht, wenn ein-Rückruf diese Dienstanbieter verwendet.</span><span class="sxs-lookup"><span data-stu-id="5d269-108">It is exposed only when a call uses these service providers.</span></span>

## <a name="members"></a><span data-ttu-id="5d269-109">Member</span><span class="sxs-lookup"><span data-stu-id="5d269-109">Members</span></span>

<span data-ttu-id="5d269-110">Die **itstreamqualitycontrol** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="5d269-110">The **ITStreamQualityControl** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="5d269-111">**Itstreamqualitycontrol** verfügt auch über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="5d269-111">**ITStreamQualityControl** also has these types of members:</span></span>

-   [<span data-ttu-id="5d269-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="5d269-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5d269-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="5d269-113">Methods</span></span>

<span data-ttu-id="5d269-114">Die **itstreamqualitycontrol** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="5d269-114">The **ITStreamQualityControl** interface has these methods.</span></span>



| <span data-ttu-id="5d269-115">Methode</span><span class="sxs-lookup"><span data-stu-id="5d269-115">Method</span></span>                                              | <span data-ttu-id="5d269-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5d269-116">Description</span></span>                                                                                                 |
|:----------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5d269-117">**Erhalten**</span><span class="sxs-lookup"><span data-stu-id="5d269-117">**Get**</span></span>](itstreamqualitycontrol-get.md)           | <span data-ttu-id="5d269-118">Ruft den Wert einer angegebenen [Stream Quality-Eigenschaft](streamqualityproperty.md)ab.</span><span class="sxs-lookup"><span data-stu-id="5d269-118">Gets the value of a given [stream quality property](streamqualityproperty.md).</span></span><br/>                  |
| [<span data-ttu-id="5d269-119">**GetRange**</span><span class="sxs-lookup"><span data-stu-id="5d269-119">**GetRange**</span></span>](itstreamqualitycontrol-getrange.md) | <span data-ttu-id="5d269-120">Ruft den Bereich der gültigen Werte für eine angegebene [Eigenschaft der Streamqualität](streamqualityproperty.md)ab.</span><span class="sxs-lookup"><span data-stu-id="5d269-120">Gets the range of valid values for a given [stream quality property](streamqualityproperty.md).</span></span><br/> |
| [<span data-ttu-id="5d269-121">**Set**</span><span class="sxs-lookup"><span data-stu-id="5d269-121">**Set**</span></span>](itstreamqualitycontrol-set.md)           | <span data-ttu-id="5d269-122">Legt den Wert einer angegebenen Eigenschaft für die [Streamqualität](streamqualityproperty.md)fest.</span><span class="sxs-lookup"><span data-stu-id="5d269-122">Sets the value of a given [stream quality property](streamqualityproperty.md).</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="5d269-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5d269-123">Requirements</span></span>



| <span data-ttu-id="5d269-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5d269-124">Requirement</span></span> | <span data-ttu-id="5d269-125">Wert</span><span class="sxs-lookup"><span data-stu-id="5d269-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5d269-126">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="5d269-126">TAPI version</span></span><br/> | <span data-ttu-id="5d269-127">Erfordert TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="5d269-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="5d269-128">Header</span><span class="sxs-lookup"><span data-stu-id="5d269-128">Header</span></span><br/>       | <dl> <span data-ttu-id="5d269-129"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d269-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5d269-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5d269-130">Library</span></span><br/>      | <dl> <span data-ttu-id="5d269-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5d269-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="5d269-132">DLL</span><span class="sxs-lookup"><span data-stu-id="5d269-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="5d269-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d269-133"><dt>Tapi3.dll</dt></span></span> </dl> |



 

