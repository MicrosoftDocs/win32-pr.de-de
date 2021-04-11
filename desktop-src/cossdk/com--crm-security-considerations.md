---
description: Com+ CRM-Sicherheitsüberlegungen
ms.assetid: e212c847-b43b-43be-b089-82336551b89a
title: Com+ CRM-Sicherheitsüberlegungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2ababde9f31c0c2655fbf4f0c46b216ca0cbfee
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126356"
---
# <a name="com-crm-security-considerations"></a>Com+ CRM-Sicherheitsüberlegungen

Eine CRM-Protokolldatei kann vertrauliche Informationen enthalten, die gesichert werden müssen. Wenn die Serveranwendung unter einer anderen Identität als interaktiver Benutzer ausgeführt wird, wenn die CRM-Protokolldatei erstmalig erstellt wird, ist die CRM-Protokolldatei nur für diesen Benutzer Sicherheits geschützt. Diese Funktion ist nur im NTFS-Dateisystem verfügbar. Wenn die Identität der Serveranwendung anschließend geändert wird, werden die Sicherheitsinformationen für die CRM-Protokolldatei nicht automatisch geändert. Sie kann mithilfe vorhandener Windows-Verwaltungs Tools manuell geändert werden. Die Alternative besteht darin, die CRM-Protokolldatei zu löschen, wenn Sie sich in einem fehlerfreien Zustand befindet (Dies wird nach einem kontrollierten Herunterfahren der Serveranwendung erwartet).

Im normalen Betrieb erstellt com+ die CRM-kompenatorkomponente und ruft die [**icrmcompensator**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator) -Schnittstelle auf. Ein Benutzer, der über Berechtigungen zum Erstellen des CRM-Kompensierungs Diensts verfügt, kann jedoch die **icrmcompensator** -Schnittstelle zu unangemessenen Zeiten aufrufen, was möglicherweise System Sicherheitsprobleme verursacht. Um diese Sicherheitsprobleme zu schützen, kann der Systemadministrator mithilfe der rollenbasierten Sicherheit die CRM-kompenatorkomponente auf die Identitäten der Server Anwendungen beschränken, in denen Sie ausgeführt wird. Wenn die Komponente in einer Bibliotheks Anwendung ausgeführt wird, würde dies alle Identitäten der Server Anwendungen einschließen.

> [!Note]  
> Ab Windows Server 2003 ist es möglich, ein sicheres System sicherzustellen, indem die CRM-kompenatorkomponente als privat gekennzeichnet wird, um die Aktivierung von außerhalb der Server Anwendung zu verhindern.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kompensierende com+-Ressourcen-Manager Konzepte](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



