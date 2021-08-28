---
title: Grundlegende Pipeterminologie
description: Wie bei anderen Parametertypen für Remoteprozeduraufrufe können Pipes die Parameter \in\ oder \ out\ sein.
ms.assetid: 377fb65a-e819-4e96-a5b7-9850afd97b73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 389885f440faa477ab22f2100685e2955cbf9fb7ddc4ffcb6440dc4b6f68e003
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930069"
---
# <a name="essential-pipe-terminology"></a>Grundlegende Pipeterminologie

Wie bei anderen Parametertypen für Remoteprozeduraufrufe können Pipes \[ [**in - oder**](/windows/desktop/Midl/in) \] \[ [**out-Parametern enthalten**](/windows/desktop/Midl/out-idl) \] sein. Da der Server die Übertragung von Daten über eine Pipe steuert, werden Pipes mit dem in-Attribut als Pulldaten \[  \] an den Server  bezeichnet. Ebenso übertragen Ausgabepipes *Daten* vom Server an den Client. Die Prozeduren für die Datenübertragung werden als *Pullprozedur* bzw. *Pushprozedur* bezeichnet.

Der MIDL-Compiler generiert die Push- und Pull-Prozeduren für den Server. Darüber hinaus wird die Zuordnung von Datenpuffern im Arbeitsspeicher verwaltet. Der Client muss jedoch eigene Push- und Pull-Prozeduren bereitstellen. Sie muss auch eine Prozedur zum Zuordnen der von der Pipe verwendeten Speicherpuffer bereitstellen. Diese werden automatisch zum entsprechenden Zeitpunkt vom Clientstub aufgerufen. Die Zuordnungsprozedur wird häufig als Zuordnungsprozedur oder zuordnungsfunktion bezeichnet.

 

 