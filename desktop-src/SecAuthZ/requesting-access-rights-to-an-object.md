---
description: Wenn Sie ein Handle für ein Objekt öffnen, verfügt das zurückgegebene Handle über eine bestimmte Kombination von Zugriffsrechten für das Objekt.
ms.assetid: 581de4ba-0f90-42d7-b7db-1324d42595e2
title: Anfordern von Zugriffsrechten für ein Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eb2e13bd5f5e51ed194b60c6ab63d1eda8eddfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360086"
---
# <a name="requesting-access-rights-to-an-object"></a>Anfordern von Zugriffsrechten für ein Objekt

Wenn Sie ein Handle für ein Objekt öffnen, verfügt das zurückgegebene Handle über eine bestimmte Kombination von Zugriffsrechten für das Objekt. Einige Funktionen, wie z. b. " [**kreatesemaphore**](/windows/desktop/api/winbase/nf-winbase-createsemaphorea)", benötigen keinen bestimmten Satz angeforderter Zugriffsrechte. Diese Funktionen versuchen immer, das Handle für den Vollzugriff zu öffnen. Andere Funktionen, wie z. b. " [**kreatefile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) " und " [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess)", ermöglichen es Ihnen, den gewünschten Satz von Zugriffsrechten anzugeben. Sie sollten nur die benötigten Zugriffsrechte anfordern, anstatt ein Handle für den Vollzugriff zu öffnen. Dadurch wird verhindert, dass das Handle unbeabsichtigt verwendet wird, und erhöht die Wahrscheinlichkeit, dass die Zugriffs Anforderung erfolgreich ist, wenn die DACL des Objekts nur eingeschränkten Zugriff zulässt.

Verwenden Sie [generische Zugriffsrechte](generic-access-rights.md) , um den Zugriffstyp anzugeben, der beim Öffnen eines Handles für ein Objekt erforderlich ist. Dies ist in der Regel einfacher, als alle entsprechenden Standard-und spezifischen Rechte anzugeben. Verwenden Sie alternativ die maximal \_ zulässige Konstante, um anzufordern, dass das Objekt mit allen Zugriffsrechten geöffnet wird, die für den Aufrufer gültig sind.

> [!Note]  
> Die maximal \_ zulässige Konstante kann nicht in einem ACE verwendet werden.

 

Um die SACL in der [*Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly)eines Objekts zu erhalten oder festzulegen, fordern Sie beim Öffnen eines Handles für das Objekt das [Zugriffs \_ System- \_ Sicherheits Zugriffsrecht](sacl-access-right.md) an.

 

 
