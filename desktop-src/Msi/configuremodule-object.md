---
description: Das "Konfigurationsmodul"-Objekt ist eine vom Client implementierte Schnittstelle.
ms.assetid: f6240837-7685-4bfe-8a2f-b4428014702a
title: Konfigurationsmodul-Objekt (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigureModule
- IMsmConfigureModule
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 0c99f8932d1d3c0e7ba7d7df5e14fc0738e8b81c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352117"
---
# <a name="configuremodule-object"></a><span data-ttu-id="c0d0c-103">"Konfiguriermodule"-Objekt</span><span class="sxs-lookup"><span data-stu-id="c0d0c-103">ConfigureModule object</span></span>

<span data-ttu-id="c0d0c-104">Das " **Konfigurationsmodul** "-Objekt ist eine vom Client implementierte Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="c0d0c-104">The **ConfigureModule object** is an interface implemented by the client.</span></span> <span data-ttu-id="c0d0c-105">Mergemod.dllruft Methoden auf der **imsmkonfigurremodule** -Schnittstelle auf, um anzufordern, dass das Client Tool Konfigurationsinformationen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="c0d0c-105">Mergemod.dllcalls methods on the **IMsmConfigureModule** interface to request that the client tool provide configuration information.</span></span> <span data-ttu-id="c0d0c-106">Das Modul wird auf der Grundlage der Client Antworten auf Aufrufe dieser Schnittstelle konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="c0d0c-106">The module is configured based on the client's responses to calls on this interface.</span></span>

## <a name="members"></a><span data-ttu-id="c0d0c-107">Member</span><span class="sxs-lookup"><span data-stu-id="c0d0c-107">Members</span></span>

<span data-ttu-id="c0d0c-108">Das Objekt " **Konfigurationsmodul** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c0d0c-108">The **ConfigureModule** object has these types of members:</span></span>

-   [<span data-ttu-id="c0d0c-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="c0d0c-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c0d0c-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="c0d0c-110">Methods</span></span>

<span data-ttu-id="c0d0c-111">Das Objekt " **konfigurierungsmodul** " verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="c0d0c-111">The **ConfigureModule** object has these methods.</span></span>



| <span data-ttu-id="c0d0c-112">Methode</span><span class="sxs-lookup"><span data-stu-id="c0d0c-112">Method</span></span>                                                           | <span data-ttu-id="c0d0c-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c0d0c-113">Description</span></span>                                                                        |
|:-----------------------------------------------------------------|:-----------------------------------------------------------------------------------|
| [<span data-ttu-id="c0d0c-114">**Provideintegerdata**</span><span class="sxs-lookup"><span data-stu-id="c0d0c-114">**ProvideIntegerData**</span></span>](configuremodule-provideintegerdata.md) | <span data-ttu-id="c0d0c-115">Wird von Mergemod.dll aufgerufen, um ganze Zahlen zu erhalten, die zum Konfigurieren des Moduls verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c0d0c-115">Called by Mergemod.dll to obtain integers used to configure the module.</span></span><br/> |
| [<span data-ttu-id="c0d0c-116">**Provide TextData**</span><span class="sxs-lookup"><span data-stu-id="c0d0c-116">**ProvideTextData**</span></span>](configuremodule-providetextdata.md)       | <span data-ttu-id="c0d0c-117">Wird von Mergemod.dll aufgerufen, um Text zu erhalten, der zum Konfigurieren des Moduls verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c0d0c-117">Called by Mergemod.dll to obtain text used to configure the module.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="c0d0c-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c0d0c-118">Remarks</span></span>

### <a name="c"></a><span data-ttu-id="c0d0c-119">C++</span><span class="sxs-lookup"><span data-stu-id="c0d0c-119">C++</span></span>

<span data-ttu-id="c0d0c-120">Schnittstelle **imsmkonfiguriermodule: IDispatch**</span><span class="sxs-lookup"><span data-stu-id="c0d0c-120">interface **IMsmConfigureModule : IDispatch**</span></span>

### <a name="interface-id"></a><span data-ttu-id="c0d0c-121">Schnittstellen-ID</span><span class="sxs-lookup"><span data-stu-id="c0d0c-121">Interface ID</span></span>



| <span data-ttu-id="c0d0c-122">Konstante</span><span class="sxs-lookup"><span data-stu-id="c0d0c-122">Constant</span></span>                     | <span data-ttu-id="c0d0c-123">Wert</span><span class="sxs-lookup"><span data-stu-id="c0d0c-123">Value</span></span>                                  |
|------------------------------|----------------------------------------|
| <span data-ttu-id="c0d0c-124">**IID \_ imsmkonfiguriterremodule**</span><span class="sxs-lookup"><span data-stu-id="c0d0c-124">**IID\_IMsmConfigureModule**</span></span> | <span data-ttu-id="c0d0c-125">{AC013209-18A7-4851-8A21-2353443D70A0}</span><span class="sxs-lookup"><span data-stu-id="c0d0c-125">{AC013209-18A7-4851-8A21-2353443D70A0}</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="c0d0c-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c0d0c-126">Requirements</span></span>



| <span data-ttu-id="c0d0c-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c0d0c-127">Requirement</span></span> | <span data-ttu-id="c0d0c-128">Wert</span><span class="sxs-lookup"><span data-stu-id="c0d0c-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0d0c-129">Version</span><span class="sxs-lookup"><span data-stu-id="c0d0c-129">Version</span></span><br/> | <span data-ttu-id="c0d0c-130">Mergemod.dll 2,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="c0d0c-130">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="c0d0c-131">Header</span><span class="sxs-lookup"><span data-stu-id="c0d0c-131">Header</span></span><br/>  | <dl> <span data-ttu-id="c0d0c-132"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0d0c-132"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="c0d0c-133">DLL</span><span class="sxs-lookup"><span data-stu-id="c0d0c-133">DLL</span></span><br/>     | <dl> <span data-ttu-id="c0d0c-134"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0d0c-134"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




