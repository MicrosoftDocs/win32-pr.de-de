---
description: Mit einem Frame basierten Ausnahmehandler können Sie die Möglichkeit behandeln, dass eine Ausnahme in einer bestimmten Code Sequenz auftritt. Ein Frame basierter Ausnahmehandler besteht aus den folgenden Elementen.
ms.assetid: 07aac772-f917-48b7-91a9-3b5d4cb43600
title: Frame basierte Ausnahmebehandlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12b268b5d02de83bca22a1d3311905b05be1f748
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483507"
---
# <a name="frame-based-exception-handling"></a>Frame basierte Ausnahmebehandlung

Mit einem *Frame basierten Ausnahmehandler* können Sie die Möglichkeit behandeln, dass eine Ausnahme in einer bestimmten Code Sequenz auftritt. Ein Frame basierter Ausnahmehandler besteht aus den folgenden Elementen.

-   Ein überwachter Codetext
-   Ein Filter Ausdruck
-   Ein Ausnahmehandlerblock.

Frame basierte Ausnahmehandler werden in sprachspezifischer Syntax deklariert. Beispielsweise werden Sie im Microsoft C/C++-Optimierungs Compiler mithilfe von **\_ \_ try** und **\_ \_ außer** implementiert. Weitere Informationen finden Sie unter [HandlerSyntax](handler-syntax.md).

Der *geschützte Code Körper* ist ein Satz von einer oder mehreren-Anweisungen, für die der Filter Ausdruck und der Ausnahmehandlerblock Ausnahme Behandlungs Schutz bereitstellen. Bei dem überwachten Text kann es sich um einen Codeblock, einen Satz von Blöcke oder eine gesamte Prozedur oder Funktion handeln. Mithilfe des Microsoft C/C++-Optimierungs Compilers wird ein geschützter Text durch geschweifte Klammern ( {} ) nach dem **\_ \_ try** -Schlüsselwort eingeschlossen.

Der *Filter Ausdruck* eines Frame basierten Ausnahme Handlers ist ein Ausdruck, der vom System ausgewertet wird, wenn im überwachten Text eine Ausnahme auftritt. Diese Auswertung führt zu einer der folgenden Aktionen vom System.

-   Das System beendet die Suche nach einem Ausnahmehandler, stellt den Computer Zustand wieder her und setzt die Thread Ausführung an dem Punkt fort, an dem die Ausnahme aufgetreten ist.
-   Das System setzt die Suche nach einem Ausnahmehandler fort.
-   Das System überträgt die Steuerung an den Ausnahmehandler, und die Thread Ausführung wird sequenziell im Stapel Rahmen fortgesetzt, in dem der Ausnahmehandler gefunden wird. Wenn sich der Handler nicht im Stapel Rahmen befindet, in dem die Ausnahme aufgetreten ist, entlädt das System den Stapel und gibt den aktuellen Stapel Rahmen und alle anderen Stapel Rahmen zurück, bis er wieder dem Stapel Rahmen des Ausnahme Handlers entspricht. Vor der Ausführung eines Ausnahmehandler werden Beendigungs Handler für alle überwachten Code Körper ausgeführt, die als Ergebnis der Übertragung der Steuerung an den Ausnahmehandler beendet wurden. Weitere Informationen zu Beendigungs Handlern finden Sie unter [Abbruch Behandlung](termination-handling.md).

Der Filter Ausdruck kann ein einfacher Ausdruck sein oder eine *Filterfunktion* aufrufen, die versucht, die Ausnahme zu behandeln. Sie können die Funktionen [**GetExceptionCode**](getexceptioncode.md) und [**GetExceptionInformation**](getexceptioninformation.md) innerhalb eines Filter Ausdrucks aufrufen, um Informationen über die zu filternde Ausnahme abzurufen. **GetExceptionCode** gibt einen Code zurück, der den Typ der Ausnahme identifiziert, und **GetExceptionInformation** gibt einen Zeiger auf eine [**Ausnahme \_ Zeiger**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) Struktur zurück, die Zeiger auf [**Kontext**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) -und [**Ausnahme \_ Daten Satz**](/windows/desktop/api/WinNT/ns-winnt-exception_record) Strukturen enthält.

Diese Funktionen können nicht innerhalb einer Filterfunktion aufgerufen werden, aber ihre Rückgabewerte können als Parameter an eine Filterfunktion übermittelt werden. [**GetExceptionCode**](getexceptioncode.md) kann im Ausnahmehandlerblock verwendet werden, aber [**GetExceptionInformation**](getexceptioninformation.md) kann nicht verwendet werden, da die Informationen, auf die Sie verweist, in der Regel auf dem Stapel abgelegt werden und zerstört werden, wenn die Steuerung an einen Ausnahmehandler übertragen wird. Eine Anwendung kann die Informationen jedoch in den sicheren Speicher kopieren, um Sie dem Ausnahmehandler zur Verfügung zu stellen.

Der Vorteil einer Filterfunktion besteht darin, dass Sie eine Ausnahme behandeln und einen Wert zurückgeben kann, der bewirkt, dass das System die Ausführung von dem Punkt aus fortsetzt, an dem die Ausnahme aufgetreten ist. Bei einem Ausnahmehandlerblock wird die Ausführung hingegen sequenziell vom Ausnahmehandler fortgesetzt und nicht vom Zeitpunkt der Ausnahme.

Das Behandeln einer Ausnahme kann so einfach sein, dass ein Fehler festgestellt und ein Flag festgelegt wird, das später untersucht wird, eine Warnung oder eine Fehlermeldung gedruckt oder eine andere eingeschränkte Aktion durchführt. Wenn die Ausführung fortgesetzt werden kann, kann es auch erforderlich sein, den Computer Zustand zu ändern, indem Sie den Kontext Daten Satz ändern. Ein Beispiel für eine Filterfunktion, die eine Seiten Fehler Ausnahme behandelt, finden [Sie unter Verwenden der Funktionen für den virtuellen Arbeitsspeicher](../memory/using-the-memory-management-functions.md).

Die [**unlenker dexceptionfilter**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-unhandledexceptionfilter) -Funktion kann als Filterfunktion in einem Filter Ausdruck verwendet werden. Es wird ein Ausnahme \_ Ausführungs Handler zurückgegeben \_ , es sei denn, der Prozess wird debuggt \_ \_

 

 
