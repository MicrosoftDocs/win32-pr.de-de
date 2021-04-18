---
title: ADSI-Dienstanbieter
description: Dieses Thema enthält eine Übersicht über die ADSI-Dienstanbieter, die auf dem Server bereitgestellt werden.
ms.assetid: 419d7953-a879-4d6c-be74-173d76c3f932
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, Dienstanbieter
- Dienstanbieter ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e44ba4ebc63338bfb38d2b9d5da1f46e51b31aa8
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106340532"
---
# <a name="adsi-service-providers"></a>ADSI-Dienstanbieter

ADSI schließt die in der folgenden Tabelle aufgeführten Dienstanbieter ein.



| Dienstanbieter | BESCHREIBUNG                                                                                | Weitere Informationen finden Sie unter                                      |
|------------------|--------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| LDAP<br/>  | Die Namespace Implementierung ist kompatibel mit dem Lightweight Directory Access Protocol.<br/> | [ADSI-LDAP-Anbieter](adsi-ldap-provider.md)<br/>   |
| WinNT<br/> | Die mit Windows kompatible Namespace Implementierung.<br/>                               | [ADSI WinNT-Anbieter](adsi-winnt-provider.md)<br/> |



 

Andere Dienstanbieter sind als Teil von anderen Produkten als ADSI enthalten. Im folgenden finden Sie die von Microsoft implementierten ADSI-Dienstanbieter.



| Dienstanbieter | Weitere Informationen finden Sie unter                                                                        |
|------------------|---------------------------------------------------------------------------------------------|
| IIS<br/>   | [IIS ADSI-Anbieter Architektur](/previous-versions/iis/6.0-sdk/ms525929(v=vs.90))<br/> |



 

Die von ADSI-Schnittstellen verfügbar gemachten Methoden und Eigenschaften Methoden werden von keinem Dienstanbieter unterstützt. Da unterschiedliche Verzeichnisdienste in den Typen der gespeicherten Objekte und Eigenschaften variieren, verwenden Sie unterschiedliche Protokolle und die Authentifizierung, ADSI ist für die nahtlose Zusammenarbeit mit unterstützten Dienstanbietern konzipiert. Folglich gibt es Schnittstellen, Methoden und Eigenschaften Methoden, die mit einem Dienstanbieter (z. b. LDAP) funktionieren, der möglicherweise nicht auf einem anderen, z. b. WinNT, funktioniert.

Dieser Abschnitt enthält anbieterspezifische Informationen, z. b. das ADsPath-Format, eine Auflistung von ADSI-Objekten, die für diesen Dienstanbieter verwendet werden, sowie Datentyp-und Syntax Informationen für die in ADSI enthaltenen Dienstanbieter. Es gibt auch eine zusammenfassende Beschreibung der ADSI-Schnittstellen, die von jedem in ADSI enthaltenen Anbieter unterstützt werden.

In ADSI sind unterschiedliche Anbieter verschiedenen DLLs zugeordnet. Der LDAP-Anbieter ist Adsldp.dll, Adsldpc.dll und Adsmsext.dll verknüpft. Der WinNT-Anbieter ist Adsnt.dll zugeordnet. Der routeranbieter ist Activeds.dll zugeordnet.

> [!Note]  
> Gehen Sie nicht davon aus, dass die standardmäßigen ADSI-Anbieter Thread sicher sind. Entwickler von Multithreadanwendungen sollten den Zugriff zwischen Threads durch die ordnungsgemäße Verwendung von Synchronisierungs Objekten wie Semaphore, Mutexen, kritischen Abschnitten usw. koordinieren.

 

Weitere Informationen zu ADSI-Dienstanbietern finden Sie unter Unterstützung von ADSI- [Routern](adsi-router.md) und [Anbietern von ADSI-Schnittstellen](provider-support-of-adsi-interfaces.md).

 

