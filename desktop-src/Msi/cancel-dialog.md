---
description: Im Dialogfeld Abbrechen wird bestätigt, dass der Benutzer die Installation beenden möchte. Dies ist ein modales Dialogfeld.
ms.assetid: 5dab4315-721e-417d-91e0-b38653a65c23
title: Dialogfeld "Abbrechen"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ac2f0ba12c442b8b0f4445077497c26649b79714d1a1d77af7b2a82e6c1a3f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105390"
---
# <a name="cancel-dialog"></a>Dialogfeld "Abbrechen"

Im **Dialogfeld** Abbrechen wird bestätigt, dass der Benutzer die Installation beenden möchte. Dies ist ein modales Dialogfeld.

Diese Art von Dialogfeld enthält in der Regel ein [Text-Steuerelement und](text-control.md) zwei [PushButtons.](pushbutton-control.md) Mit den beiden Schaltflächen kann der Benutzer entweder zum letzten Dialogfeld zurückkehren oder die Beendigung der Installation bestätigen.

Das [EndDialog](enddialog-controlevent.md) ControlEvent ist mit diesen beiden Schaltflächen in der [ControlEvent-Tabelle verknüpft.](controlevent-table.md) Der *Return-Parameter* von EndDialog ControlEvent ist mit einer  der Schaltflächen verknüpft und bewirkt, dass das Dialogfeld Abbrechen beendet wird und der Fokus zum vorherigen Dialogfeld zurückgibt. Der *Exit-Parameter* ist mit der anderen Schaltfläche verknüpft und bewirkt, dass die Benutzeroberfläche die Steuerung an das Installationsprogramm mit dem entsprechenden Code zurückgibt, der angibt, dass der Benutzer beenden möchte. Das Installationsprogramm wird dann heruntergefahren und zeigt das [UserExit-Dialogfeld an.](userexit-dialog.md)

 

 



