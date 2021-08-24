---
description: Überlegungen zur COM+-CRM-Sicherheit
ms.assetid: e212c847-b43b-43be-b089-82336551b89a
title: Überlegungen zur COM+-CRM-Sicherheit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1052f9e8cf4f23dd80e2b4706b7e13c0f39a2aedd9b9a985da2d41101118467d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119638730"
---
# <a name="com-crm-security-considerations"></a>Überlegungen zur COM+-CRM-Sicherheit

Eine CRM-Protokolldatei kann vertrauliche Informationen enthalten, die geschützt werden müssen. Aus diesem Grund ist die CRM-Protokolldatei nur für diesen Benutzer geschützt, wenn die Serveranwendung bei der ersten Erstellung der CRM-Protokolldatei unter einer anderen Identität als Interactive User ausgeführt wird. Dieses Feature ist nur im NTFS-Dateisystem verfügbar. Wenn die Identität der Serveranwendung anschließend geändert wird, werden die Sicherheitsinformationen für die CRM-Protokolldatei nicht automatisch geändert. Sie kann manuell mithilfe vorhandener Windows Verwaltungstools geändert werden. Die Alternative besteht einfach darin, die CRM-Protokolldatei zu löschen, wenn sie sich in einem fehlerfreien Zustand befindet (was nach einem kontrollierten Herunterfahren der Serveranwendung erwartet wird).

Im normalen Betrieb erstellt COM+ die CRM-Kompensatorkomponente und ruft die [**ICrmCompensator-Schnittstelle**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator) auf. Allerdings kann ein Benutzer, der über Berechtigungen zum Erstellen des CRM-Kompensators verfügt, die **ICrmCompensator-Schnittstelle** zu unpassenden Zeiten aufrufen, was möglicherweise zu Systemsicherheitsproblemen führt. Zum Schutz vor diesen Sicherheitsproblemen kann der Systemadministrator die rollenbasierte Sicherheit verwenden, um die CRM-Kompensierungskomponente auf die Identitäten der Serveranwendungen zu beschränken, in denen sie ausgeführt wird. Wenn die Komponente in einer Bibliotheksanwendung ausgeführt wird, umfasst dies alle Identitäten der Serveranwendungen.

> [!Note]  
> Ab Windows Server 2003 ist es möglich, ein sichereres System zu gewährleisten, indem Sie die CRM-Kompensatorkomponente als privat markieren, um die Aktivierung von außerhalb der Serveranwendung zu verhindern.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[COM+ Compensating Resource Manager Concepts](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



