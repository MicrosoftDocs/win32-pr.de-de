---
description: In diesem Abschnitt wird beschrieben, wie sie aus einem nativen Windows Desktopprogramm drucken.
ms.assetid: C1EDBE38-9D18-41BB-961C-12CF2283C639
title: Drucken von Desktop-Apps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bf5e0ebab666258f62b1e6bb87497d38a1b521fdde9a7668bb28e3bb3e9868e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112110"
---
# <a name="desktop-app-printing"></a>Drucken von Desktop-Apps

In diesem Abschnitt wird beschrieben, wie sie aus einem nativen Windows Desktopprogramm drucken.

## <a name="overview"></a>Übersicht

Um beim Drucken aus einem nativen Windows-Programm die beste Benutzererfahrung zu bieten, muss das Programm so konzipiert sein, dass es aus einem dedizierten Thread gedruckt wird. In einem nativen Windows ist das Programm für die Verwaltung von Benutzeroberflächenereignissen und -meldungen verantwortlich. Druckvorgänge können Zeiträume mit intensiven Berechnungen erfordern, während der Anwendungsinhalt für den Drucker gerendert wird. Dies kann verhindern, dass das Programm auf Benutzerinteraktionen reagiert, wenn diese Verarbeitung im selben Thread wie die Ereignisverarbeitung der Benutzerinteraktion ausgeführt wird.

Wenn Sie bereits mit dem Schreiben eines nativen Windows-Multithreadprogramms vertraut sind, wechseln Sie direkt zu Drucken aus einer [Windows-Anwendung](how-to--print-from-a-windows-application.md) und erfahren, wie Sie Ihrem Programm Druckfunktionen hinzufügen.

### <a name="basic-windows-program-requirements"></a>Grundlegende Windows-Programmanforderungen

Um eine optimale Leistung und Programmschnelligkeit zu erzielen, führen Sie die Druckauftragsverarbeitung eines Programms nicht im Thread durch, der die Benutzerinteraktion verarbeitet.

Diese Trennung des Druckens von der Benutzerinteraktion beeinflusst, wie das Programm die Anwendungsdaten verwaltet. Sie sollten diese Auswirkungen sorgfältig verstehen, bevor Sie mit dem Schreiben der Anwendung beginnen. In den folgenden Themen werden die grundlegenden Anforderungen für die Verarbeitung des Druckens in einem separaten Thread eines Programms beschrieben.

### <a name="windows-program-basics"></a>Windows Grundlagen des Programms

Ein systemeigenes Windows-Programm muss die Hauptfensterprozedur bereitstellen, um die Fenstermeldungen zu verarbeiten, die vom Betriebssystem empfangen werden. Jedes Fenster in einem Windows programm verfügt über eine entsprechende **WndProc-Funktion,** die diese Fenstermeldungen verarbeitet. Der Thread, in dem diese Funktion ausgeführt wird, wird als Benutzeroberfläche oder Benutzeroberflächenthread bezeichnet.

**Verwenden Sie Ressourcen für Zeichenfolgen.**  
Verwenden Sie Zeichenfolgenressourcen aus der Ressourcendatei des Programms anstelle von Zeichenfolgenkonst constants für Zeichenfolgen, die möglicherweise geändert werden müssen, wenn Sie eine andere Sprache unterstützen. Bevor ein Programm eine Zeichenfolgenressource als Zeichenfolge verwenden kann, muss das Programm die Ressource aus der Ressourcendatei abrufen und in einen lokalen Speicherpuffer kopieren. Dies erfordert am Anfang einige zusätzliche Programmierung, ermöglicht jedoch eine einfachere Änderung, Übersetzung und Lokalisierung des Programms in der Zukunft.  
**Verarbeiten Sie Daten in Schritten.**  
Verarbeiten Sie den Druckauftrag in Schritten, die unterbrochen werden können. Durch diesen Entwurf kann der Benutzer einen langen Verarbeitungsvorgang abbrechen, bevor er abgeschlossen wird, und verhindert, dass das Programm andere Programme blockiert, die möglicherweise gleichzeitig ausgeführt werden.  
**Verwenden Sie Fensterbenutzerdaten.**  
Druckanwendungen verfügen häufig über mehrere Fenster und Threads. Um die Daten zwischen Threads und Verarbeitungsschritten ohne statische globale Variablen verfügbar zu halten, verweisen Sie mit einem Datenzeiger, der Teil des Fensters ist, in dem sie verwendet werden, auf die Datenstrukturen.  


