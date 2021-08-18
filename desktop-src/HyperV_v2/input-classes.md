---
description: Die Benutzereingabegeräte werden durch diese Klassen dargestellt. Einem virtuellen Computer ist immer eine Instanz jeder Klasse zugeordnet.
ms.assetid: FFCA890D-6102-47BB-B499-4B9D77D75E9B
title: Eingabeklassen
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5df9c5a2f1d2743e062cf685dc6fd849f33333808315459560dfd840e925135
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118644862"
---
# <a name="input-classes"></a>Eingabeklassen

Die Benutzereingabegeräte werden durch diese Klassen dargestellt. Einem virtuellen Computer ist immer eine Instanz jeder Klasse zugeordnet. Diese Geräte können dem virtuellen Computer nicht hinzugefügt oder daraus entfernt werden. Daher gibt es keine Ressourcenpoolinstanzen für Tastatur- oder Mausgeräte.

Die Tastatur- und Mausgeräte werden über die [**Zuordnung Msvm \_ SystemDevice**](msvm-systemdevice.md) mit dem virtuellen Computer verknüpft. Ein virtueller Computer enthält sowohl ein PS2- als auch ein synthetisches Mausgerät. Es ist jeweils nur ein zeigendes Gerät aktiv.

Im Folgenden sind Virtualisierungs-WMI-Klassen im Zusammenhang mit Eingaben.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                          | Beschreibung                                     |
|----------------------------------------------------------------|-------------------------------------------------|
| [**\_Msvm-Tastatur**](msvm-keyboard.md)<br/>             | Stellt ein Tastaturgerät dar.<br/>        |
| [**Msvm \_ Ps2Mouse**](msvm-ps2mouse.md)<br/>             | Stellt ein PS2-Mausgerät dar.<br/>       |
| [**Msvm \_ SyntheticMouse**](msvm-syntheticmouse.md)<br/> | Stellt ein synthetisches Mausgerät dar.<br/> |



 

 

 




