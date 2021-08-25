---
description: Ereignisabfragen werden von temporären Ereignisverbrauchern, permanenten Ereignisverbrauchern und Ereignisanbietern verwendet. Ereignisverbraucher verwenden Ereignisabfragen, um ereignisse anzugeben, die von Interesse sind, und Ereignisanbieter verwenden die Abfragen, um die von ihnen angegebenen Ereignisse anzugeben.
ms.assetid: 851ad9bd-2604-4988-8de0-8d29b5300b21
ms.tgt_platform: multiple
title: Empfangen von Ereignisbenachrichtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1064fd0098ac72c6ceecbb5fcbc212fb38f6b2b25d0e61d8149bdb0fad177267
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996010"
---
# <a name="receiving-event-notifications"></a>Empfangen von Ereignisbenachrichtigungen

Ereignisabfragen werden von temporären Ereignisverbrauchern, permanenten Ereignisverbrauchern und Ereignisanbietern verwendet. Ereignisverbraucher verwenden Ereignisabfragen, um ereignisse anzugeben, die von Interesse sind, und Ereignisanbieter verwenden die Abfragen, um die von ihnen angegebenen Ereignisse anzugeben.

[Temporäre Consumers](receiving-events-for-the-duration-of-your-application.md) platzieren Abfragen in Aufrufen der [**IWbemServices::ExecNotificationQuery-**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) oder [**IWbemServices::ExecNotificationQueryAsync-Methode.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) [Permanente Ereignisverbraucher](receiving-events-at-all-times.md) platzieren Abfragen in der **Query-Eigenschaft** einer Instanz der [**\_ \_ EventFilter-Systemklasse.**](--eventfilter.md)

[Ereignisanbieter verwenden](writing-an-event-provider.md) Ereignisabfragen, um sich zu registrieren, um einen oder mehrere Ereignistypen zu unterstützen. Sie platzieren Abfragen in der **EventQueryList-Eigenschaft** einer Instanz der [**\_ \_ EventProviderRegistration-Systemklasse.**](--eventproviderregistration.md) Alle Ereignisanbieter erstellen eine **\_ \_ EventProviderRegistration-Instanz,** um sich bei der Windows Management Instrumentation (WMI) zu registrieren. Weitere Informationen finden Sie unter [Registrieren eines Ereignisanbieters.](registering-an-event-provider.md)

Ereignisverbraucher und -anbieter verwenden die [SELECT-Anweisung](select-statement-for-event-queries.md) und eine zugehörige WHERE-Klausel für Ereignisabfragen sowie eine Vielzahl von Erweiterungen, die für die WMI Query Language (WQL) spezifisch sind. Die Erweiterungen werden verwendet, um zu verhindern, dass Verbraucher mit Benachrichtigungen überflutet werden, die zu häufig auftreten, um nützlich zu sein.

Benutzer, die bei jedem Auftreten eines Ereignisses keine Benachrichtigung benötigen, können die folgenden Klauseln in ihren Abfragen angeben:

-   [WITHIN-Klausel](within-clause.md)
-   [GROUP-Klausel](group-clause.md)
-   [HAVING-Klausel](having-clause.md)

Die WITHIN- und HAVING-Klauseln wirken sich auf die Zeitlichkeit von Ereignissen aus, und die GROUP-Klausel bewirkt, dass ein repräsentatives Ereignis statt eines häufig auftretenden Ereignisses gesendet wird.

 

 



