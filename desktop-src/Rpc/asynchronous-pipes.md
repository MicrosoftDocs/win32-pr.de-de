---
title: Asynchrone Pipes
description: Durch die Verwendung von Pipeparametern mit asynchronem RPC können Sie Daten inkrementell übertragen, sobald sie verfügbar werden, ohne den Client und den Server zu binden.
ms.assetid: e5c466b8-c0b0-4fa8-8867-d0715fd614b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0957b1ddc381d2a91b77033842b2807ed8a9dd34718d0148d6853083229d408d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023790"
---
# <a name="asynchronous-pipes"></a>Asynchrone Pipes

Durch [die Verwendung](/windows/desktop/Midl/pipe) von Pipeparametern mit asynchronem RPC können Sie Daten inkrementell übertragen, sobald sie verfügbar werden, ohne den Client und den Server zu binden. Dies ist besonders nützlich, wenn Sie über eine große Menge zu übertragende Daten verfügen, kombiniert mit einem langsamen Client, einem langsamen Server oder einem langsamen Netzwerk. Wenn Sie eine Pipe in einem asynchronen Funktionsaufruf verwenden, handelt es sich definitionsgemäß um eine asynchrone Pipe. Synchrone Pipes werden in Verbindung mit asynchronen Funktionen nicht unterstützt.

Im Gegensatz zu herkömmlichen (synchronen) Pipes, bei denen der Server alle Details zum Senden und Empfangen von Pipedaten verarbeitet, sind asynchrone Pipes symmetrisch. Das heißt, sowohl der Client als auch der Server können Daten per Push und Pull über die Pipe übertragen.

> [!Note]  
> Pipeparameter können nur als Verweis übergeben werden. Auch wenn die IDL-Datei [zeigt,](/windows/desktop/Midl/pipe) dass Pipeparameter als Wert übergeben werden, akzeptieren die generierten Stubs Pipeparameter nur als Verweis.

 

In der folgenden Diskussion über asynchrone Pipes wird von Vertrautheit mit dem Pipetypkonstruktor ausgegangen. Weitere Informationen zu den in diesen Themen beschriebenen Pipeverfahren finden Sie unter [Pipes](pipes.md).

 

 