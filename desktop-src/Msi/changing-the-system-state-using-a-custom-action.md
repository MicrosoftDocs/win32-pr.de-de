---
description: Benutzerdefinierte Aktionen, die den Systemstatus ändern sollen, müssen benutzerdefinierte Aktionen verzögert ausführen.
ms.assetid: 48707ae1-9488-4bbb-8447-b24e383affb7
title: Ändern des Systemstatus mithilfe einer benutzerdefinierten Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f3ec2fafdc6f57041c087903da0c912327c967b3b188127ee1f2ff71db7c1af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086240"
---
# <a name="changing-the-system-state-using-a-custom-action"></a>Ändern des Systemstatus mithilfe einer benutzerdefinierten Aktion

Benutzerdefinierte Aktionen, die den Systemstatus ändern sollen, müssen benutzerdefinierte Aktionen verzögert ausführen. Benutzerdefinierte Aktionen, die Eigenschaften, Featurezustände, Komponentenzustände oder Zielverzeichnisse festlegen oder Systemvorgänge durch Einfügen von Zeilen in Sequenztabellen planen, können die sofortige Ausführung sicher verwenden. Benutzerdefinierte Aktionen, die das System direkt ändern oder einen anderen Systemdienst aufrufen, müssen jedoch auf den Zeitpunkt zurückgestellt werden, zu dem das Installationsskript ausgeführt wird. Weitere Informationen finden Sie unter Benutzerdefinierte Aktionen für [verzögerte Ausführung.](deferred-execution-custom-actions.md)

Sie sollten nicht versuchen, eine benutzerdefinierte Aktion zur sofortigen Ausführung zu verwenden, um den Systemstatus zu ändern, da jede benutzerdefinierte Aktion, die den Zustand ändert, über eine entsprechende benutzerdefinierte Rollbackaktion verfügen muss, um die Systemstatusänderung bei einem Installationsrollback rückgängig zu machen. Alle benutzerdefinierten Rollbackaktionen sind ebenfalls verzögerte benutzerdefinierte Aktionen und müssen der Rückgängigaktion vorangestellt werden. Weitere Informationen finden Sie unter [Rollback von benutzerdefinierten Aktionen.](rollback-custom-actions.md)

 

 



