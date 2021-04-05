---
title: Neuverteilen von Windows Media Player 10
description: Neuverteilen von Windows Media Player 10
ms.assetid: 58d601d4-e3d4-4a29-969c-799b2819f92c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4515317e0a6714d53c147671bbb83c06c172ef6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707908"
---
# <a name="redistributing-windows-media-player-10"></a><span data-ttu-id="74f54-103">Neuverteilen von Windows Media Player 10</span><span class="sxs-lookup"><span data-stu-id="74f54-103">Redistributing Windows Media Player 10</span></span>

<span data-ttu-id="74f54-104">Sie können Windows Media Player 10 unter Windows XP mit dem folgenden Setup Programm installieren.</span><span class="sxs-lookup"><span data-stu-id="74f54-104">You can install Windows Media Player 10 on Windows XP by using the following setup program.</span></span>

-   <span data-ttu-id="74f54-105">MP10Setup.exe</span><span class="sxs-lookup"><span data-stu-id="74f54-105">MP10Setup.exe</span></span>

<span data-ttu-id="74f54-106">Hier ist ein Beispiel für eine Befehlszeile für die Installation ohne Benutzeroberfläche und ohne Neustart oder Neustart Aufforderung.</span><span class="sxs-lookup"><span data-stu-id="74f54-106">Here is an example of a command line for installation with no UI and no restart or restart prompt.</span></span>


```
MP10Setup.exe /q:A /c:"setup_wm.exe /Q /R:N"
```



<span data-ttu-id="74f54-107">In der folgenden Tabelle sind zusätzliche Parameter aufgeführt, die Sie mit dem Setup Programm von Windows Media Player 10 verwenden können.</span><span class="sxs-lookup"><span data-stu-id="74f54-107">The following table shows additional parameters that you can use with the Windows Media Player 10 setup program.</span></span>



| <span data-ttu-id="74f54-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="74f54-108">Parameter</span></span>              | <span data-ttu-id="74f54-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="74f54-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74f54-110">/NoMigrate</span><span class="sxs-lookup"><span data-stu-id="74f54-110">/NoMigrate</span></span>             | <span data-ttu-id="74f54-111">Verhindern der Bibliothek Migration.</span><span class="sxs-lookup"><span data-stu-id="74f54-111">Prevent library migration.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="74f54-112">/NestedRestore</span><span class="sxs-lookup"><span data-stu-id="74f54-112">/NestedRestore</span></span>         | <span data-ttu-id="74f54-113">Erstellen Sie einen genetzten Systemwiederherstellungspunkt.</span><span class="sxs-lookup"><span data-stu-id="74f54-113">Create a nested system restore point.</span></span> <span data-ttu-id="74f54-114">Verwenden Sie diese Anwendung, wenn Ihre Anwendung einen Systemwiederherstellungspunkt erstellt, um den Windows Media Player Wiederherstellungspunkt innerhalb des Anwendungs Wiederherstellungs Punkts zu schachteln.</span><span class="sxs-lookup"><span data-stu-id="74f54-114">Use this if your application creates a system restore point to nest the Windows Media Player restore point within your application restore point.</span></span>                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="74f54-115">/DisallowSystemRestore</span><span class="sxs-lookup"><span data-stu-id="74f54-115">/DisallowSystemRestore</span></span> | <span data-ttu-id="74f54-116">Hiermit wird die Erstellung eines System Wiederherstellungs Punkts nicht zugelassen.</span><span class="sxs-lookup"><span data-stu-id="74f54-116">Disallow the creation of a system restore point.</span></span> <span data-ttu-id="74f54-117">Mit diesem Flag wird die Erstellung eines System Wiederherstellungs Punkts deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="74f54-117">This flag will disable the creation of a system restore point.</span></span> <span data-ttu-id="74f54-118">In den meisten Fällen sollte dieses Flag nicht für die allgemeine Software Verteilung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="74f54-118">Under most circumstances this flag should not be used for general software redistribution.</span></span> <span data-ttu-id="74f54-119">Dies sollte nur verwendet werden, wenn Sie im Namen des Endbenutzers eine explizite Auswahl treffen können, ohne das Rollback der Windows Media Player-Dateien auf eine frühere Version des Players zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="74f54-119">This should be used only when you can make an explicit choice on behalf of the end user not to support the rollback of the Windows Media Player files to an earlier version of the Player.</span></span> <span data-ttu-id="74f54-120">Dieses Flag sollte nur für die Unternehmens Bereitstellung oder die Installation des Originalgeräte Herstellers (OEM) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="74f54-120">This flag should be used only for corporate deployment or original equipment manufacturer (OEM) installation.</span></span> |
| <span data-ttu-id="74f54-121">/DefaultService</span><span class="sxs-lookup"><span data-stu-id="74f54-121">/DefaultService</span></span>        | <span data-ttu-id="74f54-122">Legen Sie den anfänglichen Online Store fest.</span><span class="sxs-lookup"><span data-stu-id="74f54-122">Set the initial online store.</span></span> <span data-ttu-id="74f54-123">Weitere Informationen finden Sie unter [Setup Command-Line Parameters for Online Stores](setup-command-line-parameters-for-online-stores.md).</span><span class="sxs-lookup"><span data-stu-id="74f54-123">For more information, see [Setup Command-line Parameters for Online Stores](setup-command-line-parameters-for-online-stores.md).</span></span>                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="74f54-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="74f54-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74f54-125">**Neuverteilen von Windows Media Player-Software**</span><span class="sxs-lookup"><span data-stu-id="74f54-125">**Redistributing Windows Media Player Software**</span></span>](redistributing-windows-media-player-software.md)
</dt> <dt>

[<span data-ttu-id="74f54-126">**Servicinfo-Dokument**</span><span class="sxs-lookup"><span data-stu-id="74f54-126">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 




