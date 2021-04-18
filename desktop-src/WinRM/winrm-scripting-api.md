---
title: WinRM-Skript-API
description: Windows-Remoteverwaltung Skript Objekte werden als Ebene oberhalb des WS-Management Protokolls implementiert.
ms.assetid: bd642669-554f-40ab-bd40-235013afa077
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7910213487f525b74c3d1a8819a450f95336aba1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338210"
---
# <a name="winrm-scripting-api"></a><span data-ttu-id="b8c73-103">WinRM-Skript-API</span><span class="sxs-lookup"><span data-stu-id="b8c73-103">WinRM Scripting API</span></span>

<span data-ttu-id="b8c73-104">Windows-Remoteverwaltung Skript Objekte werden als Ebene oberhalb der [WS-Management-Protokoll](ws-management-protocol.md)implementiert.</span><span class="sxs-lookup"><span data-stu-id="b8c73-104">Windows Remote Management scripting objects are implemented as a layer above the [WS-Management Protocol](ws-management-protocol.md).</span></span> <span data-ttu-id="b8c73-105">Mit den Skript Objekten können Sie Daten abrufen oder [*Ressourcen*](windows-remote-management-glossary.md) auf lokalen Computern und Remote Computern verwalten.</span><span class="sxs-lookup"><span data-stu-id="b8c73-105">The scripting objects enable you to obtain data or manage [*resources*](windows-remote-management-glossary.md) on local and remote computers.</span></span>

## <a name="ws-management-objects"></a><span data-ttu-id="b8c73-106">WS-Management Objekte</span><span class="sxs-lookup"><span data-stu-id="b8c73-106">WS-Management Objects</span></span>

