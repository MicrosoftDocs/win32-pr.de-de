---
description: In diesem Abschnitt wird beschrieben, wie Sie aus einem nativen Windows-Desktop Programm drucken.
ms.assetid: C1EDBE38-9D18-41BB-961C-12CF2283C639
title: Drucken von Desktop-Apps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbecbac997d000f50e7c912e57be42cc8fe239b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353919"
---
# <a name="desktop-app-printing"></a>Drucken von Desktop-Apps

In diesem Abschnitt wird beschrieben, wie Sie aus einem nativen Windows-Desktop Programm drucken.

## <a name="overview"></a>Übersicht

Um die beste Benutzer Leistung beim Drucken von einem systemeigenen Windows-Programm zu gewährleisten, muss das Programm so entworfen werden, dass es aus einem dedizierten Thread gedruckt wird. In einem systemeigenen Windows-Programm ist das Programm für die Verwaltung von Ereignissen und Nachrichten von Benutzeroberflächen zuständig. Druckvorgänge können Zeiträume intensiver Berechnungen erfordern, da der Anwendungs Inhalt für den Drucker gerendert wird. Dies kann verhindern, dass das Programm auf Benutzerinteraktionen reagiert, wenn diese Verarbeitung im gleichen Thread ausgeführt wird wie die Ereignisverarbeitung der Benutzerinteraktion.

Wenn Sie bereits wissen, wie Sie ein System eigenes Windows-Programm mit mehreren Threads schreiben, gehen Sie direkt zum [Drucken aus einer Windows-Anwendung](how-to--print-from-a-windows-application.md) , und erfahren Sie, wie Sie dem Programm Druckfunktionen hinzufügen.

### <a name="basic-windows-program-requirements"></a>Grundlegende Windows-Programmanforderungen

Um eine optimale Leistung und Programm Reaktionsfähigkeit zu erzielen, sollten Sie die Druckauftrags Verarbeitung eines Programms nicht in dem Thread ausführen, der die Benutzerinteraktion verarbeitet.

Diese Trennung von Druck von Benutzerinteraktion wirkt sich darauf aus, wie das Programm die Anwendungsdaten verwaltet. Sie sollten diese Implikationen gründlich verstehen, bevor Sie mit dem Schreiben der Anwendung beginnen. In den folgenden Themen werden die grundlegenden Anforderungen für die Handhabung von Druck Vorgängen in einem separaten Thread eines Programms beschrieben.

### <a name="windows-program-basics"></a>Windows-Programm Grundlagen

Ein System eigenes Windows-Programm muss die Hauptfenster Prozedur bereitstellen, um die Fenster Meldungen zu verarbeiten, die vom Betriebssystem empfangen werden. Jedes Fenster in einem Windows-Programm verfügt über eine entsprechende **WndProc** -Funktion, die diese Fenster Meldungen verarbeitet. Der Thread, in dem diese Funktion ausgeführt wird, wird als Benutzeroberfläche oder UI-Thread bezeichnet.

**Verwenden Sie Ressourcen für Zeichen folgen.**  
Verwenden Sie Zeichen folgen Ressourcen aus der Ressourcen Datei des Programms anstelle von Zeichen folgen Konstanten für Zeichen folgen, die möglicherweise geändert werden müssen, wenn Sie eine andere Sprache unterstützen. Bevor ein Programm eine Zeichen folgen Ressource als Zeichenfolge verwenden kann, muss das Programm die Ressource aus der Ressourcen Datei abrufen und in einen lokalen Speicherpuffer kopieren. Dies erfordert einige zusätzliche Programmierung am Anfang, ermöglicht aber eine einfachere Änderung, Übersetzung und Lokalisierung des Programms in der Zukunft.  
**Verarbeiten von Daten in Schritten.**  
Verarbeiten Sie den Druckauftrag in Schritten, die unterbrochen werden können. Dieser Entwurf ermöglicht dem Benutzer, einen langen Verarbeitungsvorgang abzubrechen, bevor er abgeschlossen wird, und verhindert, dass das Programm andere Programme blockiert, die möglicherweise gleichzeitig ausgeführt werden.  
**Verwenden von Windows-Benutzerdaten.**  
Das Drucken von Anwendungen hat häufig mehrere Fenster und Threads. Um die Daten zwischen Threads und Verarbeitungsschritten verfügbar zu halten, ohne statische, globale Variablen zu verwenden, verweisen Sie auf die Datenstrukturen durch einen Datenzeiger, der Teil des Fensters ist, in dem Sie verwendet werden.  


Das folgende Codebeispiel zeigt einen Haupteinstiegspunkt für eine Druckanwendung. In diesem Beispiel wird gezeigt, wie Zeichen folgen Ressourcen anstelle von Zeichen folgen Konstanten verwendet werden und wie die Hauptnachrichten Schleife zum Verarbeiten der Fenster Meldungen des Programms angezeigt wird.


