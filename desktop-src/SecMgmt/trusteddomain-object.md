---
description: Das Objekt "trustddomain" speichert Informationen zu einer Vertrauensstellung mit einer Domäne.
ms.assetid: fab69367-2143-49ef-a1b9-9c1d846fd4e1
title: Treuhänder-Domänen Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 837d8a9e56273a87b22b9697ef4e5917d73bcc81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862296"
---
# <a name="trusteddomain-object"></a>Treuhänder-Domänen Objekt

Das Objekt " **trustddomain** " speichert Informationen zu einer Vertrauensstellung mit einer Domäne. Auf dem vertrauenden System wird ein Vertrauensstellungs **Domänen** Objekt erstellt, mit dem ein Konto innerhalb der vertrauenswürdigen Domäne identifiziert wird, das zum Senden von Authentifizierungsanforderungen und zum Ausführen anderer Vorgänge, wie z. b. Name und [*Sicherheits*](/windows/desktop/SecGloss/s-gly) -ID (SID), verwendet werden kann.

Zu den in einem " **Treuhänder Domain** "-Objekt gespeicherten Informationen gehören:

-   Die SID der vertrauenswürdigen Domäne. Diese Informationen können nicht geändert werden und müssen in allen " **Treuhänder Domain** "-Objekten eindeutig sein.
-   Der Name der vertrauenswürdigen Domäne. Diese Informationen können nicht geändert werden und müssen in allen " **Treuhänder Domain** "-Objekten eindeutig sein.
-   Der Name des Kontos in der vertrauenswürdigen Domäne, das zum Senden von Authentifizierungsanforderungen und zum Ausführen von Namen-und sid-Übersetzungen verwendet wird. Dieser Name kann nicht geändert werden.
-   Das Kennwort, mit dem Authentifizierungsanforderungen gesendet und Namens-und sid-Übersetzungen durchgeführt werden

Weitere Informationen finden Sie [unter dem Objekttyp "Treuhänder Domäne](the-trusteddomain-object-type.md)".

 

 
