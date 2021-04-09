---
description: In diesem Thema werden spezifische Sicherheitsüberlegungen bei der Verwendung der Peer Infrastruktur erläutert.
ms.assetid: 088a2111-f4ee-4bec-98a9-ac138950958b
title: Überlegungen zur Sicherheit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffd3078834b3a69f988d17e5cbfd5fa1bd1591e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867003"
---
# <a name="security-considerations"></a>Überlegungen zur Sicherheit

In diesem Thema werden spezifische Sicherheitsüberlegungen bei der Verwendung der Peer Infrastruktur erläutert.

Wenn Sie eine Peer Anwendung mithilfe der Peer Infrastruktur entwickeln, müssen Sie aus Sicherheitsgründen Verzeichnis Berechtigungen, den Gast Zugriff auf Peer Netzwerkdienste, die Offenlegung von Informationen und die Implementierung des Sicherheits Dienstanbieters in Erwägung gezogen.

## <a name="directory-permissions"></a>Verzeichnis Berechtigungen

Peer-to-Peer-Netzwerkdienste speichern Daten in der Benutzerprofil-Verzeichnisstruktur eines Benutzers. Ein Benutzer muss über Schreibberechtigungen für die **Anwendungsdaten** -Unterstruktur des Profils verfügen. Standardmäßig ist diese Zugriffs Steuerungs Liste (Access Control List, ACL) ordnungsgemäß festgelegt, aber ein Benutzer kann Sie manuell ändern.

## <a name="guest-access-to-peer-networking-services"></a>Gast Zugriff auf Peer Netzwerkdienste

Ein Gastkonto und Mitglieder der Windows-Sicherheitsgruppe " **Gäste** " haben keinen Zugriff auf die meisten Peer Dienste. Anwendungen sollten über lokalen Benutzer Zugriff oder höher verfügen.

## <a name="information-disclosure"></a>Veröffentlichung von Informationen

Die Offenlegung von Informationen umfasst Adressen, Datenbank und Anmelde Informationen für die Identität und Gruppe. In den folgenden Abschnitten werden die Veröffentlichung von Informationen identifiziert und definiert.

**Offenlegung von Adressen** Das Peer Name Resolution-Protokoll (PNRP) ist ein Dienst für die bezeichnerauflösung, mit dem ein Peer Namen Bezeichner in eine IP-Adresse aufgelöst werden kann. Ähnlich wie DNS veröffentlicht PNRP eine IP-Adresse, sodass Benutzer, die den entsprechenden Bezeichner kennen, Sie in diese Adresse auflösen können.

-   Das Veröffentlichen eines Bezeichners in PNRP bedeutet, dass jeder Benutzer den Bezeichner in die veröffentlichte IP-Adresse auflösen und die IP-Adresse des PNRP-Dienstanbieter ermitteln kann, der die Identität veröffentlicht hat.
-   Die Peer Gruppierungs Infrastruktur veröffentlicht automatisch den Peer Gruppennamen der lokalen Gruppeninstanz in PNRP. Wenn eine Verbindung mit einer Peer Gruppe besteht, kann jeder, der den Peernamen der Gruppe kennt, die Adressen aktiver Mitglieder auflösen und die aktuelle Adresse der einzelnen Benutzer kennen.

Die Fähigkeit eines Benutzers, eine Verbindung mit anderen Peer Gruppenmitgliedern oder Peer Diagramm Knoten herzustellen, während er angemeldet ist, ist ein primäres Feature des Peer Netzwerks. Wenn eine Verbindung mit einer Peer Gruppe oder einem Diagramm besteht, kann die aktuelle IP-Adresse eines Benutzers in einem Anwesenheitsdaten Satz innerhalb der Peer Gruppe oder des Diagramms veröffentlicht werden. Standardmäßig kann jeder, der an dieser Peer Gruppe oder diesem Diagramm teilnimmt, Mitglieder der Gruppe oder des Diagramms auflisten und die aktuellen Adressen der Mitglieder bestimmen. Diese Möglichkeit ist eine konfigurierbare Peer Gruppierung und Peer graphingeigenschaft.

**Daten Bank Offenlegung** Die Datenbanken der Peer Gruppierung und der graphinginfrastrukturen werden auf dem lokalen Dateisystem gespeichert. Jeder Windows-Benutzer mit administrativem Zugriff auf das lokale Dateisystem (z. b. ein lokaler Administrator) kann theoretisch auf die Daten im lokalen peergraph oder in der Gruppen Datenbank zugreifen. Dies entspricht der Fähigkeit lokaler Administratoren, auf alle Daten auf dem lokalen Computer zuzugreifen.

**Veröffentlichung von Identitäts-und Gruppen Anmelde** Informationen Die Peer-zu-Peer-Gruppierung erfordert, dass Mitglieder Verbindungen untereinander herstellen, um die Authentifizierung mithilfe geänderter X. 509-Zertifikat Ketten durchführen zu können. Im Rahmen der Authentifizierung werden die entsprechenden Identitäts-und Gruppen Mitgliedschafts Zertifikate (GMC) der einzelnen Mitglieder ausgetauscht.

Wenn eine Verbindung mit einer Peer Gruppe besteht, veröffentlicht die Peer Gruppierungs Infrastruktur den gruppenpeernamen mit PNRP. Im Rahmen des normalen PNRP-Vorgangs kann die GMC-Kette für diese Gruppe anderen PNRP-Instanzen bereitgestellt werden, um die Autorisierung zum Veröffentlichen des gruppenpeernamens zu bestätigen.

## <a name="security-service-provider-implementation"></a>Implementierung des Sicherheits Dienstanbieters

Die Peer-graphinginfrastruktur ist so sicher wie der Security Service Provider (SSP), den der Anwendungsentwickler implementiert. Je stärker der SSP, desto stärker die Sicherheit der Peer graphinganwendung.

 

 



