---
description: Wenn eine Hardware-oder Software Ausnahme auftritt, beendet der Prozessor die Ausführung an dem Punkt, an dem die Ausnahme aufgetreten ist, und überträgt die Steuerung an das System.
ms.assetid: 35a1b9bd-8da9-47e6-beda-e0b159bd840d
title: Ausnahme Verteilung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e02b40aa132541fe88d692cbbf1881a8b620a209
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125713"
---
# <a name="exception-dispatching"></a>Ausnahme Verteilung

Wenn eine Hardware-oder Software Ausnahme auftritt, beendet der Prozessor die Ausführung an dem Punkt, an dem die Ausnahme aufgetreten ist, und überträgt die Steuerung an das System. Zuerst speichert das System sowohl den Computer Status des aktuellen Threads als auch Informationen, die die Ausnahme beschreiben. Das System versucht dann, einen Ausnahmehandler zu finden, der die Ausnahme behandelt.

Der Computer Zustand des Threads, in dem die Ausnahme aufgetreten ist, wird in einer [**Kontext**](/windows/desktop/api/WinNT/ns-winnt-arm64_nt_context) Struktur gespeichert. Diese Informationen (als *Kontext Daten Satz* bezeichnet) ermöglichen dem System, die Ausführung an dem Zeitpunkt der Ausnahme fortzusetzen, wenn die Ausnahme erfolgreich behandelt wird. Die Beschreibung der Ausnahme (als **Ausnahme Daten Satz** bezeichnet) wird in einer [**Ausnahme \_ Daten Satz**](/windows/desktop/api/WinNT/ns-winnt-exception_record) Struktur gespeichert. Da die Computer abhängigen Informationen des Kontext Datensatzes getrennt von den Computer unabhängigen Informationen des Ausnahme Datensatzes gespeichert werden, kann der Mechanismus für die Ausnahmebehandlung auf verschiedene Plattformen portierbar sein.

Die Informationen in den Kontext-und Ausnahme Datensätzen sind über die Funktion [**GetExceptionInformation**](getexceptioninformation.md) verfügbar und können für alle Ausnahmehandler zur Verfügung gestellt werden, die als Ergebnis der Ausnahme ausgeführt werden. Der Ausnahme Daten Satz enthält die folgenden Informationen.

-   Ein Ausnahme Code, der den Typ der Ausnahme identifiziert.
-   Flags, die angeben, ob die Ausnahme fort setzbar ist. Jeder Versuch, die Ausführung fortzusetzen, nachdem eine nicht fort Setz Bare Ausnahme eine andere Ausnahme generiert hat.
-   Ein Zeiger auf einen anderen Ausnahme Daten Satz. Dies erleichtert das Erstellen einer verknüpften Liste von Ausnahmen, wenn eine Ausnahme ausgelöst wird.
-   Die Adresse, an der die Ausnahme aufgetreten ist.
-   Ein Array von Argumenten, die zusätzliche Informationen über die Ausnahme bereitstellen.

Wenn im Benutzermoduscode eine Ausnahme auftritt, verwendet das System die folgende Such Reihenfolge, um einen Ausnahmehandler zu finden:

1.  Wenn der Prozess gedebuggt wird, benachrichtigt das System den Debugger. Weitere Informationen finden Sie unter [Debugger-Ausnahmebehandlung](debugger-exception-handling.md).
2.  Wenn der Prozess nicht debuggt wird oder der zugehörige Debugger die Ausnahme nicht behandelt, versucht das System, einen Frame basierten Ausnahmehandler zu suchen, indem er die Stapel Rahmen des Threads durchsucht, in dem die Ausnahme aufgetreten ist. Das System durchsucht zuerst den aktuellen Stapel Rahmen und durchsucht anschließend die vorangehenden Stapel Rahmen in umgekehrter Reihenfolge.
3.  Wenn kein Frame basierter Handler gefunden werden kann oder kein Frame basierter Handler die Ausnahme behandelt, aber der Prozess gerade debuggt wird, benachrichtigt das System den Debugger ein zweites Mal.
4.  Wenn der Prozess nicht debuggt wird oder der zugehörige Debugger die Ausnahme nicht behandelt, stellt das System eine Standardbehandlung auf Grundlage des Ausnahme Typs bereit. Bei den meisten Ausnahmen besteht die Standardaktion darin, die [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) -Funktion aufzurufen.

Wenn eine Ausnahme im Kernelmoduscode auftritt, durchsucht das System die Stapel Rahmen des Kernel Stapels in einem Versuch, einen Ausnahmehandler zu suchen. Wenn ein Handler nicht gefunden werden kann oder kein Handler die Ausnahme behandelt, wird das System so heruntergefahren, als ob die [**exitwindows**](/windows/win32/api/winuser/nf-winuser-exitwindows) -Funktion aufgerufen wurde.

 

 
