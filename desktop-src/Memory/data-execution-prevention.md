---
description: Die Daten Ausführungs Verhinderung (Data Execution Prevention, DEP) ist ein Feature zum Schutz von Arbeitsspeicher auf Systemebene, das in das Betriebssystem integriert ist, beginnend mit Windows XP und Windows Server 2003.
ms.assetid: 75cd83a5-4b77-4ca9-b595-e32d0dd609d0
title: Datenausführungsverhinderung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bc53febb383ef2789c2798b091960c2d20856d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106373030"
---
# <a name="data-execution-prevention"></a>Datenausführungsverhinderung

Die Daten Ausführungs Verhinderung (Data Execution Prevention, DEP) ist ein Feature zum Schutz von Arbeitsspeicher auf Systemebene, das in das Betriebssystem integriert ist, beginnend mit Windows XP und Windows Server 2003. DEP ermöglicht dem System, eine oder mehrere Seiten des Arbeitsspeichers als nicht ausführbare Datei zu markieren. Das Markieren von Speicherbereichen als nicht ausführbare Datei bedeutet, dass Code nicht von diesem Bereich des Arbeitsspeichers aus ausgeführt werden kann, was die Ausnutzung von Pufferüberläufen erschwert.

DEP verhindert, dass Code von Datenseiten ausgeführt wird, wie z. b. der Standard Heap, Stapel und Speicherpools. Wenn eine Anwendung versucht, Code auf einer geschützten Datenseite auszuführen, tritt eine Ausnahme aufgrund einer Speicherzugriffs Verletzung auf, und wenn die Ausnahme nicht behandelt wird, wird der aufrufende Prozess beendet.

DEP ist nicht als umfassende Verteidigung gegen alle Exploits vorgesehen. Es ist ein weiteres Tool, das Sie zum Sichern Ihrer Anwendung verwenden können.

## <a name="how-data-execution-prevention-works"></a>Funktionsweise der Daten Ausführungs Verhinderung

Wenn eine Anwendung versucht, Code von einer geschützten Seite auszuführen, empfängt die Anwendung eine Ausnahme mit der Statuscode **Status- \_ Zugriffs \_ Verletzung**. Wenn die Anwendung Code von einer Arbeitsspeicher Seite ausführen muss, muss Sie die richtigen Attribute für den [Schutz](memory-protection.md) von virtuellen Arbeitsspeicher zuordnen und festlegen. Der zugeordnete Arbeitsspeicher muss als " **Seite \_ Ausführen**", " **Seite \_ Ausführen \_ Lesen**", " **Seite \_ Ausführen \_**" "lesen" oder "Schreiben von **Seiten \_ Ausführen \_** " beim belegen von Speicher gekennzeichnet sein Heap Zuweisungen, die durch den Aufruf der Funktionen **malloc** und [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) vorgenommen werden, sind nicht ausführbare Dateien.

Anwendungen können keinen Code aus dem Standardprozess Heap oder dem Stapel ausführen.

DEP wird beim Systemstart gemäß der Einstellung "No-Execute Page Protection Policy" in den Start Konfigurationsdaten konfiguriert. Eine Anwendung kann die aktuelle Richtlinien Einstellung abrufen, indem Sie die [**getsystemdeppolicy**](/windows/desktop/api/WinBase/nf-winbase-getsystemdeppolicy) -Funktion aufrufen. Abhängig von der Richtlinien Einstellung kann eine Anwendung die DEP-Einstellung für den aktuellen Prozess ändern, indem Sie die Funktion [**setprocessdeppolicy**](/windows/desktop/api/WinBase/nf-winbase-setprocessdeppolicy) aufruft.

## <a name="programming-considerations"></a>Überlegungen zur Programmierung

