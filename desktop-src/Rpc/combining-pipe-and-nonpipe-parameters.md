---
title: Kombinieren von Pipe- und Nonpipe-Parametern
description: Kombinieren von Pipe- und Nichtpipeparametern im Remoteprozeduraufruf (REMOTE Procedure Call, RPC).
ms.assetid: 52109ba9-4e10-4426-8dfc-e3052d403e9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac76bc2f334325c87cbf8c4a09898cf0fe54153cd84f6f2809995e66cc08e843
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022670"
---
# <a name="combining-pipe-and-nonpipe-parameters"></a>Kombinieren von Pipe- und Nonpipe-Parametern

Wenn Sie Pipetypen und andere Typen in einem Remoteprozeduraufruf kombinieren, werden die Daten entsprechend der Richtung des Parameters übertragen:

-   In der **\[ Richtung \]** werden die Daten für alle Nichtpipeargumente zuerst übertragen, gefolgt von Pipedaten.
-   In der **\[ Richtung "Out" \]** sendet der Server zuerst die Pipedaten. Nachdem die Managerroutine zurückgegeben wurde, überträgt der Server die Nichtpipedaten.
-   Wenn **\[ \] In-Out-Pipeargumente** mit nicht pipebasierten **\[ \] In-Out-Argumenten** kombiniert sind, werden die Eingabedaten zunächst vollständig übertragen, wie zuvor beschrieben. Anschließend werden die Ausgabedaten wie zuvor beschrieben übertragen.

Die folgende Einschränkung gilt für diese MIDL 3.0-Implementierung von Pipes: Wenn Sie Pipetypen und andere Typen in einem einzelnen Remoteprozeduraufruf kombinieren, müssen die Nichtpipeparameter eine klar definierte Größe haben, damit der MIDL-Compiler die benötigte Puffergröße berechnen kann. Beispielsweise können Sie Pipeparameter nicht mit einem eindeutigen Zeiger oder einer konformen Struktur kombinieren, da ihre Größen zur Kompilierzeit \[ [](/windows/desktop/Midl/unique) \] nicht bestimmt werden können.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Rohr](/windows/desktop/Midl/pipe)
</dt> <dt>

[/Oi](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 