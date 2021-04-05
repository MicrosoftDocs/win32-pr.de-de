---
title: Client Sicherheit während eines asynchronen Aufrufes
description: Client Sicherheit während eines asynchronen Aufrufes
ms.assetid: 26d1f2c2-cb08-49f1-8beb-b99b029f0d8c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bea2f83bf6341704dd0265a37ec2f64b79e9b2a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712936"
---
# <a name="client-security-during-an-asynchronous-call"></a><span data-ttu-id="d18b0-103">Client Sicherheit während eines asynchronen Aufrufes</span><span class="sxs-lookup"><span data-stu-id="d18b0-103">Client Security During an Asynchronous Call</span></span>

<span data-ttu-id="d18b0-104">Der Proxy-Manager, der von der Mitte für Objekte erstellt wurde, die Standard-Marshalling verwenden, implementiert die [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="d18b0-104">The proxy manager created by MIDL for objects that use standard marshaling implements the [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) interface.</span></span> <span data-ttu-id="d18b0-105">Clients können die Sicherheit von gemarshallten aufrufen durch Abfragen von **IClientSecurity** im Aufruf Objekt und Abrufen oder Ändern von Sicherheitseinstellungen verwalten.</span><span class="sxs-lookup"><span data-stu-id="d18b0-105">Clients can manage the security of marshaled calls by querying for **IClientSecurity** on the call object and obtaining or changing security settings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d18b0-106">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d18b0-106">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d18b0-107">Ausführen eines asynchronen Aufrufes</span><span class="sxs-lookup"><span data-stu-id="d18b0-107">Making an Asynchronous Call</span></span>](making-an-asynchronous-call.md)
</dt> </dl>

 

 