Eine Anwendung kann die [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) -Funktion verwenden, um ausführbaren Arbeitsspeicher mit den entsprechenden Speicherschutz Optionen zuzuordnen. Es wird empfohlen, dass ein Anwendungs Satz mindestens die Option zum **\_ Ausführen** des Speicher Schutzes auf der Seite ist. Nachdem der ausführbare Code generiert wurde, empfiehlt es sich, dass die Anwendung den Speicherschutz so festlegen, dass der Schreibzugriff auf den zugewiesenen Speicher nicht zulässig ist. Anwendungen können den Schreibzugriff auf zugeordneten Speicher mithilfe der [**VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect) -Funktion nicht zulassen. Das Zulassen des Schreibzugriffs gewährleistet einen maximalen Schutz für ausführbare Bereiche des Prozess Adressraums. Sie sollten versuchen, Anwendungen zu erstellen, die den kleinsten ausführbaren, ausführbaren Adressraum verwenden. Dadurch wird die Menge an Arbeitsspeicher minimiert, die für die Speicher Ausnutzung verfügbar ist.

Außerdem sollten Sie versuchen, das Layout des virtuellen Speichers Ihrer Anwendung zu steuern und ausführbare Bereiche zu erstellen. Diese ausführbaren Bereiche sollten sich in einem geringeren Speicherplatz als nicht ausführbare Bereiche befinden. Durch die Suche nach ausführbaren Regionen unterhalb nicht ausführbarer Bereiche können Sie verhindern, dass ein Pufferüberlauf in den ausführbaren Bereich des Arbeitsspeichers übertragen wird.

## <a name="application-compatibility"></a>Anwendungskompatibilität

Einige Anwendungsfunktionen sind mit DEP nicht kompatibel. Anwendungen, die eine dynamische Codegenerierung ausführen (z. b. Just-in-Time-Codegenerierung) und generierten Code nicht explizit mit EXECUTE-Berechtigung markieren, haben möglicherweise Kompatibilitätsprobleme auf Computern, die DEP verwenden. Anwendungen, die in die Active Template Library (ATL) Version 7,1 und früher geschrieben wurden, können versuchen, Code auf Seiten auszuführen, die als nicht ausführbare Datei gekennzeichnet sind. Dadurch wird ein NX-Fehler ausgelöst und die Anwendung beendet. Weitere Informationen finden Sie unter [**setprocessdeppolicy**](/windows/desktop/api/WinBase/nf-winbase-setprocessdeppolicy). Die meisten Anwendungen, die mit DEP nicht kompatible Aktionen ausführen, müssen aktualisiert werden, damit Sie ordnungsgemäß funktionieren.

Eine kleine Anzahl ausführbarer Dateien und Bibliotheken kann ausführbaren Code im Daten Abschnitt einer Bilddatei enthalten. In einigen Fällen können Anwendungen kleinere Code Segmente (in der Regel als thunas bezeichnet) in den Daten Abschnitten platzieren. Allerdings markiert DEP-Abschnitte der Bilddatei, die im Arbeitsspeicher geladen werden, als nicht ausführbare Datei, es sei denn, der Abschnitt enthält das ausführbare Attribut.

Daher sollte der ausführbare Code in den Daten Abschnitten zu einem Code Abschnitt migriert werden, oder der Daten Abschnitt, der den ausführbaren Code enthält, sollte explizit als ausführbare Datei gekennzeichnet werden. Das ausführbare Attribut **Image \_ SCN \_ mem \_ Execute** sollte dem Feld **Merkmale** der entsprechenden Abschnitts Kopfzeile für Abschnitte hinzugefügt werden, die ausführbaren Code enthalten. Weitere Informationen zum Hinzufügen von Attributen zu einem Abschnitt finden Sie in der Dokumentation, die in Ihrem Linker enthalten ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Daten Ausführungs Verhinderung (TechNet)](/previous-versions/windows/it-pro/windows-xp/bb457155(v=technet.10))
</dt> <dt>

[Vorgehensweise beim Konfigurieren des Speicher Schutzes](https://www.microsoft.com/technet/security/prodtech/windowsxp/depcnfxp.mspx)
</dt> <dt>

[KB-Artikel 875352](https://support.microsoft.com/kb/875352)
</dt> </dl>

 

 