Das folgende Codebeispiel zeigt einen Haupteinstiegspunkt für eine Druckanwendung. Dieses Beispiel zeigt die Verwendung von Zeichenfolgenressourcen anstelle von Zeichenfolgenkonst constants sowie die Hauptnachrichtenschleife, die die Fenstermeldungen des Programms verarbeitet.


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



### <a name="document-information"></a>Dokumentinformationen

Native Windows, die drucken, sollten für die Multithreadverarbeitung konzipiert sein. Eine der Anforderungen eines Multithreadentwurfs ist der Schutz der Datenelemente des Programms, damit sie sicher sind, dass mehrere Threads gleichzeitig verwendet werden können. Sie können Datenelemente schützen, indem Sie Synchronisierungsobjekte verwenden und die Daten organisieren, um Konflikte zwischen den Threads zu vermeiden. Gleichzeitig muss das Programm Änderungen an den Programmdaten verhindern, während sie gedruckt werden. Das Beispielprogramm verwendet verschiedene Multithreadprogrammiertechniken.

 **Synchronisierungsereignisse**  
Das Beispielprogramm verwendet Ereignisse, Threadhandles und Wartefunktionen, um die Verarbeitung zwischen dem Druckthread und dem Hauptprogramm zu synchronisieren und anzugeben, dass die Daten verwendet werden.  
**Anwendungsspezifische Windows Nachrichten**  
Das Beispielprogramm verwendet anwendungsspezifische Fenstermeldungen, um das Programm besser mit anderen nativen Windows kompatibel zu machen. Das Aufbrechen der Verarbeitung in kleinere Schritte und das Einstufen dieser Schritte in die Warteschlange in der Fenstermeldungsschleife erleichtert es Windows, die Verarbeitung zu verwalten, ohne andere Anwendungen zu blockieren, die möglicherweise auch auf dem Computer ausgeführt werden.  
**Datenstrukturen**  
Das Beispielprogramm ist nicht in einem objektorientierten Stil mithilfe von Objekten und Klassen geschrieben, obwohl es Datenelemente in Datenstrukturen gruppieren kann. Das Beispiel verwendet keinen objektorientierten Ansatz, um zu vermeiden, dass ein Ansatz besser oder schlechter als ein anderer ist.  
Sie können die Funktionen und Datenstrukturen des Beispielprogramms als Ausgangspunkt beim Entwerfen des Programms verwenden. Unabhängig davon, ob Sie ein objektorientiertes Programm entwerfen möchten oder nicht, ist es wichtig, die zugehörigen Datenelemente zu gruppieren, damit Sie sie bei Bedarf sicher in verschiedenen Threads verwenden können.  


### <a name="printer-device-context"></a>Druckergerätekontext

Beim Drucken möchten Sie möglicherweise den Inhalt rendern, der in einem Gerätekontext gedruckt werden soll. [How To: Retrieve a Printer Device Context](retrieving-a-printer-device-context.md) (How To: Abrufen eines Druckergerätekontexts) beschreibt die verschiedenen Möglichkeiten zum Abrufen eines Druckergerätekontexts.

## <a name="related-topics"></a>Zugehörige Themen



[Drucken aus einer Windows Anwendung](how-to--print-from-a-windows-application.md)


 

 



