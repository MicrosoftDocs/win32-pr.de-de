---
description: Wenn Sie bereit sind, die com+-Funktionalität in den Microsoft Visual C++ Komponenten zu debuggen, können Sie Visual C++ Projekt oder das Verwaltungs Programmkomponenten Dienste konfigurieren, um den Debugger zu starten.
ms.assetid: 206467ac-108a-49de-a884-66959dc77650
title: In Visual C++ geschriebene debuggingkomponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a14e4b6324cc69531f09612c2af37fa03a036fd4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106338896"
---
# <a name="debugging-components-written-in-visual-c"></a>In Visual C++ geschriebene debuggingkomponenten

Wenn Sie bereit sind, die com+-Funktionalität in den Microsoft Visual C++ Komponenten zu debuggen, können Sie Visual C++ Projekt oder das Verwaltungs Programmkomponenten Dienste konfigurieren, um den Debugger zu starten. Wenn Sie Visual C++ verwenden, können Sie mit einem Remote Client debuggen, indem Sie das OLE-RPC-und JIT-Debugging (Just-in-Time) verwenden. Wenn Sie den Client nicht im Debugger ausführen können oder wenn der Client auf einem anderen Computer ausgeführt wird, können Sie die com+-Einstellung **in Debugger** verwenden. Diese finden Sie im Verwaltungs Programmkomponenten Dienste als Kontrollkästchen auf der Registerkarte **erweitert** im Dialogfeld COM+-Anwendungs **Eigenschaften** .

Wenn Sie das Debuggen abgeschlossen haben, sollten Sie die com+-Anwendungen Herunterfahren, die Sie Debuggen. Wenn ein Server Prozess weiterhin ausgeführt wird, erhalten Sie möglicherweise eine Fehlermeldung, wenn Sie das nächste Mal versuchen, eine DLL zu erstellen, wenn die vorhandene DLL noch in den Arbeitsspeicher geladen ist. Zum Herunterfahren einer COM+-Anwendung klicken Sie in der Konsolen Struktur mit der rechten Maustaste auf die Anwendung, und klicken Sie dann auf **herunter** fahren.

> [!Note]  
> Wenn Sie Transaktionen verwenden, möchten Sie möglicherweise auch den Transaktions Timeout erhöhen, der standardmäßig 60 Sekunden beträgt. Sie können auch den Wert 0 angeben und einen unbegrenzten Transaktions Timeout Zeitraum angeben. Ändern Sie mithilfe des Verwaltungs Programms Komponenten Dienste die Einstellung Transaktions Timeout auf der Registerkarte **Optionen** des Fensters **Eigenschaften von Arbeitsplatz** .

 

## <a name="debugging-server-application-components-with-visual-c"></a>Debuggen von Server Anwendungskomponenten mit Visual C++

Wenn Sie com+-Server Anwendungen debuggen, können Sie Remote Aufrufe Debuggen, indem Sie sowohl die Client-als auch die Serveranwendung in den Debugger laden. Mit Visual C++ können Sie Remote Aufrufe ihrer Komponenten über die Just-in-time (JIT)-und OLE-RPC-Einstellungen Debuggen. Die JIT-Einstellung bewirkt, dass die kompilierte Komponente den Visual C++ Debugger startet, wenn ein Fehler auftritt. mit der OLE-RPC-Einstellung kann der Debugger beim Durchlaufen des Codes von Client zu Komponente wechseln.

Wenn diese Funktionen aktiviert sind, können Sie den Client unter dem Debugger starten. Wenn der Client die Komponente aufruft, führt der Debugger einen Einzelschritt in den Code der Komponente im Server Prozess aus, auch wenn sich der Server auf einem anderen Computer im Netzwerk befindet. Eine Debugsitzung wird ggf. automatisch auf dem Server Computer gestartet. Ebenso wird beim einmaligen durch springen der Return-Anweisung im Code der Komponente das Debuggen zur nächsten Anweisung im Client Code zurückgegeben.

> [!Note]  
> Mithilfe der com+-Einstellung **in der Debugger** -Einstellung können Sie möglicherweise einige Schritte speichern. Dies ermöglicht es Ihnen, den Visual C++ (oder einen anderen) Debugger anzugeben, ohne spezielle Debugeinstellungen in der Visual C++ Umgebung vornehmen zu müssen. Diese finden Sie im Verwaltungs Programmkomponenten Dienste als Kontrollkästchen auf der Registerkarte **erweitert** im Dialogfeld COM+-Anwendungs **Eigenschaften** . Weitere Informationen finden Sie unter "Debuggen ohne Visual C++" in diesem Thema.

 

Wenn die COM+-Anwendung, die die Komponente enthält, eine Serveranwendung ist, müssen Sie zunächst die Anwendung mithilfe des Verwaltungs Programms Komponenten Dienste Herunterfahren. Klicken Sie hierzu in der Konsolen Struktur mit der rechten Maustaste auf die COM+-Anwendung, und klicken Sie dann auf **herunter** fahren.

