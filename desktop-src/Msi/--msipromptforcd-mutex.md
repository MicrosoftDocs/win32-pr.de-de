---
description: '\_ \_ MsiPromptForCD Mutex ist vorhanden, wenn der Benutzer vom Installationsprogramm zum Einfügen einer CD-ROM aufgefordert wird.'
ms.assetid: f6319cda-48ac-4351-8eb5-f326490e3aff
title: __MsiPromptForCD Mutex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba2c829cb0102192b4c2bc2670892f8849000a6ed9cad2a88e7f3e3e557b259
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764290"
---
# <a name="__msipromptforcd-mutex"></a>\_\_MsiPromptForCD Mutex

\_ \_ MsiPromptForCD Mutex ist vorhanden, wenn der Benutzer vom Installationsprogramm zum Einfügen einer CD-ROM aufgefordert wird. Automatische Wiedergabeprogramme sollten vor dem Start überprüfen, ob der \_ \_ MsiPromptForCD-Mutex derzeit nicht festgelegt ist. Beachten Sie, dass es möglich ist, dass eine CD-ROM-Eingabeaufforderung auftritt, bevor entweder der InProgress-Schlüssel oder \_ MSIExecute Mutex vorhanden ist.

 

 



