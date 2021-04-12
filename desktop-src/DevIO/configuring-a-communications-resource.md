---
description: Das folgende Beispiel öffnet ein Handle für COM2 und füllt eine DCB-Struktur mit der aktuellen Konfiguration aus. Die DCB-Struktur wird dann geändert und zum Neukonfigurieren des Geräts verwendet.
ms.assetid: 5b325a1e-51e1-43b4-92e7-7bcf34c6388f
title: Konfigurieren einer Kommunikations Ressource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a82622696833c9de414d3af64856a9df357e23b6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393085"
---
# <a name="configuring-a-communications-resource"></a>Konfigurieren einer Kommunikations Ressource

Das folgende Beispiel öffnet ein Handle für COM2 und füllt eine [**DCB**](/windows/desktop/api/Winbase/ns-winbase-dcb) -Struktur mit der aktuellen Konfiguration aus. Die **DCB** -Struktur wird dann geändert und zum Neukonfigurieren des Geräts verwendet.


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>

void PrintCommState(DCB dcb)
{
    //  Print some of the DCB structure values
    _tprintf( TEXT("\nBaudRate = %d, ByteSize = %d, Parity = %d, StopBits = %d\n"), 
              dcb.BaudRate, 
              dcb.ByteSize, 
              dcb.Parity,
              dcb.StopBits );
}


int _tmain( int argc, TCHAR *argv[] )
{
   DCB dcb;
   HANDLE hCom;
   BOOL fSuccess;
   TCHAR *pcCommPort = TEXT("COM1"); //  Most systems have a COM1 port

   //  Open a handle to the specified com port.
   hCom = CreateFile( pcCommPort,
                      GENERIC_READ | GENERIC_WRITE,
                      0,      //  must be opened with exclusive-access
                      NULL,   //  default security attributes
                      OPEN_EXISTING, //  must use OPEN_EXISTING
                      0,      //  not overlapped I/O
                      NULL ); //  hTemplate must be NULL for comm devices

   if (hCom == INVALID_HANDLE_VALUE) 
   {
       //  Handle the error.
       printf ("CreateFile failed with error %d.\n", GetLastError());
       return (1);
   }

   //  Initialize the DCB structure.
   SecureZeroMemory(&dcb, sizeof(DCB));
   dcb.DCBlength = sizeof(DCB);

   //  Build on the current configuration by first retrieving all current
   //  settings.
   fSuccess = GetCommState(hCom, &dcb);

   if (!fSuccess) 
   {
      //  Handle the error.
      printf ("GetCommState failed with error %d.\n", GetLastError());
      return (2);
   }

   PrintCommState(dcb);       //  Output to console

   //  Fill in some DCB values and set the com state: 
   //  57,600 bps, 8 data bits, no parity, and 1 stop bit.
   dcb.BaudRate = CBR_57600;     //  baud rate
   dcb.ByteSize = 8;             //  data size, xmit and rcv
   dcb.Parity   = NOPARITY;      //  parity bit
   dcb.StopBits = ONESTOPBIT;    //  stop bit

   fSuccess = SetCommState(hCom, &dcb);

   if (!fSuccess) 
   {
      //  Handle the error.
      printf ("SetCommState failed with error %d.\n", GetLastError());
      return (3);
   }

   //  Get the comm config again.
   fSuccess = GetCommState(hCom, &dcb);

   if (!fSuccess) 
   {
      //  Handle the error.
      printf ("GetCommState failed with error %d.\n", GetLastError());
      return (2);
   }

   PrintCommState(dcb);       //  Output to console

   _tprintf (TEXT("Serial port %s successfully reconfigured.\n"), pcCommPort);
   return (0);
```



 

 



