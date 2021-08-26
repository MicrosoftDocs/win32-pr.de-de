---
title: Empfangen der asynchronen Antwort
description: Nachdem er benachrichtigt wurde, dass der Server eine Antwort gesendet hat, ruft der Client RpcAsyncCompleteCall mit dem asynchronen Handle auf, damit er die Antwort empfangen kann.
ms.assetid: 48fb3777-d90a-474b-a1fa-9d034b5791e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24500e176a7c5a36342b4188e687c557d48646deef1de39845257d8e04ff7c45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120018820"
---
# <a name="receiving-the-asynchronous-reply"></a>Empfangen der asynchronen Antwort

Nachdem er benachrichtigt wurde, dass der Server eine Antwort gesendet hat, ruft der Client [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) mit dem asynchronen Handle auf, damit er die Antwort empfangen kann. Wenn **RpcAsyncCompleteCall** erfolgreich abgeschlossen wurde, zeigt der *Reply-Parameter* auf einen Puffer, der den Rückgabewert der Remotefunktion enthält. Alle Puffer, die vom Clientprogramm als \[ [**out-**](/windows/desktop/Midl/out-idl) \] oder \[ [**in**](/windows/desktop/Midl/in)  \] -Out-Parameter für die asynchrone Remotefunktion bereitgestellt werden, enthalten gültige Daten. Wenn der Client **RpcAsyncCompleteCall aufruft,** bevor der Server die Antwort gesendet hat, schlägt dieser Aufruf fehl und gibt den Wert RPC \_ S \_ ASYNC \_ CALL \_ PENDING zurück.

Wenn Ihr Clientprogramm E/A-Abschlussports oder -Ereignisse für Benachrichtigungen verwendet, muss [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) aufgerufen werden, um den Port freizugeben oder zu verarbeiten, wenn es sie nicht mehr benötigt.

 

 