```C++
int APIENTRY 
wWinMain(
        HINSTANCE hInstance, 
        HINSTANCE hPrevInstance, 
        LPWSTR lpCmdLine, 
        int nCmdShow
)
{
    UNREFERENCED_PARAMETER(hPrevInstance);
    UNREFERENCED_PARAMETER(lpCmdLine);

    MSG msg;
    HACCEL hAccelTable;
    HRESULT hr = S_OK;

    // Register the main window class name
    WCHAR szWindowClass[MAXIMUM_RESOURCE_STRING_LENGTH];            
    LoadString(
        hInstance, 
        IDC_PRINTSAMPLE, 
        szWindowClass, 
        MAXIMUM_RESOURCE_STRING_LENGTH);
    MyRegisterClass(hInstance, szWindowClass);

    // Perform application initialization:
    if (!InitInstance (hInstance, nCmdShow))
    {
        // Unable to initialize this instance of the application
        //  so display error message and exit
        MessageBoxWithResourceString (
            hInstance, 
            GetDesktopWindow(), 
            IDS_ERROR_INSTINITFAIL, 
            IDS_CAPTION_ERROR, 
            (MB_OK | MB_ICONEXCLAMATION));
        return FALSE;
    }    
    
    // Init COM for printing interfaces
    if (FAILED(hr = CoInitializeEx(0, COINIT_MULTITHREADED)))
    {
        // Unable to initialize COM
        //  so display error message and exit
        MessageBoxWithResourceString (
            hInstance, 
            GetDesktopWindow(), 
            IDS_ERROR_COMINITFAIL, 
            IDS_CAPTION_ERROR, 
            (MB_OK | MB_ICONEXCLAMATION));
        return FALSE;
    }

    hAccelTable = LoadAccelerators(
                    hInstance, 
                    MAKEINTRESOURCE(IDC_PRINTSAMPLE));

    // Main message handling loop
    while (GetMessage(&msg, NULL, 0, 0))
    {
        if (!TranslateAccelerator(msg.hwnd, hAccelTable, &msg))
        {
            TranslateMessage(&msg);
            DispatchMessage(&msg);
        }
    }

    // Uninitialize (close) the COM interface
    CoUninitialize();

    return (int) msg.wParam;
}
```



### <a name="document-information"></a>Dokument Informationen

Systemeigene Windows-Programme, die drucken, sollten für die Verarbeitung mit mehreren Threads entwickelt werden. Eine der Anforderungen eines Multithreaddesigns besteht darin, die Datenelemente des Programms so zu schützen, dass Sie sicher sind, dass mehrere Threads gleichzeitig verwendet werden können. Sie können Datenelemente mithilfe von Synchronisierungs Objekten schützen und die Daten so organisieren, dass Konflikte zwischen den Threads vermieden werden. Gleichzeitig muss das Programmänderungen an den Programm Daten beim Drucken verhindern. Das Beispielprogramm verwendet mehrere verschiedene multithreadprogrammierungstechniken.

 **Synchronisierungs Ereignisse**  
Das Beispielprogramm verwendet Ereignisse, Thread Handles und Wait-Funktionen, um die Verarbeitung zwischen dem Druck Thread und dem Hauptprogramm zu synchronisieren und anzugeben, dass die Daten verwendet werden.  
**Anwendungsspezifische Windows-Meldungen**  
Das Beispielprogramm verwendet anwendungsspezifische Fenster Meldungen, um das Programm mit anderen systemeigenen Windows-Programmen kompatibler zu gestalten. Wenn Sie die Verarbeitung in kleinere Schritte aufteilen und diese Schritte in der Fenster Nachrichten Schleife in eine Warteschlange stellen, erleichtert Windows die Verwaltung der Verarbeitung, ohne dass andere Anwendungen blockiert werden müssen, die möglicherweise auch auf dem Computer ausgeführt werden.  
**Datenstrukturen**  
Das Beispielprogramm wird nicht in einem objektorientierten Stil mithilfe von-Objekten und-Klassen geschrieben, obwohl Datenelemente in Datenstrukturen gruppiert werden. Das Beispiel verwendet keinen objektorientierten Ansatz, um zu verhindern, dass ein Ansatz besser oder schlechter als ein anderer Ansatz ist.  
Sie können die Funktionen und Datenstrukturen des Beispiel Programms als Ausgangspunkt verwenden, wenn Sie das Programm entwerfen. Unabhängig davon, ob Sie ein objektorientiertes Programm entwerfen oder nicht, ist es wichtig, sich daran zu erinnern, die zugehörigen Datenelemente zu gruppieren, damit Sie Sie bei Bedarf sicher in verschiedenen Threads verwenden können.  


### <a name="printer-device-context"></a>Drucker Gerätekontext

Beim drucken möchten Sie möglicherweise den zu druckenden Inhalt in einem Gerätekontext darstellen. Gewusst [wie: Abrufen eines Drucker Geräte Kontexts](retrieving-a-printer-device-context.md) beschreibt die verschiedenen Methoden, mit denen Sie einen Drucker Gerätekontext abrufen können.

## <a name="related-topics"></a>Zugehörige Themen



[Drucken aus einer Windows-Anwendung](how-to--print-from-a-windows-application.md)


 

 



