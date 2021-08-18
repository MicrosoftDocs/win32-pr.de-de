---
description: NLS-Sortierungsänderungen
ms.assetid: 24617b5f-14f1-4f1b-a288-7d20a8166da0
title: NLS-Sortierungsänderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a08f0cde98d115c129fdb7932ff3bb05063cb5c6fb8d903d55bff2a69753d774
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994880"
---
# <a name="nls-sorting-changes"></a>NLS-Sortierungsänderungen

## <a name="affected-platforms"></a>Betroffene Plattformen

 **Clients–** Windows XP, Windows Vista, Windows 7  
**Server** – Windows Server 2003, Windows Server 2008, Windows Server 2008 R2  










## <a name="feature-impact"></a>Auswirkung von Features

 **Schweregrad:** Hoch  
**Häufigkeit:** Niedrig (nur wenige Apps sind beschädigt, sind aber immer beschädigt, wenn sie nicht mehr verfügbar sind)  


## <a name="description"></a>BESCHREIBUNG

Die NlS-Funktionen (National Language Support) unterstützen Anwendungen dabei, die verschiedenen sprach- und ortsspezifischen Anforderungen von Benutzern auf der ganzen Welt zu unterstützen. Neue Windows enthalten fast immer NLS-Änderungen. Diese Änderung wirkt sich auf die Sortierung und Sortierung aus und somit auf Anwendungen, die persistente Indizes haben.

Eine Sortierungstabelle enthält zwei Zahlen, die ihre Version (Revision) identifizieren: die definierte Version und die NLS-Version. Beide Versionen sind DWORD-Werte, die aus einer Hauptversion und einer Nebenversion bestehen. Das erste Byte eines Werts ist reserviert, die nächsten zwei Bytes stellen die Hauptversion dar, und das letzte Byte stellt die Nebenversion dar. Hexadezimal ist das Muster 0xRRMMMMmm, wobei R gleich Reserved, M gleich major und m gleich minor ist. Beispielsweise wird eine Hauptversion von 3 mit einer Nebenversion von 4 als 0x304.

Bei einer Hauptversion ändern sich ein oder mehrere Codepunkte, sodass die Anwendung alle Daten erneut indizieren muss, damit Vergleiche gültig sind. Bei einer Nebenversion wird nichts bewegt, aber Codepunkte werden hinzugefügt. Bei dieser Version muss die Anwendung nur Zeichenfolgen mit zuvor nicht amortisierbaren Werten neu indizieren. Zusammengefasst bedeutet dies, was die Versionsnummern in Bezug auf die Datenänderungen in den lokalen Ausnahmetabellen und Standardtabellen bedeuten:

**NLSVersion-Hauptversion:** Geänderte Codepunkte in den "Ausnahme"- oder lokalspezifischen Tabellen  
**NLSVersion-Nebenversion:** Neue Codepunkte wurden in den Tabellen "exception" oder "locale-specific" hinzugefügt.  
**DefinedVersion Major:** Geänderte Codepunkte in der Standardtabelle  
**DefinedVersion Minor:** Neue Codepunkte in der Standardtabelle hinzugefügt  


**Sortieren von Versionsnummern für veröffentlichte Versionen:**



| Betriebssystem    | Freigabe           | Version (0xRRMMMMmm)         |
|---------------------|-------------------|------------------------------|
| Windows XP          | RTM/SP1/SP2/SP3/... | Nicht verfügbar – keine GetNLSVersion()-API |
| Windows Server 2003 | RTM/SP1           | 0x00 0000 01                 |
| Windows Vista       | RTM/SP1           | 0x00 0405 00                 |
| Windows Server 2008 | RTM               | 0x00 0501 00/0x00 5001 00  |
| Windows 7           | RTM               | 0x00060100                   |



 

## <a name="manifestation"></a>Manifestation

Anwendungen (z. B. Datenbanken) mit persistenten Indizes, die die NLS-Version nicht überprüfen und bei Versionsänderung erneut indizieren, können nicht ordnungsgemäß sortiert werden oder die angeforderten Ergebnisse nicht bereitstellen.

Bei Benutzeroberflächen können Listen (z. B. alphabetisch, numerisch, alphanumerisch, Symbole und so weiter) falsch sortiert werden.

## <a name="solution"></a>Lösung

Ihre Anwendung kann **entweder GetNLSVersionEx** (Windows Vista oder höher) oder **GetNLSVersion** (vor Windows Vista) aufrufen, um sowohl die definierte Version als auch die NLS-Version für eine Sortierungstabelle abzurufen.

