---
description: Benutzerdefinierte Aktionen, die zum Ändern des Systemstatus vorgesehen sind, müssen benutzerdefinierte Aktionen mit verzögerter Ausführung
ms.assetid: 48707ae1-9488-4bbb-8447-b24e383affb7
title: Ändern des System Status mithilfe einer benutzerdefinierten Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ace5dc323bcf809c76eeb55cfa859a8621312df7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358848"
---
# <a name="changing-the-system-state-using-a-custom-action"></a>Ändern des System Status mithilfe einer benutzerdefinierten Aktion

Benutzerdefinierte Aktionen, die zum Ändern des Systemstatus vorgesehen sind, müssen benutzerdefinierte Aktionen mit verzögerter Ausführung Benutzerdefinierte Aktionen, mit denen Eigenschaften, Funktions Zustände, Komponenten Zustände oder Zielverzeichnisse festgelegt oder System Vorgänge durch Einfügen von Zeilen in Sequenz Tabellen geplant werden, können die sofortige Ausführung sicher verwenden. Benutzerdefinierte Aktionen, die das System direkt ändern oder einen anderen Systemdienst aufzurufen, müssen jedoch bis zu dem Zeitpunkt verzögert werden, zu dem das Installationsskript ausgeführt wird. Weitere Informationen finden Sie unter [benutzerdefinierte Aktionen für die verzögerte Ausführung](deferred-execution-custom-actions.md).

Sie sollten nicht versuchen, eine benutzerdefinierte Aktion für die sofortige Ausführung zu verwenden, um den Systemstatus zu ändern, da jede benutzerdefinierte Aktion, die den Zustand ändert, eine entsprechende Rollback-Aktion aufweisen muss, um die Systemstatus Änderung bei einem Installations Rollback rückgängig zu machen. Alle benutzerdefinierten Rollbacks-Aktionen sind auch verzögerte benutzerdefinierte Aktionen und müssen der rückgängig gemachten Aktion vorangestellt sein. Weitere Informationen finden Sie unter [Rollback für benutzerdefinierte Aktionen](rollback-custom-actions.md).

 

 



