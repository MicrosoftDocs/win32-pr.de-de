---
description: Konsistente und fertige Flags
ms.assetid: a641fa95-5587-4362-9869-e5c27c6dd2ce
title: Konsistente und fertige Flags
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 568b0c614c745f46d8bbcc816b65f501e02de1e0455f0b64216662ec52308213
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954360"
---
# <a name="consistent-and-done-flags"></a>Konsistente und fertige Flags

COM+ erstellt immer ein Kontextobjekt, bevor ein Transaktionsobjekt aktiviert wird. Das Kontextobjekt enthält objektbezogene Informationen, z. B. seinen Ersteller und seinen Transaktionsbezeichner. Jedes Kontextobjekt enthält auch ein *konsistentes Flag und* ein *done-Flag.* Zusammen bestimmen diese Flags den Status des Transaktionsobjekts.

Das Konsistente Flag gibt an, dass das Transaktionsobjekt entweder konsistent oder inkonsistent ist. Die spezifischen Details dazu, was den Zustand eines Objekts konsistent macht, sind aufgabe des Programmierers. Wenn ein Methodenaufruf dieses Flag auf True setzt, ist das Objekt konsistent. False gibt an, dass das Objekt inkonsistent ist. COM+ legt das Flag auf True fest, wenn eine Objektinstanz erstellt wird. Ein konsistentes Objekt ist bereit, mit der Transaktion fortzufahren. Während ein Objekt aktiv bleibt, können nachfolgende Methodenaufrufe das konsistente Flag wiederholt von True in False ändern und umgekehrt.

Das Done-Flag bestimmt die Dauer einer Transaktion. Wenn ein Methodenaufruf zurückgegeben wird, überprüft COM+ das Flag done. Wenn die -Methode dieses Flag auf True setzt, deaktiviert COM+ das -Objekt und notiert das konsistente Flag. Wenn das flag done auf False festgelegt ist, deaktiviert COM+ weder das Objekt noch notiert das konsistente Flag. COM+ legt das Done-Flag auf False fest, wenn eine Objektinstanz erstellt wird.

Das flag consistent gibt eine Stimme zum Ausführen oder Abbrechen der Transaktion um, in der es ausgeführt wird, und das Flag done finalisiert die Abstimmung. COM+ überprüft das konsistente Flag, wenn das Flag done bei einer Methodenaufruf-Rückgabe auf TRUE festgelegt ist oder wenn das Objekt deaktiviert wird. Obwohl das konsistente Flag eines Objekts innerhalb jedes Methodenaufrufs wiederholt geändert werden kann, zählt nur die letzte Änderung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwalten automatischer Transaktionen in COM+](managing-automatic-transactions-in-com-.md)
</dt> <dt>

[Festlegen der Flags "Konsistent" und "Fertig"](setting-the-consistent-and-done-flags.md)
</dt> </dl>

 

 



