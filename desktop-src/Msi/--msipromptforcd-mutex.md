---
description: Der \_ \_ msipromptforcd Mutex ist vorhanden, wenn der Benutzer vom Installationsprogramm zum Einfügen einer CD-ROM aufgefordert wird.
ms.assetid: f6319cda-48ac-4351-8eb5-f326490e3aff
title: __MsiPromptForCD Mutex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e646b23a003d10cce29807297e56abaebf3d935
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362429"
---
# <a name="__msipromptforcd-mutex"></a>\_\_Msipromptforcd Mutex

Der \_ \_ msipromptforcd Mutex ist vorhanden, wenn der Benutzer vom Installationsprogramm zum Einfügen einer CD-ROM aufgefordert wird. Das AutoPlay-Programm sollte überprüfen, ob der \_ \_ msipromptforcd-Mutex derzeit nicht festgelegt ist. Beachten Sie, dass es möglich ist, dass eine CD-ROM-Eingabeaufforderung vorliegt, bevor der InProgress-Schlüssel oder der \_ msiexecute-Mutex vorhanden ist.

 

 



