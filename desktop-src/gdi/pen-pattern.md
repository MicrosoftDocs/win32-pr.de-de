---
description: Das Pattern-Attribut gibt das Muster eines geometrischen Stifts an.
ms.assetid: 5a330416-3b83-4f0f-825c-80e47903966e
title: Stift Muster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 577b5e2cb31e44a4631760c82e678af069322cbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528298"
---
# <a name="pen-pattern"></a>Stift Muster

Das Pattern-Attribut gibt das Muster eines geometrischen Stifts an.

Die folgende Abbildung zeigt Linien, die mit unterschiedlichen geometrischen stiften gezeichnet werden. Jeder Stift wurde mit einem anderen Pattern-Attribut erstellt.

![Abbildung, die vier Zeilen anzeigt, die jeweils mit einem anderen Stift gefüllt sind](images/cspen-02.png)

Die erste Zeile in der vorherigen Abbildung wird mit einem der sechs verfügbaren Schraffurmuster gezeichnet. Weitere Informationen zu Schraffurmustern finden Sie unter [Stift Schraffur](pen-hatch.md). Die nächste Zeile wird mithilfe des hohlen Musters gezeichnet, das mit dem NULL-Muster identisch ist. Die dritte Zeile wird mithilfe eines benutzerdefinierten Musters gezeichnet, das aus einer 8-x-8-Pixel-Bitmap erstellt wurde. (Weitere Informationen zu Bitmaps und deren Erstellung finden Sie unter [Bitmaps](bitmaps.md).) Die letzte Zeile wird mithilfe eines voll soliden Musters gezeichnet. Durch das Erstellen eines Pinsels und das Übergeben des Handles an die [**extkreatepen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) -Funktion wird ein Muster erstellt.

 

 



