---
title: Verzeichnis System-Agent
description: Der Verzeichnis System-Agent (DSA) ist eine Sammlung von Diensten und Prozessen, die auf jedem Domänen Controller ausgeführt werden und Zugriff auf den Datenspeicher bietet.
ms.assetid: a921a822-6b2e-4a84-8112-0ae516443667
ms.tgt_platform: multiple
keywords:
- Verzeichnis System-Agent-Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df39d1670f6668f933c20bcd2b9a8771ce83ec56
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103858155"
---
# <a name="directory-system-agent"></a>Verzeichnis System-Agent

Der [*Verzeichnis System-Agent*](/previous-versions/windows/desktop/legacy/ms681901(v=vs.85)) (DSA) ist eine Sammlung von Diensten und Prozessen, die auf jedem Domänen Controller ausgeführt werden und Zugriff auf den Datenspeicher bietet. Der Datenspeicher ist der physische Speicher der Verzeichnis Daten auf einer Festplatte. In Active Directory Domain Services ist das DSA Teil des Local System Authority (LSA)-Subsystems. Clients greifen mithilfe eines der folgenden Mechanismen, die von DSA unterstützt werden, auf das Verzeichnis zu:

-   LDAP-Clients stellen eine Verbindung mit dem DSA mithilfe von LDAP (Lightweight Directory Access Protocol) her. Active Directory Domain Services Unterstützung von LDAP 3,0, definiert durch RFC 3377 und LDAP 2,0, definiert durch RFC 1777. Windows-Clients verwenden LDAP 3,0, um eine Verbindung mit dem DSA herzustellen.
-   MAPI-Clients wie Microsoft Exchange Server stellen mithilfe der MAPI-Schnittstelle für Remote Prozedur Aufrufe eine Verbindung mit dem DSA her.
-   Die DSAs in Active Directory Domain Services eine Verbindung untereinander herstellen, um die Replikation über eine proprietäre Remote Prozedur aufrufsschnittstelle auszuführen.

 

 