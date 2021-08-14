---
title: Vererbung und Delegierung der Verwaltung
description: Beschreibt AD DS Unterstützung für die Vererbung von Berechtigungen in der Objektstruktur sowie für die objektspezifische Vererbung.
ms.assetid: db9cf8d9-6831-4456-b2a5-9f5b4f3e9100
ms.tgt_platform: multiple
keywords:
- Verwaltungsvererbung und Delegierung von Active Directory
- Active Directory Active Directory , Berechtigungsvererbung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b48ff4d913cbd8bf16f7b2c67adf86d61515298dcac267291641d30504e1e32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187523"
---
# <a name="inheritance-and-delegation-of-administration"></a>Vererbung und Delegierung der Verwaltung

Active Directory Domain Services unterstützt die Vererbung von Berechtigungen in der Objektstruktur, damit Verwaltungsaufgaben auf höheren Ebenen in der Struktur ausgeführt werden können. Dadurch können Administratoren vererbbare Berechtigungen für Objekte in der Nähe des Stamms einrichten, z. B. Domänen- und Organisationseinheiten, und diese Berechtigungen auf verschiedene Objekte in der Struktur verteilen lassen.

Die Vererbung kann pro ACE festgelegt werden. Die folgende Tabelle enthält Flags, die in den **AceFlags** angegeben werden können, um die Vererbung des ACE zu steuern.



| Flag                                                     | Beschreibung                                                                                                                                     |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| **ADS \_ ACEFLAG \_ INHERIT \_ ACE**<br/>                | Bewirkt, dass der ACE in der Struktur vererbt wird.<br/>                                                                                     |
| **ADS \_ ACEFLAG \_ NO \_ PROPAGATE \_ INHERIT \_ ACE**<br/> | Bewirkt, dass der ACE nur eine Ebene in der Struktur vererbt wird.<br/>                                                                      |
| **ADS \_ ACEFLAG \_ INHERIT \_ ONLY \_ ACE**<br/>          | Bewirkt, dass der ACE für das Objekt ignoriert wird, für das er angegeben ist, nur vererbt wird und dort wirksam ist, wo er geerbt wurde.<br/> |



 

Zusätzlich zum Festlegen der Vererbung unterstützt Active Directory Domain Services objektspezifische Vererbung. Dadurch können die vererbten ACEs in der Struktur vererbt werden, sind jedoch nur für einen bestimmten Objekttyp wirksam. Dies ist äußerst nützlich bei der Delegierung der Verwaltung. Dies kann beispielsweise verwendet werden, um einen objektspezifischen vererbbaren ACE in einer Organisationseinheit zu setzen, der einer Gruppe die vollständige Kontrolle über alle Benutzerobjekte in der Organisationseinheit, aber nichts anderes ermöglicht. Dadurch wird die Verwaltung von Benutzern in dieser Organisationseinheit an die Benutzer in dieser Gruppe delegiert.

### <a name="delegating-service-administration-with-security-groups"></a>Delegieren der Dienstverwaltung mit Sicherheitsgruppen

Verwenden Sie Sicherheitsgruppen, um Administratorrollen zu definieren und zu delegieren, die Ihrem Anwendungsserver zugeordnet sind. Ihr Dienst kann beispielsweise einer Gruppe MyService-Administratoren zugeordnet sein. Benutzer, die als MyService-Administratoren identifiziert werden, werden der Gruppe MyService-Administratoren hinzugefügt. Das Setupprogramm für MyService kann ACLs für das Verzeichnis festlegen, um MyService-Administratoren ausreichende Berechtigungen zum Lesen/Schreiben von MyService-bezogenen Attributen oder zum Erstellen von MyService-spezifischen Objekten zu ermöglichen.

### <a name="roles-in-security-groups-for-computers-running-your-service"></a>Rollen in Sicherheitsgruppen für Computer, auf denen Ihr Dienst ausgeführt wird

Verwenden Sie Sicherheitsgruppen, um die Gruppe von Computern zu definieren, denen Zugriff auf die Objekte Ihres Diensts im Verzeichnis gewährt wird. Ihr Dienst kann beispielsweise einer Gruppe MyService-Server zugeordnet sein. Alle Computer, auf denen der MyService-Server ausgeführt wird, werden der Gruppe MyService-Server hinzugefügt, und dieser Gruppe kann dann Zugriff auf Teile des Verzeichnisses erteilt werden, in denen MyService-Server Daten lesen/schreiben müssen. Das Setupprogramm für MyService kann ACLs für das Verzeichnis festlegen, um MyService Servers ausreichende Berechtigungen zum Lesen/Schreiben von MyService-bezogenen Attributen oder zum Erstellen von MyService-spezifischen Objekten zu ermöglichen.

 

 





