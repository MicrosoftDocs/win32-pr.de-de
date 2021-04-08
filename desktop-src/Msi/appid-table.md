---
description: Die AppID-Tabelle oder die Registrierungs Tabelle gibt an, dass das Installationsprogramm DCOM-Server konfiguriert und registriert, um einen der folgenden Schritte während einer Installation durchzuführen.
ms.assetid: d76ed6df-944b-4996-bf07-e42ceb7a1b69
title: AppID-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07fa202907c094d8c12f73d838f5ad1d6b942125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864491"
---
# <a name="appid-table"></a><span data-ttu-id="7335e-103">AppID-Tabelle</span><span class="sxs-lookup"><span data-stu-id="7335e-103">AppId Table</span></span>

<span data-ttu-id="7335e-104">Die AppID-Tabelle oder die [Registrierungs Tabelle](registry-table.md) gibt an, dass das Installationsprogramm DCOM-Server konfiguriert und registriert, um einen der folgenden Schritte während einer Installation durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="7335e-104">The AppId table or the [Registry table](registry-table.md) specifies that the installer configure and register DCOM servers to do one of the following during an installation.</span></span>

-   <span data-ttu-id="7335e-105">Führt den DCOM-Server unter einer anderen Identität aus als der Benutzer, der den Server aktiviert.</span><span class="sxs-lookup"><span data-stu-id="7335e-105">Run the DCOM server under a different identity than the user activating the server.</span></span> <span data-ttu-id="7335e-106">Beispielsweise, um einen DCOM-Server so zu konfigurieren, dass er immer als interaktiver Benutzer oder als vordefinierter Benutzer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7335e-106">For example, to configure a DCOM server to always run as an interactive user or as a predefined user.</span></span>
-   <span data-ttu-id="7335e-107">Führen Sie den DCOM-Server als Dienst aus.</span><span class="sxs-lookup"><span data-stu-id="7335e-107">Run the DCOM server as a service.</span></span>
-   <span data-ttu-id="7335e-108">Konfigurieren Sie den Standard Sicherheits Zugriff für den DCOM-Server.</span><span class="sxs-lookup"><span data-stu-id="7335e-108">Configure the default security access for the DCOM server.</span></span>
-   <span data-ttu-id="7335e-109">Registrieren Sie den DCOM-Server so, dass er auf einem anderen Computer aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="7335e-109">Register the DCOM server such that it is activated on a different computer.</span></span>

<span data-ttu-id="7335e-110">Diese Tabelle wird bei der Installation der Komponente verarbeitet, die dem DCOM-Server in der \_ Spalte Komponente der [Klassen Tabelle](class-table.md)zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="7335e-110">This table is processed at the installation of the component associated with the DCOM server in the \_Component column of the [Class table](class-table.md).</span></span> <span data-ttu-id="7335e-111">Eine AppID wird nicht angekündigt.</span><span class="sxs-lookup"><span data-stu-id="7335e-111">An AppId is not advertised.</span></span>

<span data-ttu-id="7335e-112">Die AppID-Tabelle weist die folgenden Spalten auf.</span><span class="sxs-lookup"><span data-stu-id="7335e-112">The AppId table has the following columns.</span></span>



