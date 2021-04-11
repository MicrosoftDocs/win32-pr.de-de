---
description: Die IWiaUIExtension2-Schnittstelle stellt Methoden bereit, die die vom System bereitgestellte Standardbenutzer Oberfläche durch eine benutzerdefinierte Benutzeroberfläche ersetzen und ein benutzerdefiniertes Gerätesymbol bereitstellen.
ms.assetid: 1a747ea3-2476-438b-baf0-903b86cbbb16
title: IWiaUIExtension2-Schnittstelle (wiadevd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension2
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 4bfac82f90938a89b0d0ed76d9649e8e1a7cf19c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958969"
---
# <a name="iwiauiextension2-interface"></a><span data-ttu-id="bfc4b-103">IWiaUIExtension2-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="bfc4b-103">IWiaUIExtension2 interface</span></span>

<span data-ttu-id="bfc4b-104">Die IWiaUIExtension2-Schnittstelle stellt Methoden bereit, die die vom System bereitgestellte Standardbenutzer Oberfläche durch eine benutzerdefinierte Benutzeroberfläche ersetzen und ein benutzerdefiniertes Gerätesymbol bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="bfc4b-104">The IWiaUIExtension2 interface provides methods that replace the default, system-supplied user interface with a custom user interface, and that provide a custom device icon.</span></span> <span data-ttu-id="bfc4b-105">Gerätehersteller können diese Schnittstelle implementieren, um benutzerdefinierte Benutzeroberflächen für Ihre Geräte bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="bfc4b-105">Device vendors can implement this interface to provide custom user interfaces for their devices.</span></span>

## <a name="members"></a><span data-ttu-id="bfc4b-106">Member</span><span class="sxs-lookup"><span data-stu-id="bfc4b-106">Members</span></span>

<span data-ttu-id="bfc4b-107">Die **IWiaUIExtension2** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="bfc4b-107">The **IWiaUIExtension2** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="bfc4b-108">**IWiaUIExtension2** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="bfc4b-108">**IWiaUIExtension2** also has these types of members:</span></span>

-   [<span data-ttu-id="bfc4b-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="bfc4b-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="bfc4b-110">Methoden</span><span class="sxs-lookup"><span data-stu-id="bfc4b-110">Methods</span></span>

<span data-ttu-id="bfc4b-111">Die **IWiaUIExtension2** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="bfc4b-111">The **IWiaUIExtension2** interface has these methods.</span></span>



| <span data-ttu-id="bfc4b-112">Methode</span><span class="sxs-lookup"><span data-stu-id="bfc4b-112">Method</span></span>                                                       | <span data-ttu-id="bfc4b-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bfc4b-113">Description</span></span>                                                                                  |
|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bfc4b-114">**Devicedialog**</span><span class="sxs-lookup"><span data-stu-id="bfc4b-114">**DeviceDialog**</span></span>](-wia-iwiauiextension2-devicedialog.md)   | <span data-ttu-id="bfc4b-115">Stellt eine benutzerdefinierte Benutzeroberfläche bereit, die die standardmäßige Systembenutzer Oberfläche ersetzt.</span><span class="sxs-lookup"><span data-stu-id="bfc4b-115">Provides a custom user interface that replaces the default system user interface.</span></span><br/> |
| [<span data-ttu-id="bfc4b-116">**Getde viceicon**</span><span class="sxs-lookup"><span data-stu-id="bfc4b-116">**GetDeviceIcon**</span></span>](-wia-iwiauiextension2-getdeviceicon.md) | <span data-ttu-id="bfc4b-117">Ruft ein benutzerdefiniertes Gerätesymbol ab.</span><span class="sxs-lookup"><span data-stu-id="bfc4b-117">Gets a custom device icon.</span></span><br/>                                                        |



 

## <a name="remarks"></a><span data-ttu-id="bfc4b-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bfc4b-118">Remarks</span></span>



| <span data-ttu-id="bfc4b-119">IUnknown-Methoden</span><span class="sxs-lookup"><span data-stu-id="bfc4b-119">IUnknown Methods</span></span>                                        | <span data-ttu-id="bfc4b-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bfc4b-120">Description</span></span>                               |
|---------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="bfc4b-121">[IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="bfc4b-121">[IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span> | <span data-ttu-id="bfc4b-122">Gibt Zeiger auf unterstützte Schnittstellen zurück.</span><span class="sxs-lookup"><span data-stu-id="bfc4b-122">Returns pointers to supported interfaces.</span></span> |
| [<span data-ttu-id="bfc4b-123">IUnknown:: adressf</span><span class="sxs-lookup"><span data-stu-id="bfc4b-123">IUnknown::AddRef</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | <span data-ttu-id="bfc4b-124">Inkrementiert Verweiszähler.</span><span class="sxs-lookup"><span data-stu-id="bfc4b-124">Increments reference count.</span></span>               |
| [<span data-ttu-id="bfc4b-125">IUnknown:: Release</span><span class="sxs-lookup"><span data-stu-id="bfc4b-125">IUnknown::Release</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | <span data-ttu-id="bfc4b-126">Dekrementiert Verweiszähler.</span><span class="sxs-lookup"><span data-stu-id="bfc4b-126">Decrements reference count.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="bfc4b-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bfc4b-127">Requirements</span></span>



| <span data-ttu-id="bfc4b-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bfc4b-128">Requirement</span></span> | <span data-ttu-id="bfc4b-129">Wert</span><span class="sxs-lookup"><span data-stu-id="bfc4b-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bfc4b-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bfc4b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="bfc4b-131">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bfc4b-131">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="bfc4b-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bfc4b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="bfc4b-133">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bfc4b-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="bfc4b-134">Header</span><span class="sxs-lookup"><span data-stu-id="bfc4b-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfc4b-135"><dt>Wiadevd. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfc4b-135"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 
