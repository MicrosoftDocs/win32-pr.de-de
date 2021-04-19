---
description: Das Erstellen eines neuen Patches erfordert möglicherweise eine beträchtliche Zeit.
ms.assetid: 8be9a83a-8c36-43f5-8dda-05fc2f3ce0d2
title: Zwischenspeichern von Patchinformationen (Patchwiz.dll)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7000efceea62e9eef122a34f7700622e1e6e2e60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354593"
---
# <a name="patch-information-caching-patchwizdll"></a>Zwischenspeichern von Patchinformationen (Patchwiz.dll)

Das Erstellen eines neuen Patches erfordert möglicherweise eine beträchtliche Zeit. Nachdem Sie mit [Patchwiz.dll](patchwiz-dll.md)einen Patch generiert haben, müssen Sie das Update Abbild möglicherweise erneut ändern und einen weiteren Patch generieren. Das Zwischenspeichern von Patchinformationen kann den Zeitaufwand für das Generieren von nachfolgenden Patches verringern, indem vorhandene Patches wieder verwendet werden Beispielsweise kann die Zeit, die zum Erstellen von Service Packs erforderlich ist, durch die Verwendung der binären Patches reduziert werden, die aus vorherigen Patches generiert wurden. Patchwiz.dll können den Patch \_ \_ -Cache dir verwenden, um ein vorhandenes binäres Patch zu suchen und es Service Pack der CAB-Datei hinzuzufügen, ohne dass der binäre Patch neu erstellt werden muss.

Das Zwischenspeichern von Patchinformationen erfordert die Verwendung von [Patchwiz.dll](patchwiz-dll.md). Um die patchzwischen Speicherung zu aktivieren, legen Sie die \_ Eigenschaften Patchcache \_ aktiviert und Patch \_ Cache \_ dir in der [Properties-Tabelle (Patchwiz.dll)](properties-table-patchwiz-dll-.md) der Datei mit den patcherstellungs Eigenschaften (PCP-Datei) fest. Patchwiz speichert alle Informationen zur Patcherstellung in dem Ordner, der durch die Eigenschaft Patch Cache dir identifiziert wird, \_ \_ und erstellt bei Bedarf diesen Ordner. Wenn Sie das nächste Mal versuchen, einen Patch zu erstellen, überprüft patchwiz diesen Ordner, um festzustellen, ob die zu vergleichenden Dateien mit den Dateien im Cache zu vergleichen sind. Wenn die Dateien entsprechen, verwendet patchwiz die zwischengespeicherten Informationen, anstatt den binären Patch für die Datei erneut zu generieren. Wenn die Dateien nicht stimmen oder wenn die Informationen im Cache fehlen, generiert patchwiz den Patch für die Datei.

Um das Zwischenspeichern von Patchinformationen zu verwenden, muss der durch Patch \_ Cache Dir angegebene Ordner \_ beibehalten werden, nachdem eine MSP-Datei erstellt wurde. Wenn der Ordner gelöscht wird, muss patchwiz binäre Patches für nachfolgende MSP-Dateien neu generieren. Weitere Informationen zum Beibehalten von Informationen in ausgewählten Regionen einer Zieldatei finden Sie unter [Patching Selected Regions of a file](patching-selected-regions-of-a-file.md).

 

 



