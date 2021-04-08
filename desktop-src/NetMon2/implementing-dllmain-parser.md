---
description: Netzwerkmonitor verwendet die Exportfunktion DllMain, um das vorhanden sein des Parsers zu identifizieren, und gibt Ressourcen frei, die von Netzwerkmonitor zum Speichern von Informationen über den Parser verwendet werden.
ms.assetid: 1741a12c-3645-4e83-b97f-37e67218c5eb
title: Implementieren von DllMain-Parser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55dd1ab7432920ac7496643c7c6f9aa0692daf56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750049"
---
# <a name="implementing-dllmain-parser"></a>Implementieren von DllMain-Parser

Netzwerkmonitor verwendet die Exportfunktion **DllMain** , um das vorhanden sein des Parsers zu identifizieren, und gibt Ressourcen frei, die von Netzwerkmonitor zum Speichern von Informationen über den Parser verwendet werden.

Wenn Netzwerkmonitor zum ersten Mal **DllMain** aufruft, ruft die Parser-DLL [**für Folgendes Folgendes auf:**](createprotocol.md)

-   Geben Sie das Protokoll an, das der Parser erkennt.
-   Geben Sie Einstiegspunkte für die verbleibenden Parser-Exportfunktionen an, die Netzwerkmonitor aufrufen.

Wenn Netzwerkmonitor **DllMain** zum letzten Mal aufruft, ruft **DllMain** " [**destroyprotocol**](destroyprotocol.md) " auf, um alle Ressourcen freizugeben, die Netzwerkmonitor zum Speichern von Informationen über den Parser verwendet.

Im folgenden Verfahren werden die Schritte beschrieben, die für die Implementierung von **DllMain** erforderlich sind.

**So implementieren Sie DllMain**

1.  Geben Sie die [**entryPoints**](entrypoints.md) -Struktur für [**die Funktion "**](createprotocol.md) Funktion" und die Variable "Global Attach" an. Die Attach-Variable wird verwendet, um die Anzahl der Protokoll Instanzen zu verfolgen, die ausgeführt werden.
2.  Sehen Sie sich den Wert des *Befehls* Parameters an, der vom Betriebssystem festgelegt wird.

    Wenn der *Befehls* Parameter auf DLL \_ \_ -Prozess anfügen und anfügen den Wert 0 festgelegt ist, müssen Sie zum Bereitstellen des Protokoll namens und der Einstiegspunkte für die folgenden Exportfunktionen das- [**Protokoll**](createprotocol.md) aufrufen.

    -   **Registrieren**
    -   **Registrierung aufheben**
    -   **Erkenzeframe**
    -   **Attachproperties**
    -   **Formatproperties** (nur erforderlich, wenn Netzwerkmonitor die Protokoll Eigenschaften anzeigt).

    Wenn der *Befehls* Parameter auf DLL \_ -Prozess Trennung \_ und anfügen den Wert 0 festgelegt ist, wird [**destroyprotocol**](destroyprotocol.md) mithilfe des Instanzhandles aufgerufen, das von " [**kreateprotocol**](createprotocol.md) " zurückgegeben wird.

3.  Gibt **true** zurück, da die **DllMain** -parserfunktion immer **true** zurückgeben muss.

Im folgenden finden Sie eine grundlegende Implementierung von **DllMain**. Im Codebeispiel wird eine Case-Anweisung verwendet, um Werte des *Command* -Parameters abzufangen [**, um zu**](createprotocol.md) bestimmen, ob "-" oder " [**destroyprotocol**](destroyprotocol.md) " aufgerufen werden soll.

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

 

 



