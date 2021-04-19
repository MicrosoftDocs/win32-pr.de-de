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
# <a name="changing-the-system-state-using-a-custom-action"></a><span data-ttu-id="a2d2a-103">Ändern des System Status mithilfe einer benutzerdefinierten Aktion</span><span class="sxs-lookup"><span data-stu-id="a2d2a-103">Changing the System State Using a Custom Action</span></span>

<span data-ttu-id="a2d2a-104">Benutzerdefinierte Aktionen, die zum Ändern des Systemstatus vorgesehen sind, müssen benutzerdefinierte Aktionen mit verzögerter Ausführung</span><span class="sxs-lookup"><span data-stu-id="a2d2a-104">Custom actions intended to change the system state must be deferred execution custom actions.</span></span> <span data-ttu-id="a2d2a-105">Benutzerdefinierte Aktionen, mit denen Eigenschaften, Funktions Zustände, Komponenten Zustände oder Zielverzeichnisse festgelegt oder System Vorgänge durch Einfügen von Zeilen in Sequenz Tabellen geplant werden, können die sofortige Ausführung sicher verwenden.</span><span class="sxs-lookup"><span data-stu-id="a2d2a-105">Custom actions that set properties, feature states, component states, or target directories, or schedule system operations by inserting rows into sequence tables can use immediate execution safely.</span></span> <span data-ttu-id="a2d2a-106">Benutzerdefinierte Aktionen, die das System direkt ändern oder einen anderen Systemdienst aufzurufen, müssen jedoch bis zu dem Zeitpunkt verzögert werden, zu dem das Installationsskript ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a2d2a-106">However, custom actions that change the system directly or call another system service must be deferred to the time when the installation script is executed.</span></span> <span data-ttu-id="a2d2a-107">Weitere Informationen finden Sie unter [benutzerdefinierte Aktionen für die verzögerte Ausführung](deferred-execution-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="a2d2a-107">For more information, see [Deferred Execution Custom Actions](deferred-execution-custom-actions.md).</span></span>

<span data-ttu-id="a2d2a-108">Sie sollten nicht versuchen, eine benutzerdefinierte Aktion für die sofortige Ausführung zu verwenden, um den Systemstatus zu ändern, da jede benutzerdefinierte Aktion, die den Zustand ändert, eine entsprechende Rollback-Aktion aufweisen muss, um die Systemstatus Änderung bei einem Installations Rollback rückgängig zu machen.</span><span class="sxs-lookup"><span data-stu-id="a2d2a-108">You should not attempt to use an immediate execution custom action to change the system state, because every custom action that changes the state needs to have a corresponding rollback custom action to undo the system state change on an installation rollback.</span></span> <span data-ttu-id="a2d2a-109">Alle benutzerdefinierten Rollbacks-Aktionen sind auch verzögerte benutzerdefinierte Aktionen und müssen der rückgängig gemachten Aktion vorangestellt sein.</span><span class="sxs-lookup"><span data-stu-id="a2d2a-109">All rollback custom actions are also deferred custom actions and must precede the action they undo.</span></span> <span data-ttu-id="a2d2a-110">Weitere Informationen finden Sie unter [Rollback für benutzerdefinierte Aktionen](rollback-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="a2d2a-110">For more information, see [Rollback Custom Actions](rollback-custom-actions.md).</span></span>

 

 



