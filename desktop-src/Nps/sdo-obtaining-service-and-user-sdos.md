---
title: Abrufen von Dienst-und Benutzer-SDOs
description: Rufen Sie zum Abrufen von SDOs für NPS (IAS) oder einen bestimmten Benutzer die isdomachine getservicesdo-Methode oder die isdomachine getusersdo-Methode auf.
ms.assetid: 23e23fb3-0102-4c36-b30f-18604131ee32
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c7562c3b7c6aa1150ba3ce6581441064eb386f7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315711"
---
# <a name="obtaining-service-and-user-sdos"></a><span data-ttu-id="c5cf4-103">Abrufen von Dienst-und Benutzer-SDOs</span><span class="sxs-lookup"><span data-stu-id="c5cf4-103">Obtaining Service and User SDOs</span></span>

> [!Note]  
> <span data-ttu-id="c5cf4-104">Der Internet Authentifizierungsdienst (IAS) wurde ab Windows Server 2008 in den Netzwerk Richtlinien Server (Network Policy Server, NPS) umbenannt.</span><span class="sxs-lookup"><span data-stu-id="c5cf4-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span>

 

<span data-ttu-id="c5cf4-105">Rufen Sie zum Abrufen von SDOs für NPS (IAS) oder einen bestimmten Benutzer die [**isdomachine:: getservicesdo**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) -Methode oder die [**isdomachine:: getusersdo**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="c5cf4-105">To obtain SDOs for NPS (IAS) or a particular user, call the [**ISdoMachine::GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) or [**ISdoMachine::GetUserSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo) methods.</span></span> <span data-ttu-id="c5cf4-106">Diese Methoden geben Zeiger auf [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstellen für diese Objekte zurück.</span><span class="sxs-lookup"><span data-stu-id="c5cf4-106">These methods return pointers to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interfaces for these objects.</span></span> <span data-ttu-id="c5cf4-107">Verwenden Sie für den Benutzer SDO die [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) -Methode, um eine [**isdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) -Schnittstelle für das Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c5cf4-107">For the user SDO, use the [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method to obtain an [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) interface for the object.</span></span> <span data-ttu-id="c5cf4-108">Verwenden Sie für den Dienst SDO **IUnknown:: QueryInterface** , um eine [**isdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) -Schnittstelle oder eine [**isdoservicecontrol**](/windows/desktop/api/sdoias/nn-sdoias-isdoservicecontrol) -Schnittstelle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c5cf4-108">For the service SDO, use **IUnknown::QueryInterface** to obtain an [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) interface or [**ISdoServiceControl**](/windows/desktop/api/sdoias/nn-sdoias-isdoservicecontrol) interface.</span></span>

<span data-ttu-id="c5cf4-109">Rufen Sie vor dem Aufrufen von [**isdomachine:: getservicesdo**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) oder [**isdomachine:: getusersdo**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo) [**isdomachine:: Attach**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach) auf, um das Computer Objekt dem lokalen Computer zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="c5cf4-109">Before calling either [**ISdoMachine::GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) or [**ISdoMachine::GetUserSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo), call [**ISdoMachine::Attach**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach) to associate the machine object with the local computer.</span></span>

<span data-ttu-id="c5cf4-110">Informationen zum Abrufen dieser SDOs finden Sie unter [Abrufen eines SDO-diensdo](/windows/desktop/Nps/sdo-retrieving-a-service-sdo) und [Abrufen eines Benutzers SDO (SDO](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) ).</span><span class="sxs-lookup"><span data-stu-id="c5cf4-110">See [Retrieving a Service SDO](/windows/desktop/Nps/sdo-retrieving-a-service-sdo) and [Retrieving a User SDO](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) for sample code that demonstrates how to obtain these SDOs.</span></span>

 

 