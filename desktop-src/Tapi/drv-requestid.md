---
description: Der drv \_ -Datentyp "drv RequestId" wird verwendet, um einen eindeutigen Bezeichner für eine Anforderung an den Dienstanbieter bereitzustellen.
ms.assetid: cef6a42a-2e40-4f65-8fab-79cfba143206
title: DRV_REQUESTID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f9c0db093b06b263bcdc702ff14af7e308033f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350215"
---
# <a name="drv_requestid"></a>DRV \_ -RequestId

Der **drv-Datentyp "drv \_ RequestId** " wird verwendet, um einen eindeutigen Bezeichner für eine Anforderung an den Dienstanbieter bereitzustellen. Ein Wert dieses Typs wird als Parameter an jede Funktion übergeben, die einen asynchronen Vorgang zulässt. Wenn der Vorgang asynchron ist, gibt der Dienstanbieter diesen Wert als Rückgabewert der Funktion zurück. Immer wenn der Dienstanbieter auf diese Weise eine Anforderung als asynchron ausweist, muss der Vorgang durch Aufrufen der Funktion [*Abschluss \_ proc*](/windows/win32/api/tspi/nc-tspi-async_completion) Callback abgeschlossen werden.

TAPI stellt sicher, dass die von ihm bereitgestellten **drv \_ -RequestId-** Werte genau positiv sind, d. h. zwischen den Werten von 0x00000001 und 0x7FFFFFFF (einschließlich). Außerdem sind die Werte insofern eindeutig, als dass kein Wert, der von einer Funktion zurückgegeben wird, um die Anforderung als asynchron zu markieren, wieder verwendet wird, bevor der Vorgang als beendet gemeldet wird.

 

 
