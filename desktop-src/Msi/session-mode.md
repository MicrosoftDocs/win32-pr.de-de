---
description: Dies ist die Mode-Eigenschaft des Session-Objekts. Diese Eigenschaft ist ein Wert, der das Flag für den vorgesehenen Modus für die aktuelle Installationssitzung darstellt. Die meisten modusflags sind extern schreibgeschützt, aber es können auch einige angegebene Flags festgelegt werden.
ms.assetid: 9aca413d-d653-4ec1-a39b-af956f6c95e7
title: Session. Mode (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.Mode
api_type:
- COM
api_location: ''
ms.openlocfilehash: f081859db789601f2c41bf95d65c377fba8d51f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364530"
---
# <a name="sessionmode-property"></a><span data-ttu-id="e78a0-105">Session. Mode (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e78a0-105">Session.Mode property</span></span>

<span data-ttu-id="e78a0-106">Dies ist die **Mode** -Eigenschaft des [**Session**](session-object.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="e78a0-106">This is the **Mode** property of the [**Session**](session-object.md) object.</span></span> <span data-ttu-id="e78a0-107">Diese Eigenschaft ist ein Wert, der das Flag für den vorgesehenen Modus für die aktuelle Installationssitzung darstellt.</span><span class="sxs-lookup"><span data-stu-id="e78a0-107">This property is a value representing the designated mode flag for the current install session.</span></span> <span data-ttu-id="e78a0-108">Die meisten modusflags sind extern schreibgeschützt, aber es können auch einige angegebene Flags festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e78a0-108">Most of the mode flags are read-only externally, but a few specified flags may be set as well.</span></span>

<span data-ttu-id="e78a0-109">Die [**msigetmode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) -Funktion gibt einen booleschen Wert "true" oder "false" zurück, der angibt, ob die angegebene Eigenschaft, die an die Funktion übertragen wird, aktuell festgelegt ist (true) oder nicht festgelegt</span><span class="sxs-lookup"><span data-stu-id="e78a0-109">The [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) function returns a Boolean TRUE or FALSE, indicating whether the specific property passed into the function is currently set (TRUE) or not set (FALSE).</span></span>

<span data-ttu-id="e78a0-110">Beachten Sie, dass nicht alle runmoduswerte des *Flags* verfügbar sind, wenn die **Mode** -Eigenschaft aus einer verzögerten benutzerdefinierten Aktion aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="e78a0-110">Note that not all the run mode values of *flag* are available when calling the **Mode** property from a deferred custom action.</span></span> <span data-ttu-id="e78a0-111">Weitere Informationen finden Sie unter Abrufen von [Kontextinformationen für benutzerdefinierte Aktionen der verzögerten Ausführung](obtaining-context-information-for-deferred-execution-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="e78a0-111">For more information, see [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md).</span></span>

<span data-ttu-id="e78a0-112">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="e78a0-112">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e78a0-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="e78a0-113">Syntax</span></span>


```JScript
propVal = Session.Mode
```



## <a name="property-value"></a><span data-ttu-id="e78a0-114">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="e78a0-114">Property value</span></span>

<span data-ttu-id="e78a0-115">Der erforderliche ganzzahlige Wert für das Flag.</span><span class="sxs-lookup"><span data-stu-id="e78a0-115">Required integer value for the flag.</span></span> <span data-ttu-id="e78a0-116">Dies muss eine der folgenden Ressourcen sein:</span><span class="sxs-lookup"><span data-stu-id="e78a0-116">Must be one of the following:</span></span>



| <span data-ttu-id="e78a0-117">Flagname</span><span class="sxs-lookup"><span data-stu-id="e78a0-117">Flag name</span></span>                                                                                                                                                                                                                                                                                                | <span data-ttu-id="e78a0-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e78a0-118">Meaning</span></span>                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="msiRunModeAdmin"></span><span id="msirunmodeadmin"></span><span id="MSIRUNMODEADMIN"></span><dl> <span data-ttu-id="e78a0-119"><dt>**msirun0deadmin**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e78a0-119"><dt>**msiRunModeAdmin**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="e78a0-120">Installation im administrativen Modus, sonst Produktinstallation.</span><span class="sxs-lookup"><span data-stu-id="e78a0-120">Administrative mode install, else product install.</span></span><br/>                                  |
| <span id="msiRunModeAdvertise"></span><span id="msirunmodeadvertise"></span><span id="MSIRUNMODEADVERTISE"></span><dl> <span data-ttu-id="e78a0-121"><dt>**msirunmodeankündigungs**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e78a0-121"><dt>**msiRunModeAdvertise**</dt> <dt>1</dt></span></span> </dl>                              | <span data-ttu-id="e78a0-122">Ankündigungs Modus für die Installation.</span><span class="sxs-lookup"><span data-stu-id="e78a0-122">Advertise mode of install.</span></span><br/>                                                          |
| <span id="msiRunModeMaintenance"></span><span id="msirunmodemaintenance"></span><span id="MSIRUNMODEMAINTENANCE"></span><dl> <span data-ttu-id="e78a0-123"><dt>**msirunmodemaintenance**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="e78a0-123"><dt>**msiRunModeMaintenance**</dt> <dt>2</dt></span></span> </dl>                      | <span data-ttu-id="e78a0-124">Wartungsmodus-Datenbank geladen.</span><span class="sxs-lookup"><span data-stu-id="e78a0-124">Maintenance mode database loaded.</span></span><br/>                                                   |
| <span id="msiRunModeRollbackEnabled"></span><span id="msirunmoderollbackenabled"></span><span id="MSIRUNMODEROLLBACKENABLED"></span><dl> <span data-ttu-id="e78a0-125"><dt>**msirunmoderollbackaktivierte**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="e78a0-125"><dt>**msiRunModeRollbackEnabled**</dt> <dt>3</dt></span></span> </dl>      | <span data-ttu-id="e78a0-126">Das Rollback ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="e78a0-126">Rollback is enabled.</span></span><br/>                                                                |
| <span id="msiRunModeLogEnabled"></span><span id="msirunmodelogenabled"></span><span id="MSIRUNMODELOGENABLED"></span><dl> <span data-ttu-id="e78a0-127"><dt>**msirunmodelogenabled**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="e78a0-127"><dt>**msiRunModeLogEnabled**</dt> <dt>4</dt></span></span> </dl>                          | <span data-ttu-id="e78a0-128">Die Protokolldatei ist aktiv.</span><span class="sxs-lookup"><span data-stu-id="e78a0-128">Log file is active.</span></span><br/>                                                                 |
| <span id="msiRunModeOperations"></span><span id="msirunmodeoperations"></span><span id="MSIRUNMODEOPERATIONS"></span><dl> <span data-ttu-id="e78a0-129"><dt>**msirunmodeoperations**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="e78a0-129"><dt>**msiRunModeOperations**</dt> <dt>5</dt></span></span> </dl>                          | <span data-ttu-id="e78a0-130">Ausführen oder spoolingvorgänge.</span><span class="sxs-lookup"><span data-stu-id="e78a0-130">Executing or spooling operations.</span></span><br/>                                                   |
| <span id="msiRunModeRebootAtEnd"></span><span id="msirunmoderebootatend"></span><span id="MSIRUNMODEREBOOTATEND"></span><dl> <span data-ttu-id="e78a0-131"><dt>**msirunmoderebootatend**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="e78a0-131"><dt>**msiRunModeRebootAtEnd**</dt> <dt>6</dt></span></span> </dl>                      | <span data-ttu-id="e78a0-132">Ein Neustart ist erforderlich (feststellbar).</span><span class="sxs-lookup"><span data-stu-id="e78a0-132">Reboot is needed (settable).</span></span><br/>                                                        |
| <span id="msiRunModeRebootNow"></span><span id="msirunmoderebootnow"></span><span id="MSIRUNMODEREBOOTNOW"></span><dl> <span data-ttu-id="e78a0-133"><dt>**msirunmoderebootnow**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="e78a0-133"><dt>**msiRunModeRebootNow**</dt> <dt>7</dt></span></span> </dl>                              | <span data-ttu-id="e78a0-134">Zum Fortsetzen der Installation (feststellbar) ist ein Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e78a0-134">Reboot is needed to continue installation (settable).</span></span><br/>                               |
| <span id="msiRunModeCabinet"></span><span id="msirunmodecabinet"></span><span id="MSIRUNMODECABINET"></span><dl> <span data-ttu-id="e78a0-135"><dt>**msirunmadecabinet**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="e78a0-135"><dt>**msiRunModeCabinet**</dt> <dt>8</dt></span></span> </dl>                                      | <span data-ttu-id="e78a0-136">Installieren von Dateien aus kabinatendateien und Dateien mithilfe der Medien Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e78a0-136">Installing files from cabinets and files using Media table.</span></span><br/>                         |
| <span id="msiRunModeSourceShortNames"></span><span id="msirunmodesourceshortnames"></span><span id="MSIRUNMODESOURCESHORTNAMES"></span><dl> <span data-ttu-id="e78a0-137"><dt>**msirunmodesourceshortnames**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="e78a0-137"><dt>**msiRunModeSourceShortNames**</dt> <dt>9</dt></span></span> </dl>  | <span data-ttu-id="e78a0-138">Für Quelldateien werden nur kurze Dateinamen verwendet.</span><span class="sxs-lookup"><span data-stu-id="e78a0-138">Source files use only short file names.</span></span><br/>                                             |
| <span id="msiRunModeTargetShortNames"></span><span id="msirunmodetargetshortnames"></span><span id="MSIRUNMODETARGETSHORTNAMES"></span><dl> <span data-ttu-id="e78a0-139"><dt>**msirunmodetargetshortnames**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="e78a0-139"><dt>**msiRunModeTargetShortNames**</dt> <dt>10</dt></span></span> </dl> | <span data-ttu-id="e78a0-140">Zieldateien sind nur kurze Dateinamen.</span><span class="sxs-lookup"><span data-stu-id="e78a0-140">Target files are to use only short file names.</span></span><br/>                                      |
| <span id="msiRunModeWindows9x"></span><span id="msirunmodewindows9x"></span><span id="MSIRUNMODEWINDOWS9X"></span><dl> <span data-ttu-id="e78a0-141"><dt>**msiRunModeWindows9x**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="e78a0-141"><dt>**msiRunModeWindows9x**</dt> <dt>12</dt></span></span> </dl>                             | <span data-ttu-id="e78a0-142">Das Betriebssystem ist Windows 98/95.</span><span class="sxs-lookup"><span data-stu-id="e78a0-142">Operating system is Windows 98/95.</span></span><br/>                                                  |
| <span id="msiRunModeZawEnabled"></span><span id="msirunmodezawenabled"></span><span id="MSIRUNMODEZAWENABLED"></span><dl> <span data-ttu-id="e78a0-143"><dt>**msirunmodezawenabled**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="e78a0-143"><dt>**msiRunModeZawEnabled**</dt> <dt>13</dt></span></span> </dl>                         | <span data-ttu-id="e78a0-144">Das Betriebssystem unterstützt die Werbung von Produkten.</span><span class="sxs-lookup"><span data-stu-id="e78a0-144">Operating system supports advertising of products.</span></span><br/>                                  |
| <span id="msiRunModeScheduled"></span><span id="msirunmodescheduled"></span><span id="MSIRUNMODESCHEDULED"></span><dl> <span data-ttu-id="e78a0-145"><dt>**msirunmodescheduled**</dt> <dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="e78a0-145"><dt>**msiRunModeScheduled**</dt> <dt>16</dt></span></span> </dl>                             | <span data-ttu-id="e78a0-146">Verzögerte [benutzerdefinierte Aktion](custom-actions.md) , die von der Installationsskript Ausführung aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="e78a0-146">Deferred [custom action](custom-actions.md) called from install script execution.</span></span><br/>  |
| <span id="msiRunModeRollback"></span><span id="msirunmoderollback"></span><span id="MSIRUNMODEROLLBACK"></span><dl> <span data-ttu-id="e78a0-147"><dt>**msirunmoderollback**</dt> <dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="e78a0-147"><dt>**msiRunModeRollback**</dt> <dt>17</dt></span></span> </dl>                                 | <span data-ttu-id="e78a0-148">Verzögerte [benutzerdefinierte Aktion](custom-actions.md) , die vom Rollback-Ausführungs Skript aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="e78a0-148">Deferred [custom action](custom-actions.md) called from rollback execution script.</span></span><br/> |
| <span id="msiRunModeCommit"></span><span id="msirunmodecommit"></span><span id="MSIRUNMODECOMMIT"></span><dl> <span data-ttu-id="e78a0-149"><dt>**msirunmodecommit**</dt> <dt>18</dt></span><span class="sxs-lookup"><span data-stu-id="e78a0-149"><dt>**msiRunModeCommit**</dt> <dt>18</dt></span></span> </dl>                                         | <span data-ttu-id="e78a0-150">Verzögerte [benutzerdefinierte Aktion](custom-actions.md) , die vom Commit-Ausführungs Skript aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="e78a0-150">Deferred [custom action](custom-actions.md) called from commit execution script.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="e78a0-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e78a0-151">Requirements</span></span>



| <span data-ttu-id="e78a0-152">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e78a0-152">Requirement</span></span> | <span data-ttu-id="e78a0-153">Wert</span><span class="sxs-lookup"><span data-stu-id="e78a0-153">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e78a0-154">Version</span><span class="sxs-lookup"><span data-stu-id="e78a0-154">Version</span></span><br/> | <span data-ttu-id="e78a0-155">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e78a0-155">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e78a0-156">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e78a0-156">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e78a0-157">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="e78a0-157">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



 

 




