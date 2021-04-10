---
title: Bestimmen des Speicher Orts einer Freigabe
description: Im folgenden Beispiel wird veranschaulicht, wie die wnetgetuniversalname-Funktion aufgerufen wird, um den Speicherort einer Freigabe auf einem umgeleiteten Laufwerk zu ermitteln.
ms.assetid: ce57fecb-8b14-4514-a3fd-45d7ef6eee89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c50c0d46e9ac2e520f7be15812b2f541fd3e588f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948947"
---
# <a name="determining-the-location-of-a-share"></a><span data-ttu-id="2e0b2-103">Bestimmen des Speicher Orts einer Freigabe</span><span class="sxs-lookup"><span data-stu-id="2e0b2-103">Determining the Location of a Share</span></span>

<span data-ttu-id="2e0b2-104">Im folgenden Beispiel wird veranschaulicht, wie die [**wnetgetuniversalname**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetuniversalnamea) -Funktion aufgerufen wird, um den Speicherort einer Freigabe auf einem umgeleiteten Laufwerk zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="2e0b2-104">The following example demonstrates how to call the [**WNetGetUniversalName**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetuniversalnamea) function to determine the location of a share on a redirected drive.</span></span>

<span data-ttu-id="2e0b2-105">Zuerst Ruft das Codebeispiel die **wnetgetuniversalname** -Funktion auf und gibt die [**Universal \_ Name \_ Info**](/windows/desktop/api/Winnetwk/ns-winnetwk-universal_name_infoa) -Informationsebene an, um einen Zeiger auf eine Universal Naming Convention (UNC)-namens Zeichenfolge für die Ressource abzurufen.</span><span class="sxs-lookup"><span data-stu-id="2e0b2-105">First the code sample calls the **WNetGetUniversalName** function, specifying the [**UNIVERSAL\_NAME\_INFO**](/windows/desktop/api/Winnetwk/ns-winnetwk-universal_name_infoa) information level to retrieve a pointer to a Universal Naming Convention (UNC) name string for the resource.</span></span> <span data-ttu-id="2e0b2-106">Im Beispiel wird **wnetgetuniversalname** ein zweites Mal aufgerufen. dabei wird die Informationsebene " [**Remote \_ Name \_ Info**](/windows/desktop/api/Winnetwk/ns-winnetwk-remote_name_infoa) " angegeben, um zwei zusätzliche Verbindungs Informations Zeichenfolgen für die Netzwerkverbindung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="2e0b2-106">Then the sample calls **WNetGetUniversalName** a second time, specifying the [**REMOTE\_NAME\_INFO**](/windows/desktop/api/Winnetwk/ns-winnetwk-remote_name_infoa) information level to retrieve two additional network connection information strings.</span></span> <span data-ttu-id="2e0b2-107">Wenn die Aufrufe erfolgreich sind, gibt das Beispiel den Speicherort der Freigabe aus.</span><span class="sxs-lookup"><span data-stu-id="2e0b2-107">If the calls are successful, the sample prints the location of the share.</span></span>

<span data-ttu-id="2e0b2-108">Um das folgende Codebeispiel zu testen, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="2e0b2-108">To test the following code sample, perform the following steps:</span></span>

