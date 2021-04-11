---
description: Entwickler von Windows Installer Paketen können einen benutzerdefinierten Aktionstyp 7 verwenden, wenn die Standard Aktionen nicht ausreichen, um die Installation auszuführen.
ms.assetid: 4a8f35f9-58a8-417e-b72e-159f4af7d83f
title: Benutzerdefinierter Aktionstyp 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2d3cc1c68fae098c6ef70797ed87df887ff898a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042397"
---
# <a name="custom-action-type-7"></a><span data-ttu-id="d3f91-103">Benutzerdefinierter Aktionstyp 7</span><span class="sxs-lookup"><span data-stu-id="d3f91-103">Custom Action Type 7</span></span>

<span data-ttu-id="d3f91-104">Der benutzerdefinierte Aktionstyp 7 wird bei gleichzeitigen Installationen verwendet.</span><span class="sxs-lookup"><span data-stu-id="d3f91-104">The Custom Action Type 7 is used with concurrent installations.</span></span> <span data-ttu-id="d3f91-105">Parallele Installationen werden nicht für die Installation von Anwendungen empfohlen, die für die öffentliche Veröffentlichung vorgesehen sind.</span><span class="sxs-lookup"><span data-stu-id="d3f91-105">Concurrent installations are not recommended for the installation of applications intended for release to the public.</span></span> <span data-ttu-id="d3f91-106">Weitere Informationen zu gleichzeitigen Installationen finden Sie unter [parallele Installationen](concurrent-installations.md).</span><span class="sxs-lookup"><span data-stu-id="d3f91-106">For more information about concurrent installations please see [Concurrent Installations](concurrent-installations.md).</span></span>

<span data-ttu-id="d3f91-107">Durch diese benutzerdefinierte Aktion wird ein anderes Installer-Paket installiert, das innerhalb des ersten Pakets geschachtelt ist.</span><span class="sxs-lookup"><span data-stu-id="d3f91-107">This custom action installs another installer package that is nested inside of the first package.</span></span>

## <a name="source"></a><span data-ttu-id="d3f91-108">`Source`</span><span class="sxs-lookup"><span data-stu-id="d3f91-108">Source</span></span>

