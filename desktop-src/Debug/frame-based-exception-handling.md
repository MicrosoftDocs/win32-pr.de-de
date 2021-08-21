---
description: Mit einem framebasierten Ausnahmehandler können Sie mit der Möglichkeit umgehen, dass eine Ausnahme in einer bestimmten Codesequenz auftreten kann. Ein framebasierter Ausnahmehandler besteht aus den folgenden Elementen.
ms.assetid: 07aac772-f917-48b7-91a9-3b5d4cb43600
title: Framebasierte Ausnahmebehandlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2afb72118aca7653e9bc15e7f4ff4b75e46b1abad5bab7dee4a3397ae5f98e1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119573120"
---
# <a name="frame-based-exception-handling"></a>Framebasierte Ausnahmebehandlung

Mit *einem framebasierten Ausnahmehandler* können Sie mit der Möglichkeit umgehen, dass eine Ausnahme in einer bestimmten Codesequenz auftreten kann. Ein framebasierter Ausnahmehandler besteht aus den folgenden Elementen.

-   Ein beschützter Code
-   Ein Filterausdruck
-   Ein Ausnahmehandlerblock

Framebasierte Ausnahmehandler werden in sprachspezifischer Syntax deklariert. Beispielsweise werden sie im Microsoft C/C++-Optimierungscompiler mit **\_ \_ try** und außer **\_ \_ implementiert.** Weitere Informationen finden Sie unter [Handlersyntax](handler-syntax.md).

Der *beschützte Code* besteht aus einer oder mehrere -Anweisungen, für die der Filterausdruck und der Ausnahmehandlerblock Schutz zur Ausnahmebehandlung bieten. Der bewaiste Text kann ein Codeblock, ein Satz geschachtelter Blöcke oder eine gesamte Prozedur oder Funktion sein. Mithilfe des Microsoft C/C++-Optimierungscompilers wird ein beschützter Text in geschweifte Klammern ( ) eingeschlossen, die dem {} **\_ \_ try-Schlüsselwort** folgen.

Der *Filterausdruck* eines framebasierten Ausnahmehandlers ist ein Ausdruck, der vom System ausgewertet wird, wenn eine Ausnahme innerhalb des wächter Textkörpers auftritt. Diese Auswertung führt zu einer der folgenden Aktionen des Systems.

-   Das System beendet die Suche nach einem Ausnahmehandler, stellt den Computerzustand wieder auf und setzt die Threadausführung an dem Punkt fort, an dem die Ausnahme aufgetreten ist.
-   Das System setzt die Suche nach einem Ausnahmehandler fort.
-   Das System überträgt die Steuerung an den Ausnahmehandler, und die Threadausführung wird sequenziell in dem Stapelrahmen fortgesetzt, in dem sich der Ausnahmehandler befindet. Wenn sich der Handler nicht im Stapelrahmen befindet, in dem die Ausnahme aufgetreten ist, entlädt das System den Stapel und verlässt den aktuellen Stapelrahmen und alle anderen Stapelrahmen, bis er wieder zum Stapelrahmen des Ausnahmehandlers zurückliegt. Bevor ein Ausnahmehandler ausgeführt wird, werden Beendigungshandler für alle beschützten Codekörper ausgeführt, die als Ergebnis der Übertragung der Steuerung an den Ausnahmehandler beendet wurden. Weitere Informationen zu Beendigungshandlern finden Sie unter [Beendigungsbehandlung.](termination-handling.md)

Der Filterausdruck kann ein einfacher Ausdruck  sein oder eine Filterfunktion aufrufen, die versucht, die Ausnahme zu behandeln. Sie können die [**Funktionen GetExceptionCode**](getexceptioncode.md) und [**GetExceptionInformation**](getexceptioninformation.md) in einem Filterausdruck aufrufen, um Informationen über die zu filternde Ausnahme zu erhalten. **GetExceptionCode gibt** einen Code zurück, der den Typ der Ausnahme identifiziert, und **GetExceptionInformation** gibt einen Zeiger auf eine [**EXCEPTION \_ POINTERS-Struktur**](/windows/desktop/api/WinNT/ns-winnt-exception_pointers) zurück, die Zeiger auf [**CONTEXT-**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) und [**EXCEPTION \_ RECORD-Strukturen**](/windows/desktop/api/WinNT/ns-winnt-exception_record) enthält.

Diese Funktionen können nicht innerhalb einer Filterfunktion aufgerufen werden, aber ihre Rückgabewerte können als Parameter an eine Filterfunktion übergeben werden. [**GetExceptionCode**](getexceptioncode.md) kann innerhalb des Ausnahmehandlerblocks verwendet werden, [**aber GetExceptionInformation**](getexceptioninformation.md) kann nicht verwendet werden, da sich die Informationen, auf die es zeigt, in der Regel im Stapel befindet und zerstört werden, wenn die Steuerung an einen Ausnahmehandler übertragen wird. Eine Anwendung kann die Informationen jedoch in den sicheren Speicher kopieren, um sie dem Ausnahmehandler zur Verfügung zu stellen.

Der Vorteil einer Filterfunktion ist, dass sie eine Ausnahme behandeln und einen Wert zurückgeben kann, der bewirkt, dass das System die Ausführung von dem Zeitpunkt an fortgesetzt, an dem die Ausnahme aufgetreten ist. Bei einem Ausnahmehandlerblock wird die Ausführung dagegen sequenziell über den Ausnahmehandler und nicht über den Punkt der Ausnahme fortgesetzt.

Die Behandlung einer Ausnahme kann so einfach sein, wie das Notieren eines Fehlers und das Festlegen eines Flags, das später untersucht wird, das Drucken einer Warnung oder Fehlermeldung oder das Ergreifen einer anderen eingeschränkten Aktion. Wenn die Ausführung fortgesetzt werden kann, kann es auch erforderlich sein, den Computerstatus durch Ändern des Kontextdatensatz zu ändern. Ein Beispiel für eine Filterfunktion, die eine Seitenfehlerausnahme behandelt, finden Sie unter [Using the Virtual Memory Functions](../memory/using-the-memory-management-functions.md).

Die [**UnhandledExceptionFilter-Funktion**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-unhandledexceptionfilter) kann als Filterfunktion in einem Filterausdruck verwendet werden. Sie gibt EXCEPTION EXECUTE HANDLER zurück, es sei denn, der Prozess wird debuggt. In diesem Fall wird \_ \_ EXCEPTION CONTINUE SEARCH \_ \_ zurückgegeben.

 

 
