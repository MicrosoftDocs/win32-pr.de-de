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
# <a name="implementing-dllmain-parser"></a><span data-ttu-id="f2da0-103">Implementieren von DllMain-Parser</span><span class="sxs-lookup"><span data-stu-id="f2da0-103">Implementing DllMain Parser</span></span>

<span data-ttu-id="f2da0-104">Netzwerkmonitor verwendet die Exportfunktion **DllMain** , um das vorhanden sein des Parsers zu identifizieren, und gibt Ressourcen frei, die von Netzwerkmonitor zum Speichern von Informationen über den Parser verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f2da0-104">Network Monitor uses the **DllMain** export function to identify the existence of the parser, and release resources that Network Monitor uses to store information about the parser.</span></span>

<span data-ttu-id="f2da0-105">Wenn Netzwerkmonitor zum ersten Mal **DllMain** aufruft, ruft die Parser-DLL [**für Folgendes Folgendes auf:**](createprotocol.md)</span><span class="sxs-lookup"><span data-stu-id="f2da0-105">When Network Monitor calls **DllMain** for the first time, the parser DLL calls [**CreateProtocol**](createprotocol.md) to do the following:</span></span>

-   <span data-ttu-id="f2da0-106">Geben Sie das Protokoll an, das der Parser erkennt.</span><span class="sxs-lookup"><span data-stu-id="f2da0-106">Specify the protocol that the parser detects.</span></span>
-   <span data-ttu-id="f2da0-107">Geben Sie Einstiegspunkte für die verbleibenden Parser-Exportfunktionen an, die Netzwerkmonitor aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f2da0-107">Provide entry points for remaining parser export functions that Network Monitor calls.</span></span>

<span data-ttu-id="f2da0-108">Wenn Netzwerkmonitor **DllMain** zum letzten Mal aufruft, ruft **DllMain** " [**destroyprotocol**](destroyprotocol.md) " auf, um alle Ressourcen freizugeben, die Netzwerkmonitor zum Speichern von Informationen über den Parser verwendet.</span><span class="sxs-lookup"><span data-stu-id="f2da0-108">When Network Monitor calls **DllMain** for the last time, **DllMain** calls [**DestroyProtocol**](destroyprotocol.md) to release all resources that Network Monitor uses to store information about the parser.</span></span>

<span data-ttu-id="f2da0-109">Im folgenden Verfahren werden die Schritte beschrieben, die für die Implementierung von **DllMain** erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="f2da0-109">The following procedure identifies the steps necessary to implement **DllMain**.</span></span>

<span data-ttu-id="f2da0-110">**So implementieren Sie DllMain**</span><span class="sxs-lookup"><span data-stu-id="f2da0-110">**To implement DllMain**</span></span>

1.  <span data-ttu-id="f2da0-111">Geben Sie die [**entryPoints**](entrypoints.md) -Struktur für [**die Funktion "**](createprotocol.md) Funktion" und die Variable "Global Attach" an.</span><span class="sxs-lookup"><span data-stu-id="f2da0-111">Specify the [**ENTRYPOINTS**](entrypoints.md) structure for the [**CreateProtocol**](createprotocol.md) function and global Attach variable.</span></span> <span data-ttu-id="f2da0-112">Die Attach-Variable wird verwendet, um die Anzahl der Protokoll Instanzen zu verfolgen, die ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f2da0-112">The Attach variable is used to track the number of protocol instances that are running.</span></span>
2.  <span data-ttu-id="f2da0-113">Sehen Sie sich den Wert des *Befehls* Parameters an, der vom Betriebssystem festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="f2da0-113">Look at the value of the *Command* parameter that the operating system sets.</span></span>

    <span data-ttu-id="f2da0-114">Wenn der *Befehls* Parameter auf DLL \_ \_ -Prozess anfügen und anfügen den Wert 0 festgelegt ist, müssen Sie zum Bereitstellen des Protokoll namens und der Einstiegspunkte für die folgenden Exportfunktionen das- [**Protokoll**](createprotocol.md) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f2da0-114">If the *Command* parameter is set to DLL\_PROCESS\_ATTACH and Attach is 0, then call [**CreateProtocol**](createprotocol.md) to provide the protocol name and entry points for the following export functions.</span></span>

    -   <span data-ttu-id="f2da0-115">**Registrieren**</span><span class="sxs-lookup"><span data-stu-id="f2da0-115">**Register**</span></span>
    -   <span data-ttu-id="f2da0-116">**Registrierung aufheben**</span><span class="sxs-lookup"><span data-stu-id="f2da0-116">**Deregister**</span></span>
    -   <span data-ttu-id="f2da0-117">**Erkenzeframe**</span><span class="sxs-lookup"><span data-stu-id="f2da0-117">**RecognizeFrame**</span></span>
    -   <span data-ttu-id="f2da0-118">**Attachproperties**</span><span class="sxs-lookup"><span data-stu-id="f2da0-118">**AttachProperties**</span></span>
    -   <span data-ttu-id="f2da0-119">**Formatproperties** (nur erforderlich, wenn Netzwerkmonitor die Protokoll Eigenschaften anzeigt).</span><span class="sxs-lookup"><span data-stu-id="f2da0-119">**FormatProperties** (only required if Network Monitor will be displaying the protocol properties).</span></span>

    <span data-ttu-id="f2da0-120">Wenn der *Befehls* Parameter auf DLL \_ -Prozess Trennung \_ und anfügen den Wert 0 festgelegt ist, wird [**destroyprotocol**](destroyprotocol.md) mithilfe des Instanzhandles aufgerufen, das von " [**kreateprotocol**](createprotocol.md) " zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f2da0-120">If the *Command* parameter is set to DLL\_PROCESS\_DETACH and Attach is 0, then call [**DestroyProtocol**](destroyprotocol.md) using the instance handle that [**CreateProtocol**](createprotocol.md) returns.</span></span>

3.  <span data-ttu-id="f2da0-121">Gibt **true** zurück, da die **DllMain** -parserfunktion immer **true** zurückgeben muss.</span><span class="sxs-lookup"><span data-stu-id="f2da0-121">Return **TRUE** because the **DllMain** parser function must always return **TRUE**.</span></span>

<span data-ttu-id="f2da0-122">Im folgenden finden Sie eine grundlegende Implementierung von **DllMain**.</span><span class="sxs-lookup"><span data-stu-id="f2da0-122">The following is a basic implementation of **DllMain**.</span></span> <span data-ttu-id="f2da0-123">Im Codebeispiel wird eine Case-Anweisung verwendet, um Werte des *Command* -Parameters abzufangen [**, um zu**](createprotocol.md) bestimmen, ob "-" oder " [**destroyprotocol**](destroyprotocol.md) " aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="f2da0-123">The code example uses a case statement to trap values of the *Command* parameter to determine if [**CreateProtocol**](createprotocol.md) or [**DestroyProtocol**](destroyprotocol.md) should be called.</span></span>

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

 

 



