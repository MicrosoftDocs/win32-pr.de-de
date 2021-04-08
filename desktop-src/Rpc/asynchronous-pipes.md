---
title: Asynchrone Pipes
description: Mithilfe von Pipe-Parametern mit asynchronem RPC können Sie Daten inkrementell übertragen, sobald Sie verfügbar werden, ohne den Client und den Server zu binden.
ms.assetid: e5c466b8-c0b0-4fa8-8867-d0715fd614b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be9d6dd5a3e8de7d5c4ad233a577187a49d04ed8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729432"
---
# <a name="asynchronous-pipes"></a>Asynchrone Pipes

Mithilfe von [Pipe](/windows/desktop/Midl/pipe) -Parametern mit asynchronem RPC können Sie Daten inkrementell übertragen, sobald Sie verfügbar werden, ohne den Client und den Server zu binden. Dies ist besonders nützlich, wenn Sie über eine große Menge an zu übertragenden Daten verfügen, in Kombination mit einem langsamen Client, einem langsamen Server oder einem langsamen Netzwerk. Wenn Sie eine Pipe in einem asynchronen Funktionsaufruf verwenden, handelt es sich um eine asynchrone Pipe. Synchrone Pipes werden nicht in Verbindung mit asynchronen Funktionen unterstützt.

Im Gegensatz zu herkömmlichen (synchronen) Pipes, bei denen der Server alle Details zum Senden und empfangen von pipedaten verarbeitet, sind asynchrone Pipes symmetrisch. Das heißt, sowohl der Client als auch der Server können Daten per Push per Push durchlaufen und per Pull über die Pipe abrufen

> [!Note]  
> Pipe-Parameter können nur als Verweis übergeben werden. Auch wenn die IDL-Datei die [Pipeline](/windows/desktop/Midl/pipe) Parameter anzeigt, die als Wert übergeben werden, akzeptieren die generierten stubwerte nur die Pipeline Parameter als Verweis.

 

In der folgenden Erörterung von asynchronen Pipes wird die Vertrautheit mit dem pipetypkonstruktor angenommen. Weitere Informationen zu den in diesen Themen beschriebenen Pipe-Prozeduren finden Sie unter [Pipes](pipes.md).

 

 