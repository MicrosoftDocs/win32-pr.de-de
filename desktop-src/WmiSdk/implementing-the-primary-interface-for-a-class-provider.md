---
description: 'Es gibt zwei Möglichkeiten zum Implementieren eines Klassen Anbieters: Implementieren Sie die-Schnittstelle als pushanbieter oder als Pull-Anbieter.'
ms.assetid: 2c6d3f73-e219-409b-9347-492035c1eb9f
ms.tgt_platform: multiple
title: Implementieren der primären Schnittstelle für einen Klassen Anbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f760dba053cadf56d37445c997fc52a99b242a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346728"
---
# <a name="implementing-the-primary-interface-for-a-class-provider"></a>Implementieren der primären Schnittstelle für einen Klassen Anbieter

Es gibt zwei Möglichkeiten zum Implementieren eines Klassen Anbieters: Implementieren Sie die-Schnittstelle als pushanbieter oder als Pull-Anbieter.

In diesem Thema werden die folgenden Abschnitte erläutert:

-   [Implementieren der primären Schnittstelle für einen Push-Klassen Anbieter](#implementing-the-primary-interface-for-a-push-class-provider)
-   [Implementieren der primären Schnittstelle für einen Pull-Klassen Anbieter](#implementing-the-primary-interface-for-a-pull-class-provider)

## <a name="implementing-the-primary-interface-for-a-push-class-provider"></a>Implementieren der primären Schnittstelle für einen Push-Klassen Anbieter

Während alle Anbieter [**iwbemproviderinit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) für die Initialisierung und mindestens eine andere Schnittstelle als primäre Schnittstelle implementieren, implementiert ein Push-Anbieter nur **iwbemproviderinit**.

Stellen Sie sicher, dass Ihre-Implementierung die folgenden Aufgaben ausführt:

-   Ruft die entsprechenden Klassen Daten ab.
-   Platziert die Daten im WMI-Repository.
-   Löscht veraltete Daten.

Nach Abschluss des Initialisierungs Vorgangs verarbeitet WMI alle Anwendungsanforderungen für Klassen, die zum Push-Anbieter gehören, ohne dass weitere Anbieter Interaktionen vorhanden sind. Danach fungiert der Push-Anbieter effektiv als Client von WMI anstelle eines Anbieters. Weitere Informationen zum Implementieren von [**iwbemproviderinit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit)finden Sie unter [Initialisieren eines Anbieters](initializing-a-provider.md).

> [!Note]  
> Wenn Sie WMI aufrufen, um Daten in einem Push-Anbieter zu erstellen, zu aktualisieren oder zu entfernen, legen Sie den *lFlags* -Parameter so fest, dass in allen Aufrufen von [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Methoden das kennflag für das **\_ \_ Besitzer \_ Update von WBEM**

 

## <a name="implementing-the-primary-interface-for-a-pull-class-provider"></a>Implementieren der primären Schnittstelle für einen Pull-Klassen Anbieter

Ein Pull-Anbieter für die Klasse sollte [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) als primäre Schnittstelle implementieren. Die **IWbemServices** -Schnittstelle unterstützt Datenabruf, Datenaktualisierung, Entfernen von Daten, Enumeration und Abfrage Verarbeitung. Da **IWbemServices** jedoch auch von Anwendungen und Anbietern verwendet wird, um Dienste von WMI anzufordern, enthält **IWbemServices** viele Methoden, die für einen Klassen Anbieter irrelevant sind. Ihre-Implementierung muss den Abruf und die Enumeration der Klasse über die [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) [**-Methode und**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) die-Methode der Methode "die Methode" ". In der folgenden Tabelle sind die zusätzlichen asynchronen **IWbemServices** -Methoden aufgelistet, die Sie für einen Klassen Anbieter implementieren können.



| Methode                                                     | Funktion      |
|------------------------------------------------------------|--------------|
| [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) | Modifikation (Modification) |
| [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) | Löschen     |



 

> [!Note]  
> Da der Rückruf für die Senke möglicherweise nicht auf derselben Authentifizierungs Ebene wie der Client zurückgegeben wird, wird empfohlen, semisynchrone anstelle der asynchronen Kommunikation zu verwenden. Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).

 

Der Klassen Anbieter sollte eine Stub-Implementierung bereitstellen, die den WBEM E-Anbieter zurückgibt, der nicht für alle anderen [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Methoden **\_ \_ \_ \_ geeignet ist** , die die Funktionsgruppe nicht unterstützen. WMI unterstützt insbesondere keine Abfrage Verarbeitung für Klassen Anbieter. Daher muss ein Klassen Anbieter den **WBEM E- \_ \_ Anbieter \_ \_** zurückgeben, der aus der Implementierung [**von IWbemServices:: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)nicht kompatibel ist, seine **querysupportlevels** -Registrierungs Eigenschaft auf **null** oder beides festgelegt hat.

Die Schnittstellen, die von einem Klassen Anbieter implementiert werden, ähneln den Schnittstellen für einen Instanzanbieter und einen Methoden Anbieter. Tatsächlich kann ein einzelner Anbieter als alle drei Typen von Anbietern fungieren, indem er alle Methoden implementiert und ordnungsgemäß registriert wird.

 

 



