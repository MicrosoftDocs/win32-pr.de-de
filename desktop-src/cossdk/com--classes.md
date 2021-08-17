---
description: Im Folgenden finden Sie die COM+-Klassen.
ms.assetid: 236725f6-16a3-4209-a9e3-a127c1d7243a
title: COM+-Klassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae2cdabc1f4535df6734cf525f288bf6cbd8a93543a9163848815441c9bc384c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129222"
---
# <a name="com-classes"></a>COM+-Klassen

Im Folgenden finden Sie die COM+-Klassen.



| Klasse                                                            | Beschreibung                                                                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AppDomainHelper**](appdomainhelper.md)                       | Bindet ein verwaltetes Objekt an eine Anwendungsdomäne, bei der es sich um eine isolierte Umgebung handelt, in der Anwendungen ausgeführt werden.                                                                                                                           |
| [**ClrAssemblyLocator**](clrassemblylocator.md)                 | Ruft Informationen zu einer Assembly ab, wenn verwalteter Code in der .NET Framework Common Language Runtime verwendet wird.                                                                                                                          |
| [**CServiceConfig**](cserviceconfig.md)                         | Gibt die Dienste an und konfiguriert sie, die in der Dienstdomäne aktiv sein sollen, die beim Aufrufen von [**CoCreateActivity**](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity) oder [**CoEnterServiceDomain eingegeben wird.**](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain)                     |
| [**SecurityCallContext**](securitycallcontext.md)               | Ermöglicht den Zugriff auf den Sicherheitskontext des aktuellen Aufrufs, der Informationen zu den Aufrufern eines Objekts enthält.                                                                                                                           |
| [**SecurityCallers**](securitycallers.md)                       | Bietet Zugriff auf Informationen zu einzelnen Aufrufern in einer Auflistung von Aufrufern. Die Auflistung stellt die Kette der Aufrufe dar, die mit dem aktuellen Aufruf enden, und jeder Aufrufer in der Auflistung stellt die Identität eines Aufrufers dar. |
| [**SecurityIdentity**](securityidentity.md)                     | Ermöglicht den Zugriff auf eine Auflistung von Sicherheitsinformationen, die die Identität eines Aufrufers darstellen. Mit dieser Klasse können Sie einen bestimmten Aufrufer in einer Kette von Aufrufern herausfinden, die Teil des Sicherheitsaufrufkontexts ist.                 |
| [**SharedProperty**](sharedproperty.md)                         | Legt den Wert einer freigegebenen Eigenschaft fest oder ruft sie ab.                                                                                                                                                                                       |
| [**SharedPropertyGroup**](sharedpropertygroup.md)               | Erstellt die freigegebenen Eigenschaften in einer freigegebenen Eigenschaftengruppe und greifen auf sie zu.                                                                                                                                                                  |
| [**SharedPropertyGroupManager**](sharedpropertygroupmanager.md) | Erstellt freigegebene Eigenschaftengruppen und , um Zugriff auf vorhandene freigegebene Eigenschaftengruppen zu erhalten.                                                                                                                                                 |
| [**TransactionContext**](transactioncontext.md)                 | Erstellt ein generisches Transaktionsobjekt, das eine Transaktion startet.                                                                                                                                                                       |
| [**TransactionContextEx**](transactioncontextex.md)             | Erstellt ein generisches Transaktionsobjekt, das eine Transaktion startet. Durch Aufrufen der Methoden dieser Klasse können Sie die Arbeit mehrerer COM-Objekte in einer einzelnen Transaktion zusammenstellen und die Transaktion explizit commiten oder abbrechen.        |



 

 

 



