---
description: Energie Schema Verwaltung
ms.assetid: b79e7b64-be56-4165-af59-a8251284d029
title: Energie Schema Verwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 867d7509e9a04e948818ff7a3a13638a5c9933b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353458"
---
# <a name="power-scheme-management"></a>Energie Schema Verwaltung

Jedes Energie Schema wird durch eine **GUID** eindeutig identifiziert. Verwenden Sie zum Auflisten aller verfügbaren Energie Schemas die [**powerenumerate**](/windows/desktop/api/PowrProf/nf-powrprof-powerenumerate) -Funktion. **Powerenumerate** kann auch verwendet werden, um alle Energie Einstellungen für ein angegebenes Schema abzurufen.

Das Energie Schema, das zurzeit auf dem System verwendet wird, wird als aktives Energie Schema oder Plan bezeichnet. Um die **GUID** des aktiven Plans abzurufen, rufen Sie die [**powergetactivescheme**](/windows/desktop/api/Powersetting/nf-powersetting-powergetactivescheme) -Funktion auf. Um den aktiven Energie Sparplan zu ändern, müssen Sie die Funktion " [**powersettactivescheme**](/windows/desktop/api/Powersetting/nf-powersetting-powersetactivescheme) " aufzurufen.

Um ein Energie Schema zu erstellen, müssen Sie zuerst ein vorhandenes Schema duplizieren, indem Sie die [**powerduplicatescheme**](/windows/desktop/api/PowrProf/nf-powrprof-powerduplicatescheme) -Funktion verwenden und die **GUID** des Schemas angeben, auf dem das neue Schema basieren soll. Sie sollten eines der integrierten Schemas kopieren und die Energie Einstellungen entsprechend Ihren Anforderungen ändern. Beachten Sie, dass durch das Erstellen eines Energie Sparplans der aktive Energie Sparplan nicht automatisch aktualisiert wird. Zum Aktualisieren des aktiven Energie Sparplans müssen Sie immer [**Power-tactivescheme**](/windows/desktop/api/Powersetting/nf-powersetting-powersetactivescheme) aufzurufen. Vorhandene Energie Sparpläne können geändert und dann auf die gleiche Weise angewendet werden.

Um einen Energie Sparplan zu entfernen, müssen Sie die [**powerdeletescheme**](/windows/desktop/api/PowrProf/nf-powrprof-powerdeletescheme) -Funktion aufrufen.

> [!Note]  
> Rufen Sie die [**callntpowerinformation**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation) -Funktion auf, um zusätzliche Informationen zum Energiezustand des Systems abzurufen.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Energie Schemas](power-schemes.md)
</dt> </dl>

 

 



