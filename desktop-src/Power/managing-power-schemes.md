---
description: Energieschemaverwaltung
ms.assetid: b79e7b64-be56-4165-af59-a8251284d029
title: Energieschemaverwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ab4717fd8efc91a520e178baac6ad9138028f306386ed2ee1141b76a423b16e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143403"
---
# <a name="power-scheme-management"></a>Energieschemaverwaltung

Jedes Energieschema wird durch eine **GUID** eindeutig identifiziert. Um alle verfügbaren Energieschemas aufzuzählen, verwenden Sie die [**PowerEnumerate-Funktion.**](/windows/desktop/api/PowrProf/nf-powrprof-powerenumerate) **PowerEnumerate** kann auch verwendet werden, um alle Energieeinstellungen für ein angegebenes Schema abzurufen.

Das Energieschema, das derzeit im System verwendet wird, wird als aktives Energiesparschema oder -plan bezeichnet. Rufen Sie die [**PowerGetActiveScheme-Funktion**](/windows/desktop/api/Powersetting/nf-powersetting-powergetactivescheme) auf, um die **GUID** des aktiven Plans abzurufen. Um den aktiven Energiesparplan zu ändern, rufen Sie die [**PowerSetActiveScheme-Funktion**](/windows/desktop/api/Powersetting/nf-powersetting-powersetactivescheme) auf.

Um ein Energieschema zu erstellen, müssen Sie zunächst ein vorhandenes Schema mithilfe der [**PowerDuplicateScheme-Funktion**](/windows/desktop/api/PowrProf/nf-powrprof-powerduplicatescheme) duplizieren und die **GUID** des Schemas angeben, auf dem Sie ihr neues Schema basieren möchten. Sie sollten eines der integrierten Schemas kopieren und die Energieeinstellungen an Ihre Anforderungen anpassen. Beachten Sie, dass beim Erstellen eines Energiesparplans der aktive Energiesparplan nicht automatisch aktualisiert wird. Sie müssen [**PowerSetActiveScheme**](/windows/desktop/api/Powersetting/nf-powersetting-powersetactivescheme) immer aufrufen, um den aktiven Energiesparplan zu aktualisieren. Vorhandene Energiesparpläne können auf die gleiche Weise geändert und dann angewendet werden.

Um einen Energiesparplan zu entfernen, rufen Sie die [**PowerDeleteScheme-Funktion**](/windows/desktop/api/PowrProf/nf-powrprof-powerdeletescheme) auf.

> [!Note]  
> Um zusätzliche Informationen zum Systembetriebszustand abzurufen, rufen Sie die [**CallNtPowerInformation-Funktion**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation) auf.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Energieschemas](power-schemes.md)
</dt> </dl>

 

 



