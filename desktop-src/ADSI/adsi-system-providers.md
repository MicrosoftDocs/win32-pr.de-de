---
title: ADSI-Dienstanbieter
description: Dieses Thema bietet eine Übersicht über die ADSI-Dienstanbieter, die auf dem Server bereitgestellt werden.
ms.assetid: 419d7953-a879-4d6c-be74-173d76c3f932
ms.tgt_platform: multiple
keywords:
- ADSI ADSI , Dienstanbieter
- Dienstanbieter ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e66b90aad4e9fa1a6cf6a2229910257f018a411aa7b11b9accca6fcf96dce39b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962202"
---
# <a name="adsi-service-providers"></a>ADSI-Dienstanbieter

ADSI enthält die in der folgenden Tabelle aufgeführten Dienstanbieter.



| Dienstanbieter | BESCHREIBUNG                                                                                | Weitere Informationen finden Sie unter                                      |
|------------------|--------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| LDAP<br/>  | Namespaceimplementierung, die mit dem Lightweight Directory Access Protocol kompatibel ist.<br/> | [ADSI-LDAP-Anbieter](adsi-ldap-provider.md)<br/>   |
| Winnt<br/> | Namespaceimplementierung, die mit Windows.<br/>                               | [ADSI WinNT-Anbieter](adsi-winnt-provider.md)<br/> |



 

Andere Dienstanbieter sind als Produkte enthalten, die nicht ADSI sind. Im Folgenden finden Sie die ADSI-Dienstanbieter, die von Microsoft implementiert werden.



| Dienstanbieter | Weitere Informationen finden Sie unter                                                                        |
|------------------|---------------------------------------------------------------------------------------------|
| IIS<br/>   | [ARCHITEKTUR DES IIS ADSI-Anbieters](/previous-versions/iis/6.0-sdk/ms525929(v=vs.90))<br/> |



 

Die Methoden und Eigenschaftenmethoden, die von ADSI-Schnittstellen verfügbar gemacht werden, werden nicht von jedem Dienstanbieter unterstützt. Da verschiedene Verzeichnisdienste in den Typen der gespeicherten Objekte und Eigenschaften variieren, unterschiedliche Protokolle und Authentifizierung verwenden, ist ADSI für die nahtlose Zusammenarbeit mit unterstützten Dienstanbietern konzipiert. Daher gibt es Schnittstellen, Methoden und Eigenschaftenmethoden, die mit einem Dienstanbieter wie LDAP zusammenarbeiten, die möglicherweise nicht auf einem anderen Wie z. B. WinNT funktionieren.

Dieser Abschnitt enthält anbieterspezifische Informationen, z. B. das ADsPath-Format, eine Auflistung der ADSI-Objekte, die für diesen Dienstanbieter verwendet werden, sowie Datentyp- und Syntaxinformationen für die in ADSI enthaltenen Dienstanbieter. Es gibt auch eine zusammenfassende Beschreibung der ADSI-Schnittstellen, die von jedem Anbieter unterstützt werden, der in ADSI enthalten ist.

In ADSI sind verschiedene Anbieter verschiedenen DLLs zugeordnet. Der LDAP-Anbieter ist Adsldp.dll, Adsldpc.dll und Adsmsext.dll. Der WinNT-Anbieter ist dem Adsnt.dll. Der ROUTER-Anbieter ist dem Activeds.dll.

> [!Note]  
> Gehen Sie nicht davon aus, dass ADSI-Standardanbieter threadsicher sind. Multithreadanwendungsentwickler sollten den Zugriff zwischen Threads über die ordnungsgemäße Verwendung von Synchronisierungsobjekten wie Semaphoren, Mutexen, kritischen Abschnitten und so weiter koordinieren.

 

Weitere Informationen zu ADSI-Dienstanbietern finden Sie unter ADSI Router and Provider Support of ADSI interfaces [(ADSI-Router](adsi-router.md) und [Anbieterunterstützung von ADSI-Schnittstellen).](provider-support-of-adsi-interfaces.md)

 

