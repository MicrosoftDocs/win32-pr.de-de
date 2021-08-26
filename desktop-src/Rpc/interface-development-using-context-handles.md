---
title: Schnittstellenentwicklung mit Kontexthandles
description: In der Regel erstellen Sie ein Kontexthandle, indem Sie das \_ \context handle\-Attribut für eine Typdefinition in der IDL-Datei angeben.
ms.assetid: e4caf91f-f92d-4aef-a20f-0a3073230640
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77e65e36384bda3d81526d5891eca92a77a67402e7cd3aa7af8b61e061a9d3b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020470"
---
# <a name="interface-development-using-context-handles"></a>Schnittstellenentwicklung mit Kontexthandles

In der Regel erstellen Sie ein Kontexthandle, indem Sie das \[ [**\_ Kontexthandleat**](/windows/desktop/Midl/context-handle) \] für eine Typdefinition in der IDL-Datei angeben. Die Typdefinition gibt auch implizit eine Kontext-Run-Down-Routine an, die Sie bereitstellen müssen. Wenn die Kommunikation zwischen Client und Server unterbrochen wird, ruft die Serverlaufzeit diese Routine auf, um alle erforderlichen Bereinigungen durchzuführen. Weitere Informationen zu Kontext-Run-Down-Routinen finden Sie unter [Run-down Routine für Serverkontext.](server-context-run-down-routine.md)

Eine Schnittstelle, die ein Kontexthandle verwendet, muss über ein Bindungshandle für die erste Bindung verfügen, das erfolgen muss, bevor der Server ein Kontexthandle zurückgeben kann. Sie können ein automatisches, implizites oder explizites Bindungshandle verwenden, um die Bindung zu erstellen und den Kontext einzurichten.

Ein Kontexthandle muss vom [ * *\* void* _-Typ](/windows/desktop/Midl/void) sein, oder ein Typ, der in [_ *void \** *](/windows/desktop/Midl/void)aufgelöst wird. Das Serverprogramm gibt ihn in den erforderlichen Typ um.

> [!Note]  
> Von der Verwendung von \[ [**in**](/windows/desktop/Midl/in)für [](/windows/desktop/Midl/out-idl) \] Kontexthandleparameter wird abgeraten, mit Ausnahme von Routinen, die Kontexthandles schließen. Wenn context in markierte Parameter \[ [](/windows/desktop/Midl/in)behandelt, wird [**out**](/windows/desktop/Midl/out-idl) \] verwendet. Übergeben Sie kein **NULL-** oder nicht initialisiertes Kontexthandle vom Client an den Server. Stattdessen sollte ein **NULL-Zeiger** auf ein Kontexthandle übergeben werden. Beachten Sie, dass Kontexthandleparameter, die in markiert \[ [](/windows/desktop/Midl/in) \] sind, **keine NULL-Zeiger** akzeptieren.

 

Das folgende Fragment einer Beispielschnittstellendefinition zeigt, wie eine verteilte Anwendung ein Kontexthandle verwenden kann, um einen Server zu öffnen und eine Datendatei für jeden Client zu aktualisieren.

Die Schnittstelle muss einen Remoteprozeduraufruf enthalten, um das Handle zu initialisieren und auf einen Wert ungleich **NULL** festzulegen. In diesem Beispiel führt die RemoteOpen-Funktion diesen Vorgang aus. Sie gibt das Kontexthandle mit einem \[ [**direktionalen Attribut für die Richtung "Out"**](/windows/desktop/Midl/out-idl) \] an. Alternativ können Sie das Kontexthandle als Rückgabewert der Prozedur zurückgeben. In diesem Beispiel übergeben wir jedoch das Kontexthandle über die Parameterliste.

In diesem Beispiel handelt es sich bei den Kontextinformationen um ein Dateihandle. Der aktuelle Speicherort in der Datei wird nachverfolgt. Die Schnittstelle packt das Dateihandle als Kontexthandle und übergibt es als Parameter an Remoteprozeduraufrufe. Eine -Struktur enthält den Dateinamen und das Dateihandle.

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

Die RemoteOpen-Funktion erstellt ein gültiges Kontexthandle ungleich **NULL.** Es übergibt das Kontexthandle an den Client. Nachfolgende Remoteprozeduraufrufe, z. B. RemoteRead, verwenden das Kontexthandle als in-Zeiger.

Zusätzlich zur Remoteprozedur, die das Kontexthandle initialisiert, muss die Schnittstelle eine Prozedur enthalten, die den Serverkontext freigibt und das Kontexthandle auf **NULL** festlegt. Im vorherigen Beispiel führt die RemoteClose-Funktion diesen Vorgang aus.

 

 