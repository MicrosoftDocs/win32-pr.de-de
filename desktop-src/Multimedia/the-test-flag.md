---
title: Das TESTFLAG
description: Das TESTFLAG
ms.assetid: d103a96e-8d55-413d-ac84-15c3d8dccfbe
keywords:
- MCI_TEST-Flag
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a36cddaa186a9be260cf87b7a323a6e05ed9fc4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311424"
---
# <a name="the-test-flag"></a>Das TESTFLAG

Mit dem Flag "Test" (MCI- \_ Test) wird das Gerät abgefragt, um zu bestimmen, ob der Befehl ausgeführt werden kann. Das Gerät gibt einen Fehler zurück, wenn der Befehl nicht ausgeführt werden kann. Wenn der Befehl behandelt werden kann, wird kein Fehler zurückgegeben. Wenn Sie dieses Flag angeben, gibt MCI die Steuerung an die Anwendung zurück, ohne den Befehl auszuführen.

Dieses Flag wird von Digital-Video-und VCR-Geräten für alle Befehle mit Ausnahme von [**Open**](open.md) ([**MCI \_ Open**](mci-open.md)) und [**Close**](close.md) ([**MCI \_ Close**](mci-close.md)) unterstützt.

 

 




