---
title: Windows-Ereignisprotokoll
description: Die Windows-Ereignisprotokoll-API definiert das Schema, das Sie zum Schreiben eines Instrumentierungs Manifests verwenden.
ms.assetid: 738c8afa-4714-4d4f-9231-b8fbdb5159c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9df51efc878af2770ad056e6e1f84b8f4f2566
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858461"
---
# <a name="windows-event-log"></a>Windows-Ereignisprotokoll

## <a name="purpose"></a>Zweck

Die Windows-Ereignisprotokoll-API definiert das Schema, das Sie zum Schreiben eines Instrumentierungs Manifests verwenden. Ein Instrumentations Manifest identifiziert den Ereignis Anbieter und die Ereignisse, die er protokolliert. Die API enthält auch die Funktionen, die ein Ereignisconsumer, z. b. die [Ereignisanzeige](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc766042(v=ws.11)), zum Lesen und Rendering der Ereignisse verwenden würde. Um die im Manifest definierten Ereignisse zu schreiben, verwenden Sie die Funktionen der API für die [Ereignis Ablauf Verfolgung](/windows/desktop/ETW/event-tracing-portal) (ETW).

Das Windows-Ereignisprotokoll ersetzt die [Ereignisprotokollierungs](/windows/desktop/EventLog/event-logging) -API, beginnend mit dem Betriebssystem Windows Vista.

## <a name="developer-audience"></a>Entwicklergruppe

Das Windows-Ereignisprotokoll ist für C/C++-Programmierer konzipiert.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Das Windows-Ereignisprotokoll ist ab Windows Vista und Windows Server 2008 im Betriebssystem enthalten.

Informationen zu den Lauf Zeitanforderungen für ein bestimmtes Programmier Element finden Sie im Abschnitt "Anforderungen" der Referenzseite für dieses Element.

Den vollständigen Versionsverlauf finden Sie unter [Neuerungen](what-s-new.md).

## <a name="in-this-section"></a>In diesem Abschnitt


| Thema                                                        | BESCHREIBUNG                                                                                       |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [Verwenden des Windows-Ereignis Protokolls](using-windows-event-log.md)        | Verfahrens Leit Faden, in dem die Verwendung der Windows-Ereignisprotokoll-API veranschaulicht wird.                                 |
| [Referenz zum Windows-Ereignisprotokoll](windows-event-log-reference.md)| Die Datentypen, Funktionen, Enumerationen, Strukturen, Konstanten und Schemas, die die API enthält.|