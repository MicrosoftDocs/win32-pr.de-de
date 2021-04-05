---
description: Beschreibt die Energierichtlinien Einstellungen, die ein Energie Schema bilden.
ms.assetid: cd515cd6-67f4-45d0-b769-3abc7a56faa8
title: Energierichtlinien Einstellungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f490c758a890faf314be1ddffe9ac7a503bd473
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756571"
---
# <a name="power-policy-settings"></a>Energierichtlinien Einstellungen

Energie Sparpläne und-Schemas bestehen aus Einstellungen und Richtlinien Einstellungen.

Ein Energie Sparplan besteht aus einer Gruppe von Einstellungen für die Energie Einstellung. Diese Einstellungen bestehen sowohl aus einem AC-als auch einem DC-Wert für jede der Energie Einstellungen. Jeder Energie Sparplan wird durch eine eindeutige **GUID** und einen anzeigen Amen identifiziert. Windows Vista verfügt über drei Standard Energie Sparpläne: Energiesparmodus, ausgeglichen und hohe Leistung. Diese Pläne können angepasst werden, und es können weitere Pläne erstellt werden. Alle Energie Sparpläne verfügen über ein Attribut "Personality", das das Gesamtenergie Einsparungs Verhalten des Plans angibt.

In der folgenden Tabelle werden die drei Energie Sparplan-Persönlichkeiten aufgeführt. 

| `Display name`     | BESCHREIBUNG                                                                   | **GUID**                             |
|------------------|-------------------------------------------------------------------------------|--------------------------------------|
| Energiesparmodus      | Bietet eine geringere Leistung, wodurch sich der Energiespar Aufwand erhöhen kann.                | a1841308-3541-4fab-bc81-f71556f20b4a |
| Balanced         | Die Leistung und der Stromverbrauch werden von nach Bedarf automatisch ausgeglichen. | 381b4222-f694-41f0-9685-ff5bb260df2e |
| Hohe Leistung | Bietet eine maximale Leistung bei einem höheren Stromverbrauch.      | 8c5e7lda-e8bf -4a96-9a85-a6e23a8c635c |



 

> [!Note]  
> Geräte, die den [modernen Standby](/windows-hardware/design/device-experiences/modern-standby) -Modus unterstützen, ermöglichen nur den **ausgeglichenen** Energie Sparplan. **Modern Standby** ist die neuere, optimierte Lösung für die Verwaltung von Energie Einstellungen.

 

Jeder Computer verfügt über einen einzigen, aktiven Energie Sparplan. Standardmäßig können nicht berechtigte Benutzer auf System Energie Einstellungen zugreifen. Der Zugriff auf alle oder einzelne Energie Einstellungen kann über ACLs in den Energie Einstellungen oder über Gruppenrichtlinie gesteuert werden. Anwendungen sollten [**powersettingaccesscheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) aufrufen, um zu bestimmen, ob der Benutzer Zugriff auf die Energie Einstellung hat.

Jede Energie Einstellung wird durch eine eindeutige **GUID** gekennzeichnet und enthält einen anzeigen Amen, eine Beschreibung, zulässige Werte und Standardwerte für die AC-und DC-Werte. Benutzerdefinierte Energie Einstellungen können mithilfe der Funktion " [**Power| ateseing"**](/windows/desktop/api/PowrProf/nf-powrprof-powercreatesetting) erstellt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Energie Schemas](power-schemes.md)
</dt> </dl>

 

 
