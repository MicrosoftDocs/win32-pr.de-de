---
description: Die iwiauiextension-Schnittstelle stellt Methoden bereit, die die standardmäßige Systembenutzer Oberfläche ersetzen, ein benutzerdefiniertes Geräte Bitmap-Logo bereitstellen und ein benutzerdefiniertes Gerätesymbol bereitstellen.
ms.assetid: e3c69019-0e07-44ad-b48b-ea7e3daed2b7
title: Iwiauiextension-Schnittstelle (wiadevd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 98318ba3b2b94d334834150b219c5d453c4e0d89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348415"
---
# <a name="iwiauiextension-interface"></a><span data-ttu-id="47709-103">Iwiauiextension-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="47709-103">IWiaUIExtension interface</span></span>

<span data-ttu-id="47709-104">Die **iwiauiextension** -Schnittstelle stellt Methoden bereit, die die standardmäßige Systembenutzer Oberfläche ersetzen, ein benutzerdefiniertes Geräte Bitmap-Logo bereitstellen und ein benutzerdefiniertes Gerätesymbol bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="47709-104">The **IWiaUIExtension** interface provides methods that replace the default system user interface, provide a custom device bitmap logo, and provide a custom device icon.</span></span>

## <a name="members"></a><span data-ttu-id="47709-105">Member</span><span class="sxs-lookup"><span data-stu-id="47709-105">Members</span></span>

<span data-ttu-id="47709-106">Die **iwiauiextension** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="47709-106">The **IWiaUIExtension** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="47709-107">**Iwiauiextension** verfügt auch über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="47709-107">**IWiaUIExtension** also has these types of members:</span></span>

-   [<span data-ttu-id="47709-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="47709-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="47709-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="47709-109">Methods</span></span>

<span data-ttu-id="47709-110">Die **iwiauiextension** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="47709-110">The **IWiaUIExtension** interface has these methods.</span></span>



| <span data-ttu-id="47709-111">Methode</span><span class="sxs-lookup"><span data-stu-id="47709-111">Method</span></span>                                                                  | <span data-ttu-id="47709-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="47709-112">Description</span></span>                                                                                  |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="47709-113">**Devicedialog**</span><span class="sxs-lookup"><span data-stu-id="47709-113">**DeviceDialog**</span></span>](-wia-iwiauiextension-devicedialog.md)               | <span data-ttu-id="47709-114">Stellt eine benutzerdefinierte Benutzeroberfläche bereit, die die standardmäßige Systembenutzer Oberfläche ersetzt.</span><span class="sxs-lookup"><span data-stu-id="47709-114">Provides a custom user interface that replaces the default system user interface.</span></span><br/> |
| [<span data-ttu-id="47709-115">**Getdevicebitmaplogo**</span><span class="sxs-lookup"><span data-stu-id="47709-115">**GetDeviceBitmapLogo**</span></span>](-wia-iwiauiextension-getdevicebitmaplogo.md) | <span data-ttu-id="47709-116">Ruft ein benutzerdefiniertes bitmaplogo für das Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="47709-116">Gets a custom bitmap logo for the device.</span></span><br/>                                         |
| [<span data-ttu-id="47709-117">**Getde viceicon**</span><span class="sxs-lookup"><span data-stu-id="47709-117">**GetDeviceIcon**</span></span>](-wia-iwiauiextension-getdeviceicon.md)             | <span data-ttu-id="47709-118">Ruft ein benutzerdefiniertes Gerätesymbol ab.</span><span class="sxs-lookup"><span data-stu-id="47709-118">Gets a custom device icon.</span></span><br/>                                                        |



 

## <a name="remarks"></a><span data-ttu-id="47709-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="47709-119">Remarks</span></span>



| <span data-ttu-id="47709-120">IUnknown-Methoden</span><span class="sxs-lookup"><span data-stu-id="47709-120">IUnknown Methods</span></span>                                        | <span data-ttu-id="47709-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="47709-121">Description</span></span>                               |
|---------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="47709-122">[IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="47709-122">[IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span> | <span data-ttu-id="47709-123">Gibt Zeiger auf unterstützte Schnittstellen zurück.</span><span class="sxs-lookup"><span data-stu-id="47709-123">Returns pointers to supported interfaces.</span></span> |
| [<span data-ttu-id="47709-124">IUnknown:: adressf</span><span class="sxs-lookup"><span data-stu-id="47709-124">IUnknown::AddRef</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | <span data-ttu-id="47709-125">Inkrementiert Verweiszähler.</span><span class="sxs-lookup"><span data-stu-id="47709-125">Increments reference count.</span></span>               |
| [<span data-ttu-id="47709-126">IUnknown:: Release</span><span class="sxs-lookup"><span data-stu-id="47709-126">IUnknown::Release</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | <span data-ttu-id="47709-127">Dekrementiert Verweiszähler.</span><span class="sxs-lookup"><span data-stu-id="47709-127">Decrements reference count.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="47709-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="47709-128">Requirements</span></span>



| <span data-ttu-id="47709-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="47709-129">Requirement</span></span> | <span data-ttu-id="47709-130">Wert</span><span class="sxs-lookup"><span data-stu-id="47709-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="47709-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="47709-131">Minimum supported client</span></span><br/> | <span data-ttu-id="47709-132">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="47709-132">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="47709-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="47709-133">Minimum supported server</span></span><br/> | <span data-ttu-id="47709-134">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="47709-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="47709-135">Header</span><span class="sxs-lookup"><span data-stu-id="47709-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="47709-136"><dt>Wiadevd. h</dt></span><span class="sxs-lookup"><span data-stu-id="47709-136"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 
