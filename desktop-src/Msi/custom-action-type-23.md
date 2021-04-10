---
description: Entwickler von Windows Installer Paketen können einen benutzerdefinierten Aktionstyp 23 verwenden, wenn die Standard Aktionen nicht ausreichen, um die Installation auszuführen.
ms.assetid: 8219f157-585d-4733-8e10-c05813b398ba
title: Benutzerdefinierter Aktionstyp 23
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05576c44ab634dc117501a89e6b86594f5483458
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869252"
---
# <a name="custom-action-type-23"></a><span data-ttu-id="8732b-103">Benutzerdefinierter Aktionstyp 23</span><span class="sxs-lookup"><span data-stu-id="8732b-103">Custom Action Type 23</span></span>

<span data-ttu-id="8732b-104">Der benutzerdefinierte Aktionstyp 23 wird bei gleichzeitigen Installationen verwendet.</span><span class="sxs-lookup"><span data-stu-id="8732b-104">The Custom Action Type 23 is used with concurrent installations.</span></span> <span data-ttu-id="8732b-105">Parallele Installationen werden nicht für die Installation von Anwendungen empfohlen, die für die öffentliche Veröffentlichung vorgesehen sind.</span><span class="sxs-lookup"><span data-stu-id="8732b-105">Concurrent installations are not recommended for the installation of applications intended for release to the public.</span></span> <span data-ttu-id="8732b-106">Weitere Informationen zu gleichzeitigen Installationen finden Sie unter [parallele Installationen](concurrent-installations.md).</span><span class="sxs-lookup"><span data-stu-id="8732b-106">For information about concurrent installations please see [Concurrent Installations](concurrent-installations.md).</span></span>

<span data-ttu-id="8732b-107">Durch diese benutzerdefinierte Aktion wird ein weiteres Installer-Paket installiert, das sich in der Quell Struktur der Anwendung befindet.</span><span class="sxs-lookup"><span data-stu-id="8732b-107">This custom action installs another installer package that resides in the application's source tree.</span></span>

## <a name="source"></a><span data-ttu-id="8732b-108">`Source`</span><span class="sxs-lookup"><span data-stu-id="8732b-108">Source</span></span>

