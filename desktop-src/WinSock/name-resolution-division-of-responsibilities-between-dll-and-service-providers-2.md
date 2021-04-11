---
title: Namensauflösung für dll-und Dienstanbieter
description: In den folgenden Abschnitten wird beschrieben, wie die \_ von der Winsock-API unterstützten Namensauflösungsdienste von den Ws2-32.dll und den-Namespace Anbietern implementiert werden.
ms.assetid: 25fcb1c2-2d28-41a0-9124-05608f22420f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b527f0849eb441ab7bc8d096c0198d703f2ce337
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958925"
---
# <a name="name-resolution-for-dll-and-service-providers"></a>Namensauflösung für dll-und Dienstanbieter

In den folgenden Abschnitten wird beschrieben, wie die \_ von der Winsock-API unterstützten Namensauflösungsdienste von den Ws2-32.dll und den-Namespace Anbietern implementiert werden.

## <a name="ws2_32dll-functionality-for-name-resolution"></a>Ws2 \_32.dll Funktionen für die Namensauflösung

Der Ws2 \_ -32.dll verwaltet die Registrierung und das Laden von Anforderungen einzelner Namespace Anbieter-DLLs. Er ist auch für das Routing von Namespace Vorgängen aus einer Windows Sockets 2-Anwendung an die entsprechenden Namespace Anbieter zuständig. Diese Zuordnung unterliegt dem Wert der Namespace-und Dienstanbieter-bezeichnerparameter, die in den einzelnen API-Funktionen gefunden werden. Als allgemeine Regel gilt: Wenn auf einen bestimmten Namespace Anbieter verwiesen wird, wird der Vorgang nur an einen identifizierten Anbieter weitergeleitet. Wenn der Namespace Anbieter Bezeichner NULL ist, aber auf einen bestimmten Namespace verwiesen wird, wird der Vorgang an alle Namespace Anbieter weitergeleitet, die den identifizierten Namespace unterstützen. Wenn der Namespace-Anbieter Bezeichner NULL ist und der Namespace Bezeichner als NS all angegeben wird \_ , wird der Vorgang an alle aktiven Namespace Anbieter weitergeleitet.

Im Rahmen des Starts einer Abfrage an einen oder mehrere Dienstanbieter ordnet der Ws2- \_32.dll ein Objekt zu, um den aktuellen Status der Abfrage nachzuverfolgen. Ein undurchsichtiges handle, das dieses Objekt darstellt, wird an die Anwendung zurückgegeben, die die Abfrage gestartet hat. Die Anwendung stellt dieses Handle bei jedem wiederholten Aufrufen einer Anwendungsschnittstellen Funktion als Parameter bereit, um die nächste Dateneinheit abzurufen, die sich aus der Abfrage ergibt.

Als Reaktion auf diese Aufrufe der Anwendungsschnittstellen Prozedur verwendet das Ws2- \_32.dll die im-Objekt gespeicherten Informationen, um die entsprechenden Aufrufe an die an der Abfrage beteiligten Namespace Anbieter vorzunehmen. Der Ws2- \_32.dll aktualisiert die Informationen in seinem Objekt, wenn jeder aufeinander folgende Anwendungsschnittstellen Aufruf auftritt, sodass die entsprechenden Aufrufe von Namespace Anbietern durch alle an der Abfrage beteiligten Namespace Anbieter ordnungsgemäß fortgesetzt werden.

## <a name="namespace-provider-functionality"></a>Funktionalität von Namespace Anbietern

Jeder Namespace Anbieter ist dafür verantwortlich, den Satz von Funktionen, die in der Windows Sockets 2-namens Auflösungs-SPI angezeigt werden, den entsprechenden Transaktionen mit dem unterstützten Namespace zu ordnen. In einigen Fällen besteht dies hauptsächlich darin, den SPI einer beliebigen nativen Schnittstelle für den Namespace zu ordnen. In anderen Fällen muss der Namespace Anbieter Transaktionen mit dem Namespace Anbieter über das Netzwerk ausführen. Einige Namespace Anbieter machen dies durch Aufrufe an die Windows Sockets-API. andere Benutzer verwenden private Schnittstellen zu zugeordneten Transport stapeln.

 

 



