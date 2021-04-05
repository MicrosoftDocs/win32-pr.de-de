---
title: Entwickeln des Clients
description: Die Entwicklung eines RPC-Client Programms ähnelt der Entwicklung des-Server Programms. Weitere Informationen zum Entwickeln eines RPC-Server Programms finden Sie unter Entwickeln des Servers.
ms.assetid: 92276326-d478-479e-8fa4-02a2fce58eb6
keywords:
- Remote Prozedur Aufruf RPC, Tasks, entwickeln des Clients
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10ceddedc4ccfd1d068e3452b64ed8c6b54a621d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103949021"
---
# <a name="developing-the-client"></a>Entwickeln des Clients

Die Entwicklung eines RPC-Client Programms ähnelt der Entwicklung des-Server Programms. Weitere Informationen zum Entwickeln eines RPC-Server Programms finden Sie unter [entwickeln des Servers](developing-the-server.md).

Wie bei der Serverentwicklung muss das Client Programm die Header Datei enthalten, die der-Mittell-Compiler aus der IDL-Datei generiert. Der mittlerer l-Compiler generiert außerdem eine C-Quelldatei, die den Clientstub enthält. Diese C-Quelldatei muss kompiliert und mit dem Client Programm verknüpft werden. (Zusätzlich generiert der-compilercompiler eine C-Quelldatei, die den Serverstub enthält, aber dies ist für diese Erörterung nicht relevant.)

Zusätzlich zum Kompilieren und Verknüpfen des clientstubs mit den Programmdateien müssen Sie die Import Bibliothek (und alle anderen Bibliotheken, die Ihr Client Programm benötigt) mit Ihrem Client Programm verknüpfen. Der Prozess der Erstellung eines RPC-Client Programms ist im folgenden Diagramm dargestellt.

![Prozess der Erstellung eines Client Programms für eine verteilte Anwendung](images/clntdev.png)

Das Beispiel in der obigen Abbildung zeigt die Erstellung eines RPC-Client Programms namens MyClnt.exe. Der erste Schritt besteht darin, die-Schnittstelle in der Datei "MyApp. idl" zu definieren. Der Mittelwert Compiler verwendet MyApp. idl, um die Datei MyApp \_ c. c zu generieren, die den Clientstub enthält. Außerdem wird die Datei "MyApp. h" generiert, die das Client Programm enthalten muss. Das Client Programm muss auch die Dateien "RPC. h" und "Rpcndr. h" einschließen.

Das Client Programm selbst wird in der Datei "myclnt. c" erstellt. In einem echten Projekt besteht das Client Programm in der Regel aus mehreren C-Quelldateien. Alle müssen kompiliert und miteinander verknüpft werden. In diesem Beispiel wird jedoch nur eine Datei aus Gründen der Einfachheit verwendet.

Die Dateien myclnt. c und MyApp \_ c. c werden zusammen mit der RPC-Lauf Zeit Bibliothek und allen anderen Bibliotheken, die das Client Programm benötigt, kompiliert und verknüpft. Das Ergebnis ist ein ausführbares Client Programm mit dem Namen MyClnt.exe.

Wenn Sie die IDL-Datei nicht im OSF-Kompatibilitätsmodus ([**/OSF**](/windows/desktop/Midl/-osf)) kompilieren, muss das Client Programm eine Funktion zum Zuordnen von Arbeitsspeicher und eine Funktion für die Aufhebung der Zuordnung bereitstellen. Für Windows 2000 und höhere Versionen ist [**/Oicf**](/windows/desktop/Midl/-oi)der empfohlene Modus. Weitere Informationen finden Sie unter [zuweisen und](how-memory-is-allocated-and-deallocated.md)Aufheben der Zuordnung von Arbeitsspeicher sowie [Zeiger und Speicher Belegung](pointers-and-memory-allocation.md).

 

 