---
description: In der folgenden Tabelle werden die verschiedenen Methoden angezeigt, mit denen die Anwendung die Einfügemarke, die Begründung und die Cluster verarbeiten kann.
ms.assetid: 950a24b4-62ab-4eaf-ac15-87434d3c28c0
title: Arbeiten mit Beziehungen zwischen Einfügepositionen, Ausrichtungspunkten und Clustern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d051d008a8ae991b2858be598713fe9ad1adc0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368092"
---
# <a name="working-with-relationships-among-caret-positions-justification-points-and-clusters"></a>Arbeiten mit Beziehungen zwischen Einfügepositionen, Ausrichtungspunkten und Clustern

In der folgenden Tabelle werden die verschiedenen Methoden angezeigt, mit denen die Anwendung die Einfügemarke, die Begründung und die Cluster verarbeiten kann.



| Aufgabe                             | Uniscriunterstützung                                                                                                                                                                                                                                                              |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Caretzeichen nach Zeichen Cluster verschieben  | Der *pwlogclust* -Parameter von [**scriptshape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) functionthe **fclusterstart** -Member der Skript-Struktur " [**\_ visattr**](/windows/win32/api/usp10/ns-usp10-script_visattr) "<br/> Das **fcharstopmember** der [**Skript- \_ logattr**](/windows/win32/api/usp10/ns-usp10-script_logattr) -Struktur.<br/> |
| Zeilenumbruch zwischen Zeichen | Der *pwlogclust* -Parameter von [**scriptshape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) functionthe **fclusterstart** -Member der Skript-Struktur " [**\_ visattr**](/windows/win32/api/usp10/ns-usp10-script_visattr) "<br/> Das **fcharstopmember** der [**Skript- \_ logattr**](/windows/win32/api/usp10/ns-usp10-script_logattr) -Struktur.<br/> |
| Caretzeichen nach Wort verschieben               | Der **fwordstoppt** -Member der [**\_ logattr-Skript**](/windows/win32/api/usp10/ns-usp10-script_logattr) Struktur                                                                                                                                                                                            |
| Zeilenumbruch zwischen Wörtern      | Der **fwordstoppt** -Member der [**\_ logattr-Skript**](/windows/win32/api/usp10/ns-usp10-script_logattr) Struktur                                                                                                                                                                                            |
| Begründung                    | Der Benutzer **definierte Member der** Skript- [**\_ visattr**](/windows/win32/api/usp10/ns-usp10-script_visattr) -Struktur.                                                                                                                                                                                       |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von uniscri](using-uniscribe.md)
</dt> </dl>

 

 




