---
description: 'Wenn Sie die com-API für WMI verwenden, um lokalisierte Klassen Informationen abzurufen oder zu speichern, geben Sie das Gebiets Schema im Parameter "strinlocale" an die IWbemLocator:: ConnectServer-Schnittstelle an.'
ms.assetid: 940a7bd9-c2ea-4deb-b5d8-207a0ce7a616
ms.tgt_platform: multiple
title: Abrufen von geänderten Klassen mithilfe der com-API für WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0178b0b99de2b666e2f497074a02b02c49ba400
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759762"
---
# <a name="retrieving-amended-classes-using-the-com-api-for-wmi"></a>Abrufen von geänderten Klassen mithilfe der com-API für WMI

Wenn Sie die com-API für WMI verwenden, um lokalisierte Klassen Informationen abzurufen oder zu speichern, geben Sie das Gebiets Schema im Parameter " *strinlocale* " an die [**IWBEMLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) -Schnittstelle an. Beim Lesen oder Schreiben von geänderten Klassen geben Sie an, dass Sie lokalisierte Klassendefinitionen verwenden möchten, indem Sie das WBEM- \_ Flag \_ zum Verwenden von \_ geänderten \_ *Qualifizierern* als Flag für den IFlags-Parameter angeben.

In der folgenden Tabelle werden die synchronen und asynchronen Versionen der Methoden aufgelistet, die mit dem WBEM-Flag das Flag für \_ \_ \_ geänderte \_ Qualifizierer verwenden.



| Synchrone Methode                                                            | Asynchrone Methode                                                                     |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**IWbemServices:: kreateclassenum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum)       | [**IWbemServices:: "kreateclassenumschlag"**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync)       |
| [**IWbemServices:: kreateinstanceaufumum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum) | [**IWbemServices:: kreateingestanceenumasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) |
| [**IWbemServices:: ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)                   | [**IWbemServices:: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)                   |
| [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)                   | [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)                   |
| [**IWbemServices::P utclass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass)                     | [**IWbemServices::P utclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync)                     |
| [**IWbemServices::P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance)               | [**IWbemServices::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)               |



 

 

 



