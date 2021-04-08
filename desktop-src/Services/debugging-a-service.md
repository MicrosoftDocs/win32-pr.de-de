---
description: Sie können eine der folgenden Methoden verwenden, um den Dienst zu debuggen.
ms.assetid: 6f4ae117-2120-4c1e-b69f-641ce2e633fa
title: Debuggen eines Diensts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ebd99acfc6ad0e436b7f726c96af9e5d1c58442
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750800"
---
# <a name="debugging-a-service"></a>Debuggen eines Diensts

Sie können eine der folgenden Methoden verwenden, um den Dienst zu debuggen.

-   Verwenden Sie den Debugger, um den Dienst zu debuggen, während er ausgeführt wird. Rufen Sie zuerst die Prozess-ID (PID) des Dienst Prozesses ab. Nachdem Sie die PID abgerufen haben, fügen Sie Sie an den laufenden Prozess an. Syntax Informationen finden Sie in der Dokumentation, die in Ihrem Debugger enthalten ist.
-   Rufen Sie die [**DebugBreak**](/windows/desktop/api/debugapi/nf-debugapi-debugbreak) -Funktion auf, um den Debugger für Just-in-Time-Debugging aufzurufen.
-   Geben Sie einen Debugger an, der beim Starten eines Programms verwendet werden soll. Erstellen Sie hierzu einen Schlüssel mit dem Namen " **Bild Datei Ausführungs Optionen** " im folgenden Registrierungs Speicherort:

    **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion**

    Erstellen Sie einen Unterschlüssel mit dem gleichen Namen wie Ihr Dienst (z. b. MYSERV.EXE). Fügen Sie diesem Unterschlüssel einen Wert vom Typ **reg \_ SZ** namens **Debugger** hinzu. Verwenden Sie den vollständigen Pfad zum Debugger als Zeichen folgen Wert. Wählen Sie im Applet System Steuerungs applet ihren Dienst aus, klicken Sie auf **Start** , und aktivieren Sie **die Option Dienst für die Interaktion mit dem Desktop zulassen**. Der Dienst muss ein interaktiver Dienst sein, andernfalls kann der Debugger nicht auf dem Standard Desktop ausgeführt werden. Beachten Sie, dass dieses Verfahren ab Windows Vista nicht mehr unterstützt wird, da alle Dienste in einer Sitzung ausgeführt werden, die ausschließlich für Dienste reserviert ist und die Anzeige einer Benutzeroberfläche nicht unterstützt.

-   Verwenden Sie die [Ereignis Ablauf Verfolgung](/windows/desktop/ETW/event-tracing-portal) zum Protokollieren von Informationen.

Um den Initialisierungs Code eines automatischen Start Diensts zu debuggen, müssen Sie den Dienst temporär installieren und ausführen, um einen Dienst zu starten.

Manchmal kann es erforderlich sein, einen Dienst als Konsolenanwendung zu Debuggingzwecken auszuführen. In diesem Szenario gibt die Funktion " [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) " einen Fehler bei der **\_ \_ Dienst \_ Controller \_ Verbindung** zurück. Stellen Sie daher sicher, dass Sie Ihren Code so strukturieren, dass er nicht aufgerufen wird, wenn dieser Fehler zurückgegeben wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Debuggen einer Dienst Anwendung](https://msdn.microsoft.com/library/cc267835.aspx)
</dt> <dt>

[Debuggingtools für Windows](https://msdn.microsoft.com/library/cc267445.aspx)
</dt> </dl>

 

 
