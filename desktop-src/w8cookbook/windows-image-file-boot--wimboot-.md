---
title: Start der Windows-Abbild Datei (wimboot)
description: Start der Windows-Abbild Datei (wimboot)
ms.assetid: 1C4EFC42-6698-4981-8C55-D1DFC6309F31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9f14ea506226e2c16d771ecec52fa31a8c871b4
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/10/2020
ms.locfileid: "103734641"
---
# <a name="windows-image-file-boot-wimboot"></a>Start der Windows-Abbild Datei (wimboot)

## <a name="platform"></a>Plattform

**Clients:** Windows 8.1  

## <a name="description"></a>BESCHREIBUNG

Wimboot ist eine alternative Möglichkeit für OEMs, Windows bereitzustellen. Eine wimboot-Bereitstellung startet Windows direkt aus einer komprimierten Windows-Abbild Datei (WIM) und führt Sie aus. Diese WIM-Datei ist unveränderlich, und der Zugriff darauf wird von einem neuen Dateisystem-Filtertreiber (WoF.sys) verwaltet.

Das Ergebnis ist eine erhebliche Verringerung des Speicherplatzes, der für die Installation von Windows erforderlich ist.

## <a name="manifestations"></a>Kundgebungen

Die meisten Anwendungen sollten von wimboot vollständig betroffen sein. Nur Anwendungen, die auf Systemdateien oder vorab geladene Dateien für Schreibzugriffe zugreifen und diese entsperren, sind möglicherweise betroffen. Da die WIM unveränderlich ist, werden Aktualisierungen an der Datei (d. h. System-oder vorab geladene Dateien) einfach auf der C:- \\ Partition gespeichert.

Wenn eine Anwendung den Schreibzugriff für alle WIM-gestützten Systemdateien und vorab geladenen Dateien entsperrt hat, würden die Einsparungen, die von wimboot bereitgestellt werden, vollständig verloren gehen, da alle diese Dateien dekomprimiert und auf dem Volume "C:" abgelegt werden \\ .

Außerdem müssen Sicherungs-und Wiederherstellungs Anwendungen die wimboot-bereit Stellungen beachten, da die WIM in einer separaten Partition vorhanden ist. Das heißt, bei der Sicherungskopie müssen sowohl die C: \\ -als auch die WIM-Partitionen gespeichert werden, und beide müssen gleichzeitig wieder hergestellt werden.

## <a name="solution"></a>Lösung

Es wurden neue APIs eingeführt, mit denen Anwendungen direkt abfragen können, ob ein bestimmtes Volume oder eine Datei durch eine WIM-Datei unterstützt wird. Diese Informationen ermöglichen es Anwendungen, geeignete Entscheidungen zu treffen, z. b. das Öffnen dieser Dateien nur für den Lesezugriff oder das Identifizieren von Volumes/Partitionen, die gleichzeitig gesichert und wieder hergestellt werden müssen.

## <a name="compatibility-performance-reliability-or-usability-tests"></a>Kompatibilitäts-, Leistungs-, Zuverlässigkeits-oder Nutzbarkeits Tests

Anwendungsentwickler sollten Ihre Software und die entsprechenden Szenarios auf einem wimboot-System testen, insbesondere dann, wenn diese Anwendungen auf Systemdateien oder vorab geladene Dateien zugreifen. Wenn ein Szenario abgeschlossen ist, sollte eine beträchtliche Reduzierung des verfügbaren Speicherplatzes gezahlt werden.

 

 




