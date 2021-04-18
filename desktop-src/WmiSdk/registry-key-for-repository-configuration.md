---
description: Windows-Verwaltungsinstrumentation (WMI) verfügt über einen neuen Registrierungsschlüssel, um das autorestore-Repository-Feature zu aktivieren oder zu deaktivieren.
ms.assetid: 6c93fc40-b5d8-42da-9d02-7fa04fce3f65
ms.tgt_platform: multiple
title: Registrierungsschlüssel für die Repository-Konfiguration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed981da7c0540378746c78fecceefab8fc62559b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345245"
---
# <a name="registry-key-for-repository-configuration"></a><span data-ttu-id="ac91e-103">Registrierungsschlüssel für die Repository-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="ac91e-103">Registry Key for Repository Configuration</span></span>

<span data-ttu-id="ac91e-104">Windows-Verwaltungsinstrumentation (WMI) verfügt über einen neuen Registrierungsschlüssel, um das autorestore-Repository-Feature zu aktivieren oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="ac91e-104">Windows Management Instrumentation (WMI) has a new registry key to enable or disable the AutoRestore repository feature..</span></span> <span data-ttu-id="ac91e-105">Weitere Informationen zum Wiederherstellen des WMI-Repository finden Sie unter [sichern oder Wiederherstellen des WMI-Repository](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731460(v=ws.11)).</span><span class="sxs-lookup"><span data-stu-id="ac91e-105">For more information on restoring the WMI repository, see [Backup or Restore WMI Repository](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc731460(v=ws.11)).</span></span>

<span data-ttu-id="ac91e-106">In Windows 7 ist das Standardverhalten das automatische Wiederherstellen eines Repository aus einer gesicherten Version, wenn eine Repository-Beschädigung erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="ac91e-106">In Windows 7, the default behavior is to auto-restore a repository from a backed-up version if a repository corruption is detected.</span></span> <span data-ttu-id="ac91e-107">WMI stellt den **autorestoreaktivierten** Registrierungs Wert bereit, um diese Funktion zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="ac91e-107">WMI provides the **AutoRestoreEnabled** registry value to disable this feature.</span></span>

<span data-ttu-id="ac91e-108">Die Registrierungsschlüssel für WMI befinden sich in der Registrierung unter **HKEY \_ local \_ Machine** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ .</span><span class="sxs-lookup"><span data-stu-id="ac91e-108">The registry keys for WMI are located in the registry at **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\.</span></span>

<dl> <dt>

<span data-ttu-id="ac91e-109"><span id="AutoRestoreEnabled"></span><span id="autorestoreenabled"></span><span id="AUTORESTOREENABLED"></span>**Autorestoreaktivierte**</span><span class="sxs-lookup"><span data-stu-id="ac91e-109"><span id="AutoRestoreEnabled"></span><span id="autorestoreenabled"></span><span id="AUTORESTOREENABLED"></span>**AutoRestoreEnabled**</span></span>
</dt> <dd>

<span data-ttu-id="ac91e-110">Ermöglicht es dem Benutzer, zu bestimmen, ob die autorestore-Repository-Funktion verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ac91e-110">Enables the user to determine whether or not to use the AutoRestore repository feature.</span></span> <span data-ttu-id="ac91e-111">Standardmäßig ist dieser Schlüssel auf 1 festgelegt, und die autorestore-Repository-Funktion ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="ac91e-111">By default this key is set to 1 and the AutoRestore Repository feature is enabled.</span></span>

<span data-ttu-id="ac91e-112">Folgende Einstellungen sind möglich:</span><span class="sxs-lookup"><span data-stu-id="ac91e-112">The following settings are possible:</span></span>

<dl> <dt>

<span data-ttu-id="ac91e-113"><span id="0"></span>0</span><span class="sxs-lookup"><span data-stu-id="ac91e-113"><span id="0"></span>0</span></span>
</dt> <dd>

<span data-ttu-id="ac91e-114">Disabled</span><span class="sxs-lookup"><span data-stu-id="ac91e-114">Disabled</span></span>

</dd> <dt>

<span data-ttu-id="ac91e-115"><span id="1"></span>1</span><span class="sxs-lookup"><span data-stu-id="ac91e-115"><span id="1"></span>1</span></span>
</dt> <dd>

<span data-ttu-id="ac91e-116">Aktiviert</span><span class="sxs-lookup"><span data-stu-id="ac91e-116">Enabled</span></span>

