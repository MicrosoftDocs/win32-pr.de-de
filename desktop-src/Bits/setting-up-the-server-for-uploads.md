---
title: Einrichten des Servers für Uploads
description: Zum Hochladen von Dateien auf einen Server mit Bits muss auf dem Server IIS und die BITS-Server Erweiterung ISAPI installiert sein. Informationen zu IIS-Anforderungen finden Sie unter IIS-Anforderungen für BITS-Uploads.
ms.assetid: 2f3a2f99-b9de-41da-897f-a4d9c6d5e8c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c2ef81019f4c69157c267cd2438188f440299a4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206299"
---
# <a name="setting-up-the-server-for-uploads"></a><span data-ttu-id="02254-104">Einrichten des Servers für Uploads</span><span class="sxs-lookup"><span data-stu-id="02254-104">Setting Up the Server for Uploads</span></span>

<span data-ttu-id="02254-105">Zum Hochladen von Dateien auf einen Server mit Bits muss auf dem Server IIS und die BITS-Server Erweiterung ISAPI installiert sein.</span><span class="sxs-lookup"><span data-stu-id="02254-105">To upload files to a server using BITS, the server must have IIS and the BITS server extension ISAPI installed.</span></span> <span data-ttu-id="02254-106">Informationen zu IIS-Anforderungen finden Sie unter [IIS-Anforderungen für BITS-Uploads](iis-requirements-for-bits-uploads.md).</span><span class="sxs-lookup"><span data-stu-id="02254-106">For IIS requirements, see [IIS Requirements for BITS Uploads](iis-requirements-for-bits-uploads.md).</span></span>

<span data-ttu-id="02254-107">Informationen zum Konfigurieren des virtuellen IIS-Verzeichnisses, das Bits für Uploads verwendet, finden Sie in den folgenden Themen.</span><span class="sxs-lookup"><span data-stu-id="02254-107">For information on configuring the IIS virtual directory that BITS uses for uploads, see the following topics.</span></span>

-   [<span data-ttu-id="02254-108">Festlegen von Berechtigungen für virtuelle Verzeichnisse</span><span class="sxs-lookup"><span data-stu-id="02254-108">Setting Permissions on Virtual Directories</span></span>](setting-permissions-on-virtual-directories.md)
-   [<span data-ttu-id="02254-109">Schreiben eines Skripts zum Konfigurieren des virtuellen Verzeichnisses</span><span class="sxs-lookup"><span data-stu-id="02254-109">Writing a Script to Configure the Virtual Directory</span></span>](writing-a-script-to-configure-the-virtual-directory.md)
-   [<span data-ttu-id="02254-110">Verwenden der IIS-Benutzeroberfläche zum Konfigurieren des virtuellen Verzeichnisses</span><span class="sxs-lookup"><span data-stu-id="02254-110">Using the IIS UI to Configure the Virtual Directory</span></span>](using-the-iis-ui-to-configure-the-virtual-directory.md)
-   [<span data-ttu-id="02254-111">Verhindern mehrerer Uploads</span><span class="sxs-lookup"><span data-stu-id="02254-111">Preventing Multiple Uploads</span></span>](preventing-multiple-uploads.md)
-   [<span data-ttu-id="02254-112">Bewährte Methoden für den Upload</span><span class="sxs-lookup"><span data-stu-id="02254-112">Upload Best Practices</span></span>](upload-best-practices.md)

> [!Note]  
> <span data-ttu-id="02254-113">Einige IIS-Installationen enthalten die URLScan-Filter Komponente.</span><span class="sxs-lookup"><span data-stu-id="02254-113">Some IIS installations include the UrlScan filtering component.</span></span> <span data-ttu-id="02254-114">Wenn URLScan aktiviert ist, muss der Administrator das Verb "Bits \_ Post"-Verb in der Liste der zulässigen HTTP-Verben von URLScan hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="02254-114">If UrlScan is enabled, the administrator must add the "BITS\_POST" verb to UrlScan's list of allowed HTTP verbs.</span></span> <span data-ttu-id="02254-115">Andernfalls können Bits-Client Uploads nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="02254-115">Otherwise, BITS client uploads will fail.</span></span> <span data-ttu-id="02254-116">Weitere Informationen zum Aktivieren von Verben in URLScan finden Sie in der URLScan-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="02254-116">For further details on enabling verbs in UrlScan, see the UrlScan documentation.</span></span>

 

 

 




