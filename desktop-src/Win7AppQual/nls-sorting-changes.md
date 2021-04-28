---
description: NLS-Sortierungsänderungen
ms.assetid: 24617b5f-14f1-4f1b-a288-7d20a8166da0
title: NLS-Sortierungsänderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e57cfaf2a9891c2d952637429786729670fc103c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088058"
---
# <a name="nls-sorting-changes"></a>NLS-Sortierungsänderungen

## <a name="affected-platforms"></a>Betroffene Plattformen

 **Clients:** Windows XP, Windows Vista, Windows 7  
**Server:** Windows Server 2003, Windows Server 2008, Windows Server 2008 R2  










## <a name="feature-impact"></a>Auswirkung von Features

 **Schweregrad:** Hoch  
**Häufigkeit:** Niedrig (nur wenige Apps sind beschädigt, sind jedoch immer beschädigt).  


## <a name="description"></a>BESCHREIBUNG

Die NlS-Funktionen (National Language Support) unterstützen Anwendungen dabei, die verschiedenen sprach- und ortsspezifischen Anforderungen von Benutzern auf der ganzen Welt zu unterstützen. Neue Windows-Versionen enthalten fast immer NLS-Änderungen. Diese Änderung wirkt sich auf die Sortierung und Sortierung aus und somit auf Anwendungen mit persistenten Indizes.

Eine Sortierungstabelle enthält zwei Zahlen, die ihre Version (Revision) identifizieren: die definierte Version und die NLS-Version. Beide Versionen sind DWORD-Werte, die aus einer Hauptversion und einer Nebenversion bestehen. Das erste Byte eines Werts ist reserviert, die nächsten zwei Bytes stellen die Hauptversion dar, und das letzte Byte stellt die Nebenversion dar. Hexadezimal ist das Muster 0xRRMMMMmm, wobei R gleich Reserved, M gleich major und m gleich minor ist. Beispielsweise wird eine Hauptversion von 3 mit einer Nebenversion von 4 als 0x304.

Bei einer Hauptversion ändern sich ein oder mehrere Codepunkte, sodass die Anwendung alle Daten neu indizieren muss, damit Vergleiche gültig sind. Bei einer Nebenversion wird nichts bewegt, aber Codepunkte werden hinzugefügt. Bei dieser Version muss die Anwendung nur Zeichenfolgen mit zuvor nicht amortisierbaren Werten neu indizieren. Zusammengefasst bedeutet dies, was die Versionsnummern in Bezug auf die Datenänderungen in den lokalen Ausnahmetabellen und Standardtabellen bedeuten:

**NLSVersion-Hauptversion:** Geänderte Codepunkte in den "Ausnahme"- oder lokalspezifischen Tabellen  
**NLSVersion-Nebenversion:** Neue Codepunkte in den tabellen "exception" oder "locale-specific" hinzugefügt  
**DefinedVersion Major:** Geänderte Codepunkte in der Standardtabelle  
**DefinedVersion Minor:** Neue Codepunkte in der Standardtabelle hinzugefügt  


**Sortieren von Versionsnummern für veröffentlichte Versionen:**



| Betriebssystem    | Release           | Version (0xRRMMMMmm)         |
|---------------------|-------------------|------------------------------|
| Windows XP          | RTM/SP1/SP2/SP3/... | Nicht verfügbar – keine GetNLSVersion()-API |
| Windows Server 2003 | RTM/SP1           | 0x00 0000 01                 |
| Windows Vista       | RTM/SP1           | 0x00 0405 00                 |
| Windows Server 2008 | RTM               | 0x00 0501 00/0x00 5001 00  |
| Windows 7           | RTM               | 0x00060100                   |



 

## <a name="manifestation"></a>Manifestation

Anwendungen (z. B. Datenbanken) mit persistenten Indizes, die die NLS-Version nicht überprüfen und bei Versionsänderung erneut indizieren, können nicht ordnungsgemäß sortiert werden oder liefern möglicherweise keine angeforderten Ergebnisse.

Bei Benutzeroberflächen können Listen (z. B. alphabetisch, numerisch, alphanumerisch, Symbole und so weiter) falsch sortiert werden.

## <a name="solution"></a>Lösung

Ihre Anwendung kann **entweder GetNLSVersionEx** (Windows Vista oder höher) oder **GetNLSVersion** (vor Windows Vista) aufrufen, um sowohl die definierte Version als auch die NLS-Version für eine Sortierungstabelle abzurufen.

-   GetNLSVersionEx:

