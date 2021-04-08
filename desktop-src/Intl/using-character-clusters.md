---
description: Zeichen Cluster sind Symbol Sequenzen, die nicht zwischen Zeilen aufgeteilt werden können.
ms.assetid: ab852feb-9e26-429e-a02a-11fe0abdfafc
title: Verwenden von Zeichen Clustern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11357a929cf8fec2a7b0caa2bb6ae1ac403e3b91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760488"
---
# <a name="using-character-clusters"></a>Verwenden von Zeichen Clustern

Zeichen Cluster sind Symbol Sequenzen, die nicht zwischen Zeilen aufgeteilt werden können. Einige Sprachen, z. b. Thai und indic, schränken die Platzierung von Caretzeichen auf Punkte zwischen Clustern ein. Diese Einschränkung gilt für Einfügevorgänge, die mit Tastatur-oder Mausaktionen initiiert wurden (Treffer Tests).

Unischreiber stellt Cluster Informationen sowohl in den visuellen Attributen in einer [**Skript- \_ visattr**](/windows/win32/api/usp10/ns-usp10-script_visattr) -Struktur als auch in den logischen Attributen bereit, die in einer [**Skript- \_ logattr**](/windows/win32/api/usp10/ns-usp10-script_logattr) -Struktur enthalten sind. Nachdem die Anwendung [**scriptshape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape)aufgerufen hat, werden die Cluster Informationen sowohl durch Sequenzen desselben Werts im **\_ logattr-Skript des Skripts** als auch durch den **fclusterstart** -Member im **Skript ' \_ visattr** '-Array dargestellt.

[**Scriptbreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak) ruft auch das **fcharstopmember** der Skript- [**\_ logattr**](/windows/win32/api/usp10/ns-usp10-script_logattr) -Struktur ab, um die Cluster Positionen zu identifizieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von uniscri](using-uniscribe.md)
</dt> </dl>

 

 



