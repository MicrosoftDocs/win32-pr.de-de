---
title: Kombinieren von Pipe-und nonpipe-Parametern
description: Kombinieren von Pipe-und nonpipe-Parametern im Remote Prozedur Aufruf (RPC).
ms.assetid: 52109ba9-4e10-4426-8dfc-e3052d403e9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0776f995dacb4d477724b0ee1e5c2fa969723199
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858401"
---
# <a name="combining-pipe-and-nonpipe-parameters"></a>Kombinieren von Pipe-und nonpipe-Parametern

Wenn Sie Pipetypen und andere Typen in einem Remote Prozedur aufrufsbefehl kombinieren, werden die Daten gemäß der Richtung des Parameters übertragen:

-   **In Richtung werden \[ die Daten für alle nonpipe-Argumente zuerst übertragen, gefolgt von pipedaten. \]**
-   In der **\[ Ausrichtungs \]** Richtung sendet der Server zuerst die Pipe-Daten. Nachdem die Manager-Routine zurückgegeben wurde, überträgt der Server die nonpipe-Daten.
-   Wenn **\[ in, out \]** -Pipe-Argumente in Kombination mit **\[ in \] -, out-, out** -, out-und over-Pipe-Argumenten vorhanden sind, werden zuerst die Eingabedaten wie zuvor beschrieben übertragen. Anschließend werden die Ausgabedaten wie zuvor beschrieben übertragen.

Die folgende Einschränkung gilt für diese (Mittel l 3,0) Implementierung von Pipes: Wenn Sie Pipetypen und andere Typen in einem einzelnen Remote Prozedur aufzurufen kombinieren, müssen die nonpipe-Parameter über eine klar definierte Größe verfügen, damit der Mittelwert Compiler die benötigte Puffergröße berechnen kann. Sie können z. b. keine pipenameter mit einem \[ [eindeutigen](/windows/desktop/Midl/unique) \] Zeiger oder einer konformen Struktur kombinieren, da ihre Größe zum Zeitpunkt der Kompilierung nicht bestimmt werden kann.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kanal](/windows/desktop/Midl/pipe)
</dt> <dt>

[/Oi](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 