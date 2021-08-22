---
title: TreeMightBeCyclic
description: TreeMightBeCyclic
ms.assetid: 9A997949-A1A2-448C-9739-BE176621F1B4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0af2f8d93c3b38b52871db031419756507e009f7d8adb369fde9b5b2c154fbec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119614435"
---
# <a name="treemightbecyclic"></a>TreeMightBeCyclic

## <a name="text"></a>Text

Die Struktur ist {0} ebenentiefe. Dies kann darauf hindeuten, dass die Barrierefreiheitsstruktur zyklisch ist und daher unendlich zu sein scheint.

## <a name="type"></a>Typ

Fehler

## <a name="description"></a>Beschreibung

Die Elementstruktur ist zyklisch, und die Strukturtiefe kann unendlich sein.

Dieses Problem verursacht Probleme für Personen, die sich auf eine Sprachausgabe und Tastatur für die Navigation verlassen, da es keine offensichtliche Beschränkung für das Durchlaufen von Elementen in der Zielanwendung gibt.

## <a name="possible-causes"></a>Mögliche Ursachen

Mehrere Elemente oder deren über-elemente sind benutzerdefinierte Steuerelemente, die tabbing nicht ordnungsgemäß implementieren. Beispielsweise wird die MSAA [State-Eigenschaft](state-property.md) nicht ordnungsgemäß aktualisiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Richtlinien zur Gestaltung einer tastaturgesteuerten Benutzeroberfläche](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> <dt>

[Windows Richtlinien für die Interaktion mit der Benutzeroberfläche – Tastatur](https://msdn.microsoft.com/library/bb545460.aspx#guidelines)
</dt> </dl>

 

 