</dd> </dl> </dd> </dl>

<span data-ttu-id="ac91e-117">Der Registrierungs Wert **autorestoreaktivierte** kann mithilfe der Gruppenrichtlinien-Verwaltungskonsole (GPMC) geändert werden.</span><span class="sxs-lookup"><span data-stu-id="ac91e-117">The **AutoRestoreEnabled** registry value can be modified by using the Group Policy Management Console (GPMC).</span></span> <span data-ttu-id="ac91e-118">Weitere Informationen finden Sie unter [Gruppenrichtlinien-Verwaltungskonsole](/previous-versions/windows/desktop/gpmc/group-policy-management-console-portal).</span><span class="sxs-lookup"><span data-stu-id="ac91e-118">For more information, see [Group Policy Management Console](/previous-versions/windows/desktop/gpmc/group-policy-management-console-portal).</span></span>

<span data-ttu-id="ac91e-119">Dieses Verfahren enthält Details zum Aktivieren oder Deaktivieren der autorestore-Repository-Funktion:</span><span class="sxs-lookup"><span data-stu-id="ac91e-119">This procedure provides details about how to enable or disable the AutoRestore repository feature:</span></span>

<span data-ttu-id="ac91e-120">**So ändern Sie den Standardwert des **autorestoreaktivierten** Schlüssels mithilfe von Gruppenrichtlinie**</span><span class="sxs-lookup"><span data-stu-id="ac91e-120">**To change the default value of the **AutoRestoreEnabled** key by using Group Policy**</span></span>

1.  <span data-ttu-id="ac91e-121">Öffnen Sie die Gruppenrichtlinien-Verwaltungskonsole.</span><span class="sxs-lookup"><span data-stu-id="ac91e-121">Open the GPMC.</span></span>
2.  <span data-ttu-id="ac91e-122">Erstellen Sie ein Gruppenrichtlinie Objekt (GPO).</span><span class="sxs-lookup"><span data-stu-id="ac91e-122">Create a Group Policy object (GPO).</span></span>
3.  <span data-ttu-id="ac91e-123">Bearbeiten Sie das Gruppenrichtlinien Objekt.</span><span class="sxs-lookup"><span data-stu-id="ac91e-123">Edit the GPO.</span></span>
4.  <span data-ttu-id="ac91e-124">Navigieren Sie zu Einstellungen/Windows-Einstellungen/Registrierung.</span><span class="sxs-lookup"><span data-stu-id="ac91e-124">Browse to Preferences/Windows Settings/Registry.</span></span>
5.  <span data-ttu-id="ac91e-125">Klicken Sie mit der rechten Maustaste, und wählen Sie **neu... Registrierung**.</span><span class="sxs-lookup"><span data-stu-id="ac91e-125">Right-click and select **New... Registry**.</span></span> <span data-ttu-id="ac91e-126">Diese Aktion stellt eine Benutzeroberfläche dar, auf der Sie Registrierungsinformationen eingeben können.</span><span class="sxs-lookup"><span data-stu-id="ac91e-126">This action presents a user interface where you can enter registry information.</span></span>
6.  <span data-ttu-id="ac91e-127">Wählen Sie den Befehl **Aktualisieren** aus.</span><span class="sxs-lookup"><span data-stu-id="ac91e-127">Select the **Update** command.</span></span>
7.  <span data-ttu-id="ac91e-128">Wählen Sie den folgenden Registrierungsschlüssel Pfad aus: **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ WBEM \\ CIMOM**.</span><span class="sxs-lookup"><span data-stu-id="ac91e-128">Select the following registry key path: **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\WBEM\\CIMOM**.</span></span>
8.  <span data-ttu-id="ac91e-129">Geben Sie im Feld **Name den Namen** **autorestoreaktivierte** ein.</span><span class="sxs-lookup"><span data-stu-id="ac91e-129">In the **name** field, enter **AutoRestoreEnabled**.</span></span>
9.  <span data-ttu-id="ac91e-130">Geben Sie im Feld **Daten** 0 zum Deaktivieren oder 1 ein, um das autorestore-Repository zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="ac91e-130">In the **data** field, enter 0 to disable or 1 to enable the AutoRestore repository feature.</span></span>
10. <span data-ttu-id="ac91e-131">Klicken Sie auf OK.</span><span class="sxs-lookup"><span data-stu-id="ac91e-131">Click OK.</span></span>

 

 
