---
description: Jedes Fenster ist ein Member einer bestimmten Fenster Klasse. Die Fenster Klasse bestimmt die Standardfenster Prozedur, die von einem einzelnen Fenster zum Verarbeiten der Nachrichten verwendet wird.
ms.assetid: 3a8e8f4e-910d-4863-a4a7-dd37c2dfa402
title: Informationen zu Fenster Verfahren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1f63586b9ca4ac6fe8486ba112316174533b44e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355438"
---
# <a name="about-window-procedures"></a>Informationen zu Fenster Verfahren

Jedes Fenster ist ein Member einer bestimmten Fenster Klasse. Die Fenster Klasse bestimmt die Standardfenster Prozedur, die von einem einzelnen Fenster zum Verarbeiten der Nachrichten verwendet wird. Alle Fenster, die zur gleichen Klasse gehören, verwenden dieselbe Standardfenster Prozedur. Das System definiert z. b. eine Fenster Prozedur für die Kombinations Feld-Klasse (**ComboBox**). Alle Kombinations Felder verwenden dann diese Fenster Prozedur.

Eine Anwendung registriert in der Regel mindestens eine neue Fenster Klasse und die zugehörige Fenster Prozedur. Nach dem Registrieren einer Klasse kann die Anwendung viele Fenster dieser Klasse erstellen, die alle dieselbe Fenster Prozedur verwenden. Da dies bedeutet, dass mehrere Quellen denselben Code gleichzeitig aufzurufen haben, müssen Sie beim Ändern von freigegebenen Ressourcen aus einer Fenster Prozedur Vorsicht walten lassen. Weitere Informationen finden Sie unter [Fenster Klassen](window-classes.md).

Fenster Prozeduren für Dialogfelder (Dialogfeld Prozeduren genannt) weisen eine ähnliche Struktur auf und funktionieren wie reguläre Fenster Prozeduren. Alle Punkte, die auf Fenster Prozeduren in diesem Abschnitt verweisen, gelten auch für Dialogfeld Prozeduren. Weitere Informationen finden Sie unter [Dialog Felder](/windows/desktop/dlgbox/dialog-boxes).

In diesem Abschnitt werden die folgenden Themen behandelt.

