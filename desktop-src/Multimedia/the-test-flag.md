---
title: Das Testflag
description: Das Testflag
ms.assetid: d103a96e-8d55-413d-ac84-15c3d8dccfbe
keywords:
- MCI_TEST-Flag
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 837b7812a904ed39fa0350d703b1525bbffa6f981b4736d25927840395932f32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117801475"
---
# <a name="the-test-flag"></a>Das Testflag

Das Flag "test" (MCI TEST) fragt das Gerät ab, um zu \_ ermitteln, ob es den Befehl ausführen kann. Das Gerät gibt einen Fehler zurück, wenn es den Befehl nicht ausführen kann. Es wird kein Fehler zurückgegeben, wenn der Befehl verarbeitet werden kann. Wenn Sie dieses Flag angeben, gibt MCI die Steuerung an die Anwendung zurück, ohne den Befehl auszuführen.

Dieses Flag wird von digital-video- und VCR-Geräten für alle Befehle unterstützt, mit Ausnahme von [**öffnen**](open.md) ([**MCI \_ OPEN**](mci-open.md)) und [**schließen**](close.md) ([**MCI \_ CLOSE**](mci-close.md)).

 

 




