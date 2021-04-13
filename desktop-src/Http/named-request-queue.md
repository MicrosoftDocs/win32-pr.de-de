---
title: Benannte Anforderungs Warteschlange
description: Benannte Anforderungs Warteschlange
ms.assetid: d0686a9b-fc3d-4b69-b083-d04b35ce5b50
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4aca045f84fe9f9e4b57365ba8831456f2dc1ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311094"
---
# <a name="named-request-queue"></a>Benannte Anforderungs Warteschlange

Die HTTP Server Version 2,0-API mit der Bezeichnung Anforderungs Warteschlange ermöglicht es, dass mehrere Anwendungen auf die Anforderungs Warteschlange zugreifen können. Die Anforderungs Warteschlange wird anhand des Namens geöffnet und mithilfe von Access Control Listen (ACLs) gesichert, um sicherzustellen, dass Anwendungen nicht auf die Daten anderer Daten zugreifen können. Ein einzelner Prozess erstellt die Anforderungs Warteschlange und erteilt anderen Prozessen die Berechtigung, die Anforderungs Warteschlange zu verwenden. Folglich greifen andere Prozesse auf dem Computer auf die Anforderungs Warteschlange mit den geringsten Berechtigungen zu, die für die Dienst Anforderungen erforderlich sind. Möglicherweise wird der HTTP-Dienst aufgrund von Sicherheitsrisiken in Code von Drittanbietern minimiert, wenn Anwendungen mit geringsten Rechten ausgeführt werden.

Die benannte Anforderungs Warteschlange wird mit der Funktion " [**httpkreaterequestqueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) " erstellt. Wenn die Anforderungs Warteschlange erstellt wird, gibt die Anwendung die ACL im *psecurityattribute* -Parameter an. Die ACL, die nur beim Erstellen der Anforderungs Warteschlange festgelegt werden kann, ermöglicht Workerprozessen das Öffnen der Anforderungs Warteschlange, empfangen von Anforderungen und Senden von Antworten. Standardmäßig ist es nicht zulässig, dass Prozesse eine Anforderungs Warteschlange öffnen, es sei denn, Ihnen wurde eine Berechtigung in der ACL erteilt. Anwendungen benötigen keine Administratorrechte zum Erstellen der Anforderungs Warteschlange.

Die Anforderungs Warteschlange muss mit einem Namen erstellt werden, der im *PName* -Parameter von [**httpkreaterequestqueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) für andere Prozesse angegeben ist, um die Anforderungs Warteschlange zu öffnen. Wenn *PName* **null** ist, wird eine unbenannte Anforderungs Warteschlange erstellt, die von anderen Prozessen nicht geöffnet werden kann.

## <a name="creator-and-controller-processes"></a>Ersteller-und Controller Prozesse

Wenn die Anforderungs Warteschlange erstellt wird, kann Sie von der Anwendung als Controller Prozess oder Ersteller Prozess geöffnet werden. Der Controller und der Ersteller verarbeiten beide als Administratoren für die Anforderungs Warteschlange, aber der Controller führt keine e/a-Vorgänge für ihn aus. Die Anwendung gibt an, dass es sich um einen Controller Prozess handelt, wenn die Anforderungs Warteschlange durch Angabe des **http \_ Create \_ Request \_ Queue \_ \_** -Flags-Controllers im *Flags* -Parameter von [**httpkreaterequestqueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue)erstellt wird. Wenn das Flag " **http \_ Create \_ Request \_ Queue \_ Flag \_ Controller** Flag" nicht festgelegt ist, ist die Anwendung ein Erstellungs Prozess.

Die folgende Liste enthält Tasks, die vom Controller Prozess und dem Ersteller-Prozess ausgeführt werden:

-   Erstellen Sie die Anforderungs Warteschlange und geben Sie den Namen an.
-   Konfigurieren Sie die Anforderungs Warteschlange mithilfe der [**httpabtrequestqueueproperty**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) -Funktion.
-   Fragen Sie die Konfigurationsparameter der Anforderungs Warteschlange mithilfe der [**httpqueryrequestqueueproperty**](/windows/desktop/api/Http/nf-http-httpqueryrequestqueueproperty) -Funktion ab.
-   Erstellen Sie URL-Gruppen und ordnet Sie einer Anforderungs Warteschlange zu.
-   Legen Sie die ACL fest, die die Arbeitsprozesse angibt, für die e/a-Vorgänge in der Anforderungs Warteschlange zulässig sind.
-   [**Httpwaitfordemandstart**](/windows/desktop/api/Http/nf-http-httpwaitfordemandstart) wird aufgerufen, um die Instanziierung von Arbeitsprozessen zu verzögern, bis die erste Anforderung in der Anforderungs Warteschlange eintrifft.

Zusätzlich zu diesen Aufgaben kann der Ersteller-Prozess auch e/a-Vorgänge für die Anforderungs Warteschlange durchführen.

## <a name="worker-processes"></a>Arbeitsprozesse

Ein Arbeitsprozess kann eine vorhandene Anforderungs Warteschlange nur dann öffnen, wenn Ihnen der Zugriff auf die Warteschlange in der ACL gewährt wurde. Arbeitsprozesse, die unter den geringsten Rechten ausgeführt werden, können eine Anforderungs Warteschlange öffnen und e/a-Vorgänge dafür ausführen. Anwendungen öffnen eine vorhandene Anforderungs Warteschlange, indem Sie [**httpcreaterequestqueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) mit dem **http \_ Create \_ Request \_ Queue- \_ Flag \_ \_** , das im *Flags* -Parameter vorhanden ist, und den Namen der Anforderungs Warteschlange im *PName* -Parameter aufrufen.

Der Arbeitsprozess führt die folgenden Funktionen aus:

-   Empfangen von Anforderungen und Senden von Antworten in der Anforderungs Warteschlange.
-   Öffnen Sie eine vorhandene Anforderungs Warteschlange anhand des Namens. Das Handle der Anforderungs Warteschlange, die an den Arbeitsprozess zurückgegeben wird, kann nicht zum Konfigurieren der Anforderungs Warteschlange verwendet werden
-   Fragen Sie die Konfigurationsparameter der Anforderungs Warteschlange ab.

Das folgende Diagramm zeigt das Arbeitsprozess Modell für Anforderungs Warteschlangen. Die Anforderungs Warteschlange kann mehrere Arbeitsprozesse aufweisen, die e/a-Vorgänge verarbeiten, und einen Erstellerprozess, der die Anforderungs Warteschlange konfiguriert.

![Arbeitsprozess Modell für Anforderungs Warteschlangen](images/namedrequestqueue.png)

 

 




