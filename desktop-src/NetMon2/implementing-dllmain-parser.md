---
description: Netzwerkmonitor verwendet die DllMain-Exportfunktion, um das Vorhandensein des Parsers zu identifizieren, und gibt Ressourcen frei, die Netzwerkmonitor zum Speichern von Informationen über den Parser verwenden.
ms.assetid: 1741a12c-3645-4e83-b97f-37e67218c5eb
title: Implementieren des DllMain-Parsers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb79ab862c64d8d99359965fec6c0d1ca8bf3cf9e35fdf58f1cbc063d5c3e6c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132939"
---
# <a name="implementing-dllmain-parser"></a>Implementieren des DllMain-Parsers

Netzwerkmonitor verwendet die **DllMain-Exportfunktion,** um das Vorhandensein des Parsers zu identifizieren, und gibt Ressourcen frei, die Netzwerkmonitor zum Speichern von Informationen über den Parser verwenden.

Wenn Netzwerkmonitor **dllMain zum** ersten Mal aufruft, ruft die Parser-DLL [**CreateProtocol**](createprotocol.md) auf, um Folgendes zu tun:

-   Geben Sie das Protokoll an, das der Parser erkennt.
-   Stellen Sie Einstiegspunkte für die verbleibenden Parserexportfunktionen zur Verfügung, die Netzwerkmonitor werden.

Wenn Netzwerkmonitor **dllMain** zum letzten Mal aufruft, ruft **DllMain** [**DestroyProtocol**](destroyprotocol.md) auf, um alle Ressourcen frei zu geben, die Netzwerkmonitor zum Speichern von Informationen über den Parser verwendet.

Im folgenden Verfahren werden die schritte beschrieben, die zum Implementieren von **DllMain erforderlich sind.**

**So implementieren Sie DllMain**

1.  Geben Sie [**die ENTRYPOINTS-Struktur**](entrypoints.md) für die [**CreateProtocol-Funktion**](createprotocol.md) und die globale Attach-Variable an. Die Variable Attach wird verwendet, um die Anzahl der ausgeführten Protokollinstanzen nachzuverfolgungen.
2.  Sehen Sie sich den Wert des *Command-Parameters* an, den das Betriebssystem legt.

    Wenn der *Command-Parameter* auf DLL PROCESS ATTACH und Attach auf 0 festgelegt ist, rufen Sie \_ \_ [**CreateProtocol**](createprotocol.md) auf, um den Protokollnamen und die Einstiegspunkte für die folgenden Exportfunktionen zur Verfügung zu stellen.

    -   **Registrieren**
    -   **Registrierung aufheben**
    -   **RecognizeFrame**
    -   **AttachProperties**
    -   **FormatProperties** (nur erforderlich, wenn Netzwerkmonitor die Protokolleigenschaften anzeigen).

    Wenn der *Command-Parameter* auf DLL PROCESS DETACH und Attach auf 0 festgelegt ist, rufen Sie DestroyProtocol mit dem Instanzhandle auf, das \_ \_ [**CreateProtocol zurückgibt.**](createprotocol.md) [](destroyprotocol.md)

3.  Gibt **TRUE zurück,** da **die DllMain-Parserfunktion** immer TRUE **zurückgeben muss.**

Im Folgenden finden Sie eine grundlegende Implementierung von **DllMain**. Im Codebeispiel wird eine case-Anweisung verwendet, um Werte des *Command-Parameters* zu ermitteln, um zu bestimmen, ob [**CreateProtocol**](createprotocol.md) oder [**DestroyProtocol**](destroyprotocol.md) aufgerufen werden soll.

``` syntax
#include <windows.h>

// Entry point structure for parser export functions and global
// Attach variable.
ENTRYPOINTS EntryPoints =
{
  Register,
  Deregister,
  RecognizeFrame,
  AttachProperties,
  FormatProperties
};

DWORD Attached = 0; 

BOOL WINAPI DllMain(HANDLE hInstance, ULONG Command, LPVOID Reserved)
{
  switch(Command)
  {
  // Call CreateProtocol.
  case DLL_PROCESS_ATTACH:
       // Loading parser DLL.
       if(Attached == 0)
       {
         hProtocol = CreateProtocol( "ProtocolName",
                                     &EntryPoints,
                                     ENTRYPOINTS_SIZE);
       }
       Attached++;
       break;
  // Call DestroyProtocol.
  case DLL_PROCESS_DETACH:
       // Unloading parser DLL.
       Attached--;
       if(Attached == 0)
       {
         DestroyProtocol( hProtocol);
       }
       break;
  }
  return TRUE;
}
```

 

 