| <span data-ttu-id="7335e-113">Spalte</span><span class="sxs-lookup"><span data-stu-id="7335e-113">Column</span></span>               | <span data-ttu-id="7335e-114">Typ</span><span class="sxs-lookup"><span data-stu-id="7335e-114">Type</span></span>                       | <span data-ttu-id="7335e-115">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="7335e-115">Key</span></span> | <span data-ttu-id="7335e-116">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="7335e-116">Nullable</span></span> |
|----------------------|----------------------------|-----|----------|
| <span data-ttu-id="7335e-117">AppId</span><span class="sxs-lookup"><span data-stu-id="7335e-117">AppId</span></span>                | [<span data-ttu-id="7335e-118">GUID</span><span class="sxs-lookup"><span data-stu-id="7335e-118">GUID</span></span>](guid.md)           | <span data-ttu-id="7335e-119">J</span><span class="sxs-lookup"><span data-stu-id="7335e-119">Y</span></span>   | <span data-ttu-id="7335e-120">N</span><span class="sxs-lookup"><span data-stu-id="7335e-120">N</span></span>        |
| <span data-ttu-id="7335e-121">RemoteServerName</span><span class="sxs-lookup"><span data-stu-id="7335e-121">RemoteServerName</span></span>     | [<span data-ttu-id="7335e-122">Großformatige</span><span class="sxs-lookup"><span data-stu-id="7335e-122">Formatted</span></span>](formatted.md) | <span data-ttu-id="7335e-123">N</span><span class="sxs-lookup"><span data-stu-id="7335e-123">N</span></span>   | <span data-ttu-id="7335e-124">J</span><span class="sxs-lookup"><span data-stu-id="7335e-124">Y</span></span>        |
| <span data-ttu-id="7335e-125">LocalService</span><span class="sxs-lookup"><span data-stu-id="7335e-125">LocalService</span></span>         | [<span data-ttu-id="7335e-126">Text</span><span class="sxs-lookup"><span data-stu-id="7335e-126">Text</span></span>](text.md)           | <span data-ttu-id="7335e-127">N</span><span class="sxs-lookup"><span data-stu-id="7335e-127">N</span></span>   | <span data-ttu-id="7335e-128">J</span><span class="sxs-lookup"><span data-stu-id="7335e-128">Y</span></span>        |
| <span data-ttu-id="7335e-129">Service Parameters</span><span class="sxs-lookup"><span data-stu-id="7335e-129">ServiceParameters</span></span>    | [<span data-ttu-id="7335e-130">Text</span><span class="sxs-lookup"><span data-stu-id="7335e-130">Text</span></span>](text.md)           | <span data-ttu-id="7335e-131">N</span><span class="sxs-lookup"><span data-stu-id="7335e-131">N</span></span>   | <span data-ttu-id="7335e-132">J</span><span class="sxs-lookup"><span data-stu-id="7335e-132">Y</span></span>        |
| <span data-ttu-id="7335e-133">Dllersatz</span><span class="sxs-lookup"><span data-stu-id="7335e-133">DllSurrogate</span></span>         | [<span data-ttu-id="7335e-134">Text</span><span class="sxs-lookup"><span data-stu-id="7335e-134">Text</span></span>](text.md)           | <span data-ttu-id="7335e-135">N</span><span class="sxs-lookup"><span data-stu-id="7335e-135">N</span></span>   | <span data-ttu-id="7335e-136">J</span><span class="sxs-lookup"><span data-stu-id="7335e-136">Y</span></span>        |
| <span data-ttu-id="7335e-137">Activateatstorage</span><span class="sxs-lookup"><span data-stu-id="7335e-137">ActivateAtStorage</span></span>    | [<span data-ttu-id="7335e-138">Integer</span><span class="sxs-lookup"><span data-stu-id="7335e-138">Integer</span></span>](integer.md)     | <span data-ttu-id="7335e-139">N</span><span class="sxs-lookup"><span data-stu-id="7335e-139">N</span></span>   | <span data-ttu-id="7335e-140">J</span><span class="sxs-lookup"><span data-stu-id="7335e-140">Y</span></span>        |
| <span data-ttu-id="7335e-141">Runasinteractiveuser</span><span class="sxs-lookup"><span data-stu-id="7335e-141">RunAsInteractiveUser</span></span> | [<span data-ttu-id="7335e-142">Integer</span><span class="sxs-lookup"><span data-stu-id="7335e-142">Integer</span></span>](integer.md)     | <span data-ttu-id="7335e-143">N</span><span class="sxs-lookup"><span data-stu-id="7335e-143">N</span></span>   | <span data-ttu-id="7335e-144">J</span><span class="sxs-lookup"><span data-stu-id="7335e-144">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="7335e-145">Spalten</span><span class="sxs-lookup"><span data-stu-id="7335e-145">Columns</span></span>

<dl> <dt>

<span data-ttu-id="7335e-146"><span id="AppId"></span><span id="appid"></span><span id="APPID"></span>AppID</span><span class="sxs-lookup"><span data-stu-id="7335e-146"><span id="AppId"></span><span id="appid"></span><span id="APPID"></span>AppId</span></span>
</dt> <dd>

