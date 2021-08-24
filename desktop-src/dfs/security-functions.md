---
title: Sicherheitsfunktionen
description: Die Sicherheitsfunktionen für die Netzwerkverwaltung erhalten und legen Sicherheitsbeschreibungen für domänenbasierte und eigenständige DFS-Stammstrukturen fest.
ms.assetid: 90860842-0f4d-49ad-b835-50305328a050
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d31611aa650bb55ecdc29af468e0ef784b670555b247d536d27b397de356f4ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119677800"
---
# <a name="security-functions"></a>Sicherheitsfunktionen

Die Sicherheitsfunktionen für die Netzwerkverwaltung erhalten und legen Sicherheitsbeschreibungen für domänenbasierte und eigenständige DFS-Stammstrukturen fest.

Die DFS-Sicherheitsfunktionen sind im Folgenden aufgeführt.

| Funktion                                                               | BESCHREIBUNG                                                                                                          |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**NetDfsGetSecurity**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetsecurity)                         | Ruft den Sicherheitsdeskriptor für das Stammobjekt des angegebenen DFS-Stamms ab.                                       |
| [**NetDfsSetSecurity**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetsecurity)                         | Sucht das Stammobjekt für den angegebenen DFS-Stamm und legt den angegebenen Sicherheitsdeskriptor dafür fest.                  |
| [**NetDfsGetStdContainerSecurity**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetftcontainersecurity) | Ruft den Sicherheitsdeskriptor für das Containerobjekt des angegebenen eigenständigen DFS-Stamms ab.                      |
| [**NetDfsSetStdContainerSecurity**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetstdcontainersecurity) | Sucht das Containerobjekt für den angegebenen eigenständigen DFS-Stamm und legt den angegebenen Sicherheitsdeskriptor darauf fest. |
| [**NetDfsGetFtContainerSecurity**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetftcontainersecurity)   | Ruft die Sicherheitsbeschreibung für das Containerobjekt des angegebenen DFS-Domänenstamms ab.                           |
| [**NetDfsSetFtContainerSecurity**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetftcontainersecurity)   | Sucht das Containerobjekt für den angegebenen DFS-Domänenstamm und legt den angegebenen Sicherheitsdeskriptor dafür fest.      |
