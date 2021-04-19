---
description: Ermöglicht Client Anwendungen den Zugriff auf SNMP-Informationen über WMI.
ms.assetid: d9e3fd1d-8320-4407-9a9e-e2eb5dd62fef
ms.tgt_platform: multiple
title: Zugreifen auf SNMP-Geräte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37a349053f054f3e8ad9dffb7c108d2bee6c6d8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362996"
---
# <a name="accessing-snmp-devices"></a>Zugreifen auf SNMP-Geräte

Der SNMP-Anbieter (Simple Network Management Protocol) ermöglicht Client Anwendungen den Zugriff auf SNMP-Informationen über WMI. Der [SNMP-Anbieter](snmp-provider.md) fungiert als Gateway für Systeme und Geräte, die SNMP für die Verwaltung verwenden. Nur der Verwaltungs-oder Überwachungscomputer muss WMI ausführen, da er von einem beliebigen SNMP-fähigen Gerät gelesen werden kann.

> [!Note]  
> Weitere Informationen zum Installieren des Anbieters finden Sie unter [Einrichten der WMI-SNMP-Umgebung](setting-up-the-wmi-snmp-environment.md).

 

Die Objektvariablen der SNMP-Management Information Base (MIB) können aus gelesen und geschrieben werden. SNMP-Traps können automatisch WMI-Ereignissen zugeordnet werden, die für beliebige Erstellungs-, Lösch-oder Aktualisierungs Vorgänge für Daten außerhalb der MIB-definierten Traps definiert werden können. Diese Funktion von WMI fungiert als Erweiterung von SNMP-Standardfunktionen. Weitere Informationen finden Sie unter über [Wachen von Ereignissen](monitoring-events.md).

Die in den folgenden Themen beschriebenen Tools sind für die Verwendung durch Windows Scripting und C/C++-Programmierer konzipiert. Es wird empfohlen, sich mit WMI, SNMPv1 und SNMPv2C vertraut zu machen und ein Wissen über Netzwerk-und Netzwerk Verwaltungs Konzepte zu erhalten.

Weitere Informationen zur Verwendung von WMI mit SNMP finden Sie unter [Einrichten der WMI-SNMP-Umgebung](setting-up-the-wmi-snmp-environment.md).

 

 



