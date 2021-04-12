---
title: Treemightbecyclic
description: Treemightbecyclic
ms.assetid: 9A997949-A1A2-448C-9739-BE176621F1B4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9647f4429ba17226f342a8dceb3c51b033d08b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315279"
---
# <a name="treemightbecyclic"></a>Treemightbecyclic

## <a name="text"></a>Text

Struktur ist {0} Tiefe Ebenen. Dies weist möglicherweise darauf hin, dass die Barrierefreiheits Struktur zyklisch ist und daher scheinbar unendlich wäre.

## <a name="type"></a>type

Fehler

## <a name="description"></a>BESCHREIBUNG

Die Elementstruktur ist zyklisch, und die Struktur Tiefe kann unendlich sein.

Dieses Problem bewirkt, dass Personen, die sich auf einen Bildschirm-Reader und eine Tastatur für die Navigation verlassen, keine offensichtlichen Beschränkungen für die Durchquerung der Elemente in der Zielanwendung auftreten.

## <a name="possible-causes"></a>Mögliche Ursachen

Mehrere Elemente oder ihre übergeordneten Elemente sind benutzerdefinierte Steuerelemente, die die Tabstopps nicht ordnungsgemäß implementieren. Beispielsweise wird die Eigenschaft MSAA [State](state-property.md) nicht ordnungsgemäß aktualisiert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Richtlinien zur Gestaltung einer tastaturgesteuerten Benutzeroberfläche](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> <dt>

[Windows-Benutzeroberflächen-Interaktions Richtlinien-Tastatur](https://msdn.microsoft.com/library/bb545460.aspx#guidelines)
</dt> </dl>

 

 