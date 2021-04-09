---
description: Die IWiaDevMgr2-Schnittstelle wird verwendet, um Abbild Erfassungsgeräte zu erstellen und zu verwalten sowie zum Empfangen von Geräte Ereignissen zu registrieren.
ms.assetid: 0e9fb3a1-bbe3-4dba-ba8c-b79f202d5a38
title: IWiaDevMgr2-Schnittstelle (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 1dd73733d77c80ba4f3880464000f823e0e35092
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865247"
---
# <a name="iwiadevmgr2-interface"></a><span data-ttu-id="66a81-103">IWiaDevMgr2-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="66a81-103">IWiaDevMgr2 interface</span></span>

<span data-ttu-id="66a81-104">Die **IWiaDevMgr2** -Schnittstelle wird verwendet, um Abbild Erfassungsgeräte zu erstellen und zu verwalten sowie zum Empfangen von Geräte Ereignissen zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="66a81-104">The **IWiaDevMgr2** interface is used to create and manage image acquisition devices and to register to receive device events.</span></span>

## <a name="members"></a><span data-ttu-id="66a81-105">Member</span><span class="sxs-lookup"><span data-stu-id="66a81-105">Members</span></span>

<span data-ttu-id="66a81-106">Die **IWiaDevMgr2** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="66a81-106">The **IWiaDevMgr2** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="66a81-107">**IWiaDevMgr2** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="66a81-107">**IWiaDevMgr2** also has these types of members:</span></span>

-   [<span data-ttu-id="66a81-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="66a81-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="66a81-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="66a81-109">Methods</span></span>

<span data-ttu-id="66a81-110">Die **IWiaDevMgr2** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="66a81-110">The **IWiaDevMgr2** interface has these methods.</span></span>



| <span data-ttu-id="66a81-111">Methode</span><span class="sxs-lookup"><span data-stu-id="66a81-111">Method</span></span>                                                                                    | <span data-ttu-id="66a81-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="66a81-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                  |
|:------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="66a81-113">**"Kreatedevice"**</span><span class="sxs-lookup"><span data-stu-id="66a81-113">**CreateDevice**</span></span>](-wia-iwiadevmgr2-createdevice.md)                                     | <span data-ttu-id="66a81-114">Erstellt eine hierarchische Struktur von [**IWiaItem2**](-wia-iwiaitem2.md) -Objekten für ein WIA 2,0-Gerät.</span><span class="sxs-lookup"><span data-stu-id="66a81-114">Creates a hierarchical tree of [**IWiaItem2**](-wia-iwiaitem2.md) objects for a WIA 2.0 device.</span></span> <br/>                                                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="66a81-115">**Enumdäviceingefo**</span><span class="sxs-lookup"><span data-stu-id="66a81-115">**EnumDeviceInfo**</span></span>](-wia-iwiadevmgr2-enumdeviceinfo.md)                                 | <span data-ttu-id="66a81-116">Erstellt einen Enumerator mit Eigenschafts Informationen für jedes verfügbare WIA 2,0-Gerät.</span><span class="sxs-lookup"><span data-stu-id="66a81-116">Creates an enumerator of property information for each available WIA 2.0 device.</span></span> <br/>                                                                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="66a81-117">**Getimagedlg**</span><span class="sxs-lookup"><span data-stu-id="66a81-117">**GetImageDlg**</span></span>](-wia-iwiadevmgr2-getimagedlg.md)                                       | <span data-ttu-id="66a81-118">Die [**IWiaDevMgr2:: getimagedlg**](-wia-iwiadevmgr2-getimagedlg.md) -Methode zeigt ein oder mehrere Dialogfelder an, mit denen ein Benutzer ein Bild von einem WIA 2,0-Gerät abrufen und in eine angegebene Datei schreiben kann.</span><span class="sxs-lookup"><span data-stu-id="66a81-118">The [**IWiaDevMgr2::GetImageDlg**](-wia-iwiadevmgr2-getimagedlg.md) method displays one or more dialog boxes that enable a user to acquire an image from a WIA 2.0 device and write the image to a specified file.</span></span> <span data-ttu-id="66a81-119">Mit dieser Methode wird die Funktionalität von [**IWiaDevMgr2:: SelectDeviceDlg**](-wia-iwiadevmgr2-selectdevicedlg.md) erweitert, um die Bild Erfassung innerhalb eines einzelnen API-Aufrufs zu kapseln.</span><span class="sxs-lookup"><span data-stu-id="66a81-119">This method extends the functionality of [**IWiaDevMgr2::SelectDeviceDlg**](-wia-iwiadevmgr2-selectdevicedlg.md) to encapsulate image acquisition within a single API call.</span></span> <br/> |
| [<span data-ttu-id="66a81-120">**Registereventcallbackclsid**</span><span class="sxs-lookup"><span data-stu-id="66a81-120">**RegisterEventCallbackCLSID**</span></span>](-wia-iwiadevmgr2-registereventcallbackclsid.md)         | <span data-ttu-id="66a81-121">Mit der [**IWiaDevMgr2:: registereventcallbackclsid**](-wia-iwiadevmgr2-registereventcallbackclsid.md) -Methode wird eine Anwendung zum Empfangen von Ereignissen registriert, auch wenn die Anwendung nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="66a81-121">The [**IWiaDevMgr2::RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md) method registers an application to receive events even if the application is not running.</span></span><br/>                                                                                                                                                                                                      |
| [<span data-ttu-id="66a81-122">**Registereventcallbackinterface**</span><span class="sxs-lookup"><span data-stu-id="66a81-122">**RegisterEventCallbackInterface**</span></span>](-wia-iwiadevmgr2-registereventcallbackinterface.md) | <span data-ttu-id="66a81-123">Registriert eine laufende Anwendung für die WIA 2,0-Ereignis Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="66a81-123">Registers a running application for WIA 2.0 event notification.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="66a81-124">**Registereventcallbackprogram**</span><span class="sxs-lookup"><span data-stu-id="66a81-124">**RegisterEventCallbackProgram**</span></span>](-wia-iwiadevmgr2-registereventcallbackprogram.md)     | <span data-ttu-id="66a81-125">Die [**IWiaDevMgr2:: registereventcallbackprogram**](-wia-iwiadevmgr2-registereventcallbackprogram.md) -Methode registriert eine Anwendung, um Geräte Ereignisse zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="66a81-125">The [**IWiaDevMgr2::RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md) method registers an application to receive device events.</span></span> <span data-ttu-id="66a81-126">Es wird hauptsächlich aus Gründen der Abwärtskompatibilität mit Anwendungen bereitgestellt, die nicht für WIA 2,0 geschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="66a81-126">It is primarily provided for backward compatibility with applications that were not written for WIA 2.0.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="66a81-127">**Selectde vicedlg**</span><span class="sxs-lookup"><span data-stu-id="66a81-127">**SelectDeviceDlg**</span></span>](-wia-iwiadevmgr2-selectdevicedlg.md)                               | <span data-ttu-id="66a81-128">Zeigt ein Dialogfeld an, in dem der Benutzer ein Hardware Gerät für die Abbild Erfassung auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="66a81-128">Displays a dialog box that enables the user to select a hardware device for image acquisition.</span></span> <br/>                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="66a81-129">**Selectdebug-lgid**</span><span class="sxs-lookup"><span data-stu-id="66a81-129">**SelectDeviceDlgID**</span></span>](-wia-iwiadevmgr2-selectdevicedlgid.md)                           | <span data-ttu-id="66a81-130">Zeigt ein Dialogfeld an, in dem der Benutzer ein Hardware Gerät für die Abbild Erfassung auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="66a81-130">Displays a dialog box that enables the user to select a hardware device for image acquisition.</span></span> <br/>                                                                                                                                                                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="66a81-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="66a81-131">Remarks</span></span>

