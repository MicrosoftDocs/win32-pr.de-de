---
title: Rückruf Funktionen für den Neustart-Manager
description: Die Neustart-Manager-API verwendet die Rückruf Funktionen in der folgenden Tabelle.
ms.assetid: abb78aa5-0487-4e99-85b6-adc38b600c09
keywords:
- Neustart-Manager neu starten Mgr, Referenz, Rückruf Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44c850dd805aeff664e3e09292825e342a6c5603
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729569"
---
# <a name="restart-manager-callback-functions"></a><span data-ttu-id="15dd5-104">Rückruf Funktionen für den Neustart-Manager</span><span class="sxs-lookup"><span data-stu-id="15dd5-104">Restart Manager Callback Functions</span></span>

<span data-ttu-id="15dd5-105">Die Neustart-Manager-API verwendet die Rückruf Funktionen in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="15dd5-105">The Restart Manager API uses the callback functions in the following table.</span></span>



| <span data-ttu-id="15dd5-106">Rückruffunktion</span><span class="sxs-lookup"><span data-stu-id="15dd5-106">Callback Function</span></span>                                               | <span data-ttu-id="15dd5-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="15dd5-107">Description</span></span>                                                                                                                                                            |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="15dd5-108">**RM- \_ Schreib \_ Status \_ Rückruf**</span><span class="sxs-lookup"><span data-stu-id="15dd5-108">**RM\_WRITE\_STATUS\_CALLBACK**</span></span>](/windows/win32/api/restartmanager/nc-restartmanager-rm_write_status_callback) | <span data-ttu-id="15dd5-109">Die Anwendung, die die Restart Manager-Sitzung gestartet hat, kann einen Zeiger auf diese Funktion an die Neustart-Manager-Funktionen übergeben, um einen Prozentsatz der Vollständigkeit zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="15dd5-109">The application that started the Restart Manager session can pass a pointer to this function to the Restart Manager functions to receive a percentage of completeness.</span></span> |



 

 

 