-   GetNLSVersionEx:

*Ruft Informationen zur aktuellen Version einer angegebenen NLS-Funktion für ein durch den Namen angegebenes Locale ab.*  
Mit dieser Funktion kann eine Anwendung wie Active Directory bestimmen, ob eine NLS-Änderung auswirkungen auf das für eine bestimmte Indextabelle verwendete Locale hat. Wenn dies nicht der Grund ist, ist es nicht notwendig, die Tabelle erneut zu indizieren. Weitere Informationen finden Sie unter Handling Locale and Language Information.  
Diese Funktion unterstützt benutzerdefinierte Locales. Wenn *lpLocaleName* ein zusätzliches Locale angibt, sind die abgerufenen Daten die richtigen Daten für die Sortierungsreihen reihenfolge, die diesem zusätzlichen Locale zugeordnet ist.  

**Hinweis:** Versionen von Windows vor Windows Vista unterstützen **GetNLSVersionEx nicht.**  


-   GetNLSVersion (wird für Anwendungen verwendet, die in Versionen von Windows vor Windows Vista ausgeführt werden):

*Ruft Informationen zur aktuellen Version einer angegebenen NLS-Funktion für ein durch den Bezeichner angegebenes Locale ab.*  
Mit dieser Funktion kann eine Anwendung wie Active Directory bestimmen, ob eine NLS-Änderung den für eine bestimmte Indextabelle verwendeten Locale Identifier beeinflusst. Wenn dies nicht der Grund ist, ist es nicht notwendig, die Tabelle erneut zu indizieren. Weitere Informationen finden Sie unter Handling Locale and Language Information.  
**Hinweis:** Diese Funktion ruft nur Informationen zu einem durch den Bezeichner angegebenen Locale ab. Die **GetNLSVersionEx-Funktion** unterstützt zusätzliche Locales, Features und RFC 4646-Namen. Allerdings unterstützen Versionen von Windows vor Windows Vista **getNLSVersionEx nicht.**  
Anwendungen, die nur unter Windows Vista und höher ausgeführt werden sollen, sollten **GetNLSVersionEx** vor dieser Funktion verwenden. **GetNLSVersionEx bietet** gute Unterstützung für zusätzliche Locales.  


## <a name="compatibility-test"></a>Kompatibilitätstest

**Schritte, um zu erkennen, ob sich eine Sortierungsversion geändert hat (d. h., Sie müssen die Indizierung erneut durchführen):**

-   **Verwenden Sie GetNLSVersionEx(),** um eine **NLSVERSIONINFOEX-Struktur** abzurufen, wenn Sie die ursprüngliche Indizierung Ihrer Daten verwenden.
-   Store die folgenden Eigenschaften mit Ihrem Index, um die Version zu identifizieren: **NLSVERSIONINFOEX.dwNLSVersion** und **NLSVERSIONINFOEX.dwDefinedVersion–** Diese beiden Eigenschaften geben zusammen die Version der von Ihnen verwendeten Sortiertabelle an.  
    **NLSVERSIONINFOEX.dwEffectiveId: Gibt** das effektive Locale Ihrer Sortierung an. Ein benutzerdefiniertes Locale wird auf die Sortierreihenfolge eines In-Box-Locales verweisen.  
    
-   Wenn Sie den Index verwenden, **verwenden Sie GetNlsVersionEx(),** um die Version Ihrer Daten zu finden.
-   Wenn sich eine der drei Eigenschaften geändert hat, können die von Ihnen verwendeten Sortierdaten unterschiedliche Ergebnisse zurückgeben, und jede Indizierung, die Sie erstellt haben, kann zu einem Fehler bei der Suche nach Datensätzen führen.
-   Wenn Sie wissen, dass Ihre Daten keine ungültigen Unicode-Codepunkte enthalten (d. h. alle Zeichenfolgen, die **TRUE** von einem Aufruf von **IsNLSDefinedString()** zurückgegeben haben), können Sie sie als identisch betrachten, wenn SICH NUR das niedrige Byte von **dwNLSVersion** und **dwDefinedVersion** geändert hat (die oben beschriebenen Nebenversionen).

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

-   [Internationalisierung für Windows-Anwendungen](../intl/international-support.md)
-   [GetNLSVersionEx-Funktion](/windows/win32/api/winnls/nf-winnls-getnlsversionex)
-   [GetNLSVersion-Funktion](/windows/win32/api/winnls/nf-winnls-getnlsversion)
-   [Erkennen, ob sich die Sortierungsversion geändert hat](/archive/blogs/shawnste/)

 

 
