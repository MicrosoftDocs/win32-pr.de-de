---
title: Benannte Anforderungswarteschlange
description: Benannte Anforderungswarteschlange
ms.assetid: d0686a9b-fc3d-4b69-b083-d04b35ce5b50
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d2174044f23f30470f3285e3c8fcf9bd2dbd474b10c306df7f2fbb215b992eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078344"
---
# <a name="named-request-queue"></a>Benannte Anforderungswarteschlange

Das Feature für die benannte Anforderungswarteschlange der HTTP Server-API Version 2.0 ermöglicht mehreren Anwendungen, die unter separaten Prozessen und Benutzerkonten ausgeführt werden, Zugriff auf die Anforderungswarteschlange. Die Anforderungswarteschlange wird anhand des Namens geöffnet und mithilfe von Access Control Lists (ACLs) geschützt, um sicherzustellen, dass Anwendungen nicht auf andere Daten zugreifen können. Ein einzelner Prozess erstellt die Anforderungswarteschlange und gewährt anderen Prozessen die Berechtigung zur Verwendung der Anforderungswarteschlange. Daher greifen andere Prozesse auf dem Computer mit den geringsten Berechtigungen auf die Anforderungswarteschlange zu, die zum Warten von Anforderungen erforderlich sind. Mögliche Schäden am HTTP-Dienst aufgrund von Sicherheitsrisiken im Code von Drittanbietern werden minimiert, wenn Anwendungen mit den geringsten Berechtigungen ausgeführt werden.

Die benannte Anforderungswarteschlange wird mit der [**HttpCreateRequestQueue-Funktion**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) erstellt. Wenn die Anforderungswarteschlange erstellt wird, gibt die Anwendung die ACL im *pSecurityAttribute-Parameter* an. Die ACL, die nur festgelegt werden kann, wenn die Anforderungswarteschlange erstellt wird, ermöglicht Es Workerprozessen, die Anforderungswarteschlange zu öffnen, Anforderungen zu empfangen und Antworten zu senden. Standardmäßig dürfen Prozesse keine Anforderungswarteschlange öffnen, es sei denn, ihnen wurde die Berechtigung in der ACL erteilt. Anwendungen benötigen keine Administratorrechte, um die Anforderungswarteschlange zu erstellen.

Die Anforderungswarteschlange muss mit einem Namen erstellt werden, der im *pName-Parameter* von [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) angegeben ist, damit andere Prozesse die Anforderungswarteschlange öffnen können. Wenn *pName* **NULL ist,** wird eine unbenannte Anforderungswarteschlange erstellt, und andere Prozesse können sie nicht öffnen.

## <a name="creator-and-controller-processes"></a>Ersteller- und Controllerprozesse

Wenn die Anforderungswarteschlange erstellt wird, kann die Anwendung sie als Controllerprozess oder Erstellerprozess öffnen. Sowohl der Controller als auch der Erstellerprozess fungieren als Administratoren für die Anforderungswarteschlange, aber der Controller führt keine E/A-Vorgänge dafür aus. Die Anwendung gibt an, dass es sich um einen Controllerprozess handelt, wenn die Anforderungswarteschlange erstellt wird, indem **HTTP CREATE REQUEST QUEUE FLAG \_ \_ \_ \_ \_ CONTROLLER** im *Flags-Parameter* von [**HttpCreateRequestQueue angegeben wird.**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) Wenn das **Flag HTTP CREATE REQUEST QUEUE FLAG \_ \_ \_ \_ \_ CONTROLLER** nicht festgelegt ist, ist die Anwendung ein Erstellerprozess.

Die folgende Liste enthält Aufgaben, die vom Controllerprozess und vom Erstellerprozess ausgeführt werden:

-   Erstellen Sie die Anforderungswarteschlange, und geben Sie den Namen an.
-   Konfigurieren Sie die Anforderungswarteschlange mithilfe der [**HttpSetRequestQueueProperty-Funktion.**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty)
-   Fragen Sie die Konfigurationsparameter der Anforderungswarteschlange mithilfe der [**HttpQueryRequestQueueProperty-Funktion**](/windows/desktop/api/Http/nf-http-httpqueryrequestqueueproperty) ab.
-   Erstellen Sie URL-Gruppen, und ordnet sie einer Anforderungswarteschlange zu.
-   Legen Sie die ACL fest, die die Arbeitsprozesse an, die E/A-Vorgänge in der Anforderungswarteschlange empfangen dürfen.
-   Rufen [**Sie HttpWaitForDemandStart auf,**](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) um die Instanziierung von Workerprozessen zu verzögern, bis die erste Anforderung in der Anforderungswarteschlange eintrifft.

Zusätzlich zu diesen Aufgaben kann der Erstellerprozess auch E/A-Vorgänge für die Anforderungswarteschlange ausführen.

## <a name="worker-processes"></a>Arbeitsprozesse

Ein Workerprozess kann eine vorhandene Anforderungswarteschlange nur öffnen, wenn ihnen in der ACL Zugriff darauf gewährt wurde. Workerprozesse, die mit den geringsten Berechtigungen ausgeführt werden, können eine Anforderungswarteschlange öffnen und E/A-Vorgänge für sie ausführen. Anwendungen öffnen eine vorhandene Anforderungswarteschlange, indem sie [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) mit dem **HTTP CREATE REQUEST QUEUE FLAG OPEN \_ \_ \_ \_ \_ \_ EXISTING** im Flags-Parameter und dem Namen der *Anforderungswarteschlange* im *pName-Parameter* aufrufen.

Der Workerprozess führt die folgenden Funktionen aus:

-   Empfangen von Anforderungen und Senden von Antworten in der Anforderungswarteschlange.
-   Öffnen Sie eine vorhandene Anforderungswarteschlange nach Namen. Das Handle für die Anforderungswarteschlange, die an den Arbeitsprozess zurückgegeben wird, kann nicht zum Konfigurieren der Anforderungswarteschlange verwendet werden.
-   Fragen Sie die Konfigurationsparameter der Anforderungswarteschlange ab.

Das folgende Diagramm zeigt das Arbeitsprozessmodell für Anforderungswarteschlangen. Die Anforderungswarteschlange kann über mehrere Arbeitsprozesse verfügen, die E/A verarbeiten, und ein Ersteller verarbeitet, der die Anforderungswarteschlange konfiguriert.

![Workerprozessmodell für Anforderungswarteschlangen](images/namedrequestqueue.png)

 

 




