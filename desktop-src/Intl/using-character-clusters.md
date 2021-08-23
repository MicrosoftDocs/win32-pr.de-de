---
description: Zeichencluster sind Glyphensequenzen, die nicht auf Zeilen aufgeteilt werden können.
ms.assetid: ab852feb-9e26-429e-a02a-11fe0abdfafc
title: Verwenden von Zeichenclustern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7a48dc8ec1b6fa3ea28cd116f275b1f410b8abd7e232442cff430ab843765f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631820"
---
# <a name="using-character-clusters"></a>Verwenden von Zeichenclustern

Zeichencluster sind Glyphensequenzen, die nicht auf Zeilen aufgeteilt werden können. Einige Sprachen, z. B. Thai und Indic, beschränken die Platzierung von Caretpunkten auf Punkte zwischen Clustern. Diese Einschränkung gilt für Caret-Verschiebungen, die mit Tastatur- oder Mausaktionen initiiert werden (Treffertests).

Uniscribe stellt Clusterinformationen sowohl in den visuellen Attributen, die in einer [**SCRIPT \_ CSVTTR-Struktur**](/windows/win32/api/usp10/ns-usp10-script_visattr) enthalten sind, als auch in den logischen Attributen in einer [**SCRIPT \_ LOGATTR-Struktur**](/windows/win32/api/usp10/ns-usp10-script_logattr) bereit. Nachdem die Anwendung [**ScriptShape aufruft,**](/windows/desktop/api/Usp10/nf-usp10-scriptshape)werden die Clusterinformationen sowohl durch Sequenzen desselben Werts im **SCRIPT \_ LOGATTR-Array** als auch durch den **fClusterStart-Member** im **SCRIPT \_ BAGTTR-Array** dargestellt.

[**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak) ruft auch den **fCharStop-Member** der [**SCRIPT \_ LOGATTR-Struktur**](/windows/win32/api/usp10/ns-usp10-script_logattr) ab, um Clusterpositionen zu identifizieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 



