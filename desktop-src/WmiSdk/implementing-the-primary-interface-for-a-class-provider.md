---
description: 'Es gibt zwei Möglichkeiten, einen Klassenanbieter zu implementieren: implementieren Sie die Schnittstelle als Pushanbieter oder als Pullanbieter.'
ms.assetid: 2c6d3f73-e219-409b-9347-492035c1eb9f
ms.tgt_platform: multiple
title: Implementieren der primären Schnittstelle für einen Klassenanbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3ef1b31e1228b832e4d23945f3af0c4df223ddd3edebdd1ec6e34e0e0e8d449
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030440"
---
# <a name="implementing-the-primary-interface-for-a-class-provider"></a>Implementieren der primären Schnittstelle für einen Klassenanbieter

Es gibt zwei Möglichkeiten, einen Klassenanbieter zu implementieren: implementieren Sie die Schnittstelle als Pushanbieter oder als Pullanbieter.

In diesem Thema werden die folgenden Abschnitte erläutert:

-   [Implementieren der primären Schnittstelle für einen Pushklassenanbieter](#implementing-the-primary-interface-for-a-push-class-provider)
-   [Implementieren der primären Schnittstelle für einen Pullklassenanbieter](#implementing-the-primary-interface-for-a-pull-class-provider)

## <a name="implementing-the-primary-interface-for-a-push-class-provider"></a>Implementieren der primären Schnittstelle für einen Pushklassenanbieter

Während alle Anbieter [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) für die Initialisierung und mindestens eine andere Schnittstelle als primäre Schnittstelle implementieren, implementiert ein Pushanbieter nur **IWbemProviderInit**.

Stellen Sie sicher, dass Ihre Implementierung die folgenden Aufgaben ausführt:

-   Ruft die entsprechenden Klassendaten ab.
-   Platziert die Daten im WMI-Repository.
-   Löscht veraltete Daten.

Nach Abschluss des Initialisierungsprozesses verarbeitet WMI alle Anwendungsanforderungen für Klassen, die zum Pushanbieter gehören, ohne weitere Anbieterinteraktion. Anschließend fungiert der Pushanbieter effektiv als WMI-Client und nicht als Anbieter. Weitere Informationen zum Implementieren von [**IWbemProviderInit finden**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit)Sie unter [Initialisieren eines Anbieters.](initializing-a-provider.md)

> [!Note]  
> Legen Sie beim Aufrufen von WMI zum Erstellen, Aktualisieren oder Entfernen von Daten in einem Pushanbieter den *Parameter lFlags* so fest, dass er das **WBEM \_ FLAG OWNER \_ \_ UPDATE-Flag** in alle Aufrufe von [**IWbemServices-Methoden eingibt.**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)

 

## <a name="implementing-the-primary-interface-for-a-pull-class-provider"></a>Implementieren der primären Schnittstelle für einen Pullklassenanbieter

Ein Klassen-Pullanbieter sollte [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) als primäre Schnittstelle implementieren. Die **IWbemServices-Schnittstelle** unterstützt den Datenabruf, die Datenaktualisierung, das Entfernen von Daten, die Enumeration und die Abfrageverarbeitung. Da **IWbemServices jedoch** auch von Anwendungen und Anbietern zum Anfordern von WMI-Diensten verwendet wird, enthält **IWbemServices** viele Methoden, die für einen Klassenanbieter irrelevant sind. Ihre Implementierung muss den Klassenabruf und die -Enumeration über die [**Methoden GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) bzw. [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) unterstützen. In der folgenden Tabelle sind die zusätzlichen **asynchronen IWbemServices-Methoden** aufgeführt, die Sie für einen Klassenanbieter implementieren können.



| Methode                                                     | Komponente      |
|------------------------------------------------------------|--------------|
| [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) | Modifikation (Modification) |
| [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) | Löschen     |



 

> [!Note]  
> Da der Rückruf an die Senke möglicherweise nicht auf derselben Authentifizierungsebene zurückgegeben wird, wie der Client erfordert, wird empfohlen, anstelle der asynchronen Kommunikation semisynchrone zu verwenden. Weitere Informationen finden Sie unter [Aufrufen einer Methode.](calling-a-method.md)

 

Ihr Klassenanbieter sollte eine Stubimplementierung bieten, die **WBEM \_ E PROVIDER NOT \_ \_ \_ CAPABLE** für alle anderen [**IWbemServices-Methoden**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) zurückgibt, die Ihren Featuresatz nicht unterstützen. Insbesondere unterstützt WMI keine Abfrageverarbeitung für Klassenanbieter. Daher muss ein Klassenanbieter **WBEM \_ E PROVIDER NOT \_ \_ \_ CAPABLE** aus seiner Implementierung von [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)zurückgeben, seine **QuerySupportLevels-Registrierungseigenschaft** auf **NULL** oder beides festlegen.

Die Schnittstellen, die ein Klassenanbieter implementiert, sind den Schnittstellen für einen Instanzanbieter und einen Methodenanbieter sehr ähnlich. Tatsächlich kann ein einzelner Anbieter als alle drei Anbietertypen fungieren, indem er alle Methoden implementieren und sich ordnungsgemäß registriert.

 

 



