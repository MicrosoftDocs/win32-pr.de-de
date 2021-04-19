---
description: Standardmäßig sind alle FP-Ausnahmen im System deaktiviert.
ms.assetid: efbea036-de9c-4f92-865a-494161da375e
title: Gleitkommaausnahmen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6a4db92a13a0215bb372db12d30bb11a749a0fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342572"
---
# <a name="floating-point-exceptions"></a>Gleitkommaausnahmen

Standardmäßig sind alle FP-Ausnahmen im System deaktiviert. Daher führen Berechnungen in Nan oder Infinity anstelle einer Ausnahme aus. Bevor Sie Gleit Komma Ausnahmen (FP) mithilfe der strukturierten Ausnahmebehandlung abfangen können, müssen Sie die [ \_ controlfp \_ s](/previous-versions/visualstudio/visual-studio-2010/c9676k6h(v=vs.100)) C-Lauf Zeit Bibliotheksfunktion zum Aktivieren aller möglichen FP-Ausnahmen aufruft. Wenn nur bestimmte Ausnahmen abgefangen werden sollen, verwenden Sie nur die Flags, die den zu erfassenden Ausnahmen entsprechen. Beachten Sie, dass jeder Handler für FP-Fehler [ \_ clearfp](/cpp/c-runtime-library/reference/clear87-clearfp?view=vs-2019) als erste FP-Anweisung aufrufen sollte. Diese Funktion löscht Gleit Komma Ausnahmen.

 

 
