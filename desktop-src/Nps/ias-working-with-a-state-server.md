---
title: Arbeiten mit einem Zustands Server
description: NPS führt die Authentifizierung mithilfe einer Datenbank durch, die auf der NPS-Serversite konfiguriert ist.
ms.assetid: 8313ba91-5ed1-44d0-80db-cfb82c641100
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d79ff46802d53109c7bb8b40fe3a2db2480949e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106341940"
---
# <a name="working-with-a-state-server"></a>Arbeiten mit einem Zustands Server

> [!Note]  
> Der Internet Authentifizierungsdienst (IAS) wurde ab Windows Server 2008 in den Netzwerk Richtlinien Server (Network Policy Server, NPS) umbenannt. Der Inhalt dieses Themas gilt sowohl für IAS als auch für NPS. Im gesamten Text wird NPS verwendet, um auf alle Versionen des Dienstanbieter zu verweisen, einschließlich der Versionen, die ursprünglich als IAS bezeichnet wurden.

 

NPS führt die Authentifizierung mithilfe einer Datenbank durch, die auf der NPS-Serversite konfiguriert ist. Bei dieser Authentifizierungs Datenbank kann es sich um die Benutzerdatenbank für eine Windows-Domäne oder um die Benutzerinformationen handeln, die Sie aus dem Windows-Active Directory abgerufen haben. Das folgende Diagramm veranschaulicht eine typische Konfiguration, die zeigt, wie NPS mit Authentifizierungs Datenbanken interagiert, z. b. eine Windows-Domänen Benutzerdatenbank oder Active Directory. Das Diagramm zeigt auch, wie NPS mit einem Zustands Server interagieren kann, der von einem Drittanbieter bereitgestellt wird. Der Hauptzweck eines Zustands Servers besteht darin, die Anzahl der gleichzeitigen Anmelde Sitzungen einzuschränken, die ein einzelner Benutzer ausführen kann.

![NPS-Interaktion mit Zustands Server-und Authentifizierungs Datenbanken](images/ias02.png)

Es gibt zwei Aspekte der Interaktion zwischen NPS und dem Zustands Server. Eine Interaktion findet statt, wenn NPS eine Authentifizierungsanforderung vom NAS empfängt. Der Zustands Server stellt Informationen aus seiner Datenbank bereit, um zu bestimmen, ob die Anforderung akzeptiert oder verweigert werden soll. Die andere Interaktion findet statt, wenn NPS Buchhaltungs Anforderungen vom NAS empfängt. Der Zustands Server verwendet die Informationen aus diesen Buchhaltungs Anforderungen, um seine Datenbank zu aktualisieren.

Weitere Informationen zu Status Servern finden Sie unter:

-   [Überlegungen zum Status Server Entwurf](/windows/desktop/Nps/ias-state-server-design-considerations)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Internet Authentifizierungsdienst und Netzwerk Richtlinien Server](internet-authentication-service-vs-network-policy-server.md)
</dt> <dt>

[RADIUS-Authentifizierung,-Autorisierung und-Kontoführung](/windows/desktop/Nps/ias-radius-authentication-and-accounting)
</dt> <dt>

[Protokollierung mit dem Netzwerk Richtlinien Server](/windows/desktop/Nps/ias-radius-accounting-packets)
</dt> </dl>

 

 