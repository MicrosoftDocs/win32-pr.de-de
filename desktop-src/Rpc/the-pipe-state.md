---
title: Der Pipezustand
description: Auf dem Server erstellt der MIDL-Compiler eine Zustandsvariable, die Push-, Pull- und Alloc-Prozeduren koordiniert.
ms.assetid: 7cc59cb3-cf41-40f7-a28f-b896c319ae64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d12c5ef5549d89f3aee2833599f5930f2617478e66e16c3b78188eb63a40e7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924070"
---
# <a name="the-pipe-state"></a>Der Pipezustand

Auf dem Server erstellt der  MIDL-Compiler eine Zustandsvariable, die Push-, Pull- und Alloc-Prozeduren koordiniert. Auf Clientseite muss der Entwickler die *Zustandsvariable* erstellen. Aus diesem Grund ist *die Zustandsvariable* auf beiden Seiten lokal, d. b. client und server behalten jeweils ihren eigenen Pipezustand bei. Der Serverstubcode verwaltet die Zustandsvariable auf dem Server. Sie sollten nicht versuchen, den Inhalt direkt zu ändern. Der Client muss die Felder in der Pipe-Steuerelementstruktur initialisieren und seine *Zustandsvariable* verwalten. Sie verwendet die *Zustandsvariable,* um zu identifizieren, wo Daten zu finden oder zu platzieren sind.

Die *Clientzustandsvariable* kann so einfach wie ein Dateihand handle sein, wenn Sie Daten aus einer Datei in eine andere übertragen. Es kann auch eine ganze Zahl sein, die auf ein Element in einem Array zeigt. Sie können auch eine recht komplexe Zustandsstruktur definieren, um zusätzliche Aufgaben auszuführen, z. B. die Koordination der Push- und Pullroutinen für einen \[ [in-](/windows/desktop/Midl/in)und [out-Parameter.](/windows/desktop/Midl/out-idl) \]

 

 