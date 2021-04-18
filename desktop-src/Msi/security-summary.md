---
description: Die Sicherheits Zusammenfassungs Eigenschaft gibt an, ob das Paket schreibgeschützt geöffnet werden soll.
ms.assetid: f064b899-8123-49e1-b275-511186f49750
title: Sicherheits Zusammenfassungs Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 997f75e388d504afd1d62f1ae2813943807910d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371714"
---
# <a name="security-summary-property"></a>Sicherheits Zusammenfassungs Eigenschaft

Die **Sicherheits Zusammenfassungs** Eigenschaft gibt an, ob das Paket schreibgeschützt geöffnet werden soll. Das Tool zum Bearbeiten von Datenbanken sollte eine schreibgeschützte erzwungene Datenbank nicht ändern und sollte bei versuchen, eine schreibgeschützte Datenbank zu ändern, eine Warnung ausgeben. Die folgenden Werte dieser Eigenschaft sind auf Windows Installer Dateien anwendbar.



| Wert | BESCHREIBUNG           |
|-------|-----------------------|
| 0     | Keine Einschränkung        |
| 2     | Nur Lesen empfohlen |
| 4     | Schreibgeschützt erzwungen    |



 

Diese Eigenschaft sollte auf Read-Only empfohlen (2) für eine-Installations Datenbank und auf Schreib geschütztes erzwingen (4) für eine Transformation oder einen Patch festgelegt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Beschreibungen der Zusammenfassungs Eigenschaften](summary-property-descriptions.md)
</dt> </dl>

 

 




