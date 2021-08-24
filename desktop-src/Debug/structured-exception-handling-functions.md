---
description: Die folgenden Funktionen werden bei der strukturierten Ausnahmebehandlung verwendet.
ms.assetid: 61cf055b-eb9a-4e56-9d36-21fc95adea77
title: Strukturierte Funktionen zur Ausnahmebehandlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 947cde636051e6d51428b1d75b7d299ce196b0f4335e096f99d6da6a277ae259
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815500"
---
# <a name="structured-exception-handling-functions"></a>Strukturierte Funktionen zur Ausnahmebehandlung

Die folgenden Funktionen werden bei der strukturierten Ausnahmebehandlung verwendet.

-   [**AbnormalTermination**](abnormaltermination.md)

    Gibt an, ob der **\_ \_ try-Block** eines Beendigungshandlers normal beendet wurde.

-   [**AddVectoredContinueHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredcontinuehandler)

    Registriert einen vektorierten Continue-Handler.

-   [**AddVectoredExceptionHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredexceptionhandler)

    Registriert einen Vektorausnahmehandler.

-   [**GetExceptionCode**](getexceptioncode.md)

    Ruft einen Code ab, der den Typ der aufgetretenen Ausnahme identifiziert.

-   [**GetExceptionInformation**](getexceptioninformation.md)

    Ruft eine computerunabhängige Beschreibung einer Ausnahme sowie Informationen zum Computerzustand ab, der beim Auftreten der Ausnahme für den Thread vorhanden war.

-   [**Raiseexception**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception)

    Löst eine Ausnahme im aufrufenden Thread aus.

-   [**RemoveVectoredContinueHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredcontinuehandler)

    Aufheben der Registrierung eines vektorierten Continue-Handlers.

-   [**RemoveVectoredExceptionHandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredexceptionhandler)

    Aufheben der Registrierung eines Vektorausnahmehandlers.

-   [**RtlAddGrowableFunctionTable**](/windows/desktop/api/WinNT/nf-winnt-rtladdgrowablefunctiontable)

    Informiert das System über eine dynamische Funktionstabelle, die einen Speicherbereich darstellt, der Code enthält.

-   [**RtlDeleteGrowableFunctionTable**](/windows/desktop/api/WinNT/nf-winnt-rtldeletegrowablefunctiontable)

    Informiert das System darüber, dass eine zuvor gemeldete dynamische Funktionstabelle nicht mehr verwendet wird.

-   [**RtlGrowFunctionTable**](/windows/desktop/api/WinNT/nf-winnt-rtlgrowfunctiontable)

    Meldet, dass eine dynamische Funktionstabelle vergrößert wurde.

-   [**SetUnhandledExceptionFilter**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setunhandledexceptionfilter)

    Ermöglicht einer Anwendung, den Ausnahmehandler der obersten Ebene jedes Threads und Prozesses zu ersetzen.

-   [**UnhandledExceptionFilter**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-unhandledexceptionfilter)

    Übergibt nicht behandelte Ausnahmen an den Debugger, wenn der Prozess gedebuggt wird.

-   [**VectoredHandler**](/windows/desktop/api/WinNT/nc-winnt-pvectored_exception_handler)

    Eine anwendungsdefinierte Funktion, die als Vektorausnahmehandler dient.

Die folgenden Funktionen werden nur auf 64-Bit-Windows verwendet.

-   [**RtlAddFunctionTable**](/windows/desktop/api/WinNT/nf-winnt-rtladdfunctiontable)

    Fügt der Dynamischen Funktionstabellenliste eine dynamische Funktionstabelle hinzu.

-   [**RtlCaptureContext**](/windows/desktop/api/WinNT/nf-winnt-rtlcapturecontext)

    Ruft einen Kontextdatensatz im Kontext des Aufrufers ab.

-   [**RtlDeleteFunctionTable**](/windows/desktop/api/WinNT/nf-winnt-rtldeletefunctiontable)

    Entfernt eine dynamische Funktionstabelle aus der Liste der dynamischen Funktionstabellen.

-   [**RtlInstallFunctionTableCallback**](/windows/desktop/api/WinNT/nf-winnt-rtlinstallfunctiontablecallback)

    Fügt der Dynamischen Funktionstabellenliste eine dynamische Funktionstabelle hinzu.

-   [**RtlRestoreContext**](/windows/desktop/api/WinNT/nf-winnt-rtlrestorecontext)

    Stellt den Kontext des Aufrufers im angegebenen Kontextdatensatz wieder her.

 

 