<span data-ttu-id="7335e-147">Die AppID-Spalte der [Klassen Tabelle](class-table.md) ist ein Fremdschlüssel in diese Spalte der AppID-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="7335e-147">The AppId column of the [Class table](class-table.md) is a foreign key into this column of the AppId table.</span></span> <span data-ttu-id="7335e-148">Diese Spalte enthält den AppID-Wert, der unter der CLSID geschrieben wird, und erstellt den AppID-GUID-Schlüssel unter HKCR \\ AppID.</span><span class="sxs-lookup"><span data-stu-id="7335e-148">This column contains the AppId value that will be written under the CLSID and creates the AppId GUID key under HKCR\\AppId.</span></span>

</dd> <dt>

<span data-ttu-id="7335e-149"><span id="RemoteServerName"></span><span id="remoteservername"></span><span id="REMOTESERVERNAME"></span>Remote Servername</span><span class="sxs-lookup"><span data-stu-id="7335e-149"><span id="RemoteServerName"></span><span id="remoteservername"></span><span id="REMOTESERVERNAME"></span>RemoteServerName</span></span>
</dt> <dd>

<span data-ttu-id="7335e-150">Diese Spalte enthält den Wert von "Remoteservername" = <xxxx> , der unter HKCR \\ AppID \\ {AppID} geschrieben wird \\ .</span><span class="sxs-lookup"><span data-stu-id="7335e-150">This column contains the value of "RemoteServerName"=<xxxx> that will be written under HKCR\\AppID\\{AppID}\\ .</span></span>

</dd> <dt>

<span data-ttu-id="7335e-151"><span id="LocalService"></span><span id="localservice"></span><span id="LOCALSERVICE"></span>LocalService</span><span class="sxs-lookup"><span data-stu-id="7335e-151"><span id="LocalService"></span><span id="localservice"></span><span id="LOCALSERVICE"></span>LocalService</span></span>
</dt> <dd>

<span data-ttu-id="7335e-152">Diese Spalte enthält den Wert von LocalService, der unter HKCR \\ AppID \\ { <appid> } "LocalService" = geschrieben wird <xxx> .</span><span class="sxs-lookup"><span data-stu-id="7335e-152">This column contains the value of LocalService that will be written under HKCR\\AppID\\{<appid>} "LocalService"=<xxx>.</span></span>

</dd> <dt>

<span data-ttu-id="7335e-153"><span id="ServiceParameters"></span><span id="serviceparameters"></span><span id="SERVICEPARAMETERS"></span>Service Parameters</span><span class="sxs-lookup"><span data-stu-id="7335e-153"><span id="ServiceParameters"></span><span id="serviceparameters"></span><span id="SERVICEPARAMETERS"></span>ServiceParameters</span></span>
</dt> <dd>

<span data-ttu-id="7335e-154">Diese Spalte enthält den Wert von Service Parameters, der unter HKCR \\ AppID \\ {AppID>} "Service Parameters" geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="7335e-154">This column contains the value of ServiceParameters that will be written under HKCR\\AppID\\{appid>} "ServiceParameters".</span></span>

</dd> <dt>

<span data-ttu-id="7335e-155"><span id="DllSurrogate"></span><span id="dllsurrogate"></span><span id="DLLSURROGATE"></span>Dllersatz</span><span class="sxs-lookup"><span data-stu-id="7335e-155"><span id="DllSurrogate"></span><span id="dllsurrogate"></span><span id="DLLSURROGATE"></span>DllSurrogate</span></span>
</dt> <dd>

<span data-ttu-id="7335e-156">Diese Spalte enthält den Wert von dllersatz, der unter HKCR \\ AppID \\ { <appid> } "dllersatz" = geschrieben wird <xxx> .</span><span class="sxs-lookup"><span data-stu-id="7335e-156">This column contains the value of DllSurrogate that will be written under HKCR\\AppId\\{<appid>} "DllSurrogate"=<xxx>.</span></span> <span data-ttu-id="7335e-157">Wenn diese Spalte vorhanden ist, handelt es sich in der Regel um eine leere Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="7335e-157">If this column is present it will typically be an empty string.</span></span>

</dd> <dt>

<span data-ttu-id="7335e-158"><span id="ActivateAtStorage"></span><span id="activateatstorage"></span><span id="ACTIVATEATSTORAGE"></span>Activateatstorage</span><span class="sxs-lookup"><span data-stu-id="7335e-158"><span id="ActivateAtStorage"></span><span id="activateatstorage"></span><span id="ACTIVATEATSTORAGE"></span>ActivateAtStorage</span></span>
</dt> <dd>

