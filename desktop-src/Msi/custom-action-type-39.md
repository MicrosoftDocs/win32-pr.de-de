---
description: Entwickler von Windows Installer Paketen können einen benutzerdefinierten Aktionstyp 39 verwenden, wenn die Standard Aktionen nicht ausreichen, um die Installation auszuführen.
ms.assetid: edf96cc6-ef32-4660-b4ee-50c130626e15
title: Benutzerdefinierter Aktionstyp 39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e49667fbad6e71aa8b2197b00ae9dd49f7dfff0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866091"
---
# <a name="custom-action-type-39"></a><span data-ttu-id="19db6-103">Benutzerdefinierter Aktionstyp 39</span><span class="sxs-lookup"><span data-stu-id="19db6-103">Custom Action Type 39</span></span>

<span data-ttu-id="19db6-104">Der benutzerdefinierte Aktionstyp 39 wird bei gleichzeitigen Installationen verwendet.</span><span class="sxs-lookup"><span data-stu-id="19db6-104">The Custom Action Type 39 is used with concurrent installations.</span></span> <span data-ttu-id="19db6-105">Parallele Installationen werden nicht für die Installation von Anwendungen empfohlen, die für die öffentliche Veröffentlichung vorgesehen sind.</span><span class="sxs-lookup"><span data-stu-id="19db6-105">Concurrent installations are not recommended for the installation of applications intended for release to the public.</span></span> <span data-ttu-id="19db6-106">Weitere Informationen zu gleichzeitigen Installationen finden Sie unter [parallele Installationen](concurrent-installations.md).</span><span class="sxs-lookup"><span data-stu-id="19db6-106">For information about concurrent installations please see [Concurrent Installations](concurrent-installations.md).</span></span>

<span data-ttu-id="19db6-107">Typ 39 benutzerdefinierte Aktion installiert eine Anwendung, die angekündigt oder bereits installiert ist.</span><span class="sxs-lookup"><span data-stu-id="19db6-107">Type 39 custom action installs an application that is advertised or already installed.</span></span> <span data-ttu-id="19db6-108">Dieser benutzerdefinierte Aktionstyp kann verwendet werden, um ein Produkt, das vom Installationspaket des aktuellen Produkts als gleichzeitige Installation installiert wurde, neu zu installieren oder zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="19db6-108">This custom action type may be used to reinstall or remove a product that has been installed as a concurrent installation by the current product's installation package.</span></span> <span data-ttu-id="19db6-109">Die benutzerdefinierte Aktion vom Typ 39 kann nicht zum erneuten Installieren oder Entfernen eines Produkts verwendet werden, das zuvor auf andere Weise installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="19db6-109">The Type 39 custom action cannot be used to reinstall or remove any product previously installed by any other means.</span></span> <span data-ttu-id="19db6-110">Wenn das sekundäre Produkt z. b. mithilfe des Typs 39, Typ 23 oder benutzerdefinierte Aktion 7 bei der Installation des primären Produkts installiert wird, kann eine benutzerdefinierte Aktion vom Typ 39 verwendet werden, um das sekundäre Produkt zu entfernen, wenn das primäre Produkt deinstalliert wird.</span><span class="sxs-lookup"><span data-stu-id="19db6-110">For example, if the secondary product is installed using a Type 39, Type 23, or Type 7 custom action during the installation of the primary product, a Type 39 custom action may be used to remove the secondary product when the primary product is uninstalled.</span></span>

## <a name="source"></a><span data-ttu-id="19db6-111">`Source`</span><span class="sxs-lookup"><span data-stu-id="19db6-111">Source</span></span>

