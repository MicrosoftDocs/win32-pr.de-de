---
description: Die cloudfilterapi bietet Funktionen an der Grenze zwischen dem Benutzermodus und dem Dateisystem.
ms.assetid: 72bc3e80-babd-4a39-842c-38afe4773a5e
title: Cloud Sync Engines
ms.topic: article
ms.date: 02/06/2019
ms.custom: project-verbatim
ms.openlocfilehash: debe32a1849a393a067017f90f5405c4b3ba77d1
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/20/2021
ms.locfileid: "106353411"
---
# <a name="cloud-sync-engines"></a>Cloud Sync Engines

Siehe auch [Cloud-Spiegel Beispiel](/windows/win32/cfapi/build-a-cloud-file-sync-engine#cloud-mirror-sample).

Ab Windows 10, Version 1709, stellt Windows die *Cloud Files-API* bereit. Diese API besteht aus mehreren nativen Win32-und WinRT-APIs, die die Unterstützung für Cloud-Synchronisierungs Module formalisieren und Aufgaben wie das Erstellen und Verwalten von Platzhalter Dateien und Verzeichnissen verarbeiten. Benutzer dieser API sind in der Regel Synchronisierungs Anbieter und ein gewisser Umfang von Windows-Anwendungen.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema                                                                | BESCHREIBUNG                                                                                        |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Erstellen einer Cloud-Synchronisierungs-Engine, die Platzhalter Dateien unterstützt](build-a-cloud-file-sync-engine.md)<br/> | Erfahren Sie, wie Sie die Cloud Files-API verwenden, um ein clouddateisynchronisierungs-Engine zu erstellen, das Platzhalter Dateien und Datei-Explorer-Integration <br/> |
| [Cloudfilterverweis](cloud-filter-reference.md)<br/> | Die Cloud Filter-API ist eine native Win32-API, die Teil der umfassenderen Cloud Files-API ist. Die cloudfilterapi bietet Funktionen an der Grenze zwischen dem Benutzermodus und dem Dateisystem. Diese API behandelt die Erstellung und Verwaltung von Platzhalter Dateien und Verzeichnissen. <br/> |

