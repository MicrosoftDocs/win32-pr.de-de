---
description: Die Handhabung von Benutzermodus-Ausnahmen durch das System bietet Unterstützung für anspruchsvolle debuggger.
ms.assetid: c45a7dc6-e6b2-4fc4-9522-12d96893f4c7
title: Debugger-Ausnahmebehandlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6aff6d566e8798aaf4f3113ce6d8f44a3bc71ba
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104482742"
---
# <a name="debugger-exception-handling"></a>Debugger-Ausnahmebehandlung

Die Handhabung von Benutzermodus-Ausnahmen durch das System bietet Unterstützung für anspruchsvolle debuggger. Wenn der Prozess, in dem eine Ausnahme auftritt, gedebuggt wird, generiert das System ein Debugereignis. Wenn der Debugger die [**waitfordebugevent**](/windows/win32/api/debugapi/nf-debugapi-waitfordebugevent) -Funktion verwendet, bewirkt das Debug-Ereignis, dass diese Funktion mit einem Zeiger auf eine [**Debug- \_ Ereignis**](/windows/win32/api/minwinbase/ns-minwinbase-debug_event) Struktur zurückgegeben wird. Diese Struktur enthält die Prozess-und Thread Bezeichner, mit denen der Debugger auf den Kontext Daten Satz des Threads zugreifen kann. Die Struktur enthält außerdem eine [**Ausnahme- \_ Debug- \_ Informations**](/windows/win32/api/minwinbase/ns-minwinbase-exception_debug_info) Struktur, die eine Kopie des Ausnahme Datensatzes enthält.

Wenn das System nach einem Ausnahmehandler sucht, werden zwei Versuche unternommen, den Debugger eines Prozesses zu benachrichtigen. Der erste Benachrichtigungs Versuch bietet dem Debugger die Möglichkeit, Haltepunkt-oder einstufige Ausnahmen zu verarbeiten. Dies wird als Benachrichtigung über die *erste Chance* bezeichnet. Der Benutzer kann dann Debugger-Befehle ausgeben, um die Prozessumgebung zu bearbeiten, bevor Ausnahmehandler ausgeführt werden. Der zweite Versuch, den Debugger zu benachrichtigen, tritt nur dann auf, wenn das System keinen Frame basierten Ausnahmehandler finden kann, der die Ausnahme behandelt. Dies wird als *Benachrichtigung der letzten Chance* bezeichnet. Wenn die Ausnahme vom Debugger nach der Benachrichtigung der letzten Chance nicht behandelt wird, beendet das System den Prozess, der debuggt wird.

Bei jedem Benachrichtigungs Versuch verwendet der Debugger die [**continuedebugevent**](/windows/win32/api/debugapi/nf-debugapi-continuedebugevent) -Funktion, um die Steuerung an das System zurückzugeben. Vor dem Zurückgeben der Steuerung kann der Debugger die Ausnahme behandeln und den Thread Zustand entsprechend ändern, oder er kann die Ausnahme nicht behandeln. Mithilfe von **continuedebugevent** kann der Debugger angeben, dass die Ausnahme behandelt wurde. in diesem Fall wird der Zustand des Computers wieder hergestellt, und die Thread Ausführung wird an dem Punkt fortgesetzt, an dem die Ausnahme aufgetreten ist. Der Debugger kann auch angeben, dass die Ausnahme nicht behandelt wurde, was bewirkt, dass das System die Suche nach einem Ausnahmehandler fortsetzt.

 

 
