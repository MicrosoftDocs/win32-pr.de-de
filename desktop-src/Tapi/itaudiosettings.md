---
description: Die itaudiosettings-Schnittstelle macht Methoden verfügbar, mit denen eine Anwendung Parameter für die Steuerung eines Audiogeräts erhalten und festlegen kann.
ms.assetid: 56607024-255d-4d1b-9ca0-6086eff7b7b2
title: Itaudiosettings-Schnittstelle (ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eaf2566c7438dbcd14cdacee46cc4d5ec4166731
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359729"
---
# <a name="itaudiosettings-interface"></a><span data-ttu-id="2ce88-103">Itaudiosettings-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="2ce88-103">ITAudioSettings interface</span></span>

<span data-ttu-id="2ce88-104">\[ Diese Schnittstelle ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2ce88-104">\[ This interface is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2ce88-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="2ce88-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="2ce88-106">Die **itaudiosettings** -Schnittstelle macht Methoden verfügbar, mit denen eine Anwendung Parameter für die Steuerung eines Audiogeräts erhalten und festlegen kann.</span><span class="sxs-lookup"><span data-stu-id="2ce88-106">The **ITAudioSettings** interface exposes methods that allow an application to get and set parameters for control of an audio device.</span></span>

<span data-ttu-id="2ce88-107">Diese Schnittstelle wird von [ipconf MSP](ipconf-msp.md) und [h323 MSP](h323-msp.md)implementiert.</span><span class="sxs-lookup"><span data-stu-id="2ce88-107">This interface is implemented by the [IPConf MSP](ipconf-msp.md) and the [H323 MSP](h323-msp.md).</span></span> <span data-ttu-id="2ce88-108">Sie wird nur verfügbar gemacht, wenn ein-Rückruf diese Dienstanbieter verwendet.</span><span class="sxs-lookup"><span data-stu-id="2ce88-108">It is exposed only when a call uses these service providers.</span></span>

## <a name="members"></a><span data-ttu-id="2ce88-109">Member</span><span class="sxs-lookup"><span data-stu-id="2ce88-109">Members</span></span>

<span data-ttu-id="2ce88-110">Die **itaudiosettings** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="2ce88-110">The **ITAudioSettings** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2ce88-111">**Itaudiosettings** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="2ce88-111">**ITAudioSettings** also has these types of members:</span></span>

-   [<span data-ttu-id="2ce88-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="2ce88-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2ce88-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="2ce88-113">Methods</span></span>

<span data-ttu-id="2ce88-114">Die **itaudiosettings** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="2ce88-114">The **ITAudioSettings** interface has these methods.</span></span>



| <span data-ttu-id="2ce88-115">Methode</span><span class="sxs-lookup"><span data-stu-id="2ce88-115">Method</span></span>                                              | <span data-ttu-id="2ce88-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2ce88-116">Description</span></span>                                                                                                |
|:----------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2ce88-117">**Erhalten**</span><span class="sxs-lookup"><span data-stu-id="2ce88-117">**Get**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_call)          | <span data-ttu-id="2ce88-118">Ruft den Wert einer angegebenen [audioeinstellungs Eigenschaft](audiosettingsproperty.md)ab.</span><span class="sxs-lookup"><span data-stu-id="2ce88-118">Gets the value of a given [audio setting property](audiosettingsproperty.md).</span></span><br/>                  |
| [<span data-ttu-id="2ce88-119">**GetRange**</span><span class="sxs-lookup"><span data-stu-id="2ce88-119">**GetRange**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_terminal) | <span data-ttu-id="2ce88-120">Ruft den Bereich der gültigen Werte für eine angegebene [audioeinstellungs Eigenschaft](audiosettingsproperty.md)ab.</span><span class="sxs-lookup"><span data-stu-id="2ce88-120">Gets the range of valid values for a given [audio setting property](audiosettingsproperty.md).</span></span><br/> |
| [<span data-ttu-id="2ce88-121">**Set**</span><span class="sxs-lookup"><span data-stu-id="2ce88-121">**Set**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_error)         | <span data-ttu-id="2ce88-122">Legt den Wert einer angegebenen [audioeinstellungs Eigenschaft fest](audiosettingsproperty.md).</span><span class="sxs-lookup"><span data-stu-id="2ce88-122">Sets the value of a given [audio setting property](audiosettingsproperty.md).</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="2ce88-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2ce88-123">Requirements</span></span>



| <span data-ttu-id="2ce88-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2ce88-124">Requirement</span></span> | <span data-ttu-id="2ce88-125">Wert</span><span class="sxs-lookup"><span data-stu-id="2ce88-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2ce88-126">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="2ce88-126">TAPI version</span></span><br/> | <span data-ttu-id="2ce88-127">Erfordert TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="2ce88-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="2ce88-128">Header</span><span class="sxs-lookup"><span data-stu-id="2ce88-128">Header</span></span><br/>       | <dl> <span data-ttu-id="2ce88-129"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ce88-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2ce88-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2ce88-130">Library</span></span><br/>      | <dl> <span data-ttu-id="2ce88-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2ce88-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="2ce88-132">DLL</span><span class="sxs-lookup"><span data-stu-id="2ce88-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="2ce88-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ce88-133"><dt>Tapi3.dll</dt></span></span> </dl> |



 

