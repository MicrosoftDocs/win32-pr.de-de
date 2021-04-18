---
description: Definiert ein mobiles Breitband Profil.
ms.assetid: bfec0a1d-de17-4ebd-b9fb-570e230da317
title: Schema Referenz für mobile Breitband profile
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 425db1d38002e40969bb47c03952330dd6ccd26d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347787"
---
# <a name="mobile-broadband-profile-schema-reference"></a>Schema Referenz für mobile Breitband profile

Das mobile Breitband Profil Schema definiert ein mobiles Breitband Profil.

Profile speichern Benutzer-und Netzwerk Konfigurationsparameter für mobile Breitbandverbindungen. Außerdem werden die Benutzereinstellungen für eine Verbindung gespeichert.

Das Stamm Element eines mobilen Breitband Profils ist das [**mbnprofile**](schema-mbnprofile-element.md) -Element. Jedes Profil weist genau ein Stamm Element auf. Alle von Windows 7 verwendeten Schema Elemente für das mobile Breitband Profil befinden sich im-Namespace, `https://www.microsoft.com/networking/WWAN/profile/v1` und die von Windows 8 verwendeten Elemente befinden sich im-Namespace `https://www.microsoft.com/networking/WWAN/profile/v2` .

Das mobile Breitband Profil Schema erzwingt strikt die Reihenfolge der Knoten. Die in einem Profil angegebenen Knoten müssen dem **mobilen Breitband Profil Schema** entsprechen und in der in der Schema Definition vorgeschriebenen Reihenfolge angezeigt werden. Beispielsweise muss [**userlogonkred**](schema-userlogoncred-contexttype-element.md) unmittelbar nach [**accessstring**](schema-accessstring-contexttype-element.md)angegeben werden.

-   [Mobiles Breitband Profil Schema v1](mobile-broadband-profile-schema.md)
-   [Mobiles Breitband Profil Schema v2](mobile-broadband-profile-schema-v2.md)
-   [Mobiles Breitband Profil Schema v3](mobile-broadband-profile-schema-v3.md)
-   [Mobiles Breitband Profil Schema v4](/previous-versions/windows/desktop/legacy/mt243438(v=vs.85))

 

 
