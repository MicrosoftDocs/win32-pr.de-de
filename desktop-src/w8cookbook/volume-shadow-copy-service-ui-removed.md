---
title: Die Benutzeroberfläche der früheren Versionen wurde für lokale Volumes entfernt.
description: Die Benutzeroberfläche der früheren Versionen wurde für lokale Volumes entfernt.
ms.assetid: 0BD3D046-EB06-4C9A-952C-306AC99396C6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b25d898be8d079ee713e0fa3e508e552b3cd4009
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "104474485"
---
# <a name="previous-versions-ui-removed-for-local-volumes"></a>Die Benutzeroberfläche der früheren Versionen wurde für lokale Volumes entfernt.

## <a name="platform"></a>Plattform

**Clients** – Windows 8 


## <a name="description"></a>BESCHREIBUNG

In früheren Versionen von Windows konnten Benutzer vorherige Versionen einzelner Dateien aus "Schatten Kopien" von lokalen Volumes wiederherstellen. Diese Schatten Kopien werden mithilfe des Volumeschattenkopie-Diensts (VSS) durch das Feature "vorherige Versionen" erstellt. In Windows 7 konnten Benutzer Schatten Kopien in der Benutzeroberfläche des System Schutzes konfigurieren und planen, die über Systemeigenschaften verfügbar sind.

Frühere Versionen wurden jedoch selten verwendet und beeinflussen die gesamte Windows-Leistung. Daher wurde die Funktion entfernt. In Windows 8 sind diese Features nicht mehr verfügbar:

-   Die Möglichkeit zum Durchsuchen, durchsuchen oder Wiederherstellen früherer Dateiversionen über die Benutzeroberfläche der vorherigen Versionen
-   Die Möglichkeit, frühere Versionen von Dateien über die Benutzeroberfläche des System Schutzes zu konfigurieren oder zu planen

Benutzer können jedoch weiterhin die Registerkarte Vorherige Versionen verwenden, wenn Sie auf Dateifreigaben auf einem Windows-Server zugreifen.

## <a name="manifestation"></a>Ausstrahlung

Die Option "vorherige Versionen" ist nicht mehr für lokale Volumes im Eigenschaften Menü von Windows Explorer verfügbar.

## <a name="solution"></a>Lösung

Entwickler, die Schatten Kopien von lokalen Volumes erstellen müssen, können dies weiterhin tun, indem Sie VSS-APIs in benutzerdefiniertem Code aufrufen.

 

 