1.  <span data-ttu-id="2e0b2-109">Nennen Sie das Codebeispiel getuni. cpp.</span><span class="sxs-lookup"><span data-stu-id="2e0b2-109">Name the code sample GetUni.cpp.</span></span>
2.  <span data-ttu-id="2e0b2-110">Fügen Sie das Beispiel einer Konsolenanwendung mit dem Namen getuni hinzu.</span><span class="sxs-lookup"><span data-stu-id="2e0b2-110">Add the sample to a console application called GetUni.</span></span>
3.  <span data-ttu-id="2e0b2-111">Verknüpfen Sie die Bibliotheken shell32. lib, MPR. lib und Netapi32. lib mit der compilerliste der Bibliotheken.</span><span class="sxs-lookup"><span data-stu-id="2e0b2-111">Link the libraries Shell32.lib, Mpr.lib, and NetApi32.lib to the compiler list of libraries.</span></span>
4.  <span data-ttu-id="2e0b2-112">Wechseln Sie an der Eingabeaufforderung in das Verzeichnis getuni.</span><span class="sxs-lookup"><span data-stu-id="2e0b2-112">From the command prompt, change to the GetUni directory.</span></span>
5.  <span data-ttu-id="2e0b2-113">Kompilieren Sie getuni. cpp.</span><span class="sxs-lookup"><span data-stu-id="2e0b2-113">Compile GetUni.cpp.</span></span>
6.  <span data-ttu-id="2e0b2-114">Führen Sie die Datei GetUni.exe gefolgt von einem Laufwerk Buchstaben und einem Doppelpunkt aus, wie hier:</span><span class="sxs-lookup"><span data-stu-id="2e0b2-114">Run the file GetUni.exe followed by a drive letter and colon, like this:</span></span>

    <span data-ttu-id="2e0b2-115">**Getuni H:\\**</span><span class="sxs-lookup"><span data-stu-id="2e0b2-115">**GetUni H:\\**</span></span>


```C++
#define  STRICT
#include <windows.h>
#include <tchar.h>
#include <stdio.h>

#pragma comment(lib, "mpr.lib")

#define BUFFSIZE = 1000

void main( int argc, char *argv[] )
{
  DWORD cbBuff = 1000;    // Size of Buffer
  TCHAR szBuff[1000];    // Buffer to receive information
  REMOTE_NAME_INFO  * prni = (REMOTE_NAME_INFO *)   &szBuff;
  UNIVERSAL_NAME_INFO * puni = (UNIVERSAL_NAME_INFO *) &szBuff;
  DWORD res;

  if((argc < 2) | (lstrcmp(argv[1], "/?") == 0))
  {
    printf("Syntax:  GetUni DrivePathAndFilename\n"
         "Example: GetUni U:\\WINNT\\SYSTEM32\\WSOCK32.DLL\n");
    return;
  }
  
  // Call WNetGetUniversalName with the UNIVERSAL_NAME_INFO_LEVEL option
  //
  printf("Call WNetGetUniversalName using UNIVERSAL_NAME_INFO_LEVEL.\n");
  if((res = WNetGetUniversalName((LPTSTR)argv[1],
         UNIVERSAL_NAME_INFO_LEVEL, // The structure is written to this block of memory. 
         (LPVOID) &szBuff, 
         &cbBuff)) != NO_ERROR) 
    //
    // If the call fails, print the error; otherwise, print the location of the share, 
    //  using the pointer to UNIVERSAL_NAME_INFO_LEVEL.
    //
    printf("Error: %ld\n\n", res); 
   
  else
    _tprintf(TEXT("Universal Name: \t%s\n\n"), puni->lpUniversalName); 
    
  //
  // Call WNetGetUniversalName with the REMOTE_NAME_INFO_LEVEL option
  //
  printf("Call WNetGetUniversalName using REMOTE_NAME_INFO_LEVEL.\n");
  if((res = WNetGetUniversalName((LPTSTR)argv[1], 
         REMOTE_NAME_INFO_LEVEL, 
         (LPVOID) &szBuff,    //Structure is written to this block of memory
         &cbBuff)) != NO_ERROR) 
    //
    // If the call fails, print the error; otherwise, print
    //  the location of the share, using 
    //  the pointer to REMOTE_NAME_INFO_LEVEL.
    //
    printf("Error: %ld\n", res); 
  else
    _tprintf(TEXT("Universal Name: \t%s\nConnection Name:\t%s\nRemaining Path: \t%s\n"),
          prni->lpUniversalName, 
          prni->lpConnectionName, 
          prni->lpRemainingPath);
  return;
}
```



 

 