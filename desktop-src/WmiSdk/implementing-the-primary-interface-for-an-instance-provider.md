---
title: Implementieren der primären Schnittstelle eines Instanzanbieters
description: Ein Instanzanbieter verwendet die asynchronen Methoden von IWbemServices als primäre Schnittstelle zu WMI.
ms.assetid: 80425fa8-2746-4eba-8e7d-4a61e222852a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 443b095cfbb134cf031ae8e1403565bc1fa31aea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360695"
---
# <a name="implementing-an-instance-provider-primary-interface"></a>Implementieren der primären Schnittstelle eines Instanzanbieters

Ein Instanzanbieter verwendet die asynchronen Methoden von [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) als primäre Schnittstelle zu WMI. Indem nur die Methoden implementiert werden, die die Anforderungen Ihres Instanzanbieters erfüllen, können Sie die Menge der Ressourcen verringern, die Sie codieren. Durch Implementieren von Methoden, die für andere Anbieter Typen reserviert sind, können Sie jedoch die Anzahl der von Ihnen geschriebenen Anbieter reduzieren.

Da es auch von Anwendungen und Anbietern verwendet wird, um Dienste von WMI anzufordern, enthält [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) viele Methoden, die für einen Instanzanbieter irrelevant sind. In der folgenden Tabelle sind die **IWbemServices** -Methoden aufgelistet, die Sie für einen Instanzanbieter implementieren können.



| Methode                                                                   | Funktion          |
|--------------------------------------------------------------------------|------------------|
| [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)                   | Auslagerung        |
| [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)               | Modifikation (Modification)     |
| [**Delta einstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync)         | Löschen         |
| [**"Kreateingestanceenumasync"**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) | Enumeration      |
| [**ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)                   | Abfrageverarbeitung |



 

Für Methoden, die Sie nicht verwenden, kann der Anbieter eine Stubimplementierung bereitstellen, die den **WBEM \_ E- \_ Anbieter \_ nicht \_** unterstützt. Dies schließt alle [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) -Methoden ein, die nicht in der obigen Tabelle aufgeführt sind.

Ein einzelner Anbieter kann durch ordnungsgemäße Registrierung und Implementierung aller relevanten Methoden gleichzeitig als Klasse, Instanz und Methoden Anbieter agieren. Weitere Informationen finden Sie unter [Schreiben eines Klassen Anbieters](writing-a-class-provider.md) und [Schreiben eines Methoden Anbieters](writing-a-method-provider.md).

 

 