<span data-ttu-id="b8c73-107">Jedes Skript Objekt verfügt über eine entsprechende C++-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="b8c73-107">Each scripting object has a corresponding C++ interface.</span></span> <span data-ttu-id="b8c73-108">Weitere Informationen finden Sie unter [WinRM C++ API](winrm-c---api.md) und [Scripting in Windows-Remoteverwaltung](scripting-in-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="b8c73-108">For more information, see [WinRM C++ API](winrm-c---api.md) and [Scripting in Windows Remote Management](scripting-in-windows-remote-management.md).</span></span>

<span data-ttu-id="b8c73-109">Die folgenden Objekte werden von der WinRM-Skript-API bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="b8c73-109">The following objects are provided by the WinRM Scripting API.</span></span>

<dl> <dt>

<span data-ttu-id="b8c73-110"><span id="ConnectionOptions"></span><span id="connectionoptions"></span><span id="CONNECTIONOPTIONS"></span>[**ConnectionOptions**](connectionoptions.md)</span><span class="sxs-lookup"><span data-stu-id="b8c73-110"><span id="ConnectionOptions"></span><span id="connectionoptions"></span><span id="CONNECTIONOPTIONS"></span>[**ConnectionOptions**](connectionoptions.md)</span></span>
</dt> <dd>

<span data-ttu-id="b8c73-111">Definiert den Benutzernamen und das Kennwort, die für Remote Verbindungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b8c73-111">Defines the user name and password used for remote connections.</span></span> <span data-ttu-id="b8c73-112">Der Benutzername und das Kennwort werden übergeben, wenn die [**createconnectionoptions**](wsman-createconnectionoptions.md) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="b8c73-112">The user name and password are passed when calling the [**CreateConnectionOptions**](wsman-createconnectionoptions.md) method.</span></span> <span data-ttu-id="b8c73-113">Weitere Informationen finden Sie unter Abrufen [von Daten von einem Remote Computer](obtaining-data-from-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="b8c73-113">For more information, see [Obtaining Data from a Remote Computer](obtaining-data-from-a-remote-computer.md).</span></span> <span data-ttu-id="b8c73-114">Die entsprechende C++-Schnittstelle ist [**iwsmanconnectionoptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions).</span><span class="sxs-lookup"><span data-stu-id="b8c73-114">The corresponding C++ interface is [**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions).</span></span>

</dd> <dt>

<span data-ttu-id="b8c73-115"><span id="Enumerator"></span><span id="enumerator"></span><span id="ENUMERATOR"></span>[**Enumerator**](enumerator.md)</span><span class="sxs-lookup"><span data-stu-id="b8c73-115"><span id="Enumerator"></span><span id="enumerator"></span><span id="ENUMERATOR"></span>[**Enumerator**](enumerator.md)</span></span>
</dt> <dd>

<span data-ttu-id="b8c73-116">Stellt eine Auflistung von Ergebnissen dar, die beim Auflisten einer Ressource zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b8c73-116">Represents a collection of results returned from enumerating a resource.</span></span> <span data-ttu-id="b8c73-117">Weitere Informationen finden Sie unter [auflisten oder Auflisten aller Instanzen einer Ressource](enumerating-or-listing-all-instances-of-a-resource.md).</span><span class="sxs-lookup"><span data-stu-id="b8c73-117">For more information, see [Enumerating or Listing All the Instances of a Resource](enumerating-or-listing-all-instances-of-a-resource.md).</span></span> <span data-ttu-id="b8c73-118">Die entsprechende C++-Schnittstelle ist [**iwsmanenumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator).</span><span class="sxs-lookup"><span data-stu-id="b8c73-118">The corresponding C++ interface is [**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator).</span></span>

</dd> <dt>

<span data-ttu-id="b8c73-119"><span id="ResourceLocator"></span><span id="resourcelocator"></span><span id="RESOURCELOCATOR"></span>[**ResourceLocator**](resourcelocator.md)</span><span class="sxs-lookup"><span data-stu-id="b8c73-119"><span id="ResourceLocator"></span><span id="resourcelocator"></span><span id="RESOURCELOCATOR"></span>[**ResourceLocator**](resourcelocator.md)</span></span>
</dt> <dd>

<span data-ttu-id="b8c73-120">Gibt den Pfad zu einer Ressource an.</span><span class="sxs-lookup"><span data-stu-id="b8c73-120">Supplies the path to a resource.</span></span> <span data-ttu-id="b8c73-121">Sie können ein [**ResourceLocator**](resourcelocator.md) -Objekt anstelle eines [*Ressourcen-URIs*](windows-remote-management-glossary.md) in [**Sitzungs**](session.md) Objekt Vorgängen verwenden, z. b. " [**Session. Get**](session-get.md)", " [**Session. Put**](session-put.md)" oder " [**Session. Enumerate**](session-enumerate.md)".</span><span class="sxs-lookup"><span data-stu-id="b8c73-121">You can use a [**ResourceLocator**](resourcelocator.md) object instead of a [*resource URI*](windows-remote-management-glossary.md) in [**Session**](session.md) object operations, such as [**Session.Get**](session-get.md), [**Session.Put**](session-put.md), or [**Session.Enumerate**](session-enumerate.md).</span></span> <span data-ttu-id="b8c73-122">Die entsprechende C++-Schnittstelle ist [**iwsmanresourcelocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator).</span><span class="sxs-lookup"><span data-stu-id="b8c73-122">The corresponding C++ interface is [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator).</span></span>

</dd> <dt>

<span data-ttu-id="b8c73-123"><span id="Session"></span><span id="session"></span><span id="SESSION"></span>[**Sitzung**](session.md)</span><span class="sxs-lookup"><span data-stu-id="b8c73-123"><span id="Session"></span><span id="session"></span><span id="SESSION"></span>[**Session**](session.md)</span></span>
</dt> <dd>

<span data-ttu-id="b8c73-124">Definiert die Netzwerk Vorgänge und-Eigenschaften, die für die Sitzung verfügbar sind, z. b [**. Session. Get**](session-get.md), [**Session. Enumerate**](session-enumerate.md), [**Session. aufrufen**](session-invoke.md).</span><span class="sxs-lookup"><span data-stu-id="b8c73-124">Defines the network operations and properties available for the session, such as [**Session.Get**](session-get.md), [**Session.Enumerate**](session-enumerate.md), [**Session.Invoke**](session-invoke.md).</span></span> <span data-ttu-id="b8c73-125">Weitere Informationen finden Sie unter Abrufen [von Daten vom lokalen Computer](obtaining-data-from-the-local-computer.md).</span><span class="sxs-lookup"><span data-stu-id="b8c73-125">For more information, see [Obtaining Data from the Local Computer](obtaining-data-from-the-local-computer.md).</span></span> <span data-ttu-id="b8c73-126">Die entsprechende C++-Schnittstelle ist [**iwsmansession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession).</span><span class="sxs-lookup"><span data-stu-id="b8c73-126">The corresponding C++ interface is [**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession).</span></span>

</dd> <dt>

<span data-ttu-id="b8c73-127"><span id="WSMan"></span><span id="wsman"></span><span id="WSMAN"></span>[**WSMAN**](wsman.md)</span><span class="sxs-lookup"><span data-stu-id="b8c73-127"><span id="WSMan"></span><span id="wsman"></span><span id="WSMAN"></span>[**WSMan**](wsman.md)</span></span>
</dt> <dd>

<span data-ttu-id="b8c73-128">Stellt Methoden und Eigenschaften zur Verfügung, die zum Erstellen einer neuen Sitzung oder zum Verwalten einer eingerichteten Sitzung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b8c73-128">Provides methods and properties used to create a new session or manage an established session.</span></span> <span data-ttu-id="b8c73-129">Weitere Informationen finden Sie unter [Verwenden von Windows-Remoteverwaltung](using-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="b8c73-129">For more information see, [Using Windows Remote Management](using-windows-remote-management.md).</span></span> <span data-ttu-id="b8c73-130">Die entsprechenden C++-Schnittstellen sind [**iwsman**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) und [**iwsmanex**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex).</span><span class="sxs-lookup"><span data-stu-id="b8c73-130">The corresponding C++ interfaces are [**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) and [**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex).</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="b8c73-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b8c73-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8c73-132">Informationen zu Windows-Remoteverwaltung</span><span class="sxs-lookup"><span data-stu-id="b8c73-132">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="b8c73-133">Verwenden von Windows-Remoteverwaltung</span><span class="sxs-lookup"><span data-stu-id="b8c73-133">Using Windows Remote Management</span></span>](using-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="b8c73-134">Skripterstellung in Windows-Remoteverwaltung</span><span class="sxs-lookup"><span data-stu-id="b8c73-134">Scripting in Windows Remote Management</span></span>](scripting-in-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="b8c73-135">Windows-Remoteverwaltung Referenz</span><span class="sxs-lookup"><span data-stu-id="b8c73-135">Windows Remote Management Reference</span></span>](windows-remote-management-reference.md)
</dt> </dl>

 

 




