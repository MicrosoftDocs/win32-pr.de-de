---
title: Code Übersicht
description: Die folgende Abbildung stellt eine konzeptionelle Darstellung der Code Blöcke dar, die zum Implementieren der ADSI-Beispiel Anbieter Komponente erforderlich sind.
ms.assetid: b353c2d9-ef86-4e4c-ac00-4756fc9ec57d
ms.tgt_platform: multiple
keywords:
- Code Übersicht AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e99a4974ac97488fc051ea80dbde7a8a83fa329e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039610"
---
# <a name="code-overview"></a>Code Übersicht

Die folgende Abbildung stellt eine konzeptionelle Darstellung der Code Blöcke dar, die zum Implementieren der ADSI-Beispiel Anbieter Komponente erforderlich sind. Jeder Abschnitt wird in der folgenden Abbildung beschrieben. Erfahrene com-Programmierer können dies als geeignete Übersicht über die Beispiel Anbieter Komponente feststellen. Weitere Informationen finden Sie unter [Code Details](code-details.md).

![Beispiel Anbieter Implementierung](images/dssmco.png)

Die folgenden nummerierten Elemente entsprechen Block Elementen in der Abbildung.

1.  Laden der dll (LibMain. cpp, GUID. cpp). Der Einstiegspunkt für die dll. Klassenfactorydefinitionen statischer Objekt Definitionen für die beiden Anbieter Objekte: GUID. cpp enthält die CLSID-Definitionen für die Implementierungen der verschiedenen Beispiel Anbieter-Komponenten Objekte.
2.  Anbieterobjektklassenfactory und Erstellungs Code (cprovcf. cpp, cprov. cpp, stdfact. cpp). Das Provider-Objekt ist das Objekt, das [**iparamesedisplayname**](/windows/win32/api/oleidl/nn-oleidl-iparsedisplayname) während der monikerbindungsvorgänge unterstützt, wie in suchen und binden in der Beispiel Anbieter Komponente erläutert.
3.  Binden an ein Objekt (getobj. cpp). Mit diesem Code wird der Parser aufgerufen, um zu überprüfen, ob der angegebene ADsPath syntaktisch korrekt ist, und dann alle notwendigen Zuordnungs Vorgänge vom ADsPath zum systemeigenen Verzeichnisdienst Pfad für das als Active Directory Objekt erstellte Element durchführt. Er sucht nach der Schema Definition für diesen Objekttyp und füllt die obligatorischen Eigenschaften aus. Nachdem Sie das Active Directory-Objekt erstellt haben, wird ein Schnittstellen Zeiger auf [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) für den Aufrufer abgerufen.
4.  Parser für den Anbieter Namespace (Parse. cpp). Dies ist der Code, der von Element 3 aufgerufen wird. Der Parser überprüft, ob die Übergabe der ADsPath-Zeichenfolge für einen eigenen Namespace syntaktisch korrekt ist.
5.  Klassenfactory, Erstellung und Enumeration für das Namespace-Objekt (cnamcf. cpp, cnamesp. cpp, cenumns. cpp). Das Namespace-Objekt ist ein Container Objekt, das aufgelistet werden kann, um alle Stamm Knoten Objekte für diesen Namespace zu suchen.
6.  Klassenfactory und Erstellungs Code für ein generisches Active Directory Objekt und eine Klassenfactory, den Erstellungs-und Enumerationscode für ein generisches ADS-Container Objekt (cgenobj. cpp, cenumubj. cpp, Common. cpp, Core. cpp). Dieser Code wird ausgeführt, wenn ein Active Directory Objekt erstellt wird.
7.  Filtern und Auflisten von Varianten (cenumvar. cpp, Object. cpp). Wenn eine Auflistung von Variant-Elementen eines einzelnen Typs innerhalb von ADSI verwaltet wird, wird dieser Code verwendet.
8.  Globals (Globals. cpp). Namespace Schlüsselwörter, Syntax Mapping-Strukturen aus nativen Datenformaten zum Variant-Typ ADS Automation sind hier definiert.
9.  Marshalling/Marshalling von Daten ("Pack. cpp&quot;, &quot;Property. cpp&quot;, &quot;smpoper. cpp"). Die Konvertierung von systemeigenen Datenformaten in den unterstützten Satz von Automatisierungs Varianten Typen tritt auf, wenn die Eigenschaften eines Objekts in den Eigenschafts Cache geladen werden. Es muss eine andere spezielle Verarbeitung für Daten ausgeführt werden, wenn Strukturen mit Zeigern kopiert, gelöscht oder in den Arbeitsspeicher verschoben werden.
10. Eigenschafts Cache (c-Eigenschaften. cpp). Caching-Eigenschaften sind ein Feature der ADSI-Umgebung. Die [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo), [**IADs:: GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex)-Methode und die [**IADs:: abtinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) -Methode agieren auf den Eigenschaften Cache.
11. Speicherverwaltung (Memory. cpp). Die Verwendung eines Satzes von Speicherfunktionen zum Zuordnen und Freigeben von Arbeitsspeicher ermöglicht der Beispiel Anbieter Komponente, die Speicherauslastung zu verfolgen und Speicher Verluste zu verhindern.
12. Schema Objekte und Verwaltung (cschobj. cpp, cprpobj. cpp, cclsobj. cpp, cenumsch. cpp). Dies schließt Routinen zum Erstellen, verwalten und Auflisten der Schema Objekte ein. Dies schließt Schema Klassen Objekte, Eigenschafts Objekte und Syntax Objekte ein und kann nicht nur das Schema Klassen-Container Objekt auflisten.
13. Betriebssystemspezifische Aufrufe (regdsapi. cpp). Dies schließt alle Aufrufe ein, die auf das systemeigene Betriebssystem verweisen. Neben anderen Funktionen umfassen Sie auch Funktionen zum Öffnen, schließen, lesen und Ändern von Objekten sowie zum Zugreifen auf das Schema und die Eigenschafts Daten. Die Beispiel Anbieter Komponente wurde zum Simulieren einer Verzeichnishierarchie mithilfe der Registrierung durchgeführt. Nur Funktionsnamen sollten für einen anbienerwriter von Interesse sein.
14. [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Implementierung (cdispmgr. cpp). Dieser Code greift auf die Typbibliotheks Daten zu, damit Schnittstellen Methoden in einer Automatisierungs kompatiblen Weise aufgerufen werden können.

 

 