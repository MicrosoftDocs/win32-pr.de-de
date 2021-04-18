---
description: Die itqosapplicationid-Schnittstelle macht eine Methode verfügbar, die es einer Anwendung ermöglicht, den QoS-Bezeichner für den aktuellen Aufruf abzurufen.
ms.assetid: 1df50b3a-bd16-4e9b-afca-b025bfe537a4
title: Itqosapplicationid-Schnittstelle (ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23df8da80798cc52ecd73b4f29288812f3774d9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372001"
---
# <a name="itqosapplicationid-interface"></a><span data-ttu-id="b4cf3-103">Itqosapplicationid-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="b4cf3-103">ITQOSApplicationID interface</span></span>

<span data-ttu-id="b4cf3-104">\[ Diese Schnittstelle ist nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b4cf3-104">\[ This interface is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b4cf3-105">Die RTC-Client-API bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="b4cf3-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="b4cf3-106">Die **itqosapplicationid** -Schnittstelle macht eine Methode verfügbar, die es einer Anwendung ermöglicht, den QoS-Bezeichner für den aktuellen Aufruf abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b4cf3-106">The **ITQOSApplicationID** interface exposes a method that allows an application to get the QOS identifier for the current call.</span></span>

<span data-ttu-id="b4cf3-107">Diese Schnittstelle wird vom [ipconf-MSP](ipconf-msp.md) implementiert und wird nur verfügbar gemacht, wenn ein-Rückruf IP-Konferenzen verwendet.</span><span class="sxs-lookup"><span data-stu-id="b4cf3-107">This interface is implemented by the [IPConf MSP](ipconf-msp.md) and is exposed only when a call uses IP Conferencing.</span></span>

## <a name="members"></a><span data-ttu-id="b4cf3-108">Member</span><span class="sxs-lookup"><span data-stu-id="b4cf3-108">Members</span></span>

<span data-ttu-id="b4cf3-109">Die **itqosapplicationid** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="b4cf3-109">The **ITQOSApplicationID** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="b4cf3-110">**Itqosapplicationid** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="b4cf3-110">**ITQOSApplicationID** also has these types of members:</span></span>

-   [<span data-ttu-id="b4cf3-111">Methoden</span><span class="sxs-lookup"><span data-stu-id="b4cf3-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b4cf3-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="b4cf3-112">Methods</span></span>

<span data-ttu-id="b4cf3-113">Die **itqosapplicationid** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="b4cf3-113">The **ITQOSApplicationID** interface has these methods.</span></span>



| <span data-ttu-id="b4cf3-114">Methode</span><span class="sxs-lookup"><span data-stu-id="b4cf3-114">Method</span></span>                                                                | <span data-ttu-id="b4cf3-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b4cf3-115">Description</span></span>                         |
|:----------------------------------------------------------------------|:------------------------------------|
| [<span data-ttu-id="b4cf3-116">**Setqosapplicationid**</span><span class="sxs-lookup"><span data-stu-id="b4cf3-116">**SetQOSApplicationID**</span></span>](itqosapplicationid-setqosapplicationid.md) | <span data-ttu-id="b4cf3-117">Legt den QoS-Bezeichner fest.</span><span class="sxs-lookup"><span data-stu-id="b4cf3-117">Sets the QOS identifier.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b4cf3-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b4cf3-118">Requirements</span></span>



| <span data-ttu-id="b4cf3-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b4cf3-119">Requirement</span></span> | <span data-ttu-id="b4cf3-120">Wert</span><span class="sxs-lookup"><span data-stu-id="b4cf3-120">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b4cf3-121">TAPI-Version</span><span class="sxs-lookup"><span data-stu-id="b4cf3-121">TAPI version</span></span><br/> | <span data-ttu-id="b4cf3-122">Erfordert TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="b4cf3-122">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="b4cf3-123">Header</span><span class="sxs-lookup"><span data-stu-id="b4cf3-123">Header</span></span><br/>       | <dl> <span data-ttu-id="b4cf3-124"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4cf3-124"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b4cf3-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b4cf3-125">Library</span></span><br/>      | <dl> <span data-ttu-id="b4cf3-126"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b4cf3-126"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="b4cf3-127">DLL</span><span class="sxs-lookup"><span data-stu-id="b4cf3-127">DLL</span></span><br/>          | <dl> <span data-ttu-id="b4cf3-128"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4cf3-128"><dt>Tapi3.dll</dt></span></span> </dl> |



 

