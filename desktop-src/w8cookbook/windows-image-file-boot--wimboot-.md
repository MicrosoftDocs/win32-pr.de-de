---
title: Windows Start der Imagedatei (WimBoot)
description: Windows Start der Imagedatei (WimBoot)
ms.assetid: 1C4EFC42-6698-4981-8C55-D1DFC6309F31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 687a230188c3b13317d8176d8209cf5e38026c3b6f161be7ffe0c2ed760976ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119932120"
---
# <a name="windows-image-file-boot-wimboot"></a>Windows Start der Imagedatei (WimBoot)

## <a name="platform"></a>Plattform

**Clients:** Windows 8.1  

## <a name="description"></a>Beschreibung

WimBoot ist eine alternative Möglichkeit für OEMs zum Bereitstellen Windows. Eine WimBoot-Bereitstellung wird gestartet und Windows direkt aus einer komprimierten Windows Imagedatei (WIM) ausgeführt. Diese WIM-Datei ist unveränderlich, und der Zugriff darauf wird von einem neuen Dateisystemfiltertreiber (File System Filter Driver, WoF.sys) verwaltet.

Dies führt zu einer erheblichen Verringerung des Speicherplatzes, der für die Installation des Windows.

## <a name="manifestations"></a>Manifestationen

Die meisten Anwendungen sollten von WimBoot vollständig unbeeinflusst sein. Nur Anwendungen, die auf Systemdateien oder vorab geladene Dateien für den Schreibzugriff zugreifen und diese entsperren, sind möglicherweise betroffen. Da wim unveränderlich ist, werden Updates dafür (d. h. Systemdateien oder vorab geladene Dateien) einfach auf der C:-Partition \\ gespeichert.

Wenn eine Anwendung den Schreibzugriff für alle WIM-fähigen Systeme und vorab geladenen Dateien entsperrt, gehen die von WimBoot übermittelten Einsparungen vollständig verloren, da alle diese Dateien dekomprimiert und auf dem Volume C: platziert \\ würden.

Darüber hinaus müssen Sicherungs- und Wiederherstellungsanwendungen WimBoot-Bereitstellungen beachten, da wim in einer separaten Partition vorhanden ist. Das heißt, bei der Sicherung müssen sowohl die Partitionen C: als auch WIM gespeichert und beide \\ zusammen wiederhergestellt werden.

## <a name="solution"></a>Lösung

Es wurden neue APIs eingeführt, mit denen Anwendungen direkt abfragen können, ob ein bestimmtes Volume oder eine Bestimmte Datei von einem WIM-Volume oder einer Datei als Back-Byte verwendet wird. Diese Informationen ermöglichen es Anwendungen, geeignete Entscheidungen zu treffen, z. B. das Öffnen dieser Dateien nur für den Lesezugriff oder das Identifizieren von Volumes/Partitionen, die zusammen sichern und wiederhergestellt werden müssen.

## <a name="compatibility-performance-reliability-or-usability-tests"></a>Kompatibilitäts-, Leistungs-, Zuverlässigkeits- oder Nutzbarkeitstests

Anwendungsentwickler sollten ihre Software und die entsprechenden Szenarien auf einem WimBoot-System testen, insbesondere, wenn diese Anwendungen auf system- oder vorab geladene Dateien zugreifen. Besondere Aufmerksamkeit sollte auf eine erhebliche Verringerung des verfügbaren Speicherplatzes auf dem Datenträger nach Abschluss eines Szenarios 2016 2016 2016 auf dem Datenträger zu finden sein.

 

 




