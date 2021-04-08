---
title: Neuverteilen der Windows Media Player 9-Serie
description: Neuverteilen der Windows Media Player 9-Serie
ms.assetid: 812e3fc7-e23d-489c-a486-62c7602cf46e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62f48da20123255ae08a0993d361a95deb8ed335
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037505"
---
# <a name="redistributing-windows-media-player-9-series"></a><span data-ttu-id="5478d-103">Neuverteilen der Windows Media Player 9-Serie</span><span class="sxs-lookup"><span data-stu-id="5478d-103">Redistributing Windows Media Player 9 Series</span></span>

<span data-ttu-id="5478d-104">Sie können Windows Media Player 9-Serie unter Windows XP installieren, indem Sie eines der folgenden Setup Programme verwenden.</span><span class="sxs-lookup"><span data-stu-id="5478d-104">You can install Windows Media Player 9 Series on Windows XP by using one of the following setup programs.</span></span>

-   <span data-ttu-id="5478d-105">MPSetupXP.exe</span><span class="sxs-lookup"><span data-stu-id="5478d-105">MPSetupXP.exe</span></span>
-   <span data-ttu-id="5478d-106">MPSetup.exe</span><span class="sxs-lookup"><span data-stu-id="5478d-106">MPSetup.exe</span></span>

> [!Note]  
> <span data-ttu-id="5478d-107">MPSetup.exe ist eine übergeordnete Gruppe des MPSetupXP.exe Setup Programms.</span><span class="sxs-lookup"><span data-stu-id="5478d-107">MPSetup.exe is a superset of the MPSetupXP.exe setup program.</span></span> <span data-ttu-id="5478d-108">Sie enthält Dateien, die von Betriebssystemen benötigt werden, die vor Windows XP veröffentlicht wurden.</span><span class="sxs-lookup"><span data-stu-id="5478d-108">It contains files that are needed by operating systems released before Windows XP.</span></span> <span data-ttu-id="5478d-109">MPSetup.exe ist bei der Installation unter Windows XP funktionell äquivalent zu MPSetupXP.exe, aber die Dateigröße des Setup Programms ist größer, da Sie nicht für die Installation unter Windows XP-Betriebssystemen optimiert wurde.</span><span class="sxs-lookup"><span data-stu-id="5478d-109">MPSetup.exe is functionally equivalent to MPSetupXP.exe when run on Windows XP, but the setup program file size is larger because it has not been optimized for installation on Windows XP operating systems.</span></span>

 

<span data-ttu-id="5478d-110">Sie können Windows Media Player 9-Serie unter Windows 98 Second Edition, Windows Millennium Edition oder Windows 2000 mit dem folgenden Setup Programm installieren.</span><span class="sxs-lookup"><span data-stu-id="5478d-110">You can install Windows Media Player 9 Series on Windows 98 Second Edition, Windows Millennium Edition or Windows 2000 by using the following setup program.</span></span>

-   <span data-ttu-id="5478d-111">MPSetup.exe</span><span class="sxs-lookup"><span data-stu-id="5478d-111">MPSetup.exe</span></span>

<span data-ttu-id="5478d-112">Hier ist ein Beispiel für eine Befehlszeile für die Installation ohne Benutzeroberfläche und ohne Neustart oder Neustart Aufforderung.</span><span class="sxs-lookup"><span data-stu-id="5478d-112">Here is an example of a command line for installation with no UI and no restart or restart prompt.</span></span>


```
MPSetup.exe /q:A /c:"setup_wm.exe /Q /R:N /P:#e"
```



> [!Note]  
> <span data-ttu-id="5478d-113">Der Parameter/P: \# e gibt an, dass das Windows Media Player-Installationspaket während der Einrichtung von Windows Media Player zwischengespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="5478d-113">The /P:\#e parameter specifies that the Windows Media Player installation package should be cached during Windows Media Player setup.</span></span> <span data-ttu-id="5478d-114">Dieser Befehl wird verwendet, um zukünftige Upgrades des Betriebssystems zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="5478d-114">This command is used to handle future upgrades of the operating system.</span></span> <span data-ttu-id="5478d-115">Dieser Befehl sollte nur von IT-Administratoren des Unternehmens ausgelassen werden.</span><span class="sxs-lookup"><span data-stu-id="5478d-115">This command should be omitted only by corporate IT administrators.</span></span> <span data-ttu-id="5478d-116">Der einzige Fall, in dem/P: \# e nicht in der Befehlszeile enthalten sein sollte, ist, wenn Sie das Zielsystem besitzen und wissen, dass das Zielsystem nie auf ein späteres Betriebssystem aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="5478d-116">The only case where /P:\#e should not be included on the command line is when you own the target system and know that the target system will never be upgraded to a later operating system.</span></span> <span data-ttu-id="5478d-117">Wenn Sie z. b. Windows Media Player 9-Serie unter Windows 2000 installieren, und der Computer kann an einem Tag ein Upgrade auf Windows XP durchführen, müssen Sie/P: \# e in der Befehlszeile verwenden.</span><span class="sxs-lookup"><span data-stu-id="5478d-117">For example, if you are installing Windows Media Player 9 Series on Windows 2000 and the computer may someday be upgraded to Windows XP, you must use /P:\#e on the command line.</span></span> <span data-ttu-id="5478d-118">Andernfalls werden die Windows-Media Player Dateien nach der Installation von Windows XP mit den Dateien für Windows Media Player für Windows XP überschrieben.</span><span class="sxs-lookup"><span data-stu-id="5478d-118">Otherwise, after the Windows XP installation, the Windows Media Player files will be overwritten with the files for Windows Media Player for Windows XP.</span></span>

 

