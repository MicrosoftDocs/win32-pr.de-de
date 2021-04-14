---
description: Erstellen einer grundlegenden IP-Hilfsanwendung
ms.assetid: b53f1cf5-3659-407e-8279-5c94333f3017
title: Erstellen einer grundlegenden IP-Hilfsanwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baae961f8ffb6aa899e96fd05f0cb9f0c41469ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350268"
---
# <a name="creating-a-basic-ip-helper-application"></a>Erstellen einer grundlegenden IP-Hilfsanwendung

**So erstellen Sie eine Basis-IP-Hilfsanwendung**

1.  Erstellen Sie ein neues leeres Projekt.
2.  Fügen Sie dem Projekt eine leere C++-Quelldatei hinzu.
3.  Stellen Sie sicher, dass sich die Buildumgebung auf das include-, lib-und src-Verzeichnis des Platform Software Development Kit (SDK) bezieht.
4.  Stellen Sie sicher, dass die Buildumgebung mit der IP-hilfsbibliotheks Datei iphlpapi. lib und der Winsock-Bibliotheksdatei ws2 \_ 32. lib verknüpft ist.
    > [!Note]  
    > Einige grundlegende Winsock-Funktionen werden verwendet, um IP-Adress Werte und andere Informationen zurückzugeben.

     

5.  Beginnen Sie mit der Programmierung der IP-Hilfsanwendung. Verwenden Sie die IP-hilfsprogrammapi, indem Sie die IP-hilfheaderdatei einschließen

    ```C++
    #include <winsock2.h>
    #include <iphlpapi.h>
    #include <stdio.h>

    int main() {
      return 0;
    }
    
    ```

    

    > [!Note]
    >
    > Die Header Datei " *iphlpapi. h* " ist für Anwendungen erforderlich, die die IP-Hilfsfunktionen verwenden. Die Header Datei " *iphlpapi. h* " enthält automatisch andere Header Dateien mit Strukturen und Enumerationen, die von den IP-Hilfsfunktionen verwendet werden.
    >
    > Die neuen in Windows Vista und höher eingeführten IP-Hilfsfunktionen sind in der Header Datei " *nettioapi. h* " definiert, die automatisch in der Header Datei " *iphlpapi. h* " enthalten ist. Die Header Datei " *nettioapi. h* " sollte niemals direkt verwendet werden.
    >
    > Viele der von den IP-Hilfsobjekten verwendeten Strukturen und Enumerationen werden in den Header Dateien " *iprtrmib. h*", " *ipexport. h*" und " *iptypes. h* " definiert. Diese Header Dateien werden automatisch in der Header Datei " *iphlpapi. h* " eingeschlossen und sollten niemals direkt verwendet werden.
    >
    > Im Microsoft Windows Software Development Kit (SDK), das für Windows Vista und höher veröffentlicht wurde, hat sich die Organisation der Header Dateien geändert. Einige der Strukturen sind nun in den Header Dateien " *ipmib. h*", " *tcpmib. h*" und " *udpmib. h* " definiert, nicht in der Header Datei " *iprtrmib. h* ". Die Header Datei " *ipmib. h* " enthält automatisch die Header Datei " *ifmib. h* ". Beachten Sie, dass diese Header Dateien automatisch in der Datei " *iprtrmib. h*" enthalten sind, die automatisch in der Header Datei " *iphlpapi. h* " enthalten ist.
    >
    > Die Header Datei " *Winsock2. h* " für Windows Sockets 2,0 ist für die meisten Anwendungen erforderlich, die die IP-hilfsprogrammapis verwenden. Wenn die *Winsock2. h* -Header Datei erforderlich ist, \# sollte die Include-Zeile für diese Datei vor der \# Include-Zeile für die Header Datei " *iphlpapi. h* " platziert werden.
    >
    > Die Header Datei " *Winsock2. h* " enthält intern Kernelemente aus der Header Datei " *Windows. h* ", sodass \# in IP-Hilfsanwendungen normalerweise keine Include-Zeile für die *Windows. h* -Header Datei vorhanden ist. Wenn eine \# Include-Zeile für die Header Datei " *Windows. h* " erforderlich ist, sollte diesem das \# Win32 \_ \_ -und Mean-Makro definiert werden \_ . Aus historischen Gründen hat der *Windows. h* -Header standardmäßig die *Winsock. h* -Header Datei für Windows Sockets 1,1. Die Deklarationen in der *Winsock. h* -Header Datei für Windows Sockets 1,1 stehen in Konflikt mit den Deklarationen in der *Winsock2. h* -Header Datei, die von Windows Sockets 2,0 benötigt wird. Das Win32 \_ \_ -und \_ Mean-Makro verhindert, dass die Header Datei " *Winsock. h* " in der Header Datei " *Windows. h* " enthalten ist. Im folgenden wird ein Beispiel gezeigt, das dies veranschaulicht.

     

    ```C++
    #ifndef WIN32_LEAN_AND_MEAN
    #define WIN32_LEAN_AND_MEAN
    #endif

    #include <windows.h>

    #include <winsock2.h>
    #include <iphlpapi.h>
    #include <stdio.h>

    int main() {
      return 0;
    }
    
    ```

    

    > [!Note]
    >
    > Diese grundlegende IP-Hilfsanwendung verwendet nur einige IP-Adressdaten Strukturen und eine IP-Adresse für Zeichen folgen Konvertierungs Funktionen von Windows Sockets 2,0. Diese Windows Sockets-Funktionen können verwendet werden, ohne dass [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) aufgerufen wird, um Windows Sockets-Ressourcen und [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) zu initialisieren, wenn diese Ressourcen verwendet werden.
    >
    > In IP-Hilfsanwendungen, die andere andere Winsock-Funktionen als diese IP-Adressen für Zeichen folgen Funktionen verwenden, muss die [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) -Funktion aufgerufen werden, um Windows Sockets-Ressourcen vor dem Aufrufen von Windows Sockets-Funktionen zu initialisieren, und [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) sollte aufgerufen werden, wenn die Anwendung mithilfe von Windows Sockets-Ressourcen

     

    > [!Note]
    >
    > Die Header Datei " *stdio. h* " ist für die Verwendung verschiedener Standard-C-Funktionen in dieser grundlegenden IP-Hilfsanwendung erforderlich.

     

    Nächster Schritt: [Abrufen von Informationen mithilfe von getnetworkpara](retrieving-information-using-getnetworkparams.md) Metern

 

 
