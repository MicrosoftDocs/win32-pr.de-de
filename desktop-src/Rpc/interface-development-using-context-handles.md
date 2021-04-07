---
title: Schnittstellen Entwicklung mithilfe von Kontext Handles
description: In der Regel erstellen Sie ein Kontext Handle, indem Sie das \ Context \_ handle \-Attribut für eine Typdefinition in der IDL-Datei angeben.
ms.assetid: e4caf91f-f92d-4aef-a20f-0a3073230640
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8474d533b27ba1543a9d522dfa4478d306b33cf2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729312"
---
# <a name="interface-development-using-context-handles"></a>Schnittstellen Entwicklung mithilfe von Kontext Handles

In der Regel erstellen Sie ein Kontext Handle, indem Sie das \[ [**Kontext \_ handle**](/windows/desktop/Midl/context-handle) - \] Attribut für eine Typdefinition in der IDL-Datei angeben. Die Typdefinition gibt auch implizit eine Kontext-Lauf Ablaufroutine an, die Sie bereitstellen müssen. Wenn die Kommunikation zwischen dem Client und dem Server unterbrochen wird, ruft die Server Laufzeit diese Routine auf, um alle erforderlichen Bereinigungs Vorgänge auszuführen. Weitere Informationen zu Kontext-run-down-Routinen finden Sie unter [Server Context-Lauf-ab-Routine](server-context-run-down-routine.md).

Eine Schnittstelle, die ein Kontext Handle verwendet, muss über ein Bindungs Handle für die anfängliche Bindung verfügen, das durchgeführt werden muss, bevor der Server ein Kontext Handle zurückgeben kann. Sie können ein automatisches, implizites oder explizites Bindungs Handle verwenden, um die Bindung zu erstellen und den Kontext festzulegen.

Ein Kontext Handle muss den [**void \***](/windows/desktop/Midl/void) -Typ oder einen Typ aufweisen, der in " [**void \***](/windows/desktop/Midl/void)" aufgelöst wird. Das Serverprogramm wandelt es in den erforderlichen Typ um.

> [!Note]  
> Die Verwendung von \[ [**in**](/windows/desktop/Midl/in), [**out**](/windows/desktop/Midl/out-idl) \] für Kontext handle-Parameter wird davon abgeraten, mit Ausnahme von Routinen, die Kontext Handles schließen. Wenn Kontext handle-Parameter, die \[ [**in**](/windows/desktop/Midl/in)gekennzeichnet [](/windows/desktop/Midl/out-idl) \] sind, verwendet werden, übergeben Sie kein **null** -oder nicht initialisiertes Kontext Handle vom Client an den Server. Stattdessen sollte ein **null** -Zeiger auf ein Kontext Handle übermittelt werden. Beachten Sie, dass die in markierten Kontext handle-Parameter \[ [](/windows/desktop/Midl/in) \] keine **null** -Zeiger akzeptieren.

 

Das folgende Fragment einer Beispiel Schnittstellen Definition zeigt, wie eine verteilte Anwendung ein Kontext Handle verwenden kann, um einen Server zu öffnen und eine Datendatei für jeden Client zu aktualisieren.

Die-Schnittstelle muss einen Remote Prozedur aufrufsbefehl enthalten, um das Handle zu initialisieren und es auf einen Wert ungleich **null** festzulegen. In diesem Beispiel führt die remoteopen-Funktion diesen Vorgang aus. Er gibt das Kontext Handle mit einem \[ [**out**](/windows/desktop/Midl/out-idl) - \] direktionalen Attribut an. Alternativ könnten Sie das Kontext Handle als Rückgabewert der Prozedur zurückgeben. In diesem Beispiel übergeben wir das Kontext Handle in der Parameterliste.

In diesem Beispiel handelt es sich bei den Kontextinformationen um ein Datei handle. Der aktuelle Speicherort in der Datei wird nachverfolgt. Die-Schnittstelle verpackt das Datei Handle als Kontext Handle und übergibt es als Parameter an Remote Prozedur Aufrufe. Eine-Struktur enthält den Dateinamen und das Datei handle.

``` syntax
/* file: cxhndl.idl (fragment of interface definition file) */
typedef [context_handle] void * PCONTEXT_HANDLE_TYPE;
typedef [ref] PCONTEXT_HANDLE_TYPE * PPCONTEXT_HANDLE_TYPE;
 
short RemoteOpen([out] PPCONTEXT_HANDLE_TYPE pphContext,
    [in, string] unsigned char * pszFile);
 
void RemoteRead(
    [in] PCONTEXT_HANDLE_TYPE phContext,
    [out, size_is(cbBuf)] unsigned char achBuf[],
    [in, out] short *pcbBuf);
 
short RemoteClose([in, out] PPCONTEXT_HANDLE_TYPE pphContext);
```

Die Funktion remoteopen erstellt ein gültiges Kontext Handle, das nicht **null** ist. Er übergibt das Kontext Handle an den Client. Nachfolgende Remote Prozedur Aufrufe, wie z. b. RemoteRead, verwenden das Kontext Handle als in-Zeiger.

Zusätzlich zu der Remote Prozedur, mit der das Kontext Handle initialisiert wird, muss die-Schnittstelle eine Prozedur enthalten, die den Server Kontext freigibt und das Kontext Handle auf **null** festlegt. Im vorherigen Beispiel führt die remoteclose-Funktion diesen Vorgang aus.

 

 