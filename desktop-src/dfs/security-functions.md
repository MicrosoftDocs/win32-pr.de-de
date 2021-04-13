---
title: Sicherheitsfunktionen
description: Die Sicherheitsfunktionen für die Netzwerkverwaltung erhalten und legen Sicherheits Deskriptoren für Domänen basierte und eigenständige DFS-Stämme fest.
ms.assetid: 90860842-0f4d-49ad-b835-50305328a050
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95f717ff3f5701e507087fcdac164d9357f2505a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483846"
---
# <a name="security-functions"></a>Sicherheitsfunktionen

Die Sicherheitsfunktionen für die Netzwerkverwaltung erhalten und legen Sicherheits Deskriptoren für Domänen basierte und eigenständige DFS-Stämme fest.

Die DFS-Sicherheitsfunktionen sind nachfolgend aufgeführt.

| Funktion                                                               | BESCHREIBUNG                                                                                                          |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**Netdfsgetsecurity**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetsecurity)                         | Ruft die Sicherheits Beschreibung für das Stamm Objekt des angegebenen DFS-Stamms ab.                                       |
| [**Netdfssetsecurity**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetsecurity)                         | Sucht das Stamm Objekt für den angegebenen DFS-Stamm und legt den angegebenen Sicherheits Deskriptor darauf fest.                  |
| [**Netdfsgetstdcontainersecurity**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetftcontainersecurity) | Ruft die Sicherheits Beschreibung für das Container Objekt des angegebenen eigenständigen DFS-Stamms ab.                      |
| [**Netdfssetstdcontainersecurity**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetstdcontainersecurity) | Sucht das Container Objekt für das angegebene eigenständige DFS-Stammverzeichnis und legt die angegebene Sicherheits Beschreibung darauf fest. |
| [**Netdfsgetftcontainersecurity**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetftcontainersecurity)   | Ruft die Sicherheits Beschreibung für das Container Objekt des angegebenen DFS-Domänen Stamms ab.                           |
| [**Netdfssetftcontainersecurity**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetftcontainersecurity)   | Sucht das Container Objekt für den angegebenen DFS-Domänen Stamm und legt die angegebene Sicherheits Beschreibung darauf fest.      |