**So aktivieren Sie das RPC-Debugging in Visual C++**

1.  Klicken Sie in Visual C++ im **Menü Extras** auf **Optionen**.

2.  Aktivieren Sie im Dialogfeld **Optionen** auf der Registerkarte **Debuggen** die Kontrollkästchen **OLE-RPC-Debuggen** und **Just-in-Time-Debuggen** .

3.  Klicken Sie auf **OK**.

Starten Sie das-Client Projekt im Debugger, um mit dem Debuggen zu beginnen.

Sie können die Komponente auch Debuggen, ohne den Client im Debugger zu starten. In diesem Fall muss die Komponente den Debugger eigenständig starten. Zu diesem Zweck muss das Komponenten Projekt eine ausführbare Datei für die Debugsitzung sowie die com+-Anwendungs-ID angeben.

**So aktivieren Sie eine Server Anwendungs Komponente, um den Visual C++ Debugger zu starten**

1.  Klicken Sie im Menü **Projekt** auf **Einstellungen**.

2.  Wählen Sie im Dialogfeld **Projekteinstellungen** im Feld **Einstellungen für** die Option **Win32 Debug** aus.

3.  Wählen Sie auf der Registerkarte **Debuggen** im Feld **Kategorie** die Option **Allgemein** aus.

4.  Geben Sie im Feld **ausführbare Datei für Debugsitzung** den voll qualifizierten Pfad für Dllhost.exe ein, gefolgt von einem Argument, das die Anwendungs-ID der com+-Anwendung angibt, die die Komponente enthält.

    > [!Note]  
    > Mithilfe des Verwaltungs Tools Komponenten Dienste finden Sie die Anwendungs-ID auf der Registerkarte **Allgemein** im Dialogfeld **Eigenschaften** der com+-Anwendung. Dies ist ein Beispiel:

     

    > [!Note]  
    > C: \\ Winnt \\ system32 \\Dllhost.exe/ProcessID: {ApplicationId}

     

5.  Klicken Sie auf **OK**.

Sie können jetzt Breakpoints festlegen, den Debugger starten und mit dem Ausführen von Aufrufen an die Komponente beginnen.

## <a name="debugging-library-application-components-with-visual-c"></a>Debuggen von Bibliotheks Anwendungskomponenten mit Visual C++

Wenn Sie Komponenten in einer Bibliotheks Anwendung debuggen möchten, müssen Sie das Projekt des Clients konfigurieren, da der Client Prozess die Bibliotheks Anwendung hostet.

**So aktivieren Sie das Debuggen von Bibliotheksanwendungen mit Visual C++**

1.  Klicken Sie in Visual C++ im Menü **Projekt** auf **Einstellungen**.

2.  Klicken Sie im Dialogfeld **Projekteinstellungen** im Feld **Einstellungen für** auf **Win32 Debuggen**.

3.  Klicken Sie auf der Registerkarte **Debuggen** im Feld **Kategorie** auf **zusätzliche DLLs**.

4.  Fügen Sie in der Liste **Module** die Komponenten-DLLs in der Bibliotheks Anwendung hinzu. Dies ermöglicht es Ihnen, Breakpoints festzulegen, bevor die dll tatsächlich geladen wird.

5.  Klicken Sie auf **OK**.

## <a name="debugging-without-visual-c"></a>Debuggen ohne Visual C++

Unabhängig davon, ob Sie Visual C++ für das Debuggen verwenden, können Sie die Einstellung **in Debugger starten** verwenden, um den Debugger anzugeben, in dem die Komponenten ausgeführt werden sollen.

**So geben Sie einen Debugger über das Verwaltungs Programm "Komponenten Dienste" an**

1.  Wählen Sie in der Konsolen Struktur die COM+-Bibliotheks Anwendung aus, die die Komponenten enthält, die Sie debuggen möchten.

2.  Klicken Sie mit der rechten Maustaste auf die Anwendung, und klicken Sie auf **Eigenschaften**.

3.  Klicken Sie im Dialogfeld **Eigenschaften** der Anwendung auf die Registerkarte **erweitert** .

4.  Aktivieren Sie unter **Debuggen** das Kontrollkästchen **in Debugger starten** .

5.  Geben Sie im Feld **Debuggerpfad** den Pfad zu dem Debugger ein, den Sie verwenden möchten. Sie können auch auf **Durchsuchen** klicken, um den Debugger zu suchen. Im folgenden finden Sie ein Beispiel: C: \\ Winnt \\ system32 \\Ntsd.exe.

6.  Klicken Sie auf **OK**.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[In Visual Basic geschriebene debuggingkomponenten](debugging-components-written-in-visual-basic.md)
</dt> </dl>

 

 



