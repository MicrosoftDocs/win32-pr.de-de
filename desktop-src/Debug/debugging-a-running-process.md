---
description: Um einen Prozess zu debuggen, der bereits ausgeführt wird, sollte der Debugger DebugActiveProcess mit dem Prozessbezeichner verwenden. Um eine Liste von Prozessbezeichnern abzurufen, verwenden Sie entweder die Funktion EnumProcesses oder Process32First.
ms.assetid: 2662411f-a69a-442b-a177-a27ea025bb01
title: Debuggen eines ausgeführten Prozesses
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f3cf141da9905c76659c2ae11e9b82e2e2f5fee9bd934dce835b129678995ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119279350"
---
# <a name="debugging-a-running-process"></a>Debuggen eines ausgeführten Prozesses

Um einen Prozess zu debuggen, der bereits ausgeführt wird, sollte der Debugger [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) mit dem Prozessbezeichner verwenden. Um eine Liste von Prozessbezeichnern abzurufen, verwenden Sie entweder die [**Funktion EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses) oder [**Process32First.**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first)

[**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) fügt den Debugger an den aktiven Prozess an. In diesem Fall kann nur der aktive Prozess gedebuggt werden. die untergeordneten Prozesse können nicht. Der Debugger muss über den entsprechenden Zugriff auf den ausgeführten Prozess verfügen, um **DebugActiveProcess** verwenden zu können. Weitere Informationen zu Zugriffsrechten finden Sie unter [Access Control](../secauthz/access-control.md).

Nachdem der Debugger sich entweder selbst erstellt oder an den Prozess angefügt hat, den er debuggen möchte, benachrichtigt das System den Debugger über alle Debugereignisse, die im Prozess auftreten, und, falls angegeben, in allen untergeordneten Prozessen. Weitere Informationen zum Debuggen von Ereignissen finden Sie unter [Debuggen von Ereignissen.](debugging-events.md)

Zum Trennen von dem Prozess, der gedebuggt wird, sollte der Debugger die [**DebugactiveProcessStop-Funktion**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocessstop) verwenden.

 

 
