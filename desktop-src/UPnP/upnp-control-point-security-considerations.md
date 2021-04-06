---
title: Überlegungen zur Steuerungspunkt Sicherheit
description: Wenn Sie einen Steuerungspunkt erstellen, müssen Sie die folgenden Sicherheitsprobleme berücksichtigen.
ms.assetid: 3281b4c3-d730-4273-9031-840a6ac655ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0165ad0c8a721b10d5cc34c49947a98f2c15d1de
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947930"
---
# <a name="control-point-security-considerations"></a>Überlegungen zur Steuerungspunkt Sicherheit

Wenn Sie einen Steuerungspunkt erstellen, müssen Sie die folgenden Sicherheitsprobleme berücksichtigen.

-   Alle Kontrollpunkt suchen werden standardmäßig mit einer Gültigkeitsdauer von 1 gesendet. Dies bedeutet, dass nur Geräte innerhalb desselben Subnetzes erkannt werden. Sie können eine höhere Gültigkeitsdauer in der Registrierung konfigurieren.
-   Das Gerät und die Dienst Beschreibung eines Geräts werden nur heruntergeladen, wenn es auf dem gleichen Gerät vorhanden ist, von dem die Geräte Ankündigung gesendet wurde.
-   Einem Gerät werden nur Steuerungs-und Abonnement Anforderungen gesendet, wenn sich seine Steuerungs-und Abonnement-URLs auf demselben Gerät befinden, von dem die Geräte Ankündigungen gesendet wurden.

 

 