<span data-ttu-id="5478d-119">In der folgenden Tabelle sind zusätzliche Parameter aufgeführt, die Sie mit dem Setup Programm der Windows Media Player 9-Serie verwenden können.</span><span class="sxs-lookup"><span data-stu-id="5478d-119">The following table shows additional parameters that you can use with the Windows Media Player 9 Series setup program.</span></span>



| <span data-ttu-id="5478d-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="5478d-120">Parameter</span></span>              | <span data-ttu-id="5478d-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5478d-121">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5478d-122">/NoMigrate</span><span class="sxs-lookup"><span data-stu-id="5478d-122">/NoMigrate</span></span>             | <span data-ttu-id="5478d-123">Verhindern der Bibliothek Migration.</span><span class="sxs-lookup"><span data-stu-id="5478d-123">Prevent library migration.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="5478d-124">/NestedRestore</span><span class="sxs-lookup"><span data-stu-id="5478d-124">/NestedRestore</span></span>         | <span data-ttu-id="5478d-125">Erstellen Sie einen genetzten Systemwiederherstellungspunkt.</span><span class="sxs-lookup"><span data-stu-id="5478d-125">Create a nested system restore point.</span></span> <span data-ttu-id="5478d-126">Verwenden Sie diese Anwendung, wenn Ihre Anwendung einen Systemwiederherstellungspunkt erstellt, um den Windows Media Player Wiederherstellungspunkt innerhalb des Anwendungs Wiederherstellungs Punkts zu schachteln.</span><span class="sxs-lookup"><span data-stu-id="5478d-126">Use this if your application creates a system restore point to nest the Windows Media Player restore point within your application restore point.</span></span>                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="5478d-127">/DisallowSystemRestore</span><span class="sxs-lookup"><span data-stu-id="5478d-127">/DisallowSystemRestore</span></span> | <span data-ttu-id="5478d-128">Hiermit wird die Erstellung eines System Wiederherstellungs Punkts nicht zugelassen.</span><span class="sxs-lookup"><span data-stu-id="5478d-128">Disallow the creation of a system restore point.</span></span> <span data-ttu-id="5478d-129">Mit diesem Flag wird die Erstellung eines System Wiederherstellungs Punkts deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="5478d-129">This flag will disable the creation of a system restore point.</span></span> <span data-ttu-id="5478d-130">In den meisten Fällen sollte dieses Flag nicht für die allgemeine Software Verteilung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5478d-130">Under most circumstances this flag should not be used for general software redistribution.</span></span> <span data-ttu-id="5478d-131">Dies sollte nur verwendet werden, wenn Sie im Namen des Endbenutzers eine explizite Auswahl treffen können, ohne das Rollback der Windows Media Player-Dateien auf eine frühere Version des Players zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="5478d-131">This should be used only when you can make an explicit choice on behalf of the end user not to support the rollback of the Windows Media Player files to an earlier version of the Player.</span></span> <span data-ttu-id="5478d-132">Dieses Flag sollte nur für die Unternehmens Bereitstellung oder die Installation des Originalgeräte Herstellers (OEM) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5478d-132">This flag should be used only for corporate deployment or original equipment manufacturer (OEM) installation.</span></span> |



 

## <a name="notes"></a><span data-ttu-id="5478d-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="5478d-133">Notes</span></span>

-   <span data-ttu-id="5478d-134">Bei den Befehlszeilen Parametern wird die Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="5478d-134">The command-line parameters are case-sensitive.</span></span>
-   <span data-ttu-id="5478d-135">Wenn Sie die Aufforderung zum erneuten Starten unterdrücken, müssen Sie den Registrierungsschlüssel installresult überprüfen und die Neustart Benachrichtigung in der aufrufenden Setup Anwendung behandeln.</span><span class="sxs-lookup"><span data-stu-id="5478d-135">When suppressing the restart prompt, you must check the InstallResult registry key and handle restart notification in the calling setup application.</span></span>
-   <span data-ttu-id="5478d-136">Mit der Windows Media Player 9-Serie wird auch die Windows Media-Laufzeitumgebung installiert, sodass es nicht erforderlich ist, das Windows Media Player Verteilungs Paket und das Windows Media-Lauf Zeit Verteilungs Paket in dasselbe Software Weitergabepaket einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="5478d-136">Windows Media Player 9 Series also installs the Windows Media Format runtime, so there is no need to include both the Windows Media Player distribution package and the Windows Media Format runtime distribution package in the same software redistribution package.</span></span> <span data-ttu-id="5478d-137">Wenn Sie MPSetup.exe oder MPSetupXP.exe in die Installation einschließen, müssen Sie daher nicht WMFdist.exe einschließen.</span><span class="sxs-lookup"><span data-stu-id="5478d-137">Therefore, if you include MPSetup.exe or MPSetupXP.exe in your installation, you do not need to include WMFdist.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5478d-138">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5478d-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5478d-139">**Neuverteilen von Windows Media Player-Software**</span><span class="sxs-lookup"><span data-stu-id="5478d-139">**Redistributing Windows Media Player Software**</span></span>](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




