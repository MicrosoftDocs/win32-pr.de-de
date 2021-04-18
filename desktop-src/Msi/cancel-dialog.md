---
description: Das Dialogfeld Abbrechen bestätigt, dass der Benutzer die Installation beenden möchte. Dies ist ein modales Dialogfeld.
ms.assetid: 5dab4315-721e-417d-91e0-b38653a65c23
title: Dialog Feld Abbrechen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1022a7613f3f5341d8c833b7cbe2645ce871aeb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357520"
---
# <a name="cancel-dialog"></a>Dialog Feld Abbrechen

Das Dialogfeld **Abbrechen** bestätigt, dass der Benutzer die Installation beenden möchte. Dies ist ein modales Dialogfeld.

Diese Art von Dialogfeld enthält im Allgemeinen ein [Text Steuer](text-control.md) Element und zwei [Pushbuttons](pushbutton-control.md). Die beiden Schaltflächen geben dem Benutzer die Möglichkeit, entweder zum letzten Dialogfeld zurückzukehren oder die Beendigung der Installation zu bestätigen.

Das [EndDialog](enddialog-controlevent.md) -ControlEvent ist mit diesen beiden Schaltflächen in der [ControlEvent-Tabelle](controlevent-table.md)verknüpft. Der *Rückgabe* Parameter des EndDialog-ControlEvent ist mit einer der Schaltflächen verknüpft und bewirkt, dass das Dialogfeld **Abbrechen** beendet wird und der Fokus auf das vorherige Dialogfeld zurückkehrt. Der *Exit* -Parameter ist mit der anderen Schaltfläche verknüpft und bewirkt, dass die Benutzeroberfläche die Steuerung an das Installationsprogramm zurückgibt, wobei der entsprechende Code angibt, dass der Benutzer den Vorgang beenden möchte Der Installer wird dann heruntergefahren und zeigt das [Userexit-Dialog](userexit-dialog.md)Feld an.

 

 



