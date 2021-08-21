---
description: Die Generierung eines neuen Patches kann viel Zeit erfordern.
ms.assetid: 8be9a83a-8c36-43f5-8dda-05fc2f3ce0d2
title: Zwischenspeichern von Patchinformationen (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71513ea1a9418506bbf9025f66a1689c12e9a53f8e6f2e713ddeb3b3d55de580
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942621"
---
# <a name="patch-information-caching-patchwizdll"></a>Zwischenspeichern von Patchinformationen (Patchwiz.dll)

Die Generierung eines neuen Patches kann viel Zeit erfordern. Nachdem Sie mithilfe von einen Patch generiert [Patchwiz.dll, ](patchwiz-dll.md)müssen Sie das Updateimage möglicherweise erneut ändern und einen weiteren Patch generieren. Das Zwischenspeichern von Patchinformationen kann die Zeit reduzieren, die zum Generieren nachfolgender Patches erforderlich ist, indem vorhandene Patches erneut verwendet werden. Beispielsweise kann die zum Erstellen von Service Packs benötigte Zeit mithilfe der binären Patches, die aus vorherigen Patches generiert wurden, reduziert werden. Patchwiz.dll PATCH CACHE DIR verwenden, um einen vorhandenen binären Patch zu suchen und ihn dem Service Pack-Schaltet hinzuzufügen, ohne den \_ \_ Binärpatch neu erstellen zu müssen.

Das Zwischenspeichern von Patchinformationen erfordert die Verwendung [Patchwiz.dll](patchwiz-dll.md). Legen Sie zum Aktivieren der Patchzwischenspeicherung die Eigenschaften PATCH CACHE ENABLED und PATCH CACHE DIR in der Eigenschaftentabelle (Patchwiz.dll) der Eigenschaftendatei für die Patcherstellung \_ \_ \_ \_ (PCP-Datei) fest. [](properties-table-patchwiz-dll-.md) Patchwiz speichert alle Informationen zur Patcherstellung in dem Ordner, der durch die PATCH CACHE DIR-Eigenschaft identifiziert wird, und erstellt \_ \_ diesen Ordner bei Bedarf. Wenn Sie das nächste Mal versuchen, einen Patch zu erstellen, überprüft Patchwiz diesen Ordner, um festzustellen, ob die verglichenen Dateien mit den Dateien im Cache übereinstimmen. Wenn die Dateien übereinstimmen, verwendet Patchwiz die zwischengespeicherten Informationen, anstatt den binären Patch für die Datei neu zu generieren. Wenn die Dateien nicht übereinstimmen oder die Informationen im Cache fehlen, generiert Patchwiz den Patch für die Datei.

Um die Zwischenspeicherung von Patchinformationen zu verwenden, muss der von PATCH CACHE DIR angegebene Ordner beibehalten werden, \_ \_ nachdem eine MSP-Datei erstellt wurde. Wenn der Ordner gelöscht wird, muss PatchWiz binäre Patches für nachfolgende MSP-Dateien erneut generieren. Weitere Informationen zum Beibehalten von Informationen in ausgewählten Regionen einer Zieldatei finden Sie unter [Patchen ausgewählter Bereiche einer Datei.](patching-selected-regions-of-a-file.md)

 

 