<span data-ttu-id="7335e-159">Ein ganzzahliger Wert ungleich 0 (null) in diesem Feld bewirkt, dass Windows Installer HKCR \\ AppID \\ { <appid> } "activateatstorage" = "Y" in die Registrierung schreibt.</span><span class="sxs-lookup"><span data-stu-id="7335e-159">A non-zero integer value in this field causes Windows Installer to write HKCR\\AppID\\{<appid>} "ActivateAtStorage"="Y" into the registry.</span></span> <span data-ttu-id="7335e-160">Wenn das Feld leer gelassen wird oder den Wert 0 (null) aufweist, wird kein Wert geschrieben.</span><span class="sxs-lookup"><span data-stu-id="7335e-160">If the field is left empty, or has a value of zero, no value will be written.</span></span>

</dd> <dt>

<span data-ttu-id="7335e-161"><span id="RunAsInteractiveUser"></span><span id="runasinteractiveuser"></span><span id="RUNASINTERACTIVEUSER"></span>Runasinteractiveuser</span><span class="sxs-lookup"><span data-stu-id="7335e-161"><span id="RunAsInteractiveUser"></span><span id="runasinteractiveuser"></span><span id="RUNASINTERACTIVEUSER"></span>RunAsInteractiveUser</span></span>
</dt> <dd>

<span data-ttu-id="7335e-162">Ein ganzzahliger Wert ungleich 0 (null) in diesem Feld bewirkt, dass Windows Installer HKCR \\ AppID \\ {AppID>} "runas" = "Interactive User" in die Registrierung schreibt.</span><span class="sxs-lookup"><span data-stu-id="7335e-162">A non-zero integer value in this field causes Windows Installer to write HKCR\\AppID\\{appid>} "RunAs"="Interactive User" into the registry.</span></span> <span data-ttu-id="7335e-163">Wenn das Feld leer gelassen wird oder den Wert 0 (null) aufweist, wird kein Wert geschrieben.</span><span class="sxs-lookup"><span data-stu-id="7335e-163">If the field is left empty, or has a value of zero, no value will be written.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7335e-164">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7335e-164">Remarks</span></span>

<span data-ttu-id="7335e-165">Diese Tabelle wird von der [RegisterClassInfo-Aktion](registerclassinfo-action.md) und der [unregisterclassinfo-Aktion](unregisterclassinfo-action.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="7335e-165">This table is used by the [RegisterClassInfo action](registerclassinfo-action.md) and [UnregisterClassInfo action](unregisterclassinfo-action.md).</span></span>

<span data-ttu-id="7335e-166">Beachten Sie, dass die AppID-Tabelle keine Spalte zum Registrieren eines Standard namens enthält.</span><span class="sxs-lookup"><span data-stu-id="7335e-166">Note that the AppId table does not have a column for registering a Default name.</span></span> <span data-ttu-id="7335e-167">In Fällen, in denen Sie einen benutzerfreundlichen Namen als Standardwert für den Namen schreiben müssen, müssen Sie sich daher mithilfe der [Registrierungs Tabelle](registry-table.md)registrieren.</span><span class="sxs-lookup"><span data-stu-id="7335e-167">Therefore in cases where you need to write a user friendly name as the Default name value, you must register using the [Registry table](registry-table.md).</span></span>

## <a name="validation"></a><span data-ttu-id="7335e-168">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="7335e-168">Validation</span></span>

<dl>

[<span data-ttu-id="7335e-169">ICE03</span><span class="sxs-lookup"><span data-stu-id="7335e-169">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="7335e-170">ICE06</span><span class="sxs-lookup"><span data-stu-id="7335e-170">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="7335e-171">ICE32</span><span class="sxs-lookup"><span data-stu-id="7335e-171">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="7335e-172">ICE33</span><span class="sxs-lookup"><span data-stu-id="7335e-172">ICE33</span></span>](ice33.md)  
[<span data-ttu-id="7335e-173">ICE46</span><span class="sxs-lookup"><span data-stu-id="7335e-173">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="7335e-174">ICE69</span><span class="sxs-lookup"><span data-stu-id="7335e-174">ICE69</span></span>](ice69.md)  
</dl>

 

 



