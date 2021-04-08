---
description: APIs für Personen in meiner Umgebung
ms.assetid: 3b142d23-a9b2-465c-9bdc-484afbde154e
title: APIs für Personen in meiner Umgebung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 132d358a7d51a1069f7a4d1dc1ddfe2752dbdd1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959782"
---
# <a name="people-near-me-apis"></a>APIs für Personen in meiner Umgebung

Alle Anwendungen, die [Personen in meiner](about-people-near-me.md) Umgebung (PNM) unterstützen, können die folgenden Win32-APIs verwenden:

### <a name="contacts-api"></a>Kontakte-API

Die Contacts-API wird für den Zugriff auf die Kontaktinformationen des angemeldeten Benutzers, zum Abrufen von Informationen zu zuvor gespeicherten Kontakten oder zum Speichern der Kontaktinformationen und des digitalen Zertifikats eines neuen Kontakts verwendet.

### <a name="people-near-me-api"></a>API für Personen in meiner Umgebung

Die PNM-API wird verwendet, um nach Benutzern in der Nähe, ihren angekündigten Interessen, beliebigen Objekten, die Sie veröffentlichen möchten, und angekündigten Anwendungen zu suchen.

### <a name="publication-api"></a>Veröffentlichungs-API

Die Veröffentlichungs-API wird für die Interaktion mit Remote Kontakten verwendet. Die [Peer-Signal](windows-peer-components-for-people-near-me.md) Schicht, die vom Veröffentlichungs-Manager verwendet wird, wird auch vom PNM-Modul zum Herstellen von Verbindungen verwendet.

### <a name="invitation-api"></a>Einladungs-API

Die Einladungs-API wird von einer Zusammenarbeits Anwendung verwendet, um bestimmte Peers in eine Zusammenarbeits Aktivität einzuladen.

### <a name="application-registration-api"></a>Anwendungsregistrierungs-API

Die anwendungsregistrierungs-API wird vom Installationsprogramm einer Zusammenarbeits Anwendung verwendet, um die Anwendung zu registrieren. Eine PNM-fähige Anwendung fordert den Benutzer während des Installationsvorgangs auf, um zu bestimmen, ob die Anwendung für Benutzer im Subnetz zur Verfügung gestellt werden soll.

 

 



