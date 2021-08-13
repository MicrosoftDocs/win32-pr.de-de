---
description: Wenn Sie die COM-API für WMI verwenden, um lokalisierte Klasseninformationen abzurufen oder zu speichern, geben Sie das Gebietsschema im strLocale-Parameter für die IWbemLocator::ConnectServer-Schnittstelle an.
ms.assetid: 940a7bd9-c2ea-4deb-b5d8-207a0ce7a616
ms.tgt_platform: multiple
title: Abrufen von geänderten Klassen mithilfe der COM-API für WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3752be42a7111e677e7cd60e0bfe9996350f9ae19e7bd0e168d1fa5da82fe42a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118554024"
---
# <a name="retrieving-amended-classes-using-the-com-api-for-wmi"></a>Abrufen von geänderten Klassen mithilfe der COM-API für WMI

Wenn Sie die COM-API für WMI verwenden, um lokalisierte Klasseninformationen abzurufen oder zu speichern, geben Sie das Gebietsschema im *strLocale-Parameter* für die [**IWbemLocator::ConnectServer-Schnittstelle**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) an. Geben Sie beim Lesen oder Schreiben geänderter Klassen an, dass Sie lokalisierte Klassendefinitionen verwenden möchten, indem \_ Sie WBEM-FLAG \_ USE \_ AMENDED \_ QUALIFIERS als Flag für den *iFlags-Parameter* angeben.

In der folgenden Tabelle sind die synchronen und asynchronen Versionen der Methoden aufgeführt, die das \_ WBEM-FLAG \_ USE \_ AMENDED \_ QUALIFIERS-Flag verwenden.



| Synchrone Methode                                                            | Asynchrone Methode                                                                     |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**IWbemServices::CreateClassEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum)       | [**IWbemServices::CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync)       |
| [**IWbemServices::CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum) | [**IWbemServices::CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) |
| [**IWbemServices::ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)                   | [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)                   |
| [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)                   | [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)                   |
| [**IWbemServices::P utClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass)                     | [**IWbemServices::P utClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync)                     |
| [**IWbemServices::P utInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance)               | [**IWbemServices::P utInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)               |



 

 

 



