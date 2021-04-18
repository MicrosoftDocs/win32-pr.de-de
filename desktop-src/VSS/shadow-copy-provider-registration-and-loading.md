---
description: Registrierung und Laden von schattenkopieanbietern
ms.assetid: f9bb72ce-9a2b-43cd-9697-1f6598a46e3e
title: Registrierung und Laden von schattenkopieanbietern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 725613ff37450075c964b3c66fce3ffba1a70529
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344999"
---
# <a name="shadow-copy-provider-registration-and-loading"></a><span data-ttu-id="36180-103">Registrierung und Laden von schattenkopieanbietern</span><span class="sxs-lookup"><span data-stu-id="36180-103">Shadow Copy Provider Registration and Loading</span></span>

## <a name="provider-registration"></a><span data-ttu-id="36180-104">Anbieter Registrierung</span><span class="sxs-lookup"><span data-stu-id="36180-104">Provider Registration</span></span>

<span data-ttu-id="36180-105">Nur VSS ruft Anbieter auf.</span><span class="sxs-lookup"><span data-stu-id="36180-105">Only VSS calls providers.</span></span> <span data-ttu-id="36180-106">Der Anbieter registriert sich für Aufrufe durch Aufrufen von [**ivssadmin:: RegisterProvider**](/windows/desktop/api/VsAdmin/nf-vsadmin-ivssadmin-registerprovider)und übergibt **VSS \_ Prov \_ Hardware** für den *eprovidertype* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="36180-106">The provider registers for calls by invoking [**IVssAdmin::RegisterProvider**](/windows/desktop/api/VsAdmin/nf-vsadmin-ivssadmin-registerprovider), passing **VSS\_PROV\_HARDWARE** for the *eProviderType* parameter.</span></span> <span data-ttu-id="36180-107">Nach der Registrierung wird der Anbieter an der Schattenkopieverwaltung beteiligt sein, bis die Registrierung mithilfe von [**ivssadmin:: unregisterprovider**](/windows/desktop/api/VsAdmin/nf-vsadmin-ivssadmin-unregisterprovider)aufgehoben wird.</span><span class="sxs-lookup"><span data-stu-id="36180-107">Once registered, the provider will be involved in shadow copy management until unregistering using [**IVssAdmin::UnregisterProvider**](/windows/desktop/api/VsAdmin/nf-vsadmin-ivssadmin-unregisterprovider).</span></span>

## <a name="provider-loading-and-unloading"></a><span data-ttu-id="36180-108">Laden und Entladen von Anbietern</span><span class="sxs-lookup"><span data-stu-id="36180-108">Provider Loading and Unloading</span></span>

<span data-ttu-id="36180-109">Anbieter können häufig geladen und entladen werden.</span><span class="sxs-lookup"><span data-stu-id="36180-109">Providers can be frequently loaded and unloaded.</span></span> <span data-ttu-id="36180-110">Anbieter können [**ivssproviderbenachrichtigungen**](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidernotifications) implementieren, um zu bestimmen, wann der Anbieter von VSS geladen oder entladen wird.</span><span class="sxs-lookup"><span data-stu-id="36180-110">Providers can implement [**IVssProviderNotifications**](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidernotifications) to determine when VSS is loading or unloading the provider.</span></span>

 

 



