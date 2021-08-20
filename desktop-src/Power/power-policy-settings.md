---
description: Beschreibt die Energierichtlinieneinstellungen, die ein Energieschema bilden.
ms.assetid: cd515cd6-67f4-45d0-b769-3abc7a56faa8
title: Power Policy Einstellungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43f8c0dbd4c7f2a27b6e6b96528c689c6609c175eded58a1de625af71e965f37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674310"
---
# <a name="power-policy-settings"></a>Power Policy Einstellungen

Energiesparpläne und -schemas bestehen aus Einstellungen und Richtlinieneinstellungen.

Ein Energiesparplan besteht aus einer Gruppe von Energieeinstellungseinstellungen. Diese Einstellungen bestehen sowohl aus einem Ac- als auch einem DC-Wert für jede der Energieeinstellungen. Jeder Energiesparplan wird durch eine eindeutige **GUID** und einen Anzeigenamen identifiziert. Windows Vista verfügt über drei Standard-Energiesparpläne: Power Saver, Balanced und High Performance. Diese Pläne können angepasst und zusätzliche Pläne erstellt werden. Alle Energiesparpläne verfügen über ein Persönlichkeitsattribut, das das allgemeine Energiesparverhalten des Plans angibt.

In der folgenden Tabelle sind die drei Energiesparplan-Persönlichkeiten aufgeführt. 

| `Display name`     | BESCHREIBUNG                                                                   | **GUID**                             |
|------------------|-------------------------------------------------------------------------------|--------------------------------------|
| Power Saver      | Bietet eine geringere Leistung, was die Stromeinsparungen erhöhen kann.                | a1841308-3541-4fab-bc81-f71556f20b4a |
| Balanced         | Gleicht Leistung und Stromverbrauch automatisch nach Bedarf aus. | 381b4222-f694-41f0-9685-ff5bb260df2e |
| Hohe Leistung | Bietet maximale Leistung auf Kosten eines höheren Energieverbrauchs.      | 8c5e7fda-e8bf-4a96-9a85-a6e23a8c635c |



 

> [!Note]  
> Geräte, die den [modernen Standbymodus](/windows-hardware/design/device-experiences/modern-standby) unterstützen, lassen nur den Energiesparplan **Balanced** zu. **Modern Standby** ist die neuere, optimierte Lösung für die Energieeinstellungsverwaltung.

 

Jeder Computer verfügt über einen einzelnen aktiven Energiesparplan. Standardmäßig können nicht berechtigte Benutzer auf Energieeinstellungen des Systems zugreifen. Der Zugriff auf alle oder einzelne Energieeinstellungen kann über ACLs in den Energieeinstellungen oder über Gruppenrichtlinie gesteuert werden. Anwendungen sollten [**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) aufrufen, um zu bestimmen, ob der Benutzer Zugriff auf die Energieeinstellung hat.

Jede Energieeinstellung wird durch eine eindeutige **GUID** identifiziert und enthält einen Anzeigenamen, eine Beschreibung, zulässige Werte und Standardwerte für AC und DC. Benutzerdefinierte Energieeinstellungen können mithilfe der [**PowerCreateSetting-Funktion**](/windows/desktop/api/PowrProf/nf-powrprof-powercreatesetting) erstellt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Energieschemas](power-schemes.md)
</dt> </dl>

 

 
