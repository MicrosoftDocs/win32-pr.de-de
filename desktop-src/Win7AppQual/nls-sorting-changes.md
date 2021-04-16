---
description: .
ms.assetid: 24617b5f-14f1-4f1b-a288-7d20a8166da0
title: NLS-Sortier Änderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0805eae753c1e312d26f8c84e13d19041458cf26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530146"
---
# <a name="nls-sorting-changes"></a>NLS-Sortier Änderungen

## <a name="affected-platforms"></a>Betroffene Plattformen

 **Clients** -Windows XP \| Windows Vista \| Windows 7  
**Server** -Windows Server 2003 \| Windows Server 2008 \| Windows Server 2008 R2  










## <a name="feature-impact"></a>Auswirkungen von Features

 **Schweregrad** -hoch  
**Häufigkeit** -niedrig (wenige apps betroffen, aber wenn betroffen, immer beschädigt)  


## <a name="description"></a>BESCHREIBUNG

Mithilfe der NLS-Funktionen (National Language Support) unterstützen Anwendungen die verschiedenen Sprach-und Gebiets Schema spezifischen Anforderungen von Benutzern auf der ganzen Welt. Neue Windows-Versionen enthalten fast ausnahmslos nls-Änderungen. Diese Änderung wirkt sich auf Sortierung und Sortierung aus, und damit auf Anwendungen mit permanenten Indizes.

Eine Sortierungs Tabelle verfügt über zwei Zahlen, die Ihre Version (Revision) identifizieren: die definierte Version und die NLS-Version. Beide Versionen sind DWORD-Werte, die aus einer Hauptversion und einer neben Version bestehen. Das erste Byte eines Werts ist reserviert, die nächsten zwei Bytes stellen die Hauptversion dar, und das letzte Byte stellt die neben Version dar. In hexadezimalen begriffen ist das Muster "0xrrmmmmmm", wobei "R" reserviert ist, "m" den Wert "Major" und "m" kleiner ist. Beispielsweise wird eine Hauptversion von 3 mit einer neben Version von 4 als 0x304 dargestellt.

Bei einer Hauptversion wird ein oder mehrere Code Punkte geändert, sodass die Anwendung alle Daten neu indizieren muss, damit Vergleiche gültig sind. Bei einer neben Version wird nichts verschoben, aber es werden Code Punkte hinzugefügt. Bei dieser Art von Version muss die Anwendung nur Zeichen folgen mit zuvor nicht sortierbar-Werten neu indizieren. Im folgenden finden Sie eine Zusammenfassung der Versionsnummern in Bezug auf die Datenänderungen in den Gebiets Schema spezifischen Ausnahme Tabellen und Standard Tabellen:

**Nlsversion Major** – geänderte Code Punkte in den "Exception"-oder "Locale-Specific"-Tabellen  
**Nlsversion Minor** – neue Code Punkte in den "Exception"-oder "Locale-Specific"-Tabellen hinzugefügt  
**Definedversion Major** – geänderte Code Punkte in der Standardtabelle  
**Definedversion Minor** – neue Code Punkte in der Standardtabelle hinzugefügt  


**Sortieren von Versionsnummern für veröffentlichte Versionen:**



| Betriebssystem    | Release           | Version (0xrrmmmmmm)         |
|---------------------|-------------------|------------------------------|
| Windows XP          | RTM/SP1/SP2/SP3/... | N/v-keine getnlsversion ()-API |
| Windows Server 2003 | RTM/SP1           | 0x00 0000 01                 |
| Windows Vista       | RTM/SP1           | 0x00 0405 00                 |
| Windows Server 2008 | RTM               | 0x00 0501 00/0x00 5001 00  |
| Windows 7           | RTM               | 0x00060100                   |



 

## <a name="manifestation"></a>Ausstrahlung

Anwendungen (z. b. Datenbanken) mit permanenten Indizes, die die NLS-Version nicht überprüfen und bei der Versionsänderung neu indizieren, können nicht ordnungsgemäß sortiert werden oder die angeforderten Ergebnisse nicht bereitstellen.

Im Fall von Benutzeroberflächen können Listen (z. b. alphabetisch, numerisch, alphanumerisch, Symbole usw.) falsch sortiert werden.

## <a name="solution"></a>Lösung

Die Anwendung kann entweder **GetNLSVersionEx** (Windows Vista oder höher) oder **getnlsversion** (vor Windows Vista) aufrufen, um sowohl die definierte Version als auch die NLS-Version für eine Sortierungs Tabelle abzurufen.

-   GetNLSVersionEx:

