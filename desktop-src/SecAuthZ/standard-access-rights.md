---
description: Jeder Typ von Sicherungs fähigen Objekten verfügt über einen Satz von Zugriffsrechten, die den für diesen Objekttyp spezifischen Vorgängen entsprechen.
ms.assetid: f43bccce-0f8c-4732-b678-5fd3218a9f84
title: Standard Zugriffsrechte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf28fb1ac86a60df373a9f747510b4df624a17eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863003"
---
# <a name="standard-access-rights"></a>Standard Zugriffsrechte

Jeder Typ von Sicherungs fähigen Objekten verfügt über einen Satz von Zugriffsrechten, die den für diesen Objekttyp spezifischen Vorgängen entsprechen. Zusätzlich zu diesen Objekt spezifischen Zugriffsrechten gibt es einen Satz von Standard Zugriffsrechten, die den meisten Typen von Sicherungs fähigen Objekten gemeinsam sind.

Das [Zugriffs Masken Format](access-mask-format.md) enthält einen Satz von Bits für die Standard Zugriffsrechte. Die folgenden Windows-Konstanten für Standard Zugriffsrechte werden in "Winnt. h" definiert.



| Konstante      | Bedeutung                                                                                                                                                                                                                                                                                                                                      |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Delete        | Das Recht, das Objekt zu löschen.                                                                                                                                                                                                                                                                                                              |
| Lese \_ Steuerelement | Das Recht, die Informationen in der [*Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly)des Objekts zu lesen, ohne die Informationen in der [*System-Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/s-gly) (SACL) einzubeziehen. |
| SYNCHRONIZE   | Das Recht, das Objekt für die Synchronisierung zu verwenden. Dadurch kann ein Thread warten, bis sich das Objekt im signalisierten Zustand befindet. Einige Objekttypen unterstützen dieses Zugriffsrecht nicht.                                                                                                                                                                |
| \_DAC schreiben    | Das Recht, die freigegebene [*Zugriffs Steuerungs Liste*](/windows/desktop/SecGloss/d-gly) (DACL) in der Sicherheits Beschreibung des Objekts zu ändern.                                                                                                                    |
| \_Besitzer schreiben  | Das Recht, in der Sicherheitsbeschreibung des Objekts den Besitzer zu ändern.                                                                                                                                                                                                                                                                           |



 

"Winnt. h" definiert auch die folgenden Kombinationen der standardmäßigen Zugriffsrechte Konstanten.



| Konstante                   | Bedeutung                                                                           |
|----------------------------|-----------------------------------------------------------------------------------|
| \_alle Standard Rechte \_      | Kombiniert Lösch-, Lese- \_ und Schreib Steuerung, Schreiben von \_ DAC, Schreiben von \_ Besitzern und Synchronisieren des Zugriffs. |
| Standard \_ Rechte \_ Ausführen  | Wird derzeit für das Read-Steuerelement definiert \_ .                                         |
| Standard \_ Rechte \_ Lesen     | Wird derzeit für das Read-Steuerelement definiert \_ .                                         |
| Standard \_ Rechte \_ erforderlich | Kombiniert Lösch-, Lese- \_ \_ und Schreibzugriff, DAC und Schreib \_ Zugriff.              |
| Standard \_ Rechte \_ Schreibvorgänge    | Wird derzeit für das Read-Steuerelement definiert \_ .                                         |



 

 

 