<span data-ttu-id="19db6-112">Das Feld "Source" der [Tabelle "CustomAction](customaction-table.md) " enthält den Produktcode für die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="19db6-112">The Source field of the [CustomAction table](customaction-table.md) contains the product code for the application.</span></span>

## <a name="numeric-type"></a><span data-ttu-id="19db6-113">Numerischer Typ</span><span class="sxs-lookup"><span data-stu-id="19db6-113">Numeric Type</span></span>



| <span data-ttu-id="19db6-114">Typname</span><span class="sxs-lookup"><span data-stu-id="19db6-114">Type name</span></span>                                                     | <span data-ttu-id="19db6-115">Wert</span><span class="sxs-lookup"><span data-stu-id="19db6-115">Value</span></span> |
|---------------------------------------------------------------|-------|
| <span data-ttu-id="19db6-116">msidbcustomaktiontypeingestall + msidbcustomaktiontypedirectory</span><span class="sxs-lookup"><span data-stu-id="19db6-116">msidbCustomActionTypeInstall + msidbCustomActionTypeDirectory</span></span> | <span data-ttu-id="19db6-117">39</span><span class="sxs-lookup"><span data-stu-id="19db6-117">39</span></span>    |



 

## <a name="target"></a><span data-ttu-id="19db6-118">Ziel</span><span class="sxs-lookup"><span data-stu-id="19db6-118">Target</span></span>

<span data-ttu-id="19db6-119">Das Zielfeld der [Tabelle "CustomAction](customaction-table.md) " enthält Eigenschaften Einstellungen, die an die parallele Installation übermittelt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="19db6-119">The Target field of the [CustomAction table](customaction-table.md) contains property settings that are to be passed to the concurrent installation.</span></span> <span data-ttu-id="19db6-120">Diese Eigenschafts Einstellungen können Funktionen angeben.</span><span class="sxs-lookup"><span data-stu-id="19db6-120">These property settings can specify features.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="19db6-121">Rückgabe Verarbeitungsoptionen</span><span class="sxs-lookup"><span data-stu-id="19db6-121">Return Processing Options</span></span>

<span data-ttu-id="19db6-122">Der benutzerdefinierte Aktionstyp 39 schlägt fehl, wenn die Anwendung nicht angekündigt oder installiert wird.</span><span class="sxs-lookup"><span data-stu-id="19db6-122">The custom action type 39 fails if the application is not advertised or installed.</span></span> <span data-ttu-id="19db6-123">Um diesen Fehler zu vermeiden, müssen Sie **msidbcustomaktiontypecontinueflag** festlegen.</span><span class="sxs-lookup"><span data-stu-id="19db6-123">To avoid this failure, you must set the **msidbCustomActionTypeContinueflag**.</span></span>

<span data-ttu-id="19db6-124">Eine parallele Installation kann nicht asynchron ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="19db6-124">A concurrent install cannot run asynchronously.</span></span>

<span data-ttu-id="19db6-125">Weitere Informationen finden Sie unter [benutzerdefinierte Aktion Rückgabe Verarbeitungsoptionen](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="19db6-125">See [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="19db6-126">Ausführungszeit Planungsoptionen</span><span class="sxs-lookup"><span data-stu-id="19db6-126">Execution Scheduling Options</span></span>

<span data-ttu-id="19db6-127">Options-Flags sind verfügbar, um die potenzielle mehrfache Ausführung von benutzerdefinierten Aktionen zu steuern.</span><span class="sxs-lookup"><span data-stu-id="19db6-127">Options flags are available to control the potential multiple execution of custom actions.</span></span> <span data-ttu-id="19db6-128">Siehe [Optionen für die Ausführung von benutzerdefinierten Aktionen](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="19db6-128">See [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="19db6-129">Ausführungs Optionen für In-Script</span><span class="sxs-lookup"><span data-stu-id="19db6-129">In-Script Execution Options</span></span>

<span data-ttu-id="19db6-130">Diese Option wird von der benutzerdefinierten Aktion nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="19db6-130">The custom action does not use this option.</span></span>

## <a name="return-values"></a><span data-ttu-id="19db6-131">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="19db6-131">Return Values</span></span>

<span data-ttu-id="19db6-132">Der Rückgabestatus von "Benutzer beenden", "Fehler", "aussetzen" oder "Erfolg" von einer gleichzeitigen Installation wird auf die gleiche Weise wie jede andere Aktion verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="19db6-132">The return status of user exit, failure, suspend, or success from a concurrent installation is processed in the same way as any other action.</span></span> <span data-ttu-id="19db6-133">Beachten Sie jedoch, dass Windows Installer die Rückgabewerte aller Aktionen übersetzt, wenn der Rückgabewert in die Protokolldatei geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="19db6-133">Note however that Windows Installer translates the return values from all actions when it writes the return value into the log file.</span></span> <span data-ttu-id="19db6-134">Wenn der Rückgabewert der Aktion z. b. als 1 in der Protokolldatei angezeigt wird, bedeutet dies, dass die Aktion Fehler erfolgreich zurückgegeben hat \_ .</span><span class="sxs-lookup"><span data-stu-id="19db6-134">For example, if the action return value appears as 1 in the log file, this means that the action returned ERROR\_SUCCESS.</span></span> <span data-ttu-id="19db6-135">Weitere Informationen finden Sie unter [Protokollieren von Aktions Rückgabe Werten](logging-of-action-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="19db6-135">For more information, see [Logging of Action Return Values](logging-of-action-return-values.md).</span></span>

<span data-ttu-id="19db6-136">Beachten Sie Folgendes: Wenn für eine parallele Installation **msidbcustomaktiontypecontinue** festgelegt ist, wird bei der Rückgabe des Fehlers "UserExit installieren", "Fehler Installation neu starten", " \_ \_ \_ \_ Fehler \_ Installation \_ jetzt starten" \_ oder "Fehler beim \_ \_ Neustart \_ erforderlich" als Fehler \_ Erfolg behandelt.</span><span class="sxs-lookup"><span data-stu-id="19db6-136">Note that if a concurrent installation has **msidbCustomActionTypeContinue** set, then a return of ERROR\_INSTALL\_USEREXIT, ERROR\_INSTALL\_REBOOT, ERROR\_INSTALL\_REBOOT\_NOW, or ERROR\_SUCCESS\_REBOOT\_REQUIRED is treated as ERROR\_SUCCESS.</span></span> <span data-ttu-id="19db6-137">Dies bedeutet Folgendes: Wenn Sie **msidbcustomaktiontypecontinue** festlegen und die gleichzeitige Installation einen Neustart erfordert, wird die Anforderung für den Neustart ignoriert.</span><span class="sxs-lookup"><span data-stu-id="19db6-137">This means that if you set **msidbCustomActionTypeContinue** and your concurrent installation requires a restart, the requirement for the restart will be ignored.</span></span> <span data-ttu-id="19db6-138">Außerdem wird der Fehlercode von der benutzerdefinierten Aktion für die gleichzeitige Installation ignoriert.</span><span class="sxs-lookup"><span data-stu-id="19db6-138">Additionally, the error code from the concurrent installation custom action will be ignored.</span></span>

<span data-ttu-id="19db6-139">Wenn **msidbcustomaktiontypecontinue** nicht festgelegt ist, werden die folgenden Rückgabecodes zuzüglich Fehler \_ Erfolg als Erfolg behandelt und haben die folgenden Bedeutungen.</span><span class="sxs-lookup"><span data-stu-id="19db6-139">If **msidbCustomActionTypeContinue** is not set, the following return codes plus ERROR\_SUCCESS are treated as success and have the following meanings.</span></span> <span data-ttu-id="19db6-140">Andere Rückgabecodes werden als Fehler behandelt.</span><span class="sxs-lookup"><span data-stu-id="19db6-140">Other return codes are treated as failure.</span></span>



| <span data-ttu-id="19db6-141">Nachricht</span><span class="sxs-lookup"><span data-stu-id="19db6-141">Message</span></span>                          | <span data-ttu-id="19db6-142">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="19db6-142">Meaning</span></span>                                                                                              |
|----------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19db6-143">Fehler beim \_ Installieren des \_ Starts</span><span class="sxs-lookup"><span data-stu-id="19db6-143">ERROR\_INSTALL\_REBOOT</span></span>           | <span data-ttu-id="19db6-144">Das Flag für das Neustart wird am Ende der Installation auf neu starten festgelegt.</span><span class="sxs-lookup"><span data-stu-id="19db6-144">The restart flag will be set to restart at end of the installation.</span></span>                                  |
| <span data-ttu-id="19db6-145">Fehler beim \_ Installieren des \_ Neustarts. \_</span><span class="sxs-lookup"><span data-stu-id="19db6-145">ERROR\_INSTALL\_REBOOT\_NOW</span></span>      | <span data-ttu-id="19db6-146">Vor Abschluss der Installation ist ein Neustart erforderlich.</span><span class="sxs-lookup"><span data-stu-id="19db6-146">A restart is required before completing the installation.</span></span> <span data-ttu-id="19db6-147">Der Neustart wird sofort verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="19db6-147">The restart will be processed immediately.</span></span> |
| <span data-ttu-id="19db6-148">Fehler \_ beim \_ Neustart \_ erforderlich.</span><span class="sxs-lookup"><span data-stu-id="19db6-148">ERROR\_SUCCESS\_REBOOT\_REQUIRED</span></span> | <span data-ttu-id="19db6-149">Ein Neustart war erforderlich, wurde jedoch unterdrückt.</span><span class="sxs-lookup"><span data-stu-id="19db6-149">A restart was required, but was suppressed.</span></span>                                                          |



 

## <a name="remarks"></a><span data-ttu-id="19db6-150">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="19db6-150">Remarks</span></span>

<span data-ttu-id="19db6-151">Ein bedingter Ausdruck ist erforderlich, um die gleichzeitige Installation bei Installation oder Entfernung der zugeordneten Komponente oder Funktion zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="19db6-151">A conditional expression is required to enable the concurrent installation at either installation or removal of the associated component or feature.</span></span>

## <a name="related-topics"></a><span data-ttu-id="19db6-152">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="19db6-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19db6-153">Parallele Installationen</span><span class="sxs-lookup"><span data-stu-id="19db6-153">Concurrent Installations</span></span>](concurrent-installations.md)
</dt> <dt>

[<span data-ttu-id="19db6-154">Referenz zu benutzerdefinierten Aktionen</span><span class="sxs-lookup"><span data-stu-id="19db6-154">Custom Action Reference</span></span>](custom-action-reference.md)
</dt> <dt>

[<span data-ttu-id="19db6-155">Informationen zu benutzerdefinierten Aktionen</span><span class="sxs-lookup"><span data-stu-id="19db6-155">About Custom Actions</span></span>](about-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="19db6-156">Verwenden von benutzerdefinierten Aktionen</span><span class="sxs-lookup"><span data-stu-id="19db6-156">Using Custom Actions</span></span>](using-custom-actions.md)
</dt> </dl>

 

 