-   [Struktur einer Fenster Prozedur](#structure-of-a-window-procedure)
-   [Standardfenster Prozedur](#default-window-procedure)
-   [Unterklassen für Fenster Prozeduren](#window-procedure-subclassing)
    -   [Instanzunterklassen](#instance-subclassing)
    -   [Globale Unterklassen](#global-subclassing)
-   [Fenster Prozedur-superclassingvorgang](#window-procedure-superclassing)

## <a name="structure-of-a-window-procedure"></a>Struktur einer Fenster Prozedur

Eine Fenster Prozedur ist eine Funktion, die über vier Parameter verfügt und einen signierten Wert zurückgibt. Die Parameter bestehen aus einem Fenster Handle, einem **uint** -Nachrichten Bezeichner und zwei Nachrichten Parametern, die mit den **wParam** -und **LPARAM** -Datentypen deklariert werden. Weitere Informationen finden Sie unter [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)).

Nachrichten Parameter enthalten häufig Informationen sowohl in der nieder wertigen als auch in der höchsten Reihenfolge. Es gibt mehrere Makros, die eine Anwendung verwenden kann, um Informationen aus den Nachrichten Parametern zu extrahieren. Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) -Makro extrahiert z. b. das nieder wertige Wort (Bits 0 bis 15) aus einem Message-Parameter. Weitere Makros sind [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)), [**lobyte**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85))und [**Hibyte**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)).

Die Interpretation des Rückgabewerts hängt von der jeweiligen Meldung ab. Überprüfen Sie die Beschreibung jeder Nachricht, um den entsprechenden Rückgabewert zu bestimmen.

Da es möglich ist, eine Fenster Prozedur rekursiv aufzurufen, ist es wichtig, die Anzahl der lokalen Variablen zu minimieren, die Sie verwendet. Bei der Verarbeitung einzelner Nachrichten sollte eine Anwendung Funktionen außerhalb der Fenster Prozedur aufzurufen, um eine übermäßige Verwendung lokaler Variablen zu vermeiden, was möglicherweise zu einem Überlauf des Stapels während einer tiefen Rekursion führt.

## <a name="default-window-procedure"></a>Standardfenster Prozedur

Die standardmäßige Fenster Prozedur Funktion [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) definiert ein bestimmtes grundlegendes Verhalten, das von allen Fenstern gemeinsam genutzt wird. Die standardmäßige Fenster Prozedur stellt die minimale Funktionalität für ein Fenster bereit. Eine von der Anwendung definierte Fenster Prozedur sollte alle Nachrichten übergeben, die nicht für die Standard Verarbeitung an die **defwindowproc** -Funktion verarbeitet werden.

## <a name="window-procedure-subclassing"></a>Unterklassen für Fenster Prozeduren

Wenn eine Anwendung ein Fenster erstellt, ordnet das System einen Speicherblock zum Speichern von Informationen an, die für das Fenster spezifisch sind, einschließlich der Adresse der Fenster Prozedur, mit der Nachrichten für das Fenster verarbeitet werden. Wenn das System eine Nachricht an das Fenster übergeben muss, durchsucht es die Fenster spezifischen Informationen nach der Adresse der Fenster Prozedur und übergibt die Nachricht an diese Prozedur.

*Unterklassen* sind eine Technik, die es einer Anwendung ermöglicht, Nachrichten abzufangen und zu verarbeiten, die gesendet oder an ein bestimmtes Fenster gesendet werden, bevor das Fenster die Möglichkeit hat, Sie zu verarbeiten. Durch die Unterklassen eines Fensters kann eine Anwendung das Verhalten des Fensters vergrößern, ändern oder überwachen. Eine Anwendung kann ein Fenster Unterklassen, das zu einer globalen System Klasse gehört, z. b. ein Bearbeitungs Steuerelement oder ein Listenfeld. Beispielsweise könnte eine Anwendung ein Bearbeitungs Steuerelement unterbinden, um zu verhindern, dass das Steuerelement bestimmte Zeichen akzeptiert. Es ist jedoch nicht möglich, ein Fenster oder eine Klasse zu unterteilen, das zu einer anderen Anwendung gehört. Alle Unterklassen müssen innerhalb desselben Prozesses ausgeführt werden.

Eine Anwendungs Unterklasse ein Fenster, indem die Adresse der ursprünglichen Fenster Prozedur des Fensters durch die Adresse einer neuen Fenster Prozedur ersetzt wird, die als *Unterklassen Prozedur* bezeichnet wird. Danach empfängt die Unterklassen Prozedur alle Nachrichten, die gesendet oder an das Fenster gesendet werden.

Die Unterklassen Prozedur kann beim Empfangen einer Nachricht drei Aktionen ausführen: die Nachricht kann an die ursprüngliche Fenster Prozedur übergeben, die Nachricht geändert und an die ursprüngliche Fenster Prozedur übergeben werden, oder die Nachricht kann verarbeitet und nicht an die ursprüngliche Fenster Prozedur übergeben werden. Wenn die Unterklassen Prozedur eine Nachricht verarbeitet, kann dies vor, nach oder vor und nach der Ausführung der Nachricht an die ursprüngliche Fenster Prozedur durchzuführen sein.

Das System stellt zwei Typen von Unterklassen bereit: [instance](#instance-subclassing) und [Global](#global-subclassing). In *instanzsubklassen* ersetzt eine Anwendung die Fenster Prozedur Adresse einer einzelnen Instanz eines Fensters. Eine Anwendung muss instanzsubklassen verwenden, um ein vorhandenes Fenster zu unterteilen. Bei der *globalen unter Klassifizierung* ersetzt eine Anwendung die Adresse der Fenster Prozedur in der [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) -Struktur einer Fenster Klasse. Alle nachfolgenden Fenster, die mit der-Klasse erstellt wurden, haben die Adresse der Unterklassen Prozedur, aber vorhandene Fenster der-Klasse sind nicht betroffen.

### <a name="instance-subclassing"></a>Instanzunterklassen

Eine Anwendung Unterklassen eine Instanz eines Fensters mithilfe der [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) -Funktion. Die Anwendung übergibt das **GWL-Flag \_ WndProc** , das Handle an das Fenster an die Unterklasse und die Adresse der Unterklassen Prozedur an **SetWindowLong**. Die Unterklassen Prozedur kann sich entweder in der ausführbaren Datei der Anwendung oder in einer DLL befinden.

[**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga) gibt die Adresse der ursprünglichen Fenster Prozedur des Fensters zurück. Die Anwendung muss die Adresse speichern und in nachfolgenden Aufrufen der [**callwindowproc**](/windows/win32/api/winuser/nf-winuser-callwindowproca) -Funktion verwenden, um abgefangene Nachrichten an die ursprüngliche Fenster Prozedur zu übergeben. Die Anwendung muss auch die ursprüngliche Fenster Prozedur Adresse aufweisen, um die Unterklasse aus dem Fenster zu entfernen. Um die Unterklasse zu entfernen, ruft die Anwendung **SetWindowLong** erneut auf, wobei die Adresse der ursprünglichen Fenster Prozedur mit dem **GWL-Flag \_ WndProc** und dem Handle an das Fenster übergeben wird.

Das System besitzt die globalen System Klassen, und Aspekte der Steuerelemente können sich von einer Version des Systems zur nächsten ändern. Wenn die Anwendung ein Fenster Unterklassen muss, das zu einer globalen System Klasse gehört, muss der Entwickler die Anwendung möglicherweise aktualisieren, wenn eine neue Version des Systems veröffentlicht wird.

Da instanzunterklassen nach dem Erstellen eines Fensters auftreten, können Sie dem Fenster keine zusätzlichen Bytes hinzufügen. Anwendungen, die eine Unterklasse eines Fensters verwenden, sollten die Eigenschaften Liste des Fensters verwenden, um alle Daten zu speichern, die für eine Instanz des untergeordneten-Fensters benötigt werden. Weitere Informationen finden Sie unter [Fenster Eigenschaften](window-properties.md).

Wenn eine Anwendung ein untergeordnetes Fenster Unterklassen, muss Sie die Unterklassen in umgekehrter Reihenfolge entfernen, in der Sie ausgeführt wurden. Wenn die Entfernungs Reihenfolge nicht umgekehrt ist, kann ein nicht BEHEB barer Systemfehler auftreten.

### <a name="global-subclassing"></a>Globale Unterklassen

Die Anwendung muss über ein Handle für ein Fenster der Klasse verfügen, um eine globale Unterklasse einer Fenster Klasse zu Unternehmen. Die Anwendung benötigt außerdem das Handle, um die Unterklasse zu entfernen. Um das Handle zu erhalten, erstellt eine Anwendung in der Regel ein ausgeblendetes Fenster der Klasse, das untergeordnet werden soll. Nachdem Sie das Handle erhalten haben, ruft die Anwendung die [**SetClassLong**](/windows/win32/api/winuser/nf-winuser-setclasslonga) -Funktion auf, wobei das Handle, das **gcl \_ WndProc** -Flag und die Adresse der Unterklassen Prozedur angegeben werden. **SetClassLong** gibt die Adresse der ursprünglichen Fenster Prozedur für die-Klasse zurück.

Die ursprüngliche Fenster Prozedur Adresse wird in der globalen Unterklassen auf die gleiche Weise verwendet, wie Sie in instanzsubklassen verwendet wird. Die Unterklassen Prozedur übergibt Nachrichten an die ursprüngliche Fenster Prozedur, indem [**callwindowproc**](/windows/win32/api/winuser/nf-winuser-callwindowproca)aufgerufen wird. Die Anwendung entfernt die Unterklasse aus der Fenster Klasse durch den Aufruf von [**SetClassLong**](/windows/win32/api/winuser/nf-winuser-setclasslonga) , wobei die Adresse der ursprünglichen Fenster Prozedur, das **gcl-Flag \_ WndProc** und das Handle für ein Fenster der Klasse angegeben werden, das untergeordnet wird. Eine Anwendung, die eine Steuerelement Klasse Global Unterklassen entfernt, muss die Unterklasse entfernen, wenn die Anwendung beendet wird. Andernfalls kann ein nicht BEHEB barer Systemfehler auftreten.

Bei der globalen Unterklassen Einschränkung gelten die gleichen Einschränkungen wie für instanzunterklassen sowie einige zusätzliche Einschränkungen. Eine Anwendung sollte nicht die zusätzlichen Bytes für die Klasse oder die Fenster Instanz verwenden, ohne genau zu wissen, wie Sie von der ursprünglichen Fenster Prozedur verwendet werden. Wenn die Anwendung Daten einem Fenster zuordnen muss, sollte Sie Fenster Eigenschaften verwenden.

## <a name="window-procedure-superclassing"></a>Fenster Prozedur-superclassingvorgang

*Superclassingist* ein Verfahren, mit dem eine Anwendung eine neue Fenster Klasse mit den grundlegenden Funktionen der vorhandenen Klasse erstellen kann, sowie Erweiterungen, die von der Anwendung bereitgestellt werden. Eine übergeordnete Klasse basiert auf einer vorhandenen Fenster Klasse, die als *Basisklasse* bezeichnet wird. Häufig ist die Basisklasse eine globale System Fenster Klasse, z. b. ein Bearbeitungs Steuerelement, aber es kann sich um eine beliebige Fenster Klasse handeln.

Eine übergeordnete Klasse verfügt über eine eigene Fenster Prozedur, die als übergeordneten Klasse-Prozedur bezeichnet wird. Die *übergeordneten Klasse-Prozedur* kann beim Empfangen einer Nachricht drei Aktionen ausführen: die Nachricht kann an die ursprüngliche Fenster Prozedur übergeben, die Nachricht geändert und an die ursprüngliche Fenster Prozedur übergeben werden, oder die Nachricht kann verarbeitet und nicht an die ursprüngliche Fenster Prozedur übergeben werden. Wenn die übergeordneten Klasse-Prozedur eine Nachricht verarbeitet, kann dies vor, nach oder vor und nach der Ausführung der Nachricht an die ursprüngliche Fenster Prozedur durchlaufen werden.

Anders als bei einer Unterklassen Prozedur kann eine übergeordnete Prozedur Fenster Erstellungs Meldungen verarbeiten ([**WM \_ nccreate**](wm-nccreate.md), [**WM \_ Create**](wm-create.md)usw.), Sie muss aber auch an die ursprüngliche Basisklassen Fenster-Prozedur übergeben werden, damit die Prozedur für die Basisklassen Fenster Ihre Initialisierungs Prozedur ausführen kann.

Zur übergeordneten Klasse einer Fenster Klasse ruft eine Anwendung zuerst die [**GetClassInfo**](/windows/win32/api/winuser/nf-winuser-getclassinfoa) -Funktion auf, um Informationen über die Basisklasse abzurufen. **GetClassInfo** füllt eine [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) -Struktur mit den Werten aus der **WNDCLASS** -Struktur der Basisklasse auf. Anschließend kopiert die Anwendung ihr eigenes Instanzhandle in den **HINSTANCE** -Member der **WNDCLASS** -Struktur und kopiert den Namen der übergeordneten Klasse in das **lpszClassName** -Element. Wenn die Basisklasse über ein Menü verfügt, muss die Anwendung ein neues Menü mit denselben Menü bezeichatoren bereitstellen und den Menünamen in das **lpszmenuname** -Element kopieren. Wenn die Super Class-Prozedur die [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Nachricht verarbeitet und nicht an die Fenster Prozedur der Basisklasse übergibt, muss das Menü keine entsprechenden Bezeichner aufweisen. " **GetClassInfo** " gibt nicht den Member " **lpszmenuname**", " **lpszClassName**" oder " **HINSTANCE** " der **WNDCLASS** -Struktur zurück.

Eine Anwendung muss auch den **lpfnwndproc** -Member der [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) -Struktur festlegen. Die [**GetClassInfo**](/windows/win32/api/winuser/nf-winuser-getclassinfoa) -Funktion füllt diesen Member mit der Adresse der ursprünglichen Fenster Prozedur für die-Klasse. Diese Adresse muss von der Anwendung gespeichert werden, um Nachrichten an die ursprüngliche Fenster Prozedur zu übergeben und dann die Adresse der übergeordneten Klasse in das **lpfnwndproc** -Element zu kopieren. Die Anwendung kann ggf. alle anderen Member der **WNDCLASS** -Struktur ändern. Nach dem Ausfüllen der **WNDCLASS** -Struktur wird die übergeordneten Klasse von der Anwendung registriert, indem die Adresse der-Struktur an die [**registerClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) -Funktion übergeben wird. Die übergeordnete Klasse kann dann zum Erstellen von Windows verwendet werden.

Da die übergeordnete Klasse eine neue Fenster Klasse registriert, kann eine Anwendung sowohl den zusätzlichen Klassen Bytes als auch den zusätzlichen Fenster Bytes hinzufügen. Die Super Class darf nicht die ursprünglichen zusätzlichen Bytes für die Basisklasse oder das Fenster verwenden, aus den gleichen Gründen, wie eine instanzunterklasse oder eine globale Unterklasse Sie nicht verwenden darf. Wenn die Anwendung zusätzliche Bytes für die Verwendung der-Klasse oder der Fenster Instanz hinzufügt, muss Sie außerdem auf die zusätzlichen Bytes in Relation zur Anzahl zusätzlicher Bytes verweisen, die von der ursprünglichen Basisklasse verwendet werden. Da die Anzahl von Bytes, die von der Basisklasse verwendet werden, von einer Version der Basisklasse zur nächsten variieren kann, kann der Anfangs Offset für die eigenen zusätzlichen Bytes der übergeordneten Klasse auch von einer Version der Basisklasse zum nächsten abweichen.

 

 
