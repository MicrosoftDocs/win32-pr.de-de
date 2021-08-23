---
description: Wenn der MOF-Compiler das Kompilieren einer MOF-Datei nicht beenden kann, bleibt das WMI-Repository möglicherweise in einem nicht definierten Zustand.
ms.assetid: 13adc666-6588-4cfd-a5eb-17da93434468
ms.tgt_platform: multiple
title: Behandeln von Fehlern mit dem MOF-Compiler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03f5174af836a0b27824c40486364cc81809db97b9608e6b1c813c4c1029d3aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993170"
---
# <a name="handling-errors-with-the-mof-compiler"></a>Behandeln von Fehlern mit dem MOF-Compiler

Wenn der MOF-Compiler das Kompilieren einer MOF-Datei nicht beenden kann, bleibt das WMI-Repository möglicherweise in einem nicht definierten Zustand. Wenn Sie beispielsweise eine MOF-Datei kompilieren und den Befehlszeilenschalter **-class:createonly** verwenden, wird die Kompilierung beendet, wenn bereits eine in der MOF-Datei angegebene Klasse vorhanden ist. Der MOF-Compiler speichert im Repository alle Klassen oder Instanzen, die bis zu dem Punkt definiert wurden, an dem der Compiler beendet wird. In einigen Fällen kann dies das WMI-Repository in einer nicht definierten Bedingung befingen.

In diesem Fall müssen Sie möglicherweise WMI beenden, das WMI-Repository löschen und WMI neu erstellen. Alle MOF-Dateien, die den [**Präprozessorbefehl pragma autorecover**](pragma-autorecover.md) [](preprocessor-commands.md) enthalten, werden neu erstellt, wenn WMI neu gestartet wird. Sie müssen alle MOF-Dateien, die keine -Anweisung enthalten, manuell neu `#pragma autorecover` kompilieren.

Weitere Informationen zum Deklarieren von Klassen und Instanzen mithilfe der MOF-Syntax finden Sie unter Entwerfen Managed Object Format [-Klassen (MOF).](designing-managed-object-format--mof--classes.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kompilieren von MOF-Dateien](compiling-mof-files.md)
</dt> <dt>

[**mofcomp**](mofcomp.md)
</dt> <dt>

[Präprozessorbefehle](preprocessor-commands.md)
</dt> </dl>

 

 



