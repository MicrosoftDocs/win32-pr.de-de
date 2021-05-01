---
title: WinMain The Application Entry Point description: WinMain: The Application Entry Point ms.assetid: 389da5d4-d0f9-4339-be6c-0f4fecc59316 ms.topic: article ms.date: 05/31/2018
---

# <a name="winmain-the-application-entry-point"></a>WinMain: Der Anwendungseinstiegspunkt

Jedes Windows-Programm enthält eine Einstiegspunktfunktion mit dem Namen **WinMain** oder **wWinMain.** Hier ist die Signatur für **wWinMain**.


```C++
int WINAPI wWinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, PWSTR pCmdLine, int nCmdShow);
```



Die vier Parameter sind:

-   *hInstance* wird als "Handle für eine Instanz" oder "Handle für ein Modul" bezeichnet. Das Betriebssystem verwendet diesen Wert, um die ausführbare Datei (EXE) zu identifizieren, wenn sie in den Arbeitsspeicher geladen wird. Das Instanzhand handle wird für bestimmte Windows-Funktionen benötigt, z. B. zum Laden von Symbolen oder Bitmaps.
-   *hPrevInstance hat* keine Bedeutung. Es wurde in 16-Bit-Windows verwendet, ist aber jetzt immer 0 (null).
-   *pCmdLine* enthält die Befehlszeilenargumente als Unicode-Zeichenfolge.
-   *nCmdShow ist* ein Flag, das anspricht, ob das Hauptanwendungsfenster minimiert, maximiert oder normal angezeigt wird.

Die Funktion gibt einen **int-Wert** zurück. Der Rückgabewert wird nicht vom Betriebssystem verwendet, aber Sie können den Rückgabewert verwenden, um einen Statuscode an ein anderes Programm zu übermitteln, das Sie schreiben.

**WINAPI ist** die Aufrufkonvention. Eine *Aufrufkonvention definiert,* wie eine Funktion Parameter vom Aufrufer empfängt. Beispielsweise wird die Reihenfolge definiert, in der Parameter auf dem Stapel angezeigt werden. Stellen Sie einfach sicher, dass Sie Ihre **wWinMain-Funktion wie** gezeigt deklarieren.

Die **WinMain-Funktion** ist mit **wWinMain** identisch, mit der Ausnahme, dass die Befehlszeilenargumente als ANSI-Zeichenfolge übergeben werden. Die Unicode-Version wird bevorzugt. Sie können die ANSI **WinMain-Funktion auch dann verwenden,** wenn Sie Das Programm als Unicode kompilieren. Um eine Unicode-Kopie der Befehlszeilenargumente abzurufen, rufen Sie die [**GetCommandLine-Funktion**](/windows/desktop/api/processenv/nf-processenv-getcommandlinea) auf. Diese Funktion gibt alle Argumente in einer einzelnen Zeichenfolge zurück. Wenn Sie die Argumente als *argv-style-Array* verwenden möchten, übergeben Sie diese Zeichenfolge an [**CommandLineToArgvW.**](/windows/desktop/api/shellapi/nf-shellapi-commandlinetoargvw)

Woher weiß der Compiler, dass **er wWinMain** anstelle der **Standardmäßig-Main-Funktion** aufruft? Tatsächlich stellt die Microsoft C-Laufzeitbibliothek (CRT) eine Implementierung von **main** bereit, die entweder **WinMain** oder **wWinMain** aufruft.

> [!Note]  
> Die CRT führt einige zusätzliche Arbeit innerhalb von **main** aus. Beispielsweise werden alle statischen Initialisierer vor **wWinMain** aufgerufen. Obwohl Sie den Linker anzuweisen können, eine andere Einstiegspunktfunktion zu verwenden, verwenden Sie den Standardwert, wenn Sie eine Verknüpfung mit der CRT erstellen. Andernfalls wird der CRT-Initialisierungscode mit unvorhersehbaren Ergebnissen übersprungen. (Globale Objekte werden beispielsweise nicht ordnungsgemäß initialisiert.)

 

Hier ist eine leere **WinMain-Funktion.**


```C++
INT WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance,
    PSTR lpCmdLine, INT nCmdShow)
{
    return 0;
}
```



Nachdem Sie nun über den Einstiegspunkt verfügen und einige der grundlegenden Terminologie- und Codierungskonventionen kennen, können Sie ein vollständiges Window-Programm erstellen.

## <a name="next"></a>Nächste

[Modul 1. Ihr erstes Windows-Programm.](your-first-windows-program.md)

 

 
