---
description: Bevor die Sicherheitskonfigurations-Engine die Anlagen-Engine zum Verarbeiten Dienst spezifischer Aufgaben aufruft, müssen Sie die Anlagen-Engine installieren und bei der Sicherheitskonfigurations-Engine registrieren.
ms.assetid: f7376a79-97cd-4607-9e1b-5b8c7cd76a32
title: Registrieren einer Anlage-Engine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f50827fe27e86328e7e914bfc98740fa5e15060
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347135"
---
# <a name="registering-an-attachment-engine"></a><span data-ttu-id="7db47-103">Registrieren einer Anlage-Engine</span><span class="sxs-lookup"><span data-stu-id="7db47-103">Registering an Attachment Engine</span></span>

<span data-ttu-id="7db47-104">Bevor die Sicherheitskonfigurations-Engine die Anlagen-Engine zum Verarbeiten Dienst spezifischer Aufgaben aufruft, müssen Sie die Anlagen-Engine installieren und bei der Sicherheitskonfigurations-Engine registrieren.</span><span class="sxs-lookup"><span data-stu-id="7db47-104">Before the Security Configuration Engine can call your attachment engine to process service-specific tasks, you must install your attachment engine and register it with the Security Configuration Engine.</span></span>

<span data-ttu-id="7db47-105">**So installieren und registrieren Sie die Anlage-Engine-dll**</span><span class="sxs-lookup"><span data-stu-id="7db47-105">**To install and register the attachment engine DLL**</span></span>

1.  <span data-ttu-id="7db47-106">Kopieren Sie die Anlage-Engine-dll in ein Verzeichnis auf dem System.</span><span class="sxs-lookup"><span data-stu-id="7db47-106">Copy the attachment engine DLL to a directory on the system.</span></span> <span data-ttu-id="7db47-107">Das bevorzugte Verzeichnis ist% windir% \\ secedit- \\ Anlagen.</span><span class="sxs-lookup"><span data-stu-id="7db47-107">The preferred directory is %windir%\\secedit\\attachments.</span></span> <span data-ttu-id="7db47-108">Wenn dieses Verzeichnis nicht vorhanden ist, sollten Sie es erstellen.</span><span class="sxs-lookup"><span data-stu-id="7db47-108">If this directory does not exist, you should create it.</span></span>
2.  <span data-ttu-id="7db47-109">Erstellen Sie unter dem folgenden Knoten einen Registrierungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="7db47-109">Create a registry key under the following node.</span></span> <span data-ttu-id="7db47-110">Der *Dienst Name* ist der registrierte Name für die Anlage. er muss dem Dienstnamen entsprechen, der im Dienststeuerungs-Manager verwendet wird. dabei handelt es sich um ein Modul, das das Beenden und starten von Diensten verwaltet.</span><span class="sxs-lookup"><span data-stu-id="7db47-110">The *service name* is the registered name for the attachment, and must be the same service name used in the Service Control Manager, a module which manages the stopping and starting of services.</span></span> <span data-ttu-id="7db47-111">Der Name muss auch eindeutig sein, sodass er nicht mit den Namen anderer Anhänge in Konflikt steht.</span><span class="sxs-lookup"><span data-stu-id="7db47-111">The name must also be unique so it does not conflict with the names of other attachments.</span></span>

    ```
    HKEY_LOCAL_MACHINE
       Microsoft
          Windows NT
             CurrentVersion
                SeCEdit
                   Service
                      service name
    ```

3.  <span data-ttu-id="7db47-112">Erstellen Sie den folgenden Zeichen folgen Wert im neuen Registrierungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="7db47-112">Create the following string value in the new registry key.</span></span> <span data-ttu-id="7db47-113">der *Pfad der Anlage-Engine* ist der vollständige Pfad zum Anlage-Engine-Modul.</span><span class="sxs-lookup"><span data-stu-id="7db47-113">*attachment engine path* is the full path to the attachment engine module.</span></span><dl> <dd><span data-ttu-id="7db47-114">**Serviceattachmentpath**  =  *Pfad der Anlage-Engine*</span><span class="sxs-lookup"><span data-stu-id="7db47-114">**ServiceAttachmentPath** = *attachment engine path*</span></span><dl> <dt>

<span data-ttu-id="7db47-115">Datentyp</span><span class="sxs-lookup"><span data-stu-id="7db47-115">Data type</span></span>
</dt> <dd><span data-ttu-id="7db47-116">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="7db47-116">REG_SZ</span></span></dd> </dl> </dd> </dl>

 

 



