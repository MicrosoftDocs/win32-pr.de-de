---
title: Entwickeln des Clients
description: Die Entwicklung eines RPC-Clientprogramms ähnelt der Entwicklung des Serverprogramms. Informationen zum Entwickeln eines RPC-Serverprogramms finden Sie unter Entwickeln des Servers.
ms.assetid: 92276326-d478-479e-8fa4-02a2fce58eb6
keywords:
- REMOTE PROCEDURE Call RPC , Tasks, Entwickeln des Clients
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fccc719d724ecdcc5631c5f72c5190870f864e06affd45bcce3e7f2da79fb709
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021895"
---
# <a name="developing-the-client"></a>Entwickeln des Clients

Die Entwicklung eines RPC-Clientprogramms ähnelt der Entwicklung des Serverprogramms. Informationen zum Entwickeln eines RPC-Serverprogramms finden Sie unter [Developing the Server](developing-the-server.md).

Wie bei der Serverentwicklung muss Ihr Clientprogramm die Headerdatei enthalten, die der MIDL-Compiler aus Ihrer IDL-Datei generiert. Der MIDL-Compiler generiert auch eine C-Quelldatei, die den Clientstub enthält. Sie müssen diese C-Quelldatei kompilieren und mit Ihrem Clientprogramm verknüpfen. (Darüber hinaus generiert der MIDL-Compiler eine C-Quelldatei, die den Serverstub enthält, aber dies ist für diese Diskussion nicht relevant.)

Zusätzlich zum Kompilieren und Verknüpfen des Clientstubs mit Ihren Programmdateien müssen Sie die Importbibliothek (und alle anderen Bibliotheken, die Ihr Clientprogramm benötigt) mit Ihrem Clientprogramm verknüpfen. Der Prozess zum Erstellen eines RPC-Clientprogramms wird im folgenden Diagramm veranschaulicht.

![Prozess zum Erstellen eines Clientprogramms für eine verteilte Anwendung](images/clntdev.png)

Das Beispiel in der vorherigen Abbildung veranschaulicht die Erstellung eines RPC-Clientprogramms namens MyClnt.exe. Der erste Schritt besteht im Definieren der Schnittstelle in der Datei MyApp.idl. Der MIDL-Compiler verwendet MyApp.idl, um die Datei MyApp \_ c.c zu generieren, die den Clientstub enthält. Außerdem wird die Datei MyApp.h generiert, die das Clientprogramm enthalten muss. Das Clientprogramm muss auch die Dateien RPC.h und RPCNDR.h enthalten.

Das Clientprogramm selbst wird in der Datei MyClnt.c erstellt. In einem echten Projekt würde das Clientprogramm in der Regel aus mehreren C-Quelldateien bestehen. Alle müssen kompiliert und miteinander verknüpft werden. In diesem Beispiel wird der Einfachheit halber jedoch nur eine Datei verwendet.

Die Dateien MyClnt.c und MyApp c.c werden kompiliert und zusammen mit der RPC-Laufzeitbibliothek und allen anderen Bibliotheken verknüpft, die das \_ Clientprogramm benötigt. Das Ergebnis ist ein ausführbares Clientprogramm namens MyClnt.exe.

Wenn Sie Ihre IDL-Datei nicht im OSF-Kompatibilitätsmodus [**(/osf)**](/windows/desktop/Midl/-osf)kompilieren, muss Ihr Clientprogramm eine Funktion zum Zuordnen von Arbeitsspeicher und eine Funktion zum Zuordnen bereitstellen. Für Windows 2000 und höher wird der [**Modus /Oicf empfohlen.**](/windows/desktop/Midl/-oi) Weitere Informationen finden Sie unter [How Memory Is Allocated and Deallocated](how-memory-is-allocated-and-deallocated.md), and [Pointers and Memory Allocation](pointers-and-memory-allocation.md).

 

 