<span data-ttu-id="66a81-132">Die **IWiaDevMgr2** -Schnittstelle erbt wie alle Component Object Model-Schnittstellen (com) die [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstellen Methoden.</span><span class="sxs-lookup"><span data-stu-id="66a81-132">The **IWiaDevMgr2** interface, like all Component Object Model (COM) interfaces, inherits the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface methods.</span></span>



| <span data-ttu-id="66a81-133">IUnknown-Methoden</span><span class="sxs-lookup"><span data-stu-id="66a81-133">IUnknown Methods</span></span>                                        | <span data-ttu-id="66a81-134">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="66a81-134">Description</span></span>                               |
|---------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="66a81-135">[IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span><span class="sxs-lookup"><span data-stu-id="66a81-135">[IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))</span></span> | <span data-ttu-id="66a81-136">Gibt Zeiger auf unterstützte Schnittstellen zurück.</span><span class="sxs-lookup"><span data-stu-id="66a81-136">Returns pointers to supported interfaces.</span></span> |
| [<span data-ttu-id="66a81-137">IUnknown:: adressf</span><span class="sxs-lookup"><span data-stu-id="66a81-137">IUnknown::AddRef</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | <span data-ttu-id="66a81-138">Inkrementiert Verweiszähler.</span><span class="sxs-lookup"><span data-stu-id="66a81-138">Increments reference count.</span></span>               |
| [<span data-ttu-id="66a81-139">IUnknown:: Release</span><span class="sxs-lookup"><span data-stu-id="66a81-139">IUnknown::Release</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | <span data-ttu-id="66a81-140">Dekrementiert Verweiszähler.</span><span class="sxs-lookup"><span data-stu-id="66a81-140">Decrements reference count.</span></span>               |



 

## <a name="requirements"></a><span data-ttu-id="66a81-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="66a81-141">Requirements</span></span>



| <span data-ttu-id="66a81-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="66a81-142">Requirement</span></span> | <span data-ttu-id="66a81-143">Wert</span><span class="sxs-lookup"><span data-stu-id="66a81-143">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="66a81-144">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="66a81-144">Minimum supported client</span></span><br/> | <span data-ttu-id="66a81-145">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="66a81-145">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="66a81-146">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="66a81-146">Minimum supported server</span></span><br/> | <span data-ttu-id="66a81-147">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="66a81-147">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="66a81-148">Header</span><span class="sxs-lookup"><span data-stu-id="66a81-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="66a81-149"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="66a81-149"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="66a81-150">IDL</span><span class="sxs-lookup"><span data-stu-id="66a81-150">IDL</span></span><br/>                      | <dl> <span data-ttu-id="66a81-151"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="66a81-151"><dt>Wia.idl</dt></span></span> </dl> |



 

 
