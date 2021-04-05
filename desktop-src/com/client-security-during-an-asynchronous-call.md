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
# <a name="client-security-during-an-asynchronous-call"></a>Client Sicherheit während eines asynchronen Aufrufes

Der Proxy-Manager, der von der Mitte für Objekte erstellt wurde, die Standard-Marshalling verwenden, implementiert die [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) -Schnittstelle. Clients können die Sicherheit von gemarshallten aufrufen durch Abfragen von **IClientSecurity** im Aufruf Objekt und Abrufen oder Ändern von Sicherheitseinstellungen verwalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ausführen eines asynchronen Aufrufes](making-an-asynchronous-call.md)
</dt> </dl>

 

 




