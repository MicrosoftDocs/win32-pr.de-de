---
title: WinRM-C++-API
description: Die Windows-Remoteverwaltung Schnittstellen können zum Abrufen von Daten oder zum Verwalten von Ressourcen auf einem Remote Computer verwendet werden. Diese API ist in erster Linie für die interne Verwendung vorgesehen. Es wird empfohlen, die WinRM-ClientShell-API zu verwenden, wenn möglich.
ms.assetid: e50075a1-cb43-4bd6-9bbf-6b715fde6a3a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa7cff2334d9839936d15f7258a70ce03f9751e6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947874"
---
# <a name="winrm-c-api"></a><span data-ttu-id="73a55-105">WinRM-C++-API</span><span class="sxs-lookup"><span data-stu-id="73a55-105">WinRM C++ API</span></span>

<span data-ttu-id="73a55-106">Die Windows-Remoteverwaltung Schnittstellen können zum Abrufen von Daten oder zum Verwalten von [*Ressourcen*](windows-remote-management-glossary.md) auf einem Remote Computer verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="73a55-106">The Windows Remote Management interfaces can be used to obtain data or manage [*resources*](windows-remote-management-glossary.md) on a remote computer.</span></span> <span data-ttu-id="73a55-107">Diese API ist in erster Linie für die interne Verwendung vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="73a55-107">This API is intended primarily for internal use.</span></span> <span data-ttu-id="73a55-108">Es wird empfohlen, die [WinRM-ClientShell-API](client-shell-api.md) zu verwenden, wenn möglich.</span><span class="sxs-lookup"><span data-stu-id="73a55-108">We recommend using the [WinRM Client Shell API](client-shell-api.md) instead whenever possible.</span></span> <span data-ttu-id="73a55-109">Die Schnittstellen entsprechen eng der [WinRM-Skript-API](winrm-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="73a55-109">The interfaces closely correspond to the [WinRM Scripting API](winrm-scripting-api.md).</span></span>

<span data-ttu-id="73a55-110">Die WinRM-Schnittstellen, die direkt von **IDispatch** erben, verfügen jeweils über ein entsprechendes Skript Objekt.</span><span class="sxs-lookup"><span data-stu-id="73a55-110">The WinRM interfaces that inherit directly from **IDispatch** each have a corresponding scripting object.</span></span> <span data-ttu-id="73a55-111">Weitere Informationen finden Sie in der [WinRM-Skript-API](winrm-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="73a55-111">For more information, see the [WinRM Scripting API](winrm-scripting-api.md).</span></span>

<span data-ttu-id="73a55-112">Bei Multithreadanwendungen unterstützt WinRM keine separaten Threads, die auf dasselbe [**iwsman**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) -Objekt zugreifen.</span><span class="sxs-lookup"><span data-stu-id="73a55-112">For multithreaded applications, WinRM does not support separate threads accessing the same [**IWSMAN**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) object.</span></span>

<span data-ttu-id="73a55-113">Die folgenden Schnittstellen werden von WinRM bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="73a55-113">The following interfaces are provided by WinRM.</span></span>

<dl> <dt>

<span data-ttu-id="73a55-114"><span id="IWSMan"></span><span id="iwsman"></span><span id="IWSMAN"></span>[**Iwsman**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman)</span><span class="sxs-lookup"><span data-stu-id="73a55-114"><span id="IWSMan"></span><span id="iwsman"></span><span id="IWSMAN"></span>[**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman)</span></span>
</dt> <dd>

<span data-ttu-id="73a55-115">Stellt Methoden und Eigenschaften bereit, mit denen eine neue Sitzung erstellt und eine festgelegte Sitzung verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="73a55-115">Provides methods and properties used to create a new session and manage an established session.</span></span> <span data-ttu-id="73a55-116">[**WSMAN**](wsman.md) ist das entsprechende Skript Objekt.</span><span class="sxs-lookup"><span data-stu-id="73a55-116">[**WSMan**](wsman.md) is the corresponding scripting object.</span></span>

</dd> <dt>

<span data-ttu-id="73a55-117"><span id="IWSManEx"></span><span id="iwsmanex"></span><span id="IWSMANEX"></span>[**Iwsmanex**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman)</span><span class="sxs-lookup"><span data-stu-id="73a55-117"><span id="IWSManEx"></span><span id="iwsmanex"></span><span id="IWSMANEX"></span>[**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman)</span></span>
</dt> <dd>

<span data-ttu-id="73a55-118">Stellt Methoden und Eigenschaften zur Verfügung, die zum Erstellen eines neuen [**iwsmanresourcelocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="73a55-118">Provides methods and properties used to create a new [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator).</span></span> <span data-ttu-id="73a55-119">Diese Methode ist für das [**WSMAN**](wsman.md) -Skript Objekt verfügbar.</span><span class="sxs-lookup"><span data-stu-id="73a55-119">This method is available for the [**WSMan**](wsman.md) scripting object.</span></span>

</dd> <dt>

<span data-ttu-id="73a55-120"><span id="IWSManConnectionOptions"></span><span id="iwsmanconnectionoptions"></span><span id="IWSMANCONNECTIONOPTIONS"></span>[**Iwsmanconnectionoptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions)</span><span class="sxs-lookup"><span data-stu-id="73a55-120"><span id="IWSManConnectionOptions"></span><span id="iwsmanconnectionoptions"></span><span id="IWSMANCONNECTIONOPTIONS"></span>[**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions)</span></span>
</dt> <dd>

<span data-ttu-id="73a55-121">Definiert den Benutzernamen und das Kennwort, die für Remote Verbindungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="73a55-121">Defines the user name and password used for remote connections.</span></span> <span data-ttu-id="73a55-122">[**ConnectionOptions**](connectionoptions.md) ist das entsprechende Skript Objekt.</span><span class="sxs-lookup"><span data-stu-id="73a55-122">[**ConnectionOptions**](connectionoptions.md) is the corresponding scripting object.</span></span>

</dd> <dt>

<span data-ttu-id="73a55-123"><span id="IWSManSession"></span><span id="iwsmansession"></span><span id="IWSMANSESSION"></span>[**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)</span><span class="sxs-lookup"><span data-stu-id="73a55-123"><span id="IWSManSession"></span><span id="iwsmansession"></span><span id="IWSMANSESSION"></span>[**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)</span></span>
</dt> <dd>

<span data-ttu-id="73a55-124">Definiert die Netzwerk Vorgänge und-Eigenschaften, die für die Sitzung verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="73a55-124">Defines the network operations and properties available for the session.</span></span> <span data-ttu-id="73a55-125">Die [**Sitzung**](session.md) ist das entsprechende Skript Objekt.</span><span class="sxs-lookup"><span data-stu-id="73a55-125">[**Session**](session.md) is the corresponding scripting object.</span></span>

</dd> <dt>

<span data-ttu-id="73a55-126"><span id="IWSManEnumerator"></span><span id="iwsmanenumerator"></span><span id="IWSMANENUMERATOR"></span>[**Iwsmanenumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator)</span><span class="sxs-lookup"><span data-stu-id="73a55-126"><span id="IWSManEnumerator"></span><span id="iwsmanenumerator"></span><span id="IWSMANENUMERATOR"></span>[**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator)</span></span>
</dt> <dd>

<span data-ttu-id="73a55-127">Stellt eine Auflistung von Ergebnissen dar, die beim Auflisten einer Ressource zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="73a55-127">Represents a collection of results returned from enumerating a resource.</span></span> <span data-ttu-id="73a55-128">[**Enumerator**](enumerator.md) ist das entsprechende Skript Objekt.</span><span class="sxs-lookup"><span data-stu-id="73a55-128">[**Enumerator**](enumerator.md) is the corresponding scripting object.</span></span>

</dd> <dt>

<span data-ttu-id="73a55-129"><span id="IWSManResourceLocator"></span><span id="iwsmanresourcelocator"></span><span id="IWSMANRESOURCELOCATOR"></span>[**Iwsmanresourcelocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator)</span><span class="sxs-lookup"><span data-stu-id="73a55-129"><span id="IWSManResourceLocator"></span><span id="iwsmanresourcelocator"></span><span id="IWSMANRESOURCELOCATOR"></span>[**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator)</span></span>
</dt> <dd>

<span data-ttu-id="73a55-130">Gibt den Pfad zu einer Ressource an.</span><span class="sxs-lookup"><span data-stu-id="73a55-130">Supplies the path to a resource.</span></span> <span data-ttu-id="73a55-131">Sie können ein [**iwsmanresourcelocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) -Objekt anstelle eines [*Ressourcen-URI*](windows-remote-management-glossary.md) in [**Sitzungs**](session.md) Objekt Vorgängen verwenden.</span><span class="sxs-lookup"><span data-stu-id="73a55-131">You can use an [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) object instead of a [*resource URI*](windows-remote-management-glossary.md) in [**Session**](session.md) object operations.</span></span> <span data-ttu-id="73a55-132">[**ResourceLocator**](resourcelocator.md) ist das entsprechende Skript Objekt.</span><span class="sxs-lookup"><span data-stu-id="73a55-132">[**ResourceLocator**](resourcelocator.md) is the corresponding scripting object.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="73a55-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="73a55-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73a55-134">Windows-Remoteverwaltung Referenz</span><span class="sxs-lookup"><span data-stu-id="73a55-134">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> </dl>

 

 




