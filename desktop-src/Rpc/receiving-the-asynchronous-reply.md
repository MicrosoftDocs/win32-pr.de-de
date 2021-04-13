---
title: Empfangen der asynchronen Antwort
description: Nachdem die Benachrichtigung gesendet wurde, dass der Server eine Antwort gesendet hat, ruft der Client rpcasynccompletecallcenter mit dem asynchronen Handle auf, damit er die Antwort empfangen kann.
ms.assetid: 48fb3777-d90a-474b-a1fa-9d034b5791e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9143daaf1f276f784086e2ec17efb47dfd1fb6e4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390893"
---
# <a name="receiving-the-asynchronous-reply"></a>Empfangen der asynchronen Antwort

Nachdem die Benachrichtigung gesendet wurde, dass der Server eine Antwort gesendet hat, ruft der Client [**rpcasynccompletecallcenter**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) mit dem asynchronen Handle auf, damit er die Antwort empfangen kann. Wenn **rpcasynccompletecallcenter** erfolgreich abgeschlossen wurde, verweist der *Antwort* Parameter auf einen Puffer, der den Rückgabewert der Remote Funktion enthält. Alle Puffer, die vom Client Programm als \[ [**out**](/windows/desktop/Midl/out-idl) \] oder \[ [**in**](/windows/desktop/Midl/in)bereit  gestellt werden, \] enthalten die Out-Parameter für die asynchrone Remote Funktion, die gültige Daten enthalten. Wenn der Client **rpcasynccompletecallaufruft** , bevor der Server die Antwort gesendet hat, schlägt dieser Aufruf fehl, und es wird ein Wert von RPC \_ S \_ Async- \_ Aufruf \_ Ausstehend zurückgegeben.

Wenn Ihr Client Programm e/a-Abschlussports oder-Ereignisse für die Benachrichtigung verwendet, muss es [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) zum Freigeben des Ports oder Handles aufruft, wenn es nicht mehr benötigt wird.

 

 