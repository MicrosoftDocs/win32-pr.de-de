---
description: Die itcallqualitycontrol-Schnittstelle macht Methoden verfügbar, die einer Anwendung das Abrufen und Festlegen von Parametern für die Abruf Qualität ermöglichen.
ms.assetid: 8d33e3b2-6af9-4c2d-bc65-905467f4fc6a
title: Itcallqualitycontrol-Schnittstelle (ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 447e2f34db76ba15ecaec9e7bc03a0d2d398c493
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364973"
---
# <a name="itcallqualitycontrol-interface"></a><span data-ttu-id="51878-103">Itcallqualitycontrol-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="51878-103">ITCallQualityControl interface</span></span>

<span data-ttu-id="51878-104">\[ Diese Schnittstelle ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="51878-104">\[ This interface is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="51878-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="51878-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="51878-106">Die **itcallqualitycontrol** -Schnittstelle macht Methoden verfügbar, die einer Anwendung das Abrufen und Festlegen von Parametern für die Abruf Qualität ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="51878-106">The **ITCallQualityControl** interface exposes methods that allow an application to get and set parameters for call quality control.</span></span>

<span data-ttu-id="51878-107">Diese Schnittstelle wird von [ipconf MSP](ipconf-msp.md) und [h323 MSP](h323-msp.md)implementiert.</span><span class="sxs-lookup"><span data-stu-id="51878-107">This interface is implemented by the [IPConf MSP](ipconf-msp.md) and the [H323 MSP](h323-msp.md).</span></span> <span data-ttu-id="51878-108">Sie wird nur verfügbar gemacht, wenn ein-Rückruf diese Dienstanbieter verwendet.</span><span class="sxs-lookup"><span data-stu-id="51878-108">It is exposed only when a call uses these service providers.</span></span>

## <a name="members"></a><span data-ttu-id="51878-109">Member</span><span class="sxs-lookup"><span data-stu-id="51878-109">Members</span></span>

<span data-ttu-id="51878-110">Die **itcallqualitycontrol** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="51878-110">The **ITCallQualityControl** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="51878-111">**Itcallqualitycontrol** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="51878-111">**ITCallQualityControl** also has these types of members:</span></span>

-   [<span data-ttu-id="51878-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="51878-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="51878-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="51878-113">Methods</span></span>

<span data-ttu-id="51878-114">Die **itcallqualitycontrol** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="51878-114">The **ITCallQualityControl** interface has these methods.</span></span>



| <span data-ttu-id="51878-115">Methode</span><span class="sxs-lookup"><span data-stu-id="51878-115">Method</span></span>                                            | <span data-ttu-id="51878-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="51878-116">Description</span></span>                                                                                                     |
|:--------------------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="51878-117">**Erhalten**</span><span class="sxs-lookup"><span data-stu-id="51878-117">**Get**</span></span>](itcallqualitycontrol-get.md)           | <span data-ttu-id="51878-118">Ruft den Wert einer angegebenen Eigenschaft für die [Eigenschaft "Qualitätskontrolle](callqualityproperty.md)" ab.</span><span class="sxs-lookup"><span data-stu-id="51878-118">Gets the value of a given [call quality control property](callqualityproperty.md).</span></span><br/>                  |
| [<span data-ttu-id="51878-119">**GetRange**</span><span class="sxs-lookup"><span data-stu-id="51878-119">**GetRange**</span></span>](itcallqualitycontrol-getrange.md) | <span data-ttu-id="51878-120">Ruft den Bereich der gültigen Werte für eine angegebene [Eigenschaft des Steuer](callqualityproperty.md)Elements "Callcenter" ab.</span><span class="sxs-lookup"><span data-stu-id="51878-120">Gets the range of valid values for a given [call quality control property](callqualityproperty.md).</span></span><br/> |
| [<span data-ttu-id="51878-121">**Set**</span><span class="sxs-lookup"><span data-stu-id="51878-121">**Set**</span></span>](itcallqualitycontrol-set.md)           | <span data-ttu-id="51878-122">Legt den Wert einer angegebenen [Eigenschaft zum Abrufen der Qualitätskontrolle](callqualityproperty.md)fest.</span><span class="sxs-lookup"><span data-stu-id="51878-122">Sets the value of a given [call quality control property](callqualityproperty.md).</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="51878-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="51878-123">Requirements</span></span>



| <span data-ttu-id="51878-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="51878-124">Requirement</span></span> | <span data-ttu-id="51878-125">Wert</span><span class="sxs-lookup"><span data-stu-id="51878-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="51878-126">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="51878-126">TAPI version</span></span><br/> | <span data-ttu-id="51878-127">Erfordert TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="51878-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="51878-128">Header</span><span class="sxs-lookup"><span data-stu-id="51878-128">Header</span></span><br/>       | <dl> <span data-ttu-id="51878-129"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="51878-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="51878-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="51878-130">Library</span></span><br/>      | <dl> <span data-ttu-id="51878-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="51878-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="51878-132">DLL</span><span class="sxs-lookup"><span data-stu-id="51878-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="51878-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51878-133"><dt>Tapi3.dll</dt></span></span> </dl> |



 

