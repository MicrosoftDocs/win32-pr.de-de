---
title: Neuverteilen von Windows Media Player 11
description: Neuverteilen von Windows Media Player 11
ms.assetid: 3348821f-6d72-40c2-954b-0046ce502401
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 674da0298196f0749a549670bf9bd7c4095b6e7a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036736"
---
# <a name="redistributing-windows-media-player-11"></a><span data-ttu-id="5864b-103">Neuverteilen von Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="5864b-103">Redistributing Windows Media Player 11</span></span>

<span data-ttu-id="5864b-104">Sie können Windows Media Player 11 unter Windows XP installieren, indem Sie eines der folgenden Setup Programme verwenden, wobei *LocaleID* ein Gebiets Schema Bezeichner ist.</span><span class="sxs-lookup"><span data-stu-id="5864b-104">You can install Windows Media Player 11 on Windows XP by using one of the following setup programs, where *localeId* is a locale identifier.</span></span>

-   <span data-ttu-id="5864b-105">wmp11-windowsxp-x86-*LocaleID*. exe</span><span class="sxs-lookup"><span data-stu-id="5864b-105">wmp11-windowsxp-x86-*localeId*.exe</span></span>
-   <span data-ttu-id="5864b-106">wmp11-windowsxp-x64-*LocaleID*. exe</span><span class="sxs-lookup"><span data-stu-id="5864b-106">wmp11-windowsxp-x64-*localeId*.exe</span></span>

<span data-ttu-id="5864b-107">Hier ist ein Beispiel für eine Befehlszeile für die Installation ohne Benutzeroberfläche und ohne Neustart oder Neustart Aufforderung.</span><span class="sxs-lookup"><span data-stu-id="5864b-107">Here is an example of a command line for installation with no UI and no restart or restart prompt.</span></span>


```
wmp11-windowsxp-x86-enu.exe /q:A /c:"setup_wm.exe /Q /R:N"
```



<span data-ttu-id="5864b-108">In der folgenden Tabelle sind zusätzliche Parameter aufgeführt, die Sie mit dem Setup Programm von Windows Media Player 11 verwenden können.</span><span class="sxs-lookup"><span data-stu-id="5864b-108">The following table shows additional parameters that you can use with the Windows Media Player 11 setup program.</span></span>



| <span data-ttu-id="5864b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="5864b-109">Parameter</span></span>              | <span data-ttu-id="5864b-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5864b-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5864b-111">/NoMigrate</span><span class="sxs-lookup"><span data-stu-id="5864b-111">/NoMigrate</span></span>             | <span data-ttu-id="5864b-112">Verhindern der Bibliothek Migration.</span><span class="sxs-lookup"><span data-stu-id="5864b-112">Prevent library migration.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="5864b-113">/NestedRestore</span><span class="sxs-lookup"><span data-stu-id="5864b-113">/NestedRestore</span></span>         | <span data-ttu-id="5864b-114">Erstellen Sie einen genetzten Systemwiederherstellungspunkt.</span><span class="sxs-lookup"><span data-stu-id="5864b-114">Create a nested system restore point.</span></span> <span data-ttu-id="5864b-115">Verwenden Sie diese Anwendung, wenn Ihre Anwendung einen Systemwiederherstellungspunkt erstellt, um den Windows Media Player Wiederherstellungspunkt innerhalb des Anwendungs Wiederherstellungs Punkts zu schachteln.</span><span class="sxs-lookup"><span data-stu-id="5864b-115">Use this if your application creates a system restore point to nest the Windows Media Player restore point within your application restore point.</span></span>                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="5864b-116">/DisallowSystemRestore</span><span class="sxs-lookup"><span data-stu-id="5864b-116">/DisallowSystemRestore</span></span> | <span data-ttu-id="5864b-117">Hiermit wird die Erstellung eines System Wiederherstellungs Punkts nicht zugelassen.</span><span class="sxs-lookup"><span data-stu-id="5864b-117">Disallow the creation of a system restore point.</span></span> <span data-ttu-id="5864b-118">Mit diesem Flag wird die Erstellung eines System Wiederherstellungs Punkts deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="5864b-118">This flag will disable the creation of a system restore point.</span></span> <span data-ttu-id="5864b-119">In den meisten Fällen sollte dieses Flag nicht für die allgemeine Software Verteilung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5864b-119">Under most circumstances this flag should not be used for general software redistribution.</span></span> <span data-ttu-id="5864b-120">Dies sollte nur verwendet werden, wenn Sie im Namen des Endbenutzers eine explizite Auswahl treffen können, ohne das Rollback der Windows Media Player-Dateien auf eine frühere Version des Players zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="5864b-120">This should be used only when you can make an explicit choice on behalf of the end user not to support the rollback of the Windows Media Player files to an earlier version of the Player.</span></span> <span data-ttu-id="5864b-121">Dieses Flag sollte nur für die Unternehmens Bereitstellung oder die Installation des Originalgeräte Herstellers (OEM) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5864b-121">This flag should be used only for corporate deployment or original equipment manufacturer (OEM) installation.</span></span> |
| <span data-ttu-id="5864b-122">/DefaultService</span><span class="sxs-lookup"><span data-stu-id="5864b-122">/DefaultService</span></span>        | <span data-ttu-id="5864b-123">Legen Sie den anfänglichen Online Store fest.</span><span class="sxs-lookup"><span data-stu-id="5864b-123">Set the initial online store.</span></span> <span data-ttu-id="5864b-124">Weitere Informationen finden Sie unter [Setup Command-Line Parameters for Online Stores](setup-command-line-parameters-for-online-stores.md).</span><span class="sxs-lookup"><span data-stu-id="5864b-124">For more information, see [Setup Command-line Parameters for Online Stores](setup-command-line-parameters-for-online-stores.md).</span></span>                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="5864b-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5864b-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5864b-126">**Neuverteilen von Windows Media Player-Software**</span><span class="sxs-lookup"><span data-stu-id="5864b-126">**Redistributing Windows Media Player Software**</span></span>](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




