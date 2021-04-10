---
title: Verwenden von IProvideClassInfo
description: Verwenden von IProvideClassInfo
ms.assetid: 16541aab-474f-4ae5-a6b6-fb2fea6d38ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32a3abd61bb330a2a7d681b6d53648c5fbde8c53
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039679"
---
# <a name="using-iprovideclassinfo"></a><span data-ttu-id="346b5-103">Verwenden von IProvideClassInfo</span><span class="sxs-lookup"><span data-stu-id="346b5-103">Using IProvideClassInfo</span></span>

<span data-ttu-id="346b5-104">Ein Verbindungs fähigen-Objekt kann die [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) -Schnittstelle und die [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2) -Schnittstelle anbieten, damit Ihre Clients ihre Typinformationen problemlos überprüfen können.</span><span class="sxs-lookup"><span data-stu-id="346b5-104">A connectable object can offer the [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) and [**IProvideClassInfo2**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo2) interfaces so that its clients can easily examine its type information.</span></span> <span data-ttu-id="346b5-105">Diese Funktion ist wichtig beim Umgang mit ausgehenden Schnittstellen, die definitionsgemäß durch ein Objekt definiert, aber von einem Client auf einem eigenen Sink-Objekt implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="346b5-105">This capability is important when dealing with outgoing interfaces, which, by definition, are defined by an object but implemented by a client on its own sink object.</span></span> <span data-ttu-id="346b5-106">In einigen Fällen ist eine ausgehende Schnittstelle zum Zeitpunkt der Kompilierung sowohl dem Verbindungs fähigen-Objekt als auch dem sink-Objekt bekannt. Dies ist der Fall bei [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink).</span><span class="sxs-lookup"><span data-stu-id="346b5-106">In some cases, an outgoing interface is known at compile time to both the connectable object and the sink object; such is the case with [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink).</span></span>

<span data-ttu-id="346b5-107">In anderen Fällen kennt jedoch nur das Verbindungs fähige Objekt seine ausgehenden Schnittstellendefinitionen zur Kompilierzeit.</span><span class="sxs-lookup"><span data-stu-id="346b5-107">In other cases, however, only the connectable object knows its outgoing interface definitions at compile time.</span></span> <span data-ttu-id="346b5-108">In diesen Fällen muss der Client die Typinformationen für die ausgehende Schnittstelle abrufen, damit eine Senke, die die richtigen Einstiegspunkte unterstützt, dynamisch bereitgestellt werden kann, wie im folgenden dargestellt:</span><span class="sxs-lookup"><span data-stu-id="346b5-108">In these cases, the client must obtain the type information for the outgoing interface so that it can dynamically provide a sink supporting the right entry points, as follows:</span></span>

1.  <span data-ttu-id="346b5-109">Der Client listet die Verbindungspunkte auf und ruft dann die IIDs der ausgehenden Schnittstellen ab, die vom Verbindungs fähigen-Objekt unterstützt werden, und ruft für jeden Verbindungspunkt [**IConnectionPoint:: GetConnectionInterface**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-getconnectioninterface) auf.</span><span class="sxs-lookup"><span data-stu-id="346b5-109">The client enumerates the connection points and then, to obtain the IIDs of outgoing interfaces supported by the connectable object, calls [**IConnectionPoint::GetConnectionInterface**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-getconnectioninterface) for each connection point.</span></span>
2.  <span data-ttu-id="346b5-110">Der Client fragt das Verbindungs fähige Objekt für eine der [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) -Schnittstellen ab.</span><span class="sxs-lookup"><span data-stu-id="346b5-110">The client queries the connectable object for one of the [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) interfaces.</span></span>
3.  <span data-ttu-id="346b5-111">Der Client ruft Methoden in der [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) -Schnittstelle auf, um die Typinformationen für die ausgehende Schnittstelle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="346b5-111">The client calls methods in the [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) interfaces to get the type information for the outgoing interface.</span></span>
4.  <span data-ttu-id="346b5-112">Der Client erstellt ein Sink-Objekt, das die Ausgangs Schnittstelle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="346b5-112">The client creates a sink object supporting the outgoing interface.</span></span>
5.  <span data-ttu-id="346b5-113">Der Prozess wird fortgesetzt, und der Client ruft [**IConnectionPoint:: Empfehlung**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) auf, um seine Senke mit dem Verbindungspunkt zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="346b5-113">The process continues, and the client calls [**IConnectionPoint::Advise**](/windows/desktop/api/OCIdl/nf-ocidl-iconnectionpoint-advise) to connect its sink to the connection point.</span></span>

<span data-ttu-id="346b5-114">In den Typinformationen markiert die Attribut [**Quelle**](/windows/desktop/Midl/source) eine [**Schnittstelle**](/windows/desktop/Midl/interface) oder eine [**dispinterface**](/windows/desktop/Midl/dispinterface) , die unter einer [**Co-Klasse**](/windows/desktop/Midl/coclass) als ausgehende Schnittstelle aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="346b5-114">In the type information, the attribute [**source**](/windows/desktop/Midl/source) marks an [**interface**](/windows/desktop/Midl/interface) or [**dispinterface**](/windows/desktop/Midl/dispinterface) listed under a [**coclass**](/windows/desktop/Midl/coclass) as an outgoing interface.</span></span> <span data-ttu-id="346b5-115">Die ohne dieses Attribut aufgelisteten werden als eingehende Schnittstellen betrachtet.</span><span class="sxs-lookup"><span data-stu-id="346b5-115">Those listed without this attribute are considered incoming interfaces.</span></span>

## <a name="related-topics"></a><span data-ttu-id="346b5-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="346b5-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="346b5-117">Verbindungs fähige Objekt Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="346b5-117">Connectable Object Interfaces</span></span>](connectable-object-interfaces.md)
</dt> <dt>

[<span data-ttu-id="346b5-118">Bereitstellen von Klassen Informationen</span><span class="sxs-lookup"><span data-stu-id="346b5-118">Providing Class Information</span></span>](providing-class-information.md)
</dt> </dl>

 

 