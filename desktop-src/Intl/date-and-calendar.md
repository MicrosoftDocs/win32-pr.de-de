---
description: Jedem Gebiets Schema ist ein Standard Kalendertyp (Datentyp "caltype") zugeordnet. Ein Gebiets Schema kann auch einen alternativen Kalendertyp aufweisen. Ausführliche Informationen zu Kalender Typen finden Sie unter Calendar Type-Informationen.
ms.assetid: 32772cba-eb30-4cd3-adaf-57fb8425a6d5
title: Datum und Kalender
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96a3c21965bfbf8c4215b478e5c3b4adbae579ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867936"
---
# <a name="date-and-calendar"></a>Datum und Kalender

Jedem [Gebiets](locales-and-languages.md) Schema ist ein Standard Kalendertyp (Datentyp "caltype") zugeordnet. Ein Gebiets Schema kann auch einen alternativen Kalendertyp aufweisen. Ausführliche Informationen zu Kalender Typen finden Sie unter [Calendar Type-Informationen](calendar-type-information.md).

> [!Note]  
> Um einen alternativen Kalendertyp für ein Gebiets Schema zu verwenden, muss die Anwendung das Gebiets Schema [ \_ ioptionalcalendar](locale-ioptionalcalendar.md) -Konstante auf den alternativen Kalendertyp für das Gebiets Schema festlegen.

 

Die meisten Gebiets Schemas verwenden den gregorianischen Standardkalender und eine festgelegte Anzahl von Datumsformaten. Diese Standardoptionen für Datumsformate können mithilfe der Funktion " [**enumdateformatsex**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa) " oder " [**enumdateformatsexex**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex) " angezeigt werden.

Bei einigen Gebiets Schemas müssen beim Erstellen einer kompletten Liste von Formatoptionen besondere Aspekte berücksichtigt werden. Für einige dieser Gebiets Schemas müssen Text Zeichenfolgen in die Datumsformat Zeichenfolge eingefügt werden, während andere eine völlig andere Berechnungsmethode für die Werte benötigen. Eine Anwendung adressiert diese speziellen Anforderungen durch das Hinzufügen bestimmter Gebiets Schema-Informationstypen und Kalender Typen.

Ausführliche Informationen zum Implementieren von Datumsangaben und Kalender in Ihren Anwendungen finden Sie unter [Abrufen von Zeit-und Datumsangaben](retrieving-time-and-date-information.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur Unterstützung der Landessprache](about-national-language-support.md)
</dt> <dt>

[Kalendertyp Informationen](calendar-type-information.md)
</dt> <dt>

[Abrufen von Zeit-und Datumsinformationen](retrieving-time-and-date-information.md)
</dt> <dt>

[**Enumdateformatsex**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa)
</dt> <dt>

[**Enumdateformatsexex**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex)
</dt> </dl>

 

 



