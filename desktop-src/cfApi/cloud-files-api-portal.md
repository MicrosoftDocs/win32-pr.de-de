---
description: Die Cloudfilter-API stellt Funktionen an der Grenze zwischen Benutzermodus und Dateisystem bereit.
ms.assetid: 72bc3e80-babd-4a39-842c-38afe4773a5e
title: Cloudsynchronisierungs-Engines
ms.topic: article
ms.date: 02/06/2019
ms.custom: project-verbatim
ms.openlocfilehash: 39dd28779c07dfd6e44fde0e53f583e72971d5883205f42581e3b5ac4102c0eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118551374"
---
# <a name="cloud-sync-engines"></a>Cloudsynchronisierungs-Engines

Siehe auch [Cloud Mirror-Beispiel](./build-a-cloud-file-sync-engine.md#cloud-mirror-sample).

Ab Version Windows 10 Version 1709 stellt Windows die *Clouddateien-API bereit.* Diese API besteht aus mehreren nativen Win32- und WinRT-APIs, die die Unterstützung für Cloudsynchronisierungs-Engines formalisieren und Aufgaben wie das Erstellen und Verwalten von Platzhalterdateien und -verzeichnissen durchführen. Benutzer dieser API sind in der Regel Synchronisierungsanbieter und in gewissem Umfang Windows Anwendungen.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema                                                                | Beschreibung                                                                                        |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [Erstellen einer Cloudsynchronisierungs-Engine, die Platzhalterdateien unterstützt](build-a-cloud-file-sync-engine.md)<br/> | Erfahren Sie, wie Sie mithilfe der Clouddatei-API eine Clouddateisynchronisierungs-Engine erstellen, die Platzhalterdateien und die Datei-Explorer-Integration enthält. <br/> |
| [Cloudfilterreferenz](cloud-filter-reference.md)<br/> | Die Cloudfilter-API ist eine native Win32-API, die Teil der umfassenderen Clouddateien-API ist. Die Cloudfilter-API stellt Funktionen an der Grenze zwischen dem Benutzermodus und dem Dateisystem bereit. Diese API übernimmt die Erstellung und Verwaltung von Platzhalterdateien und Verzeichnissen. <br/> |