---
description: Die LSA speichert Informationen zu lokalen Sicherheitsrichtlinien in einem Satz von Objekten. Die Anwendung kann die lokale Sicherheitsrichtlinie Abfragen oder bearbeiten, indem Sie auf diese Objekte zugreift.
ms.assetid: c8ed5cd8-55cf-43e7-92a3-9bd17a1147a9
title: LSA-Richtlinien Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1481b6a6f49e973ecc2a2e1b53830bf22c67a77f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959861"
---
# <a name="lsa-policy-objects"></a>LSA-Richtlinien Objekte

Die LSA speichert Informationen zu lokalen Sicherheitsrichtlinien in einem Satz von Objekten. Die Anwendung kann die lokale Sicherheitsrichtlinie Abfragen oder bearbeiten, indem Sie auf diese Objekte zugreift.

Der Satz besteht aus den folgenden vier Objekten:

-   Die [Richtlinie](policy-object.md) enthält Informationen zur globalen Richtlinie.
-   " [Treuhänder Domäne](trusteddomain-object.md) " enthält Informationen zu einer vertrauenswürdigen Domäne.
-   Das [Konto](account-object.md) enthält Informationen zu einem Benutzer-, Gruppen-oder lokalen Gruppenkonto.
-   [Private Daten](private-data-object.md) enthalten geschützte Informationen, wie z. b. Server Konto Kennwörter. Diese Informationen werden als verschlüsselte Zeichen folgen gespeichert.

Weitere Informationen zur Verwendung der LSA-Richtlinien Funktionen zum Verwalten der in diesen Objekten gespeicherten Informationen finden [Sie unter Verwenden der LSA-Richtlinie](using-lsa-policy.md).

 

 



