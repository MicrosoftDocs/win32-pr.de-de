---
description: Wenn eine Hardware- oder Softwareausnahme auftritt, beendet der Prozessor die Ausführung an dem Punkt, an dem die Ausnahme aufgetreten ist, und überträgt die Steuerung an das System.
ms.assetid: 35a1b9bd-8da9-47e6-beda-e0b159bd840d
title: Ausnahmedisponierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b7b4f73c9d2c3fbaf15b4390ee6ecc6b9aa06b50524ec080fc45319d3b94767
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912730"
---
# <a name="exception-dispatching"></a>Ausnahmedisponierung

Wenn eine Hardware- oder Softwareausnahme auftritt, beendet der Prozessor die Ausführung an dem Punkt, an dem die Ausnahme aufgetreten ist, und überträgt die Steuerung an das System. Zunächst speichert das System sowohl den Computerstatus des aktuellen Threads als auch Informationen, die die Ausnahme beschreiben. Das System versucht dann, einen Ausnahmehandler zu finden, um die Ausnahme zu behandeln.

Der Computerzustand des Threads, in dem die Ausnahme aufgetreten ist, wird in einer [**CONTEXT-Struktur**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) gespeichert. Diese Informationen (als *Kontextdatensatz* bezeichnet) ermöglichen es dem System, die Ausführung am Punkt der Ausnahme fortzusetzen, wenn die Ausnahme erfolgreich behandelt wurde. Die Beschreibung der Ausnahme **(ausnahmedatensatz** genannt) wird in einer [**EXCEPTION \_ RECORD-Struktur**](/windows/desktop/api/WinNT/ns-winnt-exception_record) gespeichert. Da die computerabhängigen Informationen des Kontextdatensatzes getrennt von den computerunabhängigen Informationen des Ausnahmedatensatzes gespeichert werden, ist der Ausnahmebehandlungsmechanismus auf verschiedene Plattformen übertragbar.

Die Informationen in den Kontext- und Ausnahmedatensätzen sind über die [**GetExceptionInformation-Funktion**](getexceptioninformation.md) verfügbar und können allen Ausnahmehandlern zur Verfügung gestellt werden, die als Ergebnis der Ausnahme ausgeführt werden. Der Ausnahmedatensatz enthält die folgenden Informationen.

-   Ein Ausnahmecode, der den Ausnahmetyp identifiziert.
-   Flags, die angeben, ob die Ausnahme zusammenhängend ist. Jeder Versuch, die Ausführung fortzusetzen, nachdem eine nichttinuierbare Ausnahme ausgelöst wurde, generiert eine weitere Ausnahme.
-   Ein Zeiger auf einen anderen Ausnahmedatensatz. Dies erleichtert die Erstellung einer verknüpften Liste von Ausnahmen, wenn geschachtelte Ausnahmen auftreten.
-   Die Adresse, an der die Ausnahme aufgetreten ist.
-   Ein Array von Argumenten, die zusätzliche Informationen über die Ausnahme bereitstellen.

Wenn eine Ausnahme im Benutzermoduscode auftritt, verwendet das System die folgende Suchreihenfolge, um einen Ausnahmehandler zu finden:

1.  Wenn der Prozess gedebuggt wird, benachrichtigt das System den Debugger. Weitere Informationen finden Sie unter [Ausnahmebehandlung des Debuggers.](debugger-exception-handling.md)
2.  Wenn der Prozess nicht gedebuggt wird oder der zugeordnete Debugger die Ausnahme nicht behandelt, versucht das System, einen framebasierten Ausnahmehandler zu finden, indem es die Stapelrahmen des Threads durchsucht, in dem die Ausnahme aufgetreten ist. Das System durchsucht zuerst den aktuellen Stapelrahmen und dann vorherige Stapelrahmen in umgekehrter Reihenfolge.
3.  Wenn kein framebasierter Handler gefunden werden kann oder kein framebasierter Handler die Ausnahme behandelt, der Prozess jedoch gedebuggt wird, benachrichtigt das System den Debugger ein zweites Mal.
4.  Wenn der Prozess nicht gedebuggt wird oder der zugeordnete Debugger die Ausnahme nicht behandelt, stellt das System die Standardbehandlung basierend auf dem Ausnahmetyp bereit. Für die meisten Ausnahmen besteht die Standardaktion darin, die [**ExitProcess-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) aufzurufen.

Wenn eine Ausnahme im Kernelmoduscode auftritt, durchsucht das System die Stapelrahmen des Kernelstapels, um einen Ausnahmehandler zu finden. Wenn ein Handler nicht gefunden werden kann oder kein Handler die Ausnahme behandelt, wird das System so heruntergefahren, als ob die [**ExitWindows-Funktion**](/windows/win32/api/winuser/nf-winuser-exitwindows) aufgerufen worden wäre.

 

 
