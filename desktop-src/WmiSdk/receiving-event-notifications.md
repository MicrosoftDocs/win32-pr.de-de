---
description: Ereignis Abfragen werden von temporären Ereignisverbrauchern, permanenten Ereignisconsumern und Ereignis Anbietern verwendet. Ereignisconsumer verwenden Ereignis Abfragen, um relevante Ereignisse anzugeben, und Ereignis Anbieter verwenden die Abfragen, um die von Ihnen bereitgestellten Ereignisse anzugeben.
ms.assetid: 851ad9bd-2604-4988-8de0-8d29b5300b21
ms.tgt_platform: multiple
title: Empfangen von Ereignis Benachrichtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43873c03155f2186f9d3a9a3daff9b8e322e511f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347070"
---
# <a name="receiving-event-notifications"></a>Empfangen von Ereignis Benachrichtigungen

Ereignis Abfragen werden von temporären Ereignisverbrauchern, permanenten Ereignisconsumern und Ereignis Anbietern verwendet. Ereignisconsumer verwenden Ereignis Abfragen, um relevante Ereignisse anzugeben, und Ereignis Anbieter verwenden die Abfragen, um die von Ihnen bereitgestellten Ereignisse anzugeben.

[Temporäre](receiving-events-for-the-duration-of-your-application.md) Consumer platzieren Abfragen in Aufrufen der Methode [**IWbemServices:: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) oder [**IWbemServices:: ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) . [Permanente](receiving-events-at-all-times.md) [**\_ \_ Ereignisconsumer**](--eventfilter.md) platzieren Abfragen in der **Query** -Eigenschaft einer Instanz der EventFilter-System Klasse.

[Ereignis Anbieter](writing-an-event-provider.md) verwenden Ereignis Abfragen, um sich zu registrieren, um einen oder mehrere Ereignis Typen zu unterstützen. Sie platzieren Abfragen in der **EventQueryList** -Eigenschaft einer Instanz der [**\_ \_ eventproviderregistration**](--eventproviderregistration.md) -System Klasse. Alle Ereignis Anbieter erstellen eine **\_ \_ eventproviderregistration** -Instanz, um sich bei Windows-Verwaltungsinstrumentation (WMI) zu registrieren. Weitere Informationen finden Sie unter [Registrieren eines Ereignis Anbieters](registering-an-event-provider.md).

Ereignisconsumer und-Anbieter verwenden die [SELECT-Anweisung](select-statement-for-event-queries.md) und eine verwandte WHERE-Klausel für Ereignis Abfragen sowie eine Vielzahl von Erweiterungen, die für die WMI Query Language (WQL) spezifisch sind. Die Erweiterungen werden verwendet, um zu verhindern, dass Consumer mit Benachrichtigungen überflutet werden, die zu häufig vorkommen, damit Sie hilfreich sind.

Consumer, die bei Auftreten eines Ereignisses keine Benachrichtigung benötigen, können in Ihren Abfragen die folgenden Klauseln angeben:

-   [Within](within-clause.md) -Klausel
-   [Group](group-clause.md) -Klausel
-   [Hat](having-clause.md) -Klausel

Die in-und-Klauseln beeinflussen die zeitliche Steuerung von Ereignissen, und die Group-Klausel bewirkt, dass ein repräsentatives Ereignis anstelle eines häufig auftretenden Ereignisses gesendet wird.

 

 