<span data-ttu-id="8732b-109">Der Speicherort des gleichzeitigen Installationspakets wird relativ zum Stamm des Quell Speicher Orts angegeben, der im Quellfeld der [Tabelle "CustomAction](customaction-table.md)" angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="8732b-109">The location of the concurrent installation package is specified relative to the root of the source location shown in the Source field of the [CustomAction table](customaction-table.md).</span></span>

## <a name="numeric-type"></a><span data-ttu-id="8732b-110">Numerischer Typ</span><span class="sxs-lookup"><span data-stu-id="8732b-110">Numeric Type</span></span>



| <span data-ttu-id="8732b-111">Typname</span><span class="sxs-lookup"><span data-stu-id="8732b-111">Type name</span></span>                                                      | <span data-ttu-id="8732b-112">Wert</span><span class="sxs-lookup"><span data-stu-id="8732b-112">Value</span></span> |
|----------------------------------------------------------------|-------|
| <span data-ttu-id="8732b-113">msidbcustomaktiontypeinstall + msidbcustomaktionsesourcefile</span><span class="sxs-lookup"><span data-stu-id="8732b-113">msidbCustomActionTypeInstall + msidbCustomActionTypeSourceFile</span></span> | <span data-ttu-id="8732b-114">23</span><span class="sxs-lookup"><span data-stu-id="8732b-114">23</span></span>    |



 

## <a name="target"></a><span data-ttu-id="8732b-115">Ziel</span><span class="sxs-lookup"><span data-stu-id="8732b-115">Target</span></span>

<span data-ttu-id="8732b-116">Das Zielfeld der [Tabelle "CustomAction](customaction-table.md) " enthält Eigenschaften Einstellungen, die an die parallele Installation übermittelt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8732b-116">The Target field of the [CustomAction table](customaction-table.md) contains property settings that are to be passed to the concurrent installation.</span></span> <span data-ttu-id="8732b-117">Diese Eigenschafts Einstellungen können Funktionen angeben.</span><span class="sxs-lookup"><span data-stu-id="8732b-117">These property settings can specify features.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="8732b-118">Rückgabe Verarbeitungsoptionen</span><span class="sxs-lookup"><span data-stu-id="8732b-118">Return Processing Options</span></span>

<span data-ttu-id="8732b-119">Die Sitzung für die gleichzeitige Installation wird im aktuellen Prozess als separater Thread ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8732b-119">The concurrent installation session runs as a separate thread in the current process.</span></span> <span data-ttu-id="8732b-120">Eine parallele Installation kann nicht asynchron ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="8732b-120">A concurrent installation cannot run asynchronously.</span></span>

<span data-ttu-id="8732b-121">Weitere Informationen finden Sie unter " [benutzerdefinierte Aktion: Rückgabe Verarbeitungsoptionen](custom-action-return-processing-options.md)".</span><span class="sxs-lookup"><span data-stu-id="8732b-121">For more information, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="8732b-122">Ausführungszeit Planungsoptionen</span><span class="sxs-lookup"><span data-stu-id="8732b-122">Execution Scheduling Options</span></span>

<span data-ttu-id="8732b-123">Options-Flags sind verfügbar, um die potenzielle mehrfache Ausführung von benutzerdefinierten Aktionen zu steuern.</span><span class="sxs-lookup"><span data-stu-id="8732b-123">Options flags are available to control the potential multiple execution of custom actions.</span></span> <span data-ttu-id="8732b-124">Weitere Informationen finden Sie unter [Optionen für die Ausführungsplanung für benutzerdefinierte Aktionen](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="8732b-124">For more information, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="8732b-125">Ausführungs Optionen für In-Script</span><span class="sxs-lookup"><span data-stu-id="8732b-125">In-Script Execution Options</span></span>

<span data-ttu-id="8732b-126">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="8732b-126">Not used.</span></span>

## <a name="return-values"></a><span data-ttu-id="8732b-127">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="8732b-127">Return Values</span></span>

<span data-ttu-id="8732b-128">Der Rückgabestatus von "Benutzer beenden", "Fehler", "aussetzen" oder "Erfolg" von einer gleichzeitigen Installation wird auf die gleiche Weise wie jede andere Aktion verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="8732b-128">The return status of user exit, failure, suspend, or success from a concurrent installation is processed in the same way as any other action.</span></span> <span data-ttu-id="8732b-129">Beachten Sie jedoch, dass Windows Installer die Rückgabewerte aller Aktionen übersetzt, wenn der Rückgabewert in die Protokolldatei geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="8732b-129">Note however, that Windows Installer translates the return values from all actions when it writes the return value into the log file.</span></span> <span data-ttu-id="8732b-130">Wenn der Rückgabewert der Aktion z. b. als 1 in der Protokolldatei angezeigt wird, bedeutet dies, dass die Aktion Fehler erfolgreich zurückgegeben hat \_ .</span><span class="sxs-lookup"><span data-stu-id="8732b-130">For example, if the action return value appears as 1 in the log file, this means that the action returned ERROR\_SUCCESS.</span></span> <span data-ttu-id="8732b-131">Weitere Informationen finden Sie unter [Protokollieren von Aktions Rückgabe Werten](logging-of-action-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="8732b-131">For more information, see [Logging of Action Return Values](logging-of-action-return-values.md).</span></span>

<span data-ttu-id="8732b-132">Beachten Sie Folgendes: Wenn für eine parallele Installation **msidbcustomaktiontypecontinue** festgelegt ist, wird bei der Rückgabe des Fehlers "UserExit installieren", "Fehler Installation neu starten", " \_ \_ \_ \_ Fehler \_ Installation \_ jetzt starten" \_ oder "Fehler beim \_ \_ Neustart \_ erforderlich" als Fehler \_ Erfolg behandelt.</span><span class="sxs-lookup"><span data-stu-id="8732b-132">Note that if a concurrent installation has **msidbCustomActionTypeContinue** set, then a return of ERROR\_INSTALL\_USEREXIT, ERROR\_INSTALL\_REBOOT, ERROR\_INSTALL\_REBOOT\_NOW, or ERROR\_SUCCESS\_REBOOT\_REQUIRED is treated as ERROR\_SUCCESS.</span></span> <span data-ttu-id="8732b-133">Dies bedeutet Folgendes: Wenn Sie **msidbcustomaktiontypecontinue** festlegen und die gleichzeitige Installation einen Neustart erfordert, wird die Anforderung für den Neustart ignoriert.</span><span class="sxs-lookup"><span data-stu-id="8732b-133">This means that if you set **msidbCustomActionTypeContinue** and your concurrent installation requires a restart, the requirement for the restart will be ignored.</span></span> <span data-ttu-id="8732b-134">Außerdem wird der Fehlercode von der benutzerdefinierten Aktion für die gleichzeitige Installation ignoriert.</span><span class="sxs-lookup"><span data-stu-id="8732b-134">Additionally, the error code from the concurrent installation custom action will be ignored.</span></span>

<span data-ttu-id="8732b-135">Wenn **msidbcustomaktiontypecontinue** nicht festgelegt ist, werden die folgenden Rückgabecodes zuzüglich Fehler \_ Erfolg als Erfolg behandelt und haben die folgenden Bedeutungen.</span><span class="sxs-lookup"><span data-stu-id="8732b-135">If **msidbCustomActionTypeContinue** is not set, the following return codes plus ERROR\_SUCCESS are treated as success and have the following meanings.</span></span> <span data-ttu-id="8732b-136">Andere Rückgabecodes werden als Fehler behandelt.</span><span class="sxs-lookup"><span data-stu-id="8732b-136">Other return codes are treated as failure.</span></span>



| <span data-ttu-id="8732b-137">Nachricht</span><span class="sxs-lookup"><span data-stu-id="8732b-137">Message</span></span>                          | <span data-ttu-id="8732b-138">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="8732b-138">Meaning</span></span>                                                                                              |
|----------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8732b-139">Fehler beim \_ Installieren des \_ Starts</span><span class="sxs-lookup"><span data-stu-id="8732b-139">ERROR\_INSTALL\_REBOOT</span></span>           | <span data-ttu-id="8732b-140">Das Flag für das Neustart wird am Ende der Installation auf neu starten festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8732b-140">The restart flag will be set to restart at end of the installation.</span></span>                                  |
| <span data-ttu-id="8732b-141">Fehler beim \_ Installieren des \_ Neustarts. \_</span><span class="sxs-lookup"><span data-stu-id="8732b-141">ERROR\_INSTALL\_REBOOT\_NOW</span></span>      | <span data-ttu-id="8732b-142">Vor Abschluss der Installation ist ein Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8732b-142">A restart is required before completing the installation.</span></span> <span data-ttu-id="8732b-143">Der Neustart wird sofort verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="8732b-143">The restart will be processed immediately.</span></span> |
| <span data-ttu-id="8732b-144">Fehler \_ beim \_ Neustart \_ erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8732b-144">ERROR\_SUCCESS\_REBOOT\_REQUIRED</span></span> | <span data-ttu-id="8732b-145">Ein Neustart war erforderlich, wurde jedoch unterdrückt.</span><span class="sxs-lookup"><span data-stu-id="8732b-145">A restart was required, but was suppressed.</span></span>                                                          |



 

## <a name="remarks"></a><span data-ttu-id="8732b-146">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8732b-146">Remarks</span></span>

<span data-ttu-id="8732b-147">Ein bedingter Ausdruck ist erforderlich, um die gleichzeitige Installation bei Installation oder Entfernung der zugeordneten Komponente oder Funktion zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="8732b-147">A conditional expression is required to enable the concurrent installation at either installation or removal of the associated component or feature.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8732b-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8732b-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8732b-149">Parallele Installationen</span><span class="sxs-lookup"><span data-stu-id="8732b-149">Concurrent Installations</span></span>](concurrent-installations.md)
</dt> <dt>

[<span data-ttu-id="8732b-150">Referenz zu benutzerdefinierten Aktionen</span><span class="sxs-lookup"><span data-stu-id="8732b-150">Custom Action Reference</span></span>](custom-action-reference.md)
</dt> <dt>

[<span data-ttu-id="8732b-151">Informationen zu benutzerdefinierten Aktionen</span><span class="sxs-lookup"><span data-stu-id="8732b-151">About Custom Actions</span></span>](about-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="8732b-152">Verwenden von benutzerdefinierten Aktionen</span><span class="sxs-lookup"><span data-stu-id="8732b-152">Using Custom Actions</span></span>](using-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="8732b-153">Rückgabewerte für benutzerdefinierte Aktionen</span><span class="sxs-lookup"><span data-stu-id="8732b-153">Custom Action Return Values</span></span>](custom-action-return-values.md)
</dt> </dl>

 

 



