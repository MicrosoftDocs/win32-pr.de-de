---
description: Konsistente und done-Flags
ms.assetid: a641fa95-5587-4362-9869-e5c27c6dd2ce
title: Konsistente und done-Flags
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56a61d1f715d06e6bfb6632b9bbb59276074c4d7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524371"
---
# <a name="consistent-and-done-flags"></a>Konsistente und done-Flags

Com+ erstellt vor dem Aktivieren eines transaktionalen Objekts immer ein Kontext Objekt. Das Kontext Objekt enthält objektbezogene Informationen, z. b. den Ersteller und den zugehörigen Transaktions Bezeichner. Jedes Kontext Objekt enthält auch ein *konsistentes Flag* und ein *done-Flag*. Diese Flags bestimmen den Status des Transaktions Objekts.

Das konsistente Flag gibt an, dass das Transaktions Objekt entweder konsistent oder inkonsistent ist. Die Details, die den Zustand eines Objekts konsistent machen, sind der Programmierer. Wenn ein Methoden Aufrufflag dieses Flag auf true festlegt, ist das Objekt konsistent. False gibt an, dass das Objekt inkonsistent ist. Com+ legt das-Flag auf "true" fest, wenn eine Objektinstanz erstellt wird. Ein konsistentes Objekt ist bereit, mit der Transaktion fortzufahren. Während ein Objekt aktiv bleibt, können nachfolgende Methodenaufrufe das konsistente Flag wiederholt von true auf false und umgekehrt wechseln.

Das done-Flag bestimmt die Dauer einer Transaktion. Wenn ein Methoden Rückruf zurückgegeben wird, prüft com+ das done-Flag. Wenn die Methode dieses Flag auf true festlegt, deaktiviert com+ das-Objekt und notiert das konsistente-Flag. Wenn das done-Flag false ist, deaktiviert com+ das Objekt weder und bemerkt auch das konsistente Flag. Com+ legt das done-Flag auf "false" fest, wenn eine Objektinstanz erstellt wird.

Das konsistente Flag wandelt eine Stimme ein, um das Commit auszuführen oder die Transaktion abzubrechen, in der es ausgeführt wird, und das done-Flag schließt die Stimme ab. Com+ prüft das konsistente Flag, wenn das done-Flag bei einem Methoden Rückruf auf true festgelegt ist oder wenn das Objekt deaktiviert wird. Obwohl sich das konsistente Flag eines Objekts innerhalb der einzelnen Methodenaufrufe wiederholt ändern kann, wird nur die letzte Änderung gezählt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwalten von automatischen Transaktionen in com+](managing-automatic-transactions-in-com-.md)
</dt> <dt>

[Festlegen der konsistenten und done-Flags](setting-the-consistent-and-done-flags.md)
</dt> </dl>

 

 



