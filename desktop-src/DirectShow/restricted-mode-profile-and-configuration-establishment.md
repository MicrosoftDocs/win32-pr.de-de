---
description: Eingeschränktes Modusprofil und Einrichtung der Konfiguration
ms.assetid: 550f5413-eaa4-4530-867e-fd9b1907cadf
title: Eingeschränktes Modusprofil und Einrichtung der Konfiguration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9bb4d4bea3f42eaf897e781ccf859d094a0d0321815e7457aa6c79f96cb5ded
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747050"
---
# <a name="restricted-mode-profile-and-configuration-establishment"></a>Eingeschränktes Modusprofil und Einrichtung der Konfiguration

Aufgrund der Vielzahl von Datentypen, die von DirectX VA decodiert werden können, und der in DirectX VA für jeden dieser Datentypen unterstützten Decodierungskonfigurationen (z. B. die Verwendung von Bitstreampuffern im Vergleich zur Host-Restdifferenzdecodierung im Vergleich zur zugriffsbasierten IDCT mit und ohne Verschlüsselung der einzelnen relevanten Puffertypen und so weiter),  Wir sind der Meinung, dass es etwas unvoreinig wäre, einfach eine eindeutige GUID für jeden eindeutigen Datentyp und jede Decodierungskonfiguration anzugeben. Dies würde eine große Anzahl von GUIDs erstellen (wenn beispielsweise hypothetisch 16 Profile mit DirectX VA- und 16 Konfigurationen möglich wären, müssten 256 guiDs definiert sein, was 4 Kilobyte Arbeitsspeicher erfordert, um sie alle zu speichern). Dieses Problem ist der schwierigste Teil der Entscheidung, wie DirectX VA **IAMVideoAccelerator** zuordnen soll. Der Rest der Betriebsdefinition ist größtenteils recht einfach. Daher geben wir eine eindeutige GUID nur für jeden Datentyp (für jedes Profil im eingeschränkten Modus) an und lassen zu, dass jedem Verschlüsselungstyp eine zusätzliche GUID zugeordnet wird. Die Decodierungskonfiguration wird dann zwischen decoder und accelerator durch eine untergeordnete Aushandlung auf niedrigerer Ebene mithilfe von Such- und Sperrvorgängen eingerichtet, um Konfigurationen für jeden Typ von DirectX VA-Funktion zu erstellen.

 

 



