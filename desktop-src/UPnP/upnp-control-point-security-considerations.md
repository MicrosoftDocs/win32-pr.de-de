---
title: Sicherheitsüberlegungen für Kontrollpunkt
description: Wenn Sie einen Steuerungspunkt erstellen, müssen Sie die folgenden Sicherheitsprobleme berücksichtigen.
ms.assetid: 3281b4c3-d730-4273-9031-840a6ac655ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85378d7f530177bb42a6751a13f643bad984e994ae65178c0ab06cd5ce4792a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118126007"
---
# <a name="control-point-security-considerations"></a>Sicherheitsüberlegungen für Kontrollpunkt

Wenn Sie einen Steuerungspunkt erstellen, müssen Sie die folgenden Sicherheitsprobleme berücksichtigen.

-   Alle Suchvorgänge für Steuerungspunkt werden standardmäßig mit einer Tl von 1 gesendet. Dies bedeutet, dass nur Geräte innerhalb desselben Subnetzes gefunden werden. Sie können eine höhere Tl in der Registrierung konfigurieren.
-   Die Geräte- und Dienstbeschreibung eines Geräts wird nur heruntergeladen, wenn sie auf demselben Gerät vorhanden ist, das die Geräteankündigung gesendet hat.
-   Einem Gerät werden nur Steuerungs- und Abonnementanforderungen gesendet, wenn sich die Steuerungs- und Abonnement-URLs auf demselben Gerät befinden, das die Geräteankündigungen gesendet hat.

 

 




