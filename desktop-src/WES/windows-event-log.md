---
title: Windows-Ereignisprotokoll
description: Die Windows-Ereignisprotokoll-API definiert das Schema, das Sie zum Schreiben eines Instrumentierungsmanifests verwenden.
ms.assetid: 738c8afa-4714-4d4f-9231-b8fbdb5159c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c4306ce9722aba5b06109265c71cf387af2b35f63aef1cec070936400fff61f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118587195"
---
# <a name="windows-event-log"></a>Windows-Ereignisprotokoll

## <a name="purpose"></a>Zweck

Die Windows-Ereignisprotokoll-API definiert das Schema, das Sie zum Schreiben eines Instrumentierungsmanifests verwenden. Ein Instrumentierungsmanifest identifiziert Ihren Ereignisanbieter und die von ihm protokollierten Ereignisse. Die API enthält auch die Funktionen, die ein Ereignisverbraucher, z. B. der Ereignisanzeige [,](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc766042(v=ws.11))zum Lesen und Rendern der Ereignisse verwenden würde. Um die im Manifest definierten Ereignisse zu schreiben, verwenden Sie die Funktionen, die in der ETW-API [(Event Tracing)](/windows/desktop/ETW/event-tracing-portal) enthalten sind.

Windows Das Ereignisprotokoll ersetzt [](/windows/desktop/EventLog/event-logging) die Ereignisprotokollierungs-API, die mit dem Windows Vista-Betriebssystem beginnt.

## <a name="developer-audience"></a>Entwicklergruppe

Windows Das Ereignisprotokoll ist für C/C++-Programmierer konzipiert.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Windows Das Ereignisprotokoll ist ab Windows Vista und Windows Server 2008 im Betriebssystem enthalten.

Informationen zu Laufzeitanforderungen für ein bestimmtes Programmierelement finden Sie im Abschnitt Anforderungen der Referenzseite für dieses Element.

Den vollständigen Versionsverlauf finden Sie [unter Neues.](what-s-new.md)

## <a name="in-this-section"></a>In diesem Abschnitt


| Thema                                                        | BESCHREIBUNG                                                                                       |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [Verwenden Windows Ereignisprotokolls](using-windows-event-log.md)        | Anleitung zur Verwendung der Ereignisprotokoll-API Windows- und Ereignisprotokoll-API                                 |
| [Windows Ereignisprotokollreferenz](windows-event-log-reference.md)| Die Datentypen, Funktionen, Enumerationen, Strukturen, Konstanten und Schemas, die die API enthält.|