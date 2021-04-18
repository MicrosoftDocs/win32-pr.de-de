---
description: Die folgenden Funktionen werden bei der strukturierten Ausnahmebehandlung verwendet.
ms.assetid: 61cf055b-eb9a-4e56-9d36-21fc95adea77
title: Funktionen für die strukturierte Ausnahmebehandlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c70b431be2961a55bba28bdfe07723e93b95ac69
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343590"
---
# <a name="structured-exception-handling-functions"></a>Funktionen für die strukturierte Ausnahmebehandlung

Die folgenden Funktionen werden bei der strukturierten Ausnahmebehandlung verwendet.

-   [**AbnormalTermination**](abnormaltermination.md)

    Gibt an, ob der **\_ \_ try** -Block eines Beendigungs Handlers normal beendet wurde.

-   [**Addvector edcontinuehandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredcontinuehandler)

    Registriert einen Vektoren Continue-Handler.

-   [**Addvector edexceptionhandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-addvectoredexceptionhandler)

    Registriert einen Vektor Ausnahmehandler.

-   [**GetExceptionCode**](getexceptioncode.md)

    Ruft einen Code ab, der den Typ der aufgetretenen Ausnahme identifiziert.

-   [**GetExceptionInformation**](getexceptioninformation.md)

    Ruft eine Computer unabhängige Beschreibung einer Ausnahme und Informationen zum Computer Zustand ab, der für den Thread vorhanden war, als die Ausnahme aufgetreten ist.

-   [**RaiseException**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception)

    Löst eine Ausnahme im aufrufenden Thread aus.

-   [**Removevector edcontinuehandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredcontinuehandler)

    Hebt die Registrierung eines vektorcontinue Continue-Handlers auf.

-   [**Removevector edexceptionhandler**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-removevectoredexceptionhandler)

    Hebt die Registrierung eines Vektoren Ausnahme Handlers auf.

-   [**Rtladdgrowablefunctiontable**](/windows/desktop/api/WinNT/nf-winnt-rtladdgrowablefunctiontable)

    Informiert das System über eine dynamische Funktions Tabelle, die einen Bereich des Arbeitsspeichers darstellt, der Code enthält.

-   [**Rtldeletegrowablefunctiontable**](/windows/desktop/api/WinNT/nf-winnt-rtldeletegrowablefunctiontable)

    Informiert das System darüber, dass eine zuvor gemeldete dynamische Funktions Tabelle nicht mehr verwendet wird.

-   [**Rtlgrowfunctiontable**](/windows/desktop/api/WinNT/nf-winnt-rtlgrowfunctiontable)

    Meldet, dass eine dynamische Funktions Tabelle die Größe übersteigt.

-   [**"Set"-Filter**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-setunhandledexceptionfilter)

    Ermöglicht es einer Anwendung, den Ausnahmehandler der obersten Ebene jedes Threads und Prozesses zu ersetzen.

-   [**UnhandledExceptionFilter "**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-unhandledexceptionfilter)

    Übergibt nicht behandelte Ausnahmen an den Debugger, wenn der Prozess gedebuggt wird.

-   [**Vectoriedhandler**](/windows/desktop/api/WinNT/nc-winnt-pvectored_exception_handler)

    Eine Anwendungs definierte Funktion, die als ein Vektoren-Ausnahmehandler fungiert.

Die folgenden Funktionen werden nur für 64-Bit-Fenster verwendet.

-   [**RtlAddFunctionTable**](/windows/desktop/api/WinNT/nf-winnt-rtladdfunctiontable)

    Fügt der Liste der dynamischen Funktionstabellen eine dynamische Funktions Tabelle hinzu.

-   [**Rtlcapturecontext**](/windows/desktop/api/WinNT/nf-winnt-rtlcapturecontext)

    Ruft einen Kontext Daten Satz im Kontext des Aufrufers ab.

-   [**Rtldeletefunctiontable**](/windows/desktop/api/WinNT/nf-winnt-rtldeletefunctiontable)

    Entfernt eine dynamische Funktions Tabelle aus der Liste der dynamischen Funktionstabellen.

-   [**Rtlinstallfunctiontablecallback**](/windows/desktop/api/WinNT/nf-winnt-rtlinstallfunctiontablecallback)

    Fügt der Liste der dynamischen Funktionstabellen eine dynamische Funktions Tabelle hinzu.

-   [**Rtlrestorecontext**](/windows/desktop/api/WinNT/nf-winnt-rtlrestorecontext)

    Stellt den Kontext des Aufrufers für den angegebenen Kontext Daten Satz wieder her.

 

 
