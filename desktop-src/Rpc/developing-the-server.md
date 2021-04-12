---
title: Entwickeln des Servers
description: Wenn Sie ein Serverprogramm für eine verteilte Anwendung erstellen, müssen Sie die Header Datei und den Serverstub verwenden, die der Mittelwert Compiler generiert.
ms.assetid: 2b7b14f5-5692-41b8-bb98-7edd36309d21
keywords:
- Remote Prozedur Aufruf RPC, Tasks, entwickeln des Servers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fc3405c52c48f531572ab159ad083bad93f95e0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316076"
---
# <a name="developing-the-server"></a>Entwickeln des Servers

Wenn Sie ein Serverprogramm für eine verteilte Anwendung erstellen, müssen Sie die Header Datei und den Serverstub verwenden, die der Mittelwert Compiler generiert. Weitere Informationen finden Sie unter [entwickeln der-Schnittstelle](developing-the-interface.md). Fügen Sie die Header Datei in die C-Programmdatei des Servers ein. Kompilieren Sie den Serverstub mit den C-Quelldateien, aus denen sich Ihre Anwendung zusammensetzt. Verknüpfen Sie die resultierenden Objektdateien mit der Import Bibliothek. Dieser Vorgang wird in der folgenden Abbildung veranschaulicht.

![Prozess der Erstellung eines Server Programms für eine verteilte Anwendung](images/srvrdev.png)

Wie Sie im Beispiel in der Abbildung sehen können, wurde eine Mittel l-Datei mit dem Namen MyApp. idl verwendet, um die-Schnittstelle zu definieren. Der mittlerer l-Compiler hat MyApp. idl verwendet, um MyApp \_ s. c und MyApp. h zu entwickeln. Außerdem wird eine C-Quelldatei für den Clientstub erstellt, die für diese besondere Erörterung jedoch nicht relevant ist. Die C-Quelldatei für das Serverprogramm (in diesem Fall mysrvr. C) muss die Datei "MyApp. h" enthalten. Außerdem müssen Sie die Dateien "RPC. h" und "Rpcndr. h" einschließen.

Die Serveranwendung wurde in zwei Dateien (mysrvr. c und rprocs. c) entwickelt. Die Datei mysrvr. c enthält die Funktionen, die zum Einrichten und Ausführen des Server Programms erforderlich sind. Die vom Serverprogramm angebotenen Remote Prozeduren sind in der Datei rprocs. c enthalten.

Die Dateien mysrvr. c und rprocs. c wurden zusammen mit MyApp \_ s. c kompiliert, um Objektdateien zu erstellen. Die Objektdateien wurden dann mit der RPC-Lauf Zeit Bibliothek und allen anderen Bibliotheken verknüpft, die Sie möglicherweise benötigen. Das Ergebnis ist ein ausführbares Serverprogramm mit dem Namen Mysrvr.exe.

Wenn Sie die IDL-Datei nicht im Modus "Open Software Foundation (OSF)" ([**/OSF**](/windows/desktop/Midl/-osf)) kompilieren, muss das Serverprogramm eine Funktion zum Zuordnen von Speicher und eine Funktion zum Aufheben der Zuordnung bereitstellen. Für Windows 2000 und höhere Versionen von Windows lautet der empfohlene Modus [**/Oicf**](/windows/desktop/Midl/-oi). Weitere Informationen finden Sie unter [zuweisen und](how-memory-is-allocated-and-deallocated.md)Aufheben der Zuordnung von Arbeitsspeicher sowie [Zeiger und Speicher Belegung](pointers-and-memory-allocation.md).

 

 