*Ruft Informationen zur aktuellen Version einer angegebenen NLS-Funktion für ein durch den Namen angegebenes Gebietsschema ab.*  
Mit dieser Funktion kann eine Anwendung wie Active Directory bestimmen, ob sich eine NLS-Änderung auf das gebietsschema auswirkt, das für eine bestimmte Indextabelle verwendet wird. Wenn dies nicht dere ist, ist es nicht erforderlich, die Tabelle neu zu indizieren. Weitere Informationen finden Sie unter Behandeln von Gebietsschema- und Sprachinformationen.  
Diese Funktion unterstützt benutzerdefinierte Gebietsschemas. Wenn *lpLocaleName* ein zusätzliches Gebietsschema angibt, sind die abgerufenen Daten die richtigen Daten für die Sortierungsreihenfolge, die diesem ergänzenden Gebietsschema zugeordnet ist.  

**Hinweis:** Versionen von Windows vor Windows Vista unterstützen **GetNLSVersionEx** nicht.  


-   GetNLSVersion (wird für Anwendungen verwendet, die unter Windows-Versionen vor Windows Vista ausgeführt werden):

*Ruft Informationen zur aktuellen Version einer angegebenen NLS-Funktion für ein gebietsschema ab, das durch bezeichner angegeben wird.*  
Mit dieser Funktion kann eine Anwendung wie Active Directory bestimmen, ob sich eine NLS-Änderung auf den Gebietsschemabezeichner auswirkt, der für eine bestimmte Indextabelle verwendet wird. Wenn dies nicht dere ist, ist es nicht erforderlich, die Tabelle neu zu indizieren. Weitere Informationen finden Sie unter Behandeln von Gebietsschema- und Sprachinformationen.  
**Hinweis:** Diese Funktion ruft nur Informationen zu einem gebietsschema ab, das vom Bezeichner angegeben wird. Die **GetNLSVersionEx-Funktion** unterstützt zusätzliche Gebietsschemas, Features und RFC 4646-Namen. Versionen von Windows vor Windows Vista unterstützen **getNLSVersionEx** jedoch nicht.  
Anwendungen, die nur unter Windows Vista und höher ausgeführt werden sollen, sollten **GetNLSVersionEx** vor dieser Funktion verwenden. **GetNLSVersionEx** bietet gute Unterstützung für zusätzliche Gebietsschemas.  


## <a name="compatibility-test"></a>Kompatibilitätstest

**Schritte, mit denen Sie feststellen können, ob sich eine Sortierungsversion geändert hat (d. b. sie müssen neu indiziert werden):**

-   **Verwenden Sie GetNLSVersionEx(),** um eine **NLSVERSIONINFOEX-Struktur** abzurufen, wenn Sie die ursprüngliche Indizierung Ihrer Daten durchführen.
-   Speichern Sie die folgenden Eigenschaften mit Ihrem Index, um die Version zu identifizieren:  **NLSVERSIONINFOEX.dwNLSVersion** und **NLSVERSIONINFOEX.dwDefinedVersion–** Diese beiden Eigenschaften geben zusammen die Version der von Ihnen verwendeten Sortiertabelle an.  
    **NLSVERSIONINFOEX.dwEffectiveId: Gibt** das effektive Locale Ihrer Sortierung an. Ein benutzerdefiniertes Locale wird auf die Sortierreihenfolge eines In-Box-Locales verweisen.  
    
-   Wenn Sie den Index verwenden, **verwenden Sie GetNlsVersionEx(),** um die Version Ihrer Daten zu finden.
-   Wenn sich eine der drei Eigenschaften geändert hat, können die von Ihnen verwendeten Sortierdaten unterschiedliche Ergebnisse zurückgeben, und jede Indizierung, die Sie erstellt haben, kann zu einem Fehler bei der Suche nach Datensätzen führen.
-   Wenn Sie wissen, dass Ihre Daten keine ungültigen Unicode-Codepunkte enthalten (d. h. alle Zeichenfolgen, die **true** von einem Aufruf von **IsNLSDefinedString() zurückgegeben** haben), können Sie sie als identisch betrachten, wenn SICH NUR das niedrige Byte von **dwNLSVersion** und **dwDefinedVersion** geändert hat (die oben beschriebenen Nebenversionen).

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

-   [Internationalisierung für Windows-Anwendungen](../intl/international-support.md)
-   [GetNLSVersionEx-Funktion](/windows/win32/api/winnls/nf-winnls-getnlsversionex)
-   [GetNLSVersion-Funktion](/windows/win32/api/winnls/nf-winnls-getnlsversion)
-   [Erkennen, ob sich die Sortierungsversion geändert hat](/archive/blogs/shawnste/)

 

 
