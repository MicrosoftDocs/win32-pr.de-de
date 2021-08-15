---
description: Ermöglicht Clientanwendungen den Zugriff auf SNMP-Informationen über WMI.
ms.assetid: d9e3fd1d-8320-4407-9a9e-e2eb5dd62fef
ms.tgt_platform: multiple
title: Zugreifen auf SNMP-Geräte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3acf8fd67ee9153167cd328b7a50f6aafc5853327a64baf80c3b2e20b663d3ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118320302"
---
# <a name="accessing-snmp-devices"></a>Zugreifen auf SNMP-Geräte

Der SNMP-Anbieter (Simple Network Management Protocol) ermöglicht Clientanwendungen den Zugriff auf SNMP-Informationen über WMI. Der [SNMP-Anbieter](snmp-provider.md) fungiert als Gateway für Systeme und Geräte, die SNMP für die Verwaltung verwenden. Nur auf dem Verwaltungs- oder Überwachungscomputer muss WMI ausgeführt werden, da von jedem SNMP-fähigen Gerät gelesen werden kann.

> [!Note]  
> Weitere Informationen zum Installieren des Anbieters finden Sie unter [Einrichten der WMI-SNMP-Umgebung.](setting-up-the-wmi-snmp-environment.md)

 

MiB-Objektvariablen (SNMP Management Information Base) können gelesen und in diese geschrieben werden, und SNMP-Traps können automatisch WMI-Ereignissen zugeordnet werden, die für beliebige Erstellungs-, Lösch- oder Aktualisierungsvorgänge für Daten außerhalb der MIB-definierten Traps definiert werden können. Dieses Feature von WMI fungiert als Erweiterung der SNMP-Standardfunktionen. Weitere Informationen finden Sie unter [Überwachen von Ereignissen.](monitoring-events.md)

Die in den folgenden Themen beschriebenen Tools sind für die Verwendung durch skriptgesteuerte Windows C/C++-Programmierer konzipiert. Es wird empfohlen, mit WMI, SNMPv1 und SNMPv2C vertraut zu sein und mit netzwerk- und netzwerkverwaltungskonzepte vertraut zu sein.

Weitere Informationen zur Verwendung von WMI mit SNMP finden Sie unter [Einrichten der WMI-SNMP-Umgebung.](setting-up-the-wmi-snmp-environment.md)

 

 