*Ruft Informationen über die aktuelle Version einer angegebenen nls-Funktion für ein durch den Namen angegebenes Gebiets Schema ab.*  
Mit dieser Funktion kann eine Anwendung wie Active Directory bestimmen, ob sich eine NLS-Änderung auf das für eine bestimmte Indextabelle verwendete Gebiets Schema auswirkt. Wenn dies nicht der Fall ist, muss die Tabelle nicht neu indiziert werden. Weitere Informationen finden Sie unter Behandeln von Gebiets Schema-und Sprachinformationen.  
Diese Funktion unterstützt benutzerdefinierte Gebiets Schemas. Wenn *lplocalename* ein zusätzliches Gebiets Schema angibt, sind die abgerufenen Daten die richtigen Daten für die Sortierreihenfolge, die dem ergänzenden Gebiets Schema zugeordnet ist.  

**Hinweis:** Von Windows-Versionen vor Windows Vista wird **GetNLSVersionEx** nicht unterstützt.  


-   Getnlsversion (Verwendung für Anwendungen, die auf Windows-Versionen vor Windows Vista ausgeführt werden):

*Ruft Informationen über die aktuelle Version einer angegebenen nls-Funktion für ein durch den Bezeichner festgelegtes Gebiets Schema ab.*  
Diese Funktion ermöglicht es einer Anwendung, wie z. b. Active Directory, festzustellen, ob eine NLS-Änderung den für eine bestimmte Indextabelle verwendeten Gebiets Schema Bezeichner beeinflusst Wenn dies nicht der Fall ist, muss die Tabelle nicht neu indiziert werden. Weitere Informationen finden Sie unter Behandeln von Gebiets Schema-und Sprachinformationen.  
**Hinweis:** Diese Funktion ruft nur Informationen über ein durch den Bezeichner festgelegtes Gebiets Schema ab. Die **GetNLSVersionEx** -Funktion unterstützt zusätzliche Gebiets Schemata, Features und RFC 4646-Namen. Allerdings wird von Windows-Versionen vor Windows Vista **GetNLSVersionEx** nicht unterstützt.  
Anwendungen, die nur unter Windows Vista und höher ausgeführt werden sollen, sollten **GetNLSVersionEx** für diese Funktion verwenden. **GetNLSVersionEx** bietet eine gute Unterstützung für zusätzliche Gebiets Schemas.  


## <a name="compatibility-test"></a>Kompatibilitäts Test

**Schritte, um zu ermitteln, ob eine Sortierungs Version geändert wurde (d. h., Sie müssen den Index neu indizieren):**

-   **Verwenden Sie GetNLSVersionEx ()** , um eine **nlsversioninfoex** -Struktur abzurufen, wenn Sie die ursprüngliche Indizierung Ihrer Daten durchführen.
-   Speichern Sie die folgenden Eigenschaften mit Ihrem Index, um die Version zu identifizieren:  **nlsversioninfoex. dwnlsversion** und **nlsversioninfoex. dwdefinedversion** – diese beiden Eigenschaften geben die Version der Sortier Tabelle an, die Sie verwenden.  
    **Nlsversioninfoex. dweffectiveid** : gibt das effektive Gebiets Schema Ihrer Sortierreihenfolge an. Ein benutzerdefiniertes Gebiets Schema verweist auf die Sortierung eines in Box-Box-Schemas.  
    
-   Wenn Sie den Index verwenden, verwenden Sie **GetNLSVersionEx ()** , um die Version der Daten zu ermitteln.
-   Wenn eine der drei Eigenschaften geändert wurde, können die von Ihnen verwendeten Sortier Daten andere Ergebnisse zurückgeben, und jede Indizierung kann möglicherweise keine Datensätze finden.
-   Wenn Sie wissen, dass Ihre Daten keine ungültigen Unicode-Code Punkte enthalten (d. h., alle Zeichen folgen werden von einem **IsNLSDefinedString ()-IsNLSDefinedString**-Befehl als " **true** " zurückgegeben), dann können Sie diese identisch sein, wenn nur das niedrige Byte von **dwnlsversion** und **dwdefinedversion** geändert wurde

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

-   [Internationalisierung für Windows-Anwendungen](../intl/international-support.md)
-   [GetNLSVersionEx-Funktion](/windows/win32/api/winnls/nf-winnls-getnlsversionex)
-   [Getnlsversion-Funktion](/windows/win32/api/winnls/nf-winnls-getnlsversion)
-   [Erkennen, ob die Sortierungs Version geändert wurde](/archive/blogs/shawnste/)

 

 
