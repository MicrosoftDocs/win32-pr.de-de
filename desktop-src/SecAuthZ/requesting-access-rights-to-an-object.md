---
description: Wenn Sie ein Handle für ein Objekt öffnen, verfügt das zurückgegebene Handle über eine Kombination von Zugriffsrechten für das Objekt.
ms.assetid: 581de4ba-0f90-42d7-b7db-1324d42595e2
title: Anfordern von Zugriffsrechten für ein Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a168a5c9aa97d95acb13cb1cfeb3e776ea1e7ae6e2e090df5c8395a4b61fabea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907540"
---
# <a name="requesting-access-rights-to-an-object"></a>Anfordern von Zugriffsrechten für ein Objekt

Wenn Sie ein Handle für ein Objekt öffnen, verfügt das zurückgegebene Handle über eine Kombination von Zugriffsrechten für das Objekt. Einige Funktionen wie [**CreateSemaphore**](/windows/desktop/api/winbase/nf-winbase-createsemaphorea)erfordern keinen bestimmten Satz angeforderter Zugriffsrechte. Diese Funktionen versuchen immer, das Handle für Vollzugriff zu öffnen. Mit anderen Funktionen, z. B. [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) und [**OpenProcess,**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess)können Sie den satz von Zugriffsrechten angeben, den Sie wünschen. Sie sollten nur die benötigten Zugriffsrechte anfordern, anstatt ein Handle für Vollzugriff zu öffnen. Dies verhindert die unbeabsichtigte Verwendung des Handles und erhöht die Wahrscheinlichkeit, dass die Zugriffsanforderung erfolgreich ist, wenn die DACL des Objekts nur eingeschränkten Zugriff zulässt.

Verwenden [Sie generische Zugriffsrechte,](generic-access-rights.md) um den Zugriffstyp anzugeben, der beim Öffnen eines Handles für ein Objekt erforderlich ist. Dies ist in der Regel einfacher als die Angabe aller entsprechenden Standard- und spezifischen Rechte. Alternativ können Sie die Konstante MAXIMUM ALLOWED verwenden, um an fordern, dass das Objekt mit allen Zugriffsrechten geöffnet wird, die \_ für den Aufrufer gültig sind.

> [!Note]  
> Die MAXIMUM \_ ALLOWED-Konstante kann nicht in einem ACE verwendet werden.

 

Um die SACL in der Sicherheitsbeschreibung eines Objekts zu erhalten oder zu [*festlegen,*](/windows/desktop/SecGloss/s-gly)fordern Sie das [Zugriffsrecht ACCESS \_ SYSTEM \_ SECURITY](sacl-access-right.md) an, wenn Sie ein Handle für das Objekt öffnen.

 

 
