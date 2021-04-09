---
title: Remotedesktopprotokoll Anbieter-API
description: Verwenden Sie die Remotedesktopprotokoll Anbieter-API, um ein Protokoll zu erstellen, um die Kommunikation zwischen dem Remotedesktopdienste-Dienst und mehreren Clients bereitzustellen.
ms.assetid: dd14c569-195e-460e-a1c3-2a74d0f49ff5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95aed1c6866f3078c3761ad8ec631ef23b43a9ae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947305"
---
# <a name="remote-desktop-protocol-provider-api"></a><span data-ttu-id="6e86a-103">Remotedesktopprotokoll Anbieter-API</span><span class="sxs-lookup"><span data-stu-id="6e86a-103">Remote Desktop Protocol Provider API</span></span>

<span data-ttu-id="6e86a-104">Verwenden Sie die Remotedesktopprotokoll Anbieter-API, um ein Protokoll zu erstellen, um die Kommunikation zwischen dem Remotedesktopdienste-Dienst und mehreren Clients bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="6e86a-104">You use the Remote Desktop Protocol Provider API to create a protocol to provide communication between the Remote Desktop Services service and multiple clients.</span></span>

<span data-ttu-id="6e86a-105">Wenn Windows Server geladen wird, wird der Remotedesktopdienste-Dienst (auch als Remote Verbindungs-Manager (RCM) bezeichnet) gestartet.</span><span class="sxs-lookup"><span data-stu-id="6e86a-105">When Windows Server loads, the Remote Desktop Services service (also known as Remote Connection Manager (RCM)) starts.</span></span> <span data-ttu-id="6e86a-106">Der Dienst startet auch Listenerobjekte für die Remotedesktopprotokoll-Anbieter, die wiederum auf Clientverbindungen lauschen.</span><span class="sxs-lookup"><span data-stu-id="6e86a-106">The service also starts listener objects for the Remote Desktop Protocol Providers that in turn listen for client connections.</span></span> <span data-ttu-id="6e86a-107">Der Dienst und die Protokoll Anbieter sind Benutzermodus-Objekte, die mithilfe der in dieser Dokumentation beschriebenen APIs kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="6e86a-107">The service and the protocol providers are user-mode objects that communicate by using the APIs discussed in this documentation.</span></span> <span data-ttu-id="6e86a-108">Die Protokoll Anbieter können mithilfe von Eingabe-/ausgabesteuerelementen (IOCTLs) mit Kernelmodustreibern kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="6e86a-108">The protocol providers can communicate with kernel-mode drivers by using input/output controls (IOCTLs).</span></span> <span data-ttu-id="6e86a-109">Dies ist in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="6e86a-109">This is shown in the following illustration.</span></span>

![benutzerdefinierte Protokoll-API-Architektur](images/protocol-architecture.png)

<span data-ttu-id="6e86a-111">Microsoft hat die Remotedesktopprotokoll (RDP) implementiert, um die Kommunikation zwischen dem Remotedesktopdienste Dienst und den Clientverbindungen zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="6e86a-111">Microsoft has implemented the Remote Desktop Protocol (RDP) to provide communication between the Remote Desktop Services service and client connections.</span></span> <span data-ttu-id="6e86a-112">Sie können ein eigenes Protokoll erstellen, indem Sie die Schnittstellen, Strukturen, Unions und Enumerationstypen verwenden, die die Remotedesktopprotokoll Anbieter-API bilden.</span><span class="sxs-lookup"><span data-stu-id="6e86a-112">You can create your own protocol by using the interfaces, structures, unions, and enumeration types that make up the Remote Desktop Protocol Provider API.</span></span> <span data-ttu-id="6e86a-113">Weitere Informationen finden Sie in den nachfolgenden Themen.</span><span class="sxs-lookup"><span data-stu-id="6e86a-113">For more information, see the following topics.</span></span>

<dl> <dt>

[<span data-ttu-id="6e86a-114">Erstellen eines Remotedesktopprotokoll Anbieters</span><span class="sxs-lookup"><span data-stu-id="6e86a-114">Creating a Remote Desktop Protocol Provider</span></span>](creating-a-custom-remote-protocol.md)
</dt> <dd>

<span data-ttu-id="6e86a-115">Informationen zum Erstellen eines Remotedesktopprotokoll Anbieters.</span><span class="sxs-lookup"><span data-stu-id="6e86a-115">Information about creating a Remote Desktop Protocol Provider.</span></span> <span data-ttu-id="6e86a-116">Der Protokoll-Manager wird als com-Server implementiert und an einem Speicherort registriert, der beim Starten des Remotedesktopdienste Dienstanbieter durchsucht wird.</span><span class="sxs-lookup"><span data-stu-id="6e86a-116">The protocol manager is implemented as a COM server and registered in a location searched when the Remote Desktop Services service starts.</span></span>

</dd> <dt>

[<span data-ttu-id="6e86a-117">Remotedesktopprotokoll Anbieter Referenz</span><span class="sxs-lookup"><span data-stu-id="6e86a-117">Remote Desktop Protocol Provider reference</span></span>](custom-remote-protocol-reference.md)
</dt> <dd>

<span data-ttu-id="6e86a-118">Enthält Schnittstellen, Strukturen, Unions und Enumerationstypen, die es Ihnen ermöglichen, eine benutzerdefinierte Remotedesktopprotokoll (RDP) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6e86a-118">Contains interfaces, structures, unions, and enumeration types that enable you to create a custom Remote Desktop Protocol (RDP).</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="6e86a-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6e86a-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e86a-120">Informationen zu Remotedesktopdienste</span><span class="sxs-lookup"><span data-stu-id="6e86a-120">About Remote Desktop Services</span></span>](about-terminal-services.md)
</dt> </dl>

 

 




