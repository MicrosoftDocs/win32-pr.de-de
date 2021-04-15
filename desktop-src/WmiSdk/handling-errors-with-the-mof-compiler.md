---
description: Wenn der MOF-Compiler die Kompilierung einer MOF-Datei nicht abschließen kann, bleibt das WMI-Repository möglicherweise in einem nicht definierten Zustand.
ms.assetid: 13adc666-6588-4cfd-a5eb-17da93434468
ms.tgt_platform: multiple
title: Behandeln von Fehlern mit dem MOF-Compiler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 905b406020787de894a2821b501ee465ab63ea5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485819"
---
# <a name="handling-errors-with-the-mof-compiler"></a>Behandeln von Fehlern mit dem MOF-Compiler

Wenn der MOF-Compiler die Kompilierung einer MOF-Datei nicht abschließen kann, bleibt das WMI-Repository möglicherweise in einem nicht definierten Zustand. Wenn Sie z. b. eine MOF-Datei kompilieren und den Befehls Zeilenschalter **-Class: comateonly** verwenden, wird die Kompilierung beendet, wenn bereits eine in der MOF-Datei angegebene Klasse vorhanden ist. Der MOF-Compiler speichert alle Klassen oder Instanzen, die bis zu dem Punkt definiert wurden, an dem der Compiler anhält, im Repository. In einigen Fällen kann dies das WMI-Repository in einem nicht definierten Zustand belassen.

In diesem Fall müssen Sie möglicherweise WMI abbrechen, das WMI-Repository löschen und die WMI-Datei neu erstellen. Alle MOF-Dateien, die den [**pragma Auto Wiederherstellen**](pragma-autorecover.md) - [Präprozessorbefehl](preprocessor-commands.md) enthalten, werden neu erstellt, wenn WMI neu gestartet wird. Sie müssen alle MOF-Dateien, die keine-Anweisung enthalten, manuell neu kompilieren `#pragma autorecover` .

Weitere Informationen zum Deklarieren von Klassen und Instanzen mithilfe der MOF-Syntax finden Sie unter [Entwerfen von Managed Object Format Klassen (MOF)](designing-managed-object-format--mof--classes.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kompilieren von MOF-Dateien](compiling-mof-files.md)
</dt> <dt>

[**Mofcomp**](mofcomp.md)
</dt> <dt>

[Präprozessorbefehle](preprocessor-commands.md)
</dt> </dl>

 

 