<span data-ttu-id="d3f91-109">Die Datenbank der gleichzeitigen Anwendung wird als unter Speicher des Pakets gespeichert, und der Name des unter Speichers wird im Feld "Source" der [Tabelle "CustomAction](customaction-table.md)" angegeben.</span><span class="sxs-lookup"><span data-stu-id="d3f91-109">The database of the concurrent application is stored as a substorage of the package, and the name of the substorage is designated in the Source field of the [CustomAction table](customaction-table.md).</span></span>

## <a name="numeric-type"></a><span data-ttu-id="d3f91-110">Numerischer Typ</span><span class="sxs-lookup"><span data-stu-id="d3f91-110">Numeric Type</span></span>



| <span data-ttu-id="d3f91-111">Typname</span><span class="sxs-lookup"><span data-stu-id="d3f91-111">Type name</span></span>                                                      | <span data-ttu-id="d3f91-112">Wert</span><span class="sxs-lookup"><span data-stu-id="d3f91-112">Value</span></span> |
|----------------------------------------------------------------|-------|
| <span data-ttu-id="d3f91-113">msidbcustomaktiontypeingestall + msidbcustomaktiontypebinarydata</span><span class="sxs-lookup"><span data-stu-id="d3f91-113">msidbCustomActionTypeInstall + msidbCustomActionTypeBinaryData</span></span> | <span data-ttu-id="d3f91-114">7</span><span class="sxs-lookup"><span data-stu-id="d3f91-114">7</span></span>     |



 

## <a name="target"></a><span data-ttu-id="d3f91-115">Ziel</span><span class="sxs-lookup"><span data-stu-id="d3f91-115">Target</span></span>

<span data-ttu-id="d3f91-116">Das Zielfeld der [Tabelle "CustomAction](customaction-table.md) " enthält Eigenschaften Einstellungen, die an die parallele Installation übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="d3f91-116">The Target field of the [CustomAction table](customaction-table.md) contains property settings to be passed to the concurrent installation.</span></span> <span data-ttu-id="d3f91-117">Diese Eigenschafts Einstellungen können Funktionen angeben.</span><span class="sxs-lookup"><span data-stu-id="d3f91-117">These property settings can specify features.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="d3f91-118">Rückgabe Verarbeitungsoptionen</span><span class="sxs-lookup"><span data-stu-id="d3f91-118">Return Processing Options</span></span>

<span data-ttu-id="d3f91-119">Die Sitzung für die gleichzeitige Installation wird im aktuellen Prozess als separater Thread ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d3f91-119">The concurrent installation session runs as a separate thread in the current process.</span></span> <span data-ttu-id="d3f91-120">Eine parallele Installation kann nicht asynchron ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d3f91-120">A concurrent installation cannot run asynchronously.</span></span>

<span data-ttu-id="d3f91-121">Weitere Informationen finden Sie unter [benutzerdefinierte Aktion Rückgabe Verarbeitungsoptionen](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="d3f91-121">See [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="d3f91-122">Ausführungszeit Planungsoptionen</span><span class="sxs-lookup"><span data-stu-id="d3f91-122">Execution Scheduling Options</span></span>

<span data-ttu-id="d3f91-123">Options-Flags sind verfügbar, um die potenzielle mehrfache Ausführung von benutzerdefinierten Aktionen zu steuern.</span><span class="sxs-lookup"><span data-stu-id="d3f91-123">Options flags are available to control the potential multiple execution of custom actions.</span></span> <span data-ttu-id="d3f91-124">Siehe [Optionen für die Ausführung von benutzerdefinierten Aktionen](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="d3f91-124">See [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="d3f91-125">Ausführungs Optionen für In-Script</span><span class="sxs-lookup"><span data-stu-id="d3f91-125">In-Script Execution Options</span></span>

<span data-ttu-id="d3f91-126">Diese benutzerdefinierte Aktion verwendet diese Option nicht.</span><span class="sxs-lookup"><span data-stu-id="d3f91-126">This custom action does not use this option.</span></span>

## <a name="return-values"></a><span data-ttu-id="d3f91-127">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="d3f91-127">Return Values</span></span>

<span data-ttu-id="d3f91-128">Der Rückgabestatus von "Benutzer beenden", "Fehler", "aussetzen" oder "Erfolg" von einer gleichzeitigen Installation wird auf die gleiche Weise wie jede andere Aktion verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="d3f91-128">The return status of user exit, failure, suspend, or success from a concurrent installation is processed in the same way as any other action.</span></span> <span data-ttu-id="d3f91-129">Beachten Sie jedoch, dass Windows Installer die Rückgabewerte aller Aktionen übersetzt, wenn der Rückgabewert in die Protokolldatei geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="d3f91-129">Note however that Windows Installer translates the return values from all actions when it writes the return value into the log file.</span></span> <span data-ttu-id="d3f91-130">Wenn der Rückgabewert der Aktion z. b. als 1 in der Protokolldatei angezeigt wird, bedeutet dies, dass die Aktion Fehler erfolgreich zurückgegeben hat \_ .</span><span class="sxs-lookup"><span data-stu-id="d3f91-130">For example, if the action return value appears as 1 in the log file, this means that the action returned ERROR\_SUCCESS.</span></span> <span data-ttu-id="d3f91-131">Weitere Informationen zu dieser Übersetzung finden Sie [unter Protokollieren von Aktions Rückgabe Werten](logging-of-action-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="d3f91-131">For more information about this translation see [Logging of Action Return Values](logging-of-action-return-values.md).</span></span>

<span data-ttu-id="d3f91-132">Beachten Sie Folgendes: Wenn für eine parallele Installation **msidbcustomaktiontypecontinue** festgelegt ist, wird bei der Rückgabe des Fehlers "UserExit installieren", "Fehler Installation neu starten", " \_ \_ \_ \_ Fehler \_ Installation \_ jetzt starten" \_ oder "Fehler beim \_ \_ Neustart \_ erforderlich" als Fehler \_ Erfolg behandelt.</span><span class="sxs-lookup"><span data-stu-id="d3f91-132">Note that if a concurrent install has **msidbCustomActionTypeContinue** set, then a return of ERROR\_INSTALL\_USEREXIT, ERROR\_INSTALL\_REBOOT, ERROR\_INSTALL\_REBOOT\_NOW, or ERROR\_SUCCESS\_REBOOT\_REQUIRED is treated as ERROR\_SUCCESS.</span></span> <span data-ttu-id="d3f91-133">Dies bedeutet Folgendes: Wenn Sie **msidbcustomaktiontypecontinue** festlegen und die gleichzeitige Installation einen Neustart erfordert, wird die Anforderung für den Neustart ignoriert.</span><span class="sxs-lookup"><span data-stu-id="d3f91-133">This means that if you set **msidbCustomActionTypeContinue** and your concurrent installation requires a restart, the requirement for the restart will be ignored.</span></span> <span data-ttu-id="d3f91-134">Außerdem wird der Fehlercode von der benutzerdefinierten Aktion für die gleichzeitige Installation ignoriert.</span><span class="sxs-lookup"><span data-stu-id="d3f91-134">Additionally, the error code from the concurrent installation custom action will be ignored.</span></span>

<span data-ttu-id="d3f91-135">Wenn **msidbcustomaktiontypecontinue** nicht festgelegt ist, werden die folgenden Rückgabecodes zuzüglich Fehler \_ Erfolg als Erfolg behandelt und haben die folgenden Bedeutungen.</span><span class="sxs-lookup"><span data-stu-id="d3f91-135">If **msidbCustomActionTypeContinue** is not set, the following return codes plus ERROR\_SUCCESS are treated as success and have the following meanings.</span></span> <span data-ttu-id="d3f91-136">Andere Rückgabecodes werden als Fehler behandelt.</span><span class="sxs-lookup"><span data-stu-id="d3f91-136">Other return codes are treated as failure.</span></span>



| <span data-ttu-id="d3f91-137">Nachricht</span><span class="sxs-lookup"><span data-stu-id="d3f91-137">Message</span></span>                          | <span data-ttu-id="d3f91-138">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d3f91-138">Meaning</span></span>                                                                                              |
|----------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3f91-139">Fehler beim \_ Installieren des \_ Starts</span><span class="sxs-lookup"><span data-stu-id="d3f91-139">ERROR\_INSTALL\_REBOOT</span></span>           | <span data-ttu-id="d3f91-140">Das Flag für das Neustart wird am Ende der Installation auf neu starten festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d3f91-140">The restart flag will be set to restart at end of the installation.</span></span>                                  |
| <span data-ttu-id="d3f91-141">Fehler beim \_ Installieren des \_ Neustarts. \_</span><span class="sxs-lookup"><span data-stu-id="d3f91-141">ERROR\_INSTALL\_REBOOT\_NOW</span></span>      | <span data-ttu-id="d3f91-142">Vor Abschluss der Installation ist ein Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d3f91-142">A restart is required before completing the installation.</span></span> <span data-ttu-id="d3f91-143">Der Neustart wird sofort verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="d3f91-143">The restart will be processed immediately.</span></span> |
| <span data-ttu-id="d3f91-144">Fehler \_ beim \_ Neustart \_ erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d3f91-144">ERROR\_SUCCESS\_REBOOT\_REQUIRED</span></span> | <span data-ttu-id="d3f91-145">Ein Neustart war erforderlich, wurde jedoch unterdrückt.</span><span class="sxs-lookup"><span data-stu-id="d3f91-145">A restart was required, but was suppressed.</span></span>                                                          |



 

## <a name="remarks"></a><span data-ttu-id="d3f91-146">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d3f91-146">Remarks</span></span>

<span data-ttu-id="d3f91-147">Ein bedingter Ausdruck ist erforderlich, um die gleichzeitige Installation bei Installation oder Entfernung der zugeordneten Komponente oder Funktion zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d3f91-147">A conditional expression is required to enable the concurrent installation at either installation or removal of the associated component or feature.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d3f91-148">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d3f91-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3f91-149">Parallele Installationen</span><span class="sxs-lookup"><span data-stu-id="d3f91-149">Concurrent Installations</span></span>](concurrent-installations.md)
</dt> <dt>

[<span data-ttu-id="d3f91-150">Referenz zu benutzerdefinierten Aktionen</span><span class="sxs-lookup"><span data-stu-id="d3f91-150">Custom Action Reference</span></span>](custom-action-reference.md)
</dt> <dt>

[<span data-ttu-id="d3f91-151">Informationen zu benutzerdefinierten Aktionen</span><span class="sxs-lookup"><span data-stu-id="d3f91-151">About Custom Actions</span></span>](about-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="d3f91-152">Verwenden von benutzerdefinierten Aktionen</span><span class="sxs-lookup"><span data-stu-id="d3f91-152">Using Custom Actions</span></span>](using-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="d3f91-153">Rückgabewerte für benutzerdefinierte Aktionen</span><span class="sxs-lookup"><span data-stu-id="d3f91-153">Custom Action Return Values</span></span>](custom-action-return-values.md)
</dt> </dl>

 

 



