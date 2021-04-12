---
title: WinMain der Einstiegspunkt der Anwendung
description: .
ms.assetid: 389da5d4-d0f9-4339-be6c-0f4fecc59316
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bef44c4d31aa53dfd60f579b68c438a539058b85
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104208887"
---
# <a name="winmain-the-application-entry-point"></a>WinMain: der Einstiegspunkt der Anwendung

Jedes Windows-Programm enthält eine Einstiegspunkt Funktion, die entweder **WinMain** oder **wWinMain** heißt. Hier ist die Signatur für **wWinMain**.


```C++
int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, PWSTR pCmdLine, int nCmdShow);
```



Die vier Parameter sind:

-   *HINSTANCE* wird als "Handle für eine Instanz" oder "Handle für ein Modul" bezeichnet. Das Betriebssystem verwendet diesen Wert, um die ausführbare Datei (exe) zu identifizieren, wenn Sie in den Arbeitsspeicher geladen wird. Der Instanzhandle ist für bestimmte Windows-Funktionen erforderlich, z. –. zum Laden von Symbolen oder Bitmaps.
-   *hPrevInstance* hat keine Bedeutung. Es wurde in 16-Bit-Fenstern verwendet, ist aber jetzt immer 0 (null).
-   *pCmdLine* enthält die Befehlszeilenargumente als Unicode-Zeichenfolge.
-   *nCmdShow* ist ein Flag, das besagt, ob das Hauptanwendungsfenster minimiert, maximiert oder normal angezeigt wird.

Die-Funktion gibt einen **int** -Wert zurück. Der Rückgabewert wird vom Betriebssystem nicht verwendet, Sie können jedoch den Rückgabewert verwenden, um einen Statuscode an ein anderes Programm zu übermitteln, das Sie schreiben.

**WinAPI** ist die Aufruf Konvention. Eine *Aufruf Konvention* definiert, wie eine Funktion Parameter vom Aufrufer empfängt. Beispielsweise wird die Reihenfolge definiert, in der die Parameter im Stapel angezeigt werden. Stellen Sie einfach sicher, dass Sie Ihre **wWinMain** -Funktion wie gezeigt deklarieren.

Die **WinMain** -Funktion ist mit **wWinMain** identisch, mit dem Unterschied, dass die Befehlszeilenargumente als ANSI-Zeichenfolge übermittelt werden. Die Unicode-Version wird bevorzugt. Sie können die ANSI- **WinMain** -Funktion auch dann verwenden, wenn Sie das Programm als Unicode kompilieren. Um eine Unicode-Kopie der Befehlszeilenargumente abzurufen, müssen Sie die [**GetCommandLine**](/windows/desktop/api/processenv/nf-processenv-getcommandlinea) -Funktion aufrufen. Diese Funktion gibt alle Argumente in einer einzelnen Zeichenfolge zurück. Wenn die Argumente als Array im *argv*-Format angezeigt werden sollen, übergeben Sie diese Zeichenfolge an [**commandlineumargvw**](/windows/desktop/api/shellapi/nf-shellapi-commandlinetoargvw).

Wie weiß der Compiler, dass **wWinMain** anstelle der Standard- **Main** -Funktion aufgerufen werden soll? Tatsächlich ist zu tun, dass die Microsoft C-Lauf Zeit Bibliothek (CRT) eine Implementierung von **Main** bereitstellt, die entweder **WinMain** oder **wWinMain** aufruft.

> [!Note]  
> Die CRT führt einige zusätzliche Aufgaben in **Main** aus. Beispielsweise werden alle statischen Initialisierer vor **wWinMain** aufgerufen. Obwohl Sie den Linker anweisen können, eine andere Einstiegspunkt Funktion zu verwenden, verwenden Sie den Standardwert, wenn Sie mit der CRT verknüpfen. Andernfalls wird der CRT-Initialisierungs Code übersprungen, mit unvorhersehbaren Ergebnissen. (Beispielsweise werden globale Objekte nicht ordnungsgemäß initialisiert.)

 

Hier ist eine leere **WinMain** -Funktion.


```C++
INT WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance,
    PSTR lpCmdLine, INT nCmdShow)
{
    return 0;
}
```



Nachdem Sie nun über den Einstiegspunkt verfügen und einige grundlegende Terminologie und Codierungs Konventionen verstanden haben, sind Sie bereit, ein umfassendes Fensterprogramm zu erstellen.

## <a name="next"></a>Nächste

[Modul 1. Ihr erstes Windows-Programm](your-first-windows-program.md).

 

 