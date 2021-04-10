---
title: Abrufen des Status eines Neustart-Manager-Vorgangs
description: Wenn viele Anwendungen und Dienste heruntergefahren oder neu gestartet werden müssen, kann der Neustart-Manager-Vorgang eine längere Zeit in Anspruch nehmen. Die folgende Methode kann verwendet werden, um den Status des aktuellen Vorgangs abzurufen.
ms.assetid: 0df9de1f-df37-46a5-8010-6c8b34429376
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7afa5f329a8f21aa625c5c7b61a3e65b2c907bbf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102175"
---
# <a name="getting-the-status-of-a-restart-manager-operation"></a><span data-ttu-id="bce56-104">Abrufen des Status eines Neustart-Manager-Vorgangs</span><span class="sxs-lookup"><span data-stu-id="bce56-104">Getting the Status of a Restart Manager Operation</span></span>

<span data-ttu-id="bce56-105">Wenn viele Anwendungen und Dienste heruntergefahren oder neu gestartet werden müssen, kann der Neustart-Manager-Vorgang eine längere Zeit in Anspruch nehmen.</span><span class="sxs-lookup"><span data-stu-id="bce56-105">When many applications and services must be shut down or restarted, the Restart Manager operation can take an extended period of time.</span></span> <span data-ttu-id="bce56-106">Die folgende Methode kann verwendet werden, um den Status des aktuellen Vorgangs abzurufen.</span><span class="sxs-lookup"><span data-stu-id="bce56-106">The following method can be used to obtain the status of the current operation.</span></span>

<span data-ttu-id="bce56-107">**So erhalten Sie den Status des aktuellen Vorgangs zum Neustart-Manager**</span><span class="sxs-lookup"><span data-stu-id="bce56-107">**To get the status of the current Restart Manager operation**</span></span>

1.  <span data-ttu-id="bce56-108">Das Installationsprogramm sollte eine [**RM- \_ Schreib \_ Status- \_ Rückruf**](/windows/win32/api/restartmanager/nc-restartmanager-rm_write_status_callback) Funktion implementieren, die den Status der herunter gefahrenen oder neu gestarteten Anwendungen bestimmt.</span><span class="sxs-lookup"><span data-stu-id="bce56-108">The installer should implement a [**RM\_WRITE\_STATUS\_CALLBACK**](/windows/win32/api/restartmanager/nc-restartmanager-rm_write_status_callback) function that determines the status of the applications that have been shut down or restarted.</span></span> <span data-ttu-id="bce56-109">Die-Funktion kann die Informationen für die Benutzeroberfläche oder das Protokoll bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="bce56-109">The function can provide the information to the user interface or log.</span></span>
2.  <span data-ttu-id="bce56-110">Das Installationsprogramm übergibt den Zeiger an die [**RM- \_ Schreib Status- \_ \_ Rückruf**](/windows/win32/api/restartmanager/nc-restartmanager-rm_write_status_callback) Funktion, wenn die Funktion [**rmshutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) oder [**rmrestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="bce56-110">The installer passes the pointer to the [**RM\_WRITE\_STATUS\_CALLBACK**](/windows/win32/api/restartmanager/nc-restartmanager-rm_write_status_callback) function when calling the [**RmShutdown**](/windows/desktop/api/RestartManager/nf-restartmanager-rmshutdown) or [**RmRestart**](/windows/desktop/api/RestartManager/nf-restartmanager-rmrestart) function.</span></span>

 

 