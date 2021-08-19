---
title: STRICT Compliance
description: Ein Quellcode, der erfolgreich kompiliert wird, erzeugt möglicherweise Fehlermeldungen, wenn Sie die STRICT-Typüberprüfung aktivieren.
ms.assetid: 88368fec-b375-4ad0-aa13-ffadf0338a44
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29baee071bd8d7c236ec5f2f99d1dff11aeac37deb44b0d8a6254325c9a75df0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117928145"
---
# <a name="strict-compliance"></a>STRICT Compliance

Ein Quellcode, der erfolgreich kompiliert wird, erzeugt  möglicherweise Fehlermeldungen, wenn Sie die STRICT-Typüberprüfung aktivieren. In den folgenden Abschnitten werden die minimalen Anforderungen für die Kompilierung Ihres Codes beschrieben, wenn **STRICT** aktiviert ist. Es werden zusätzliche Schritte empfohlen, insbesondere zum Erstellen von portablem Code.

## <a name="general-requirements"></a>Allgemeine Anforderungen

Die Hauptanforderung besteht darin, dass Sie die richtigen Handletypen und Funktionszeiger deklarieren müssen, anstatt sich auf allgemeinere Typen zu verlassen. Sie können keinen Handletyp verwenden, bei dem ein anderer erwartet wird. Dies bedeutet auch, dass Sie möglicherweise Funktionsdeklarationen ändern und weitere Typumwandelungen verwenden müssen.

Um optimale Ergebnisse zu erzielen, sollte der generische **HANDLE-Typ** nur bei Bedarf verwendet werden.

## <a name="declaring-functions-within-your-application"></a>Deklarieren von Funktionen in Ihrer Anwendung

Stellen Sie sicher, dass alle Anwendungsfunktionen deklariert sind. Es wird empfohlen, alle Funktionsdeklarationen in einer Includedatei zu platzieren, da Sie Ihre Deklarationen einfach überprüfen und nach Parameter- und Rückgabetypen suchen können, die geändert werden sollten.

Wenn Sie die Compileroption **/Zg** verwenden, um Headerdateien für Ihre Funktionen zu erstellen, denken Sie daran, dass Sie unterschiedliche Ergebnisse erhalten, je nachdem, ob Sie die **STRICT-Typüberprüfung** aktiviert haben. Wenn **STRICT** deaktiviert ist, generieren alle Handletypen den gleichen Basistyp. Wenn **STRICT** aktiviert ist, generieren sie verschiedene Basistypen. Um Konflikte zu vermeiden, müssen Sie die Headerdatei jedes Mal neu erstellen, wenn Sie **STRICT** aktivieren oder deaktivieren, oder die Headerdatei so bearbeiten, dass anstelle der Basistypen die Typen **HWND,** **HDC,** **HANDLE** usw. verwendet werden.

Alle Funktionsdeklarationen, die Sie aus Windows.h in den Quellcode kopiert haben, haben sich möglicherweise geändert, und ihre lokale Deklaration ist möglicherweise veraltet. Entfernen Sie die lokale Deklaration.

## <a name="types-that-require-casts"></a>Typen, die Umwandlungen erfordern

Einige Funktionen verfügen über generische Rückgabetypen oder Parameter. Die [**SendMessage-Funktion**](/windows/win32/api/winuser/nf-winuser-sendmessage) gibt beispielsweise Daten zurück, die je nach Kontext eine beliebige Anzahl von Typen aufweisen können. Wenn eine dieser Funktionen in Ihrem Quellcode angezeigt wird, stellen Sie sicher, dass Sie die richtige Typform verwenden und so spezifisch wie möglich sind. Die folgende Liste ist ein Beispiel für diese Funktionen.

-   [**LocalLock**](/windows/desktop/api/winbase/nf-winbase-locallock)
-   [**GlobalLock**](/windows/desktop/api/winbase/nf-winbase-globallock)
-   [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga)
-   [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga)
-   [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage)
-   [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
-   [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea)

Wenn Sie [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage), [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)oder [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea)aufrufen, sollten Sie zuerst das Ergebnis in den Typ **UINT \_ PTR** umschalten. Sie müssen ähnliche Schritte für jede Funktion ausführen, die einen **LRESULT-** oder **LONG \_ PTR-Wert** zurückgibt, wobei das Ergebnis ein Handle enthält. Dies ist erforderlich, um portablen Code zu schreiben, da die Größe eines Handles je nach Version von Windows variiert. Die Umwandlung (**UINT \_ PTR**) stellt eine ordnungsgemäße Konvertierung sicher. Der folgende Code zeigt ein Beispiel, in dem **SendMessage** ein Handle an einen Pinsel zurückgibt:


```C++
HBRUSH hbr;

hbr = (HBRUSH)(UINT_PTR)SendMessage(hwnd, WM_CTLCOLOR, ..., ...);
```



Der **CreateWindow-** und **CreateWindowEx-Parameter** *hmenu* wird manchmal verwendet, um einen ganzzahligen Steuerelementbezeichner (ID) zu übergeben. In diesem Fall müssen Sie die ID in einen **HMENU-Typ umwandlungen:**


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

Um den größten  Nutzen aus der STRICT-Typüberprüfung zu ziehen, sollten Sie zusätzliche Richtlinien befolgen. Ihr Code ist in zukünftigen Versionen von Windows portierbarer, wenn Sie die folgenden Änderungen vornehmen.

Die Typen **WPARAM,** **LPARAM,** **LRESULT** und **LPVOID** sind *polymorphe Datentypen.* Sie enthalten unterschiedliche Arten von Daten  zu unterschiedlichen Zeiten, auch wenn die STRICT-Typüberprüfung aktiviert ist. Um die Vorteile der Typüberprüfung nutzen zu können, sollten Sie Werte dieser Typen so schnell wie möglich umformen. (Beachten Sie, dass Nachrichtentisser *wParam* und *lParam* automatisch portabel für Sie umgestalten.)

Achten Sie besonders darauf, die Typen **HMODULE** und **HINSTANCE** zu unterscheiden. Selbst wenn **STRICT** aktiviert ist, werden sie als derselbe Basistyp definiert. Die meisten Kernelmodulverwaltungsfunktionen verwenden **HINSTANCE-Typen,** aber es gibt einige Funktionen, die nur **HMODULE-Typen** zurückgeben oder akzeptieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Deaktivieren von STRICT](disabling-strict.md)
</dt> <dt>

[Aktivieren von STRICT](enabling-strict.md)
</dt> </dl>

 

 