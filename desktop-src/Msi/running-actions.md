---
description: Die Installer-Funktionen können verwendet werden, um bestimmte Aktionen oder Aktions Sequenzen auszuführen.
ms.assetid: ceb4f70b-1179-416a-9030-3d87341cb956
title: Ausführen von Aktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4ab566b90ec43a33f3e70b994b01446700e353b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343398"
---
# <a name="running-actions"></a>Ausführen von Aktionen

Die Installer-Funktionen können verwendet werden, um bestimmte Aktionen oder Aktions Sequenzen auszuführen. Diese Aktionen können entweder [standardmäßige](standard-actions.md) oder [benutzerdefinierte](custom-actions.md) Aktionen sein. Im folgenden Verfahren wird beschrieben, wie Sie Aktionen ausführen:

**So führen Sie eine Aktions Sequenz aus**

1.  Führen Sie eine Sequenz von Aktionen aus, die in einer Tabelle durch Aufrufen der [**msisequence**](/windows/desktop/api/Msiquery/nf-msiquery-msisequencea) -Funktion definiert sind.

    Das Installationsprogramm fragt die entsprechende Tabelle ab und führt jede Aktion aus, wenn der bedingte Ausdruck true ergibt.

2.  Überprüfen Sie bedingte Ausdrücke, indem Sie die [**msievaluatecondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) -Funktion aufrufen.
3.  Führen Sie die Aktion aus, indem Sie die [**msidoaction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) -Funktion aufrufen. Bei der Aktion kann es sich um eine Standardaktion, eine benutzerdefinierte Aktion oder ein Benutzeroberflächen Dialogfeld handeln.
4.  Wenn während der Ausführung dieser Aktion ein Fehler aufgetreten ist, wird die [**msiprocessmessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) -Funktion aufgerufen. Der Fehler wird vom Installationsprogramm verarbeitet.

 

 



