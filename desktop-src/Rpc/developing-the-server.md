---
title: Entwickeln des Servers
description: Wenn Sie ein Serverprogramm für eine verteilte Anwendung erstellen, müssen Sie die Headerdatei und den Serverstub verwenden, die der MIDL-Compiler generiert.
ms.assetid: 2b7b14f5-5692-41b8-bb98-7edd36309d21
keywords:
- Remoteprozeduraufruf RPC , Tasks, Entwickeln des Servers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efeba77168abe53e1df823f416c80a015cc63bc7b89c79a0a86d79174a7c78fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073404"
---
# <a name="developing-the-server"></a>Entwickeln des Servers

Wenn Sie ein Serverprogramm für eine verteilte Anwendung erstellen, müssen Sie die Headerdatei und den Serverstub verwenden, die der MIDL-Compiler generiert. Weitere Informationen finden Sie unter [Entwickeln der Schnittstelle](developing-the-interface.md). Schließen Sie die Headerdatei in die C-Programmdatei Ihres Servers ein. Kompilieren Sie den Serverstub mit den C-Quelldateien, aus denen ihre Anwendung besteht. Verknüpfen Sie die resultierenden Objektdateien mit der Importbibliothek. Dieser Vorgang wird im folgenden Diagramm veranschaulicht.

![Prozess der Erstellung eines Serverprogramms für eine verteilte Anwendung](images/srvrdev.png)

Wie Sie im Beispiel in der Abbildung sehen können, wurde eine MIDL-Datei mit dem Namen MyApp.idl verwendet, um die Schnittstelle zu definieren. Der MIDL-Compiler hat MyApp.idl verwendet, um MyApp \_ s.c und MyApp.h zu erstellen. Außerdem wird eine C-Quelldatei für den Clientstub erzeugt, aber dies ist für diese spezielle Diskussion nicht relevant. Die C-Quelldatei für das Serverprogramm (in diesem Fall Mysrvr.c) muss die Datei Myapp.h enthalten. Außerdem müssen die Dateien Rpc.h und Rpcndr.h eingeschlossen werden.

Die Serveranwendung wurde in zwei Dateien entwickelt: Mysrvr.c und Rprocs.c. Die Datei Mysrvr.c enthält die Funktionen, die zum Einrichten und Ausführen des Serverprogramms erforderlich sind. Die Remoteprozeduren, die das Serverprogramm bietet, sind in der Datei Rprocs.c enthalten.

Die Dateien Mysrvr.c und Rprocs.c wurden zusammen mit Myapp \_ s.c kompiliert, um Objektdateien zu erstellen. Die Objektdateien wurden dann mit der RPC-Laufzeitbibliothek und allen anderen Bibliotheken verknüpft, die sie möglicherweise benötigen. Das Ergebnis ist ein ausführbares Serverprogramm mit dem Namen Mysrvr.exe.

Wenn Sie Ihre IDL-Datei nicht im OSF-Kompatibilitätsmodus (Open Software Foundation) kompilieren ([**/osf),**](/windows/desktop/Midl/-osf)muss Ihr Serverprogramm eine Funktion zum Zuordnen von Arbeitsspeicher und eine Funktion für die Zuordnung bereitstellen. Für Windows 2000 und höhere Versionen von Windows wird der Modus [**/Oicf**](/windows/desktop/Midl/-oi)empfohlen. Weitere Informationen finden Sie unter [How Memory Is Allocated and Deallocated](how-memory-is-allocated-and-deallocated.md), und [Pointers and Memory Allocation](pointers-and-memory-allocation.md).

 

 