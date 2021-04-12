---
title: Vererbung und Delegierung der Verwaltung
description: Beschreibt AD DS Unterstützung der Vererbung von Berechtigungen in der Objektstruktur und auch der Objekt spezifischen Vererbung.
ms.assetid: db9cf8d9-6831-4456-b2a5-9f5b4f3e9100
ms.tgt_platform: multiple
keywords:
- Verwaltungs Vererbung und Delegierungs Active Directory
- Active Directory Active Directory, Vererbung von Berechtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d76db80497b54e71c806f3ccff9df549f9b2c1a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206262"
---
# <a name="inheritance-and-delegation-of-administration"></a>Vererbung und Delegierung der Verwaltung

Active Directory Domain Services unterstützt die Vererbung von Berechtigungen in der Objektstruktur, um die Ausführung von Verwaltungsaufgaben auf höheren Ebenen in der Struktur zuzulassen. Dadurch können Administratoren vererbbare Berechtigungen für Objekte in der Nähe des Stamms einrichten, wie z. b. Domänen-und Organisationseinheiten, und diese Berechtigungen an verschiedene Objekte in der Struktur verteilen.

Die Vererbung kann pro-ACE-Basis festgelegt werden. In der folgenden Tabelle sind die Flags aufgelistet, die in den **AceFlags** angegeben werden können, um die Vererbung des ACE zu steuern.



| Flag                                                     | Beschreibung                                                                                                                                     |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| **ADS- \_ aceflag \_ erben \_**<br/>                | Bewirkt, dass der ACE in der Struktur geerbt wird.<br/>                                                                                     |
| **ADS- \_ aceflag \_ No \_ propagieren- \_ \_ ACE**<br/> | Bewirkt, dass der ACE nur eine Ebene in der Struktur geerbt wird.<br/>                                                                      |
| **ADS- \_ aceflag \_ \_ nur von \_ ACE erben**<br/>          | Bewirkt, dass der ACE für das Objekt ignoriert wird, für das es angegeben ist, nur geerbt werden und wirksam ist, wo es geerbt wurde.<br/> |



 

Zusätzlich zum Festlegen der Vererbung unterstützt Active Directory Domain Services objektspezifische Vererbung. Dies ermöglicht es, dass vererbbare ACEs in der Struktur vererbt werden, aber nur für einen bestimmten Objekttyp wirksam werden. Dies ist für die Delegierung der Verwaltung äußerst nützlich. Dies kann z. b. verwendet werden, um einen Objekt spezifischen vererbbaren ACE in einer Organisationseinheit festzulegen, der einer Gruppe die vollständige Kontrolle über alle Benutzer Objekte in der Organisationseinheit, aber nichts anderes ermöglicht. Dadurch wird die Verwaltung der Benutzer in dieser Organisationseinheit an die Benutzer in dieser Gruppe delegiert.

### <a name="delegating-service-administration-with-security-groups"></a>Delegieren der Dienst Verwaltung mit Sicherheitsgruppen

Verwenden Sie Sicherheitsgruppen, um die Ihrem Anwendungsserver zugeordneten Administrator Rollen zu definieren und zu delegieren. Der Dienst kann z. b. einer Gruppe MyService-Administratoren zugeordnet werden. Benutzer, die als MyService-Administratoren identifiziert werden, werden der Gruppe MyService-Administratoren hinzugefügt. Das Setup Programm für MyService kann Zugriffs Steuerungs Listen für das Verzeichnis festlegen, damit MyService-Administratoren über ausreichende Berechtigungen zum Lesen/Schreiben von MyService-bezogenen Attributen oder zum Erstellen von MyService-spezifischen Objekten verfügen.

### <a name="roles-in-security-groups-for-computers-running-your-service"></a>Rollen in Sicherheitsgruppen für Computer, auf denen der Dienst ausgeführt wird

Verwenden Sie Sicherheitsgruppen, um die Gruppe von Computern zu definieren, denen der Zugriff auf die Objekte des Diensts im Verzeichnis gewährt wird. Der Dienst kann z. b. einer Gruppe MyService-Server zugeordnet werden. Alle Computer, auf denen der MyService-Server ausgeführt wird, werden der Gruppe "MyService Servers" hinzugefügt. dieser Gruppe kann dann Zugriff auf Teile des Verzeichnisses gewährt werden, in denen MyService-Serverdaten lesen/schreiben müssen. Das Setup Programm für MyService kann Zugriffs Steuerungs Listen für das Verzeichnis festlegen, damit MyService-Server über ausreichende Berechtigungen zum Lesen/Schreiben von MyService-bezogenen Attributen oder zum Erstellen von MyService-spezifischen Objekten verfügen.

 

 





