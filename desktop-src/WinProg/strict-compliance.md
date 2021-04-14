---
title: Strikte Konformität
description: Wenn Sie eine strikte Typüberprüfung aktivieren, kann es vorkommen, dass einige Quellcode, die erfolgreich kompiliert werden, Fehlermeldungen erzeugt.
ms.assetid: 88368fec-b375-4ad0-aa13-ffadf0338a44
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02d04c3a849dc62647758e3515728e3dd3f65dcb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390580"
---
# <a name="strict-compliance"></a>Strikte Konformität

Wenn Sie eine **strikte** Typüberprüfung aktivieren, kann es vorkommen, dass einige Quellcode, die erfolgreich kompiliert werden, Fehlermeldungen erzeugt. In den folgenden Abschnitten werden die Mindestanforderungen beschrieben, mit denen der Code kompiliert werden kann, wenn **Strict** aktiviert ist. Es werden zusätzliche Schritte empfohlen, insbesondere zum Entwickeln von portablen Code.

## <a name="general-requirements"></a>Allgemeine Anforderungen

Die Hauptanforderung besteht darin, dass Sie korrekte handle-Typen und Funktionszeiger deklarieren müssen, anstatt sich auf allgemeinere Typen zu verlassen. Sie können einen Handles-Typ nicht verwenden, wenn ein anderer Typ erwartet wird. Dies bedeutet auch, dass Sie möglicherweise Funktions Deklarationen ändern und weitere Typumwandlungen verwenden müssen.

Um optimale Ergebnisse zu erzielen, sollte der generische **Handlertyp** nur bei Bedarf verwendet werden.

## <a name="declaring-functions-within-your-application"></a>Deklarieren von Funktionen in der Anwendung

Stellen Sie sicher, dass alle Anwendungsfunktionen deklariert sind. Die Platzierung aller Funktions Deklarationen in einer Includedatei wird empfohlen, da Sie problemlos Ihre Deklarationen Scannen und nach Parametern und Rückgabe Typen suchen können, die geändert werden sollten.

Wenn Sie die **/ZG** -Compileroption verwenden, um Header Dateien für ihre Funktionen zu erstellen, denken Sie daran, dass Sie unterschiedliche Ergebnisse erhalten, je nachdem, ob Sie die **strikte** Typüberprüfung aktiviert haben. Wenn **Strict** deaktiviert ist, generieren alle handle-Typen denselben Basistyp. Wenn **Strict** aktiviert ist, generieren Sie unterschiedliche Basis Typen. Um Konflikte zu vermeiden, müssen Sie die Header Datei bei jeder Aktivierung oder Deaktivierung von **Strict** neu erstellen oder die Header Datei so bearbeiten, dass die Typen **HWND**, **hdc**, **handle** usw. anstelle der Basis Typen verwendet werden.

Alle Funktions Deklarationen, die Sie aus Windows. h in Ihren Quellcode kopiert haben, haben sich möglicherweise geändert, und Ihre lokale Deklaration ist möglicherweise veraltet. Entfernen Sie die lokale Deklaration.

## <a name="types-that-require-casts"></a>Typen, die Umwandlungen erfordern

Einige Funktionen verfügen über generische Rückgabe Typen oder Parameter. Beispielsweise gibt die [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) -Funktion Daten zurück, die je nach Kontext eine beliebige Anzahl von Typen sein können. Wenn eine dieser Funktionen in Ihrem Quellcode angezeigt wird, stellen Sie sicher, dass Sie die richtige Typumwandlung verwenden und so spezifisch wie möglich sind. Die folgende Liste ist ein Beispiel für diese Funktionen.

-   [**Loczuweisung**](/windows/desktop/api/winbase/nf-winbase-locallock)
-   [**GlobalLock**](/windows/desktop/api/winbase/nf-winbase-globallock)
-   [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga)
-   [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga)
-   [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage)
-   [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
-   [**SendDlgItemMess age**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea)

Wenn Sie [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage), [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)oder [**SendDlgItemMess**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea)aufzurufen, sollten Sie zuerst das Ergebnis in den Typ **uint \_ ptr** umwandeln. Sie müssen ähnliche Schritte für jede Funktion ausführen, die einen **LRESULT** -oder **Long \_ ptr** -Wert zurückgibt, bei dem das Ergebnis ein Handle enthält. Dies ist für das Schreiben von portablen Code erforderlich, da die Größe eines Handles abhängig von der Windows-Version variiert. Durch die Umwandlung von (**uint \_ ptr**) wird eine ordnungsgemäße Konvertierung sichergestellt. Der folgende Code zeigt ein Beispiel, in dem **SendMessage** ein Handle für einen Pinsel zurückgibt:


```C++
HBRUSH hbr;

hbr = (HBRUSH)(UINT_PTR)SendMessage(hwnd, WM_CTLCOLOR, ..., ...);
```



Der *Parameter "* **upatewindow** " und " **upatewindowex** " wird manchmal verwendet, um einen ganzzahligen Steuerelement Bezeichner (ID) zu übergeben. In diesem Fall müssen Sie die ID in einen **HMENU** -Typ umwandeln:


```C++
HWND hwnd;
int id;

hwnd = CreateWindow(
        TEXT("Button"), TEXT("OK"), BS_PUSHBUTTON,
        x, y, cx, cy, hwndParent,
        (HMENU)id,    // Cast required here
        hinst,
        NULL);
```



## <a name="additional-considerations"></a>Weitere Überlegungen

Um die **strikte** Typüberprüfung optimal zu nutzen, gibt es weitere Richtlinien, die Sie befolgen sollten. Der Code wird in zukünftigen Versionen von Windows besser portierbar sein, wenn Sie die folgenden Änderungen vornehmen.

Die Typen **wParam**, **LPARAM**, **LRESULT** und **LPVOID** sind *polymorphe Datentypen*. Sie speichern verschiedene Arten von Daten zu unterschiedlichen Zeitpunkten, auch wenn die **strikte** Typüberprüfung aktiviert ist. Um den Vorteil der Typüberprüfung zu erhalten, sollten Sie Werte dieser Typen so bald wie möglich umwandeln. (Beachten Sie, dass nachrichtencracker *wParam* und *LPARAM* automatisch für Sie neu umgestalten.)

Achten Sie besonders darauf, **HMODULE** -und **HINSTANCE** -Typen zu unterscheiden. Auch wenn **Strict** aktiviert ist, werden Sie als derselbe Basistyp definiert. Die meisten Verwaltungsfunktionen für Kernelmodule verwenden **HINSTANCE** -Typen, aber es gibt einige Funktionen, die nur **HMODULE** -Typen zurückgeben oder akzeptieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Deaktivieren von Strict](disabling-strict.md)
</dt> <dt>

[Aktivieren von Strict](enabling-strict.md)
</dt> </dl>

 

 