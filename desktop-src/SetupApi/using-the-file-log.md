---
description: Bevor Sie ein Datei Protokoll verwenden können, müssen Sie setupinitializefilelog aufrufen, um es zu öffnen oder zu erstellen. Wenn Sie diese Funktion aufgerufen haben, können Sie Flags angeben, um ein Datei Protokoll zu erstellen oder zu überschreiben, das System Protokoll zu öffnen oder ein Datei Protokoll als schreibgeschützt zu öffnen.
ms.assetid: 7ab133f6-2088-4bca-bf24-d3dcb29376a1
title: Verwenden des Datei Protokolls
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf7f1e3d27ba7d42d448a1eac48d60246c2b40db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960998"
---
# <a name="using-the-file-log"></a><span data-ttu-id="b96d1-104">Verwenden des Datei Protokolls</span><span class="sxs-lookup"><span data-stu-id="b96d1-104">Using the File Log</span></span>

<span data-ttu-id="b96d1-105">Bevor Sie ein Datei Protokoll verwenden können, müssen Sie [**setupinitializefilelog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga) aufrufen, um es zu öffnen oder zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b96d1-105">Before you can use a file log, you must call [**SetupInitializeFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga) to open or create it.</span></span> <span data-ttu-id="b96d1-106">Wenn Sie diese Funktion aufgerufen haben, können Sie Flags angeben, um ein Datei Protokoll zu erstellen oder zu überschreiben, das System Protokoll zu öffnen oder ein Datei Protokoll als schreibgeschützt zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b96d1-106">When you call this function, you can specify flags to create or overwrite a file log, open the system log, or open a file log as read-only.</span></span>

<span data-ttu-id="b96d1-107">Nachdem [**setupinitializefilelog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga) ein Handle für ein Datei Protokoll zurückgegeben hat, können Sie einen Eintrag hinzufügen, indem Sie [**SetupLogFile**](/windows/desktop/api/Setupapi/nf-setupapi-setuplogfilea)aufrufen, einen Eintrag durch Aufrufen von [**setupremumuvefilelogentry**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefilelogentrya)löschen oder Informationen zu einer bestimmten Datei in einem Datei Protokoll abrufen, indem Sie [**setupqueryfilelog**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryfileloga)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b96d1-107">After [**SetupInitializeFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga) returns a handle to a file log, you can add an entry by calling [**SetupLogFile**](/windows/desktop/api/Setupapi/nf-setupapi-setuplogfilea), delete an entry by calling [**SetupRemoveFileLogEntry**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefilelogentrya), or retrieve information about a particular file in a file log by calling [**SetupQueryFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryfileloga).</span></span>

<span data-ttu-id="b96d1-108">Wenn das Datei Protokoll nicht mehr benötigt wird, sollte [**setupterminatefilelog**](/windows/desktop/api/Setupapi/nf-setupapi-setupterminatefilelog) aufgerufen werden, um die während des Aufrufs von [**setupinitializefilelog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga)zugeordneten Ressourcen freizugeben.</span><span class="sxs-lookup"><span data-stu-id="b96d1-108">When the file log is no longer needed, [**SetupTerminateFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupterminatefilelog) should be called to release the resources allocated during the call to [**SetupInitializeFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga).</span></span>

 

 



