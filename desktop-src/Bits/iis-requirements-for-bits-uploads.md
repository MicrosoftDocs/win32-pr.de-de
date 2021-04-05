---
title: IIS-Anforderungen für BITS-Uploads
description: Für Uploads erfordert BITS IIS 6,0 unter Windows Server 2003 und IIS 7,0 unter Windows Server 2008; IIS 5,1 wird von Bits unter Windows XP nicht unterstützt.
ms.assetid: 8ab07af5-3b59-4c98-8e57-f614deb8b594
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8fc1eb9bae86e7bb2635b3a250e8a9efe1bc630
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708118"
---
# <a name="iis-requirements-for-bits-uploads"></a><span data-ttu-id="12ec2-103">IIS-Anforderungen für BITS-Uploads</span><span class="sxs-lookup"><span data-stu-id="12ec2-103">IIS Requirements for BITS Uploads</span></span>

<span data-ttu-id="12ec2-104">Für Uploads erfordert BITS IIS 6,0 unter Windows Server 2003 und IIS 7,0 unter Windows Server 2008; IIS 5,1 wird von Bits unter Windows XP nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="12ec2-104">For uploads, BITS requires IIS 6.0 on Windows Server 2003, and IIS 7.0 on Windows Server 2008; BITS does not support IIS 5.1 on Windows XP.</span></span> <span data-ttu-id="12ec2-105">Das virtuelle IIS-Verzeichnis muss für Uploads aktiviert sein, und die BITS-IIS-Erweiterungen müssen konfiguriert sein.</span><span class="sxs-lookup"><span data-stu-id="12ec2-105">The IIS virtual directory must be enabled for uploads and have the BITS IIS extensions configured.</span></span>

<span data-ttu-id="12ec2-106">**Core-Installationen von Windows Server:** BITS-IIS-Erweiterungen werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="12ec2-106">**Core installations of Windows Server:** BITS IIS extensions are not supported.</span></span>

<span data-ttu-id="12ec2-107">Verwenden Sie unter Windows Server 2008 die **Server-Manager** , um das Feature für BITS-Server Erweiterungen zu installieren.</span><span class="sxs-lookup"><span data-stu-id="12ec2-107">On Windows Server 2008, use the **Server Manager** to install the BITS Server Extensions feature.</span></span> <span data-ttu-id="12ec2-108">Klicken Sie im linken Bereich von **Server-Manager** auf **Features** .</span><span class="sxs-lookup"><span data-stu-id="12ec2-108">From **Server Manager**, click **Features** in the left pane.</span></span> <span data-ttu-id="12ec2-109">Überprüfen Sie im **Assistenten zum Hinzufügen von Features** BITS-Server Erweiterungen.</span><span class="sxs-lookup"><span data-stu-id="12ec2-109">In the **Add Features Wizard**, check BITS Server Extensions.</span></span> <span data-ttu-id="12ec2-110">Beachten Sie, dass die IIS 6-Verwaltungs Kompatibilitäts Rollen installiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="12ec2-110">Note that the IIS 6 Management Compatibility roles must be installed.</span></span>

<span data-ttu-id="12ec2-111">Verwenden Sie unter Windows Server 2003 den **Assistenten für Windows-Komponenten** , um die BITS-Server Erweiterung zu installieren.</span><span class="sxs-lookup"><span data-stu-id="12ec2-111">On Windows Server 2003, use the **Windows Components Wizard** to install the BITS server extension.</span></span> <span data-ttu-id="12ec2-112">Wählen Sie in der **Systemsteuerung** die Option **Programme hinzufügen oder entfernen** aus.</span><span class="sxs-lookup"><span data-stu-id="12ec2-112">From **Control Panel**, select **Add or Remove Programs**.</span></span> <span data-ttu-id="12ec2-113">Wählen Sie dann **Windows-Komponenten hinzufügen/entfernen** aus, um den **Assistenten für Windows-Komponenten** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="12ec2-113">Then, select **Add/Remove Windows Components** to display the **Windows Components Wizard**.</span></span> <span data-ttu-id="12ec2-114">Die BITS-Server Erweiterung ist eine Unterkomponente von Internetinformationsdienste (IIS), bei der es sich um eine Unterkomponente des Webanwendungs Servers handelt.</span><span class="sxs-lookup"><span data-stu-id="12ec2-114">The BITS server extension is a subcomponent of Internet Information Services (IIS) which is a sub-component of Web Application Server.</span></span>

> [!Note]  
> <span data-ttu-id="12ec2-115">Wenn der IISAdmin-Dienst neu gestartet wird, muss der IIS-Arbeitsprozess wieder verwendet werden, bevor der BITS-Dienst Uploads fortsetzen kann.</span><span class="sxs-lookup"><span data-stu-id="12ec2-115">If the IISAdmin service is restarted, the IIS worker process must be recycled before the BITS service can resume uploads.</span></span> <span data-ttu-id="12ec2-116">Der IIS-Arbeitsprozess kann mithilfe des Befehlszeilen-Hilfsprogramms **IISReset.exe** manuell wieder verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="12ec2-116">The IIS worker process can be manually recycled by using the **IISReset.exe** command line utility.</span></span>

 

<span data-ttu-id="12ec2-117">Weitere Informationen zum Konfigurieren von IIS für Uploads finden [Sie unter Einrichten des Servers für Uploads](setting-up-the-server-for-uploads.md).</span><span class="sxs-lookup"><span data-stu-id="12ec2-117">For information on configuring IIS for uploads, see [Setting Up the Server for Uploads](setting-up-the-server-for-uploads.md).</span></span>

<span data-ttu-id="12ec2-118">Ausführliche Informationen zu den Eigenschaften, die von Bits zu IIS hinzugefügt werden, finden Sie unter [BITS-Server Einstellungen für Upload-Aufträge](bits-server-settings-for-upload-jobs.md).</span><span class="sxs-lookup"><span data-stu-id="12ec2-118">For details on the properties that BITS adds to IIS, see [BITS Server Settings for Upload Jobs](bits-server-settings-for-upload-jobs.md).</span></span>

 

 




