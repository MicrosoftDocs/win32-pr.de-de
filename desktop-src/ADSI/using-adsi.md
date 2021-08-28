---
title: Verwenden von Active Directory-Dienstschnittstellen
description: Active Directory Service Interfaces (ADSI) bietet Clientanwendungen von Verzeichnisdiensten die Möglichkeit, einen Satz von Schnittstellen für die Kommunikation mit jedem Namespace zu verwenden, der eine ADSI-Implementierung bietet.
ms.assetid: 58bde1ea-30d1-4601-a6fb-df0bb837e2ab
ms.tgt_platform: multiple
keywords:
- Verwenden von ADSI für Active Directory-Dienstschnittstellen
- ADSI ADSI , Using
- Active Directory-Dienstschnittstellen ADSI mit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15495f9fa21f436570381ea8f0b2a7c7fff5f4efed645a5f3465a3b5d2929776
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648850"
---
# <a name="using-active-directory-service-interfaces"></a>Verwenden von Active Directory-Dienstschnittstellen

Active Directory Service Interfaces (ADSI) bietet Clientanwendungen von Verzeichnisdiensten die Möglichkeit, einen Satz von Schnittstellen für die Kommunikation mit jedem Namespace zu verwenden, der eine ADSI-Implementierung bietet. ADSI-Clients verwenden die klar definierten Active Directory-Dienstschnittstellen statt der netzwerkspezifischen API-Aufrufe, um einfacheren Zugriff auf die Dienste für einen Namespace zu erhalten.

Active Directory-Dienstschnittstellen entsprechen dem Component Object Model (COM) und unterstützen COM-Standardfeatures.

ADSI stellt Schnittstellen bereit, die mit Automation für namensgebundene Controller wie Java, das Microsoft Visual Basic-Entwicklungssystem und Visual Basic Scripting Edition (VBScript) kompatibel sind. ADSI kann auch eine Schnittstelle bereitstellen, die die Leistung für Schnittstellen optimieren kann, die nicht mit Automation kompatibel sind, um sie mit Sprachumgebungen wie C und C++ zu verwenden.

ADSI stellt auch die nicht automatisierungsbasierten Schnittstellen [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) und [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)bereit, um die Verzeichnisobjektverwaltung und Abfragen zu unterstützen.

Darüber hinaus stellt ADSI einen eigenen OLE DB-Anbieter zur Verfügung, sodass jeder Client, der bereits OLE DB verwendet, einschließlich der Clients, die ActiveX Data Objects verwenden, Verzeichnisdienste direkt abfragen kann.

Webanwendungen, die Active Server Pages verwenden, können den Zugriff auf Verzeichnisdienste auch über ADSI programmieren.

ADSI-Clients können programmgesteuert alle ADSI-Anbieter an einem Standort entdecken und dieselben Schnittstellen für die Kommunikation mit den einzelnen Namespaces verwenden. Wenn zusätzliche Anbieter installiert sind, können die ADSI-Clients auch mit den neuen Namespaces kommunizieren, ohne neu zu kompilieren.

Dieser Programmierleitfaden beschreibt die Funktionsweise von ADSI und enthält Informationen zum Ausführen bestimmter Aufgaben in ADSI. Die folgenden Themen werden erörtert:

-   [Binden an ein ADSI-Objekt](binding-to-an-adsi-object.md)
-   [Erstellen und Löschen von Objekten](creating-and-deleting-objects.md)
-   [Zugreifen auf und Bearbeiten von Daten mit ADSI](accessing-and-manipulating-data-with-adsi.md)
-   [Verwenden des ADSI-Schemas](using-the-adsi-schema.md)
-   [Sammlungen und Gruppen](collections-and-groups.md)
-   [Aufzählen von ADSI-Objekten](enumerating-adsi-objects.md)
-   [Suchen nach Active Directory](searching-active-directory.md)
-   [ADSI-Sicherheitsmodell](adsi-security-model.md)
-   [ADSI-Erweiterungen](adsi-extensions.md)
-   [Verwenden von ADSI mit Exchange](using-adsi-with-exchange.md)
-   [ADSI-Hilfsprogrammschnittstellen](adsi-utility-interfaces.md)
-   [Programmieren von ADSI mit Java/COM](programming-adsi-with-javacom.md)

 

 




