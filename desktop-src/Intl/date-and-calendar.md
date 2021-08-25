---
description: Jedem Gebietsschema ist ein Standardkalendertyp (Datentyp CALTYPE) zugeordnet. Ein Gebietsschema kann auch einen alternativen Kalendertyp aufweisen. Ausführliche Informationen zu Kalendertypen finden Sie unter Kalendertypinformationen.
ms.assetid: 32772cba-eb30-4cd3-adaf-57fb8425a6d5
title: Datum und Kalender
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a3f200ccd60a5a5d121a8774c01808794e744b98d8611210fcc98b0f8e5e1f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822810"
---
# <a name="date-and-calendar"></a>Datum und Kalender

Jedem [Gebietsschema](locales-and-languages.md) ist ein Standardkalendertyp (Datentyp CALTYPE) zugeordnet. Ein Gebietsschema kann auch einen alternativen Kalendertyp aufweisen. Ausführliche Informationen zu Kalendertypen finden Sie unter [Kalendertypinformationen.](calendar-type-information.md)

> [!Note]  
> Um einen alternativen Kalendertyp für ein Gebietsschema zu verwenden, muss Ihre Anwendung die [LOCALE \_ IOPTIONALCALENDAR-Konstante](locale-ioptionalcalendar.md) auf den alternativen Kalendertyp für das Gebietsschema festlegen.

 

Die meisten Gebietsschemas verwenden den gregorianischen Standardkalender und eine festgelegte Anzahl von Datumsformaten. Diese Standardoptionen für Datumsformate können mithilfe der [**EnumDateFormatsEx-**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa) oder [**EnumDateFormatsEx-Funktion**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex) angezeigt werden.

Einige Gebietsschemas erfordern besondere Überlegungen beim Erstellen einer vollständigen Liste von Formatoptionen. Einige dieser Gebietsschemas erfordern, dass Textzeichenfolgen in die Datumsformatzeichenfolge eingefügt werden, während andere eine völlig andere Methode zur Berechnung der Werte erfordern. Eine Anwendung erfüllt diese speziellen Anforderungen durch hinzufügen bestimmter Gebietsschemainformationstypen und Kalendertypen.

Ausführliche Informationen zum Implementieren von Datumsangaben und Kalendern in Ihren Anwendungen finden Sie unter [Abrufen von Uhrzeit- und Datumsinformationen.](retrieving-time-and-date-information.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur Unterstützung der nationalen Sprache](about-national-language-support.md)
</dt> <dt>

[Kalendertypinformationen](calendar-type-information.md)
</dt> <dt>

[Abrufen von Uhrzeit- und Datumsinformationen](retrieving-time-and-date-information.md)
</dt> <dt>

[**EnumDateFormatsEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa)
</dt> <dt>

[**EnumDateFormatsExEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex)
</dt> </dl>

 

 



