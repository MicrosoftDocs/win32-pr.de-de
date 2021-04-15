---
title: Wichtige Pipe-Terminologie
description: Wie bei anderen Typen von Parametern für Remote Prozedur Aufrufe können Pipes in den Parametern \ oder \ out \ Parameter lauten.
ms.assetid: 377fb65a-e819-4e96-a5b7-9850afd97b73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3df183d18d7962ad0c63ecaa0d350006a4144f23
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104517018"
---
# <a name="essential-pipe-terminology"></a>Wichtige Pipe-Terminologie

Wie bei anderen Typen von Parametern für Remote Prozedur Aufrufe können Pipes \[ [**in**](/windows/desktop/Midl/in) - \] oder \[ [**out**](/windows/desktop/Midl/out-idl) - \] Parameter sein. Da der Server die Übertragung von Daten über eine Pipe steuert, werden Pipes mit dem \[ **in** - \] Attribut zum *Abrufen* von Daten an den Server verwendet. Auf ähnliche Weise überträgt *Output Pipes Daten* vom Server an den Client. Die Prozeduren, die die Datenübertragung ausführen, werden als *Pull-Prozedur* bzw. als *pushprozedur* bezeichnet.

Der mittlerer l-Compiler generiert die Push-und Pull-Prozeduren für den Server. Außerdem wird die Zuordnung von Daten Puffern im Arbeitsspeicher verwaltet. Der Client muss jedoch eigene Push-und Pull-Prozeduren bereitstellen. Außerdem muss Sie eine Prozedur zum Zuordnen der von der Pipe verwendeten Speicherpuffer bereitstellen. Diese werden automatisch vom Clientstub zum richtigen Zeitpunkt aufgerufen. Die Zuordnungs Prozedur wird häufig als Zuordnungseinheits-Prozedur oder Zuordnungseinheits-Funktion bezeichnet.

 

 