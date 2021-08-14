---
title: Codeübersicht
description: Die folgende Abbildung ist eine konzeptionelle Darstellung der Codeblöcke, die zum Implementieren der ADSI-Beispielanbieterkomponente erforderlich sind.
ms.assetid: b353c2d9-ef86-4e4c-ac00-4756fc9ec57d
ms.tgt_platform: multiple
keywords:
- Codeübersicht AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc23f4a3a51c33f24748347a2941bc09dbda8bc3bd99d133f99d0377eb0bda90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118017725"
---
# <a name="code-overview"></a>Codeübersicht

Die folgende Abbildung ist eine konzeptionelle Darstellung der Codeblöcke, die zum Implementieren der ADSI-Beispielanbieterkomponente erforderlich sind. Jeder Abschnitt wird in der folgenden Abbildung beschrieben. Erfahrene COM-Programmierer finden, dass dies eine geeignete Übersicht über die Beispielanbieterkomponente ist. Weitere Informationen finden Sie unter [Codedetails.](code-details.md)

![Beispielanbieterimplementierungen](images/dssmco.png)

Die folgenden nummerierten Elemente entsprechen Blockelementen in der Abbildung.

1.  Laden der DLL (Libmain.cpp, Guid.cpp). Der Einstiegspunkt für die DLL. Statische Objektdefinitionen der Klassenfactory für die beiden Anbieterobjekte: Guid.cpp enthält die CLSID-Definitionen für die Implementierungen der verschiedenen Beispielanbieterkomponentenobjekte.
2.  Anbieterobjektklassenfactory und Erstellungscode (Cprovcf.cpp, Cprov.cpp, Stdfact.cpp). Das Anbieterobjekt ist das Objekt, das [**IParseDisplayName**](/windows/win32/api/oleidl/nn-oleidl-iparsedisplayname) während der Monikerbindungsvorgänge unterstützt, wie unter Suchen und Binden in der Beispielanbieterkomponente erläutert.
3.  Binden an ein Objekt (Getobj.cpp). Dieser Code ruft den Parser auf, um zu überprüfen, ob der angegebene ADsPath syntaktisch korrekt ist, und führt dann alle erforderlichen Zuordnungen vom ADsPath zum systemeigenen Verzeichnisdienstpfad für das Element aus, das als Active Directory-Objekt erstellt wird. Er sucht die Schemadefinition für diesen Objekttyp und füllt die obligatorischen Eigenschaften aus. Nach dem Erstellen des Active Directory-Objekts wird ein Schnittstellenzeiger auf [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) für den Aufrufer abgerufen.
4.  Parser für den Anbieternamespace (Parse.cpp). Dies ist der Code, der von Element 3 aufgerufen wird. Der Parser überprüft, ob die übergebene ADsPath-Zeichenfolge syntaktisch für ihren eigenen Namespace korrekt ist.
5.  Klassenfactory, Erstellung und Enumeration für das Namespaceobjekt (Cnamcf.cpp, Cnamesp.cpp, Cenumns.cpp). Das Namespaceobjekt ist ein Containerobjekt, das aufzählt werden kann, um alle Stammknotenobjekte für diesen Namespace zu finden.
6.  Klassenfactory und Erstellungscode für ein generisches Active Directory-Objekt und Klassenfactory, Erstellungs- und Enumerationscode für ein generisches ADs-Containerobjekt (Cgenobj.cpp, Cenumobj.cpp, Common.cpp, Core.cpp). Dieser Code wird ausgeführt, wenn ein Active Directory-Objekt erstellt wird.
7.  Filtern und Aufzählen von VLVATs (Cenumvar.cpp, Object.cpp). Wenn eine Auflistung von VARIANT-Elementen eines einzelnen Typs in in ADSI verwaltet wird, wird dieser Code verwendet.
8.  Globals (Globals.cpp). Namespaceschlüsselwörter und Syntaxzuordnungsstrukturen aus nativen Datenformaten zum VARIANT-Typ von ADs Automation sind hier definiert.
9.  Marshalling/Unmarshaling von Daten (Pack.cpp, Property.cpp, Smpoper.cpp). Die Konvertierung von nativen Datenformaten in den unterstützten Satz von Automation VARIANT-Typen erfolgt, wenn Eigenschaften eines Objekts in den Eigenschaftencache geladen werden. Wenn Strukturen mit Zeigern kopiert, gelöscht oder in den Arbeitsspeicher verschoben werden, muss eine andere spezielle Behandlung für Daten durchgeführt werden.
10. Eigenschaftencache (Cprops.cpp). Das Zwischenspeichern von Eigenschaften ist ein Feature der ADSI-Umgebung. Die [**Methoden IADs::GetInfo,**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) [**IADs::GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex)und [**IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) fungieren für den Eigenschaftencache.
11. Speicherverwaltung (Memory.cpp). Die Verwendung eines Satzes von Arbeitsspeicherfunktionen zum Zuordnen und Freigeben von Arbeitsspeicher ermöglicht es der Beispielanbieterkomponente, die Speichernutzung nachzuverfolgen und Speicherverluste zu beenden.
12. Schemaobjekte und -verwaltung (Cschobj.cpp, Cprpobj.cpp, Cclsobj.cpp, Cenumsch.cpp). Dies schließt Routinen zum Erstellen, Verwalten und Aufzählen der Schemaobjekte ein. Dazu gehören Schemaklassenobjekte, Eigenschaftenobjekte und Syntaxobjekte sowie die Möglichkeit, das Containerobjekt der Schemaklasse aufzuzählen.
13. Betriebssystemspezifische Aufrufe (RegDSAPI.cpp). Dies schließt alle Aufrufe ein, die auf das native Betriebssystem verweisen. Zu diesen Funktionen gehören neben anderen Funktionen das Öffnen, Schließen, Lesen und Ändern von Objekten sowie funktionen, die auf schema- und eigenschaftsdaten zugreifen. Die Beispielanbieterkomponente simulierte eine Verzeichnishierarchie mithilfe der Registrierung. Nur Funktionsnamen sollten für einen Anbieterwriter von großem Interesse sein.
14. [**IDispatch-Implementierung**](/windows/win32/api/oaidl/nn-oaidl-idispatch) (Cdispmgr.cpp). Dieser Code greift auf die Typbibliotheksdaten zu, damit Schnittstellenmethoden auf automatisierungskompatible Weise aufgerufen werden können.

 

 