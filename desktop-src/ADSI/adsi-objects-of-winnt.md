---
title: ADSI-Objekte von Winnt
description: Der ADSI WinNT-Anbieter implementiert die folgenden COM-Objekte, um Features und Dienste verschiedener ADSI-Schnittstellen zu unterstützen.
ms.assetid: ce6f8638-aa9e-4036-b597-077da4c3c534
ms.tgt_platform: multiple
keywords:
- WinNT-Dienstanbieter ADSI, ADSI-Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77d0c9e5c486d07e1e392a9f307ecd9af4509ed3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100582"
---
# <a name="adsi-objects-of-winnt"></a><span data-ttu-id="dcabc-104">ADSI-Objekte von Winnt</span><span class="sxs-lookup"><span data-stu-id="dcabc-104">ADSI Objects of WinNT</span></span>

<span data-ttu-id="dcabc-105">Der ADSI WinNT-Anbieter implementiert die folgenden COM-Objekte, um Features und Dienste verschiedener ADSI-Schnittstellen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="dcabc-105">The ADSI WinNT provider implement the following COM objects to support features and services of various ADSI interfaces.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dcabc-106">ADSI-Objekt</span><span class="sxs-lookup"><span data-stu-id="dcabc-106">ADSI Object</span></span></th>
<th><span data-ttu-id="dcabc-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dcabc-107">Description</span></span></th>
<th><span data-ttu-id="dcabc-108">Unterstützte Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="dcabc-108">Supported Interfaces</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dcabc-109"><strong>Klasse</strong></span><span class="sxs-lookup"><span data-stu-id="dcabc-109"><strong>Class</strong></span></span></td>
<td><span data-ttu-id="dcabc-110">Ein ADSI-Objekt, das eine Klassendefinition darstellt.</span><span class="sxs-lookup"><span data-stu-id="dcabc-110">An ADSI object that represents a class definition.</span></span></td>
<td><dl> <span data-ttu-id="dcabc-111"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadsclass"> <strong>iadsclass</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="dcabc-111"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsclass"><strong>IADsClass</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dcabc-112"><strong>Computer</strong></span><span class="sxs-lookup"><span data-stu-id="dcabc-112"><strong>Computer</strong></span></span></td>
<td><span data-ttu-id="dcabc-113">Ein ADSI-Objekt, das einen Computer darstellt.</span><span class="sxs-lookup"><span data-stu-id="dcabc-113">An ADSI object that represents a computer.</span></span></td>
<td><dl> <span data-ttu-id="dcabc-114"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscomputer"><strong>iadscomputer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscomputeroperations"><strong>iadscomputeroperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="dcabc-114"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscomputer"><strong>IADsComputer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscomputeroperations"><strong>IADsComputerOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dcabc-115"><strong>Domäne</strong></span><span class="sxs-lookup"><span data-stu-id="dcabc-115"><strong>Domain</strong></span></span></td>
<td><span data-ttu-id="dcabc-116">Ein ADSI-Objekt, das eine Domäne über das Netzwerk darstellt.</span><span class="sxs-lookup"><span data-stu-id="dcabc-116">An ADSI object that represents a domain over the network.</span></span></td>
<td><dl> <span data-ttu-id="dcabc-117"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsdomain"><strong>iadsdomain</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="dcabc-117"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsdomain"><strong>IADsDomain</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dcabc-118"><strong>File Service</strong></span><span class="sxs-lookup"><span data-stu-id="dcabc-118"><strong>FileService</strong></span></span></td>
<td><span data-ttu-id="dcabc-119">Ein ADSI-Objekt, das einen Datei Dienst darstellt.</span><span class="sxs-lookup"><span data-stu-id="dcabc-119">An ADSI object that represents a file service.</span></span></td>
<td><dl> <span data-ttu-id="dcabc-120"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileservice"><strong>iadsfileservice</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations"><strong>iadsfileserviceoperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="dcabc-120"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileservice"><strong>IADsFileService</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations"><strong>IADsFileServiceOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dcabc-121"><strong>FileShare</strong></span><span class="sxs-lookup"><span data-stu-id="dcabc-121"><strong>FileShare</strong></span></span></td>
<td><span data-ttu-id="dcabc-122">Ein ADSI-Objekt, das eine Dateifreigabe darstellt.</span><span class="sxs-lookup"><span data-stu-id="dcabc-122">An ADSI object that represents a file share.</span></span></td>
<td><dl> <span data-ttu-id="dcabc-123"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileshare"><strong>iadsfileshare</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="dcabc-123"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileshare"><strong>IADsFileShare</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dcabc-124"><strong>Fpnwfileservice</strong></span><span class="sxs-lookup"><span data-stu-id="dcabc-124"><strong>FPNWFileService</strong></span></span></td>
<td><span data-ttu-id="dcabc-125">Ein ADSI-Objekt, das einen Datei Dienst darstellt.</span><span class="sxs-lookup"><span data-stu-id="dcabc-125">An ADSI object that represents a file service.</span></span></td>
<td><dl> <span data-ttu-id="dcabc-126"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileservice"><strong>iadsfileservice</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations"><strong>iadsfileserviceoperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="dcabc-126"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileservice"><strong>IADsFileService</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations"><strong>IADsFileServiceOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dcabc-127"><strong>Fpnwfileshare</strong></span><span class="sxs-lookup"><span data-stu-id="dcabc-127"><strong>FPNWFileShare</strong></span></span></td>
<td><span data-ttu-id="dcabc-128">Ein ADSI-Objekt, das eine Dateifreigabe darstellt.</span><span class="sxs-lookup"><span data-stu-id="dcabc-128">An ADSI object that represents a file share.</span></span></td>
<td><dl> <span data-ttu-id="dcabc-129"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileshare"><strong>iadsfileshare</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="dcabc-129"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileshare"><strong>IADsFileShare</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dcabc-130"><strong>Fpnwresource</strong></span><span class="sxs-lookup"><span data-stu-id="dcabc-130"><strong>FPNWResource</strong></span></span></td>
<td><span data-ttu-id="dcabc-131">Ein ADSI-Objekt, das eine Ressource darstellt.</span><span class="sxs-lookup"><span data-stu-id="dcabc-131">An ADSI object that represents a resource.</span></span></td>
<td><dl> <span data-ttu-id="dcabc-132"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsresource"><strong>iadsresource</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="dcabc-132"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsresource"><strong>IADsResource</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dcabc-133"><strong>Fpnwresourcescollection</strong></span><span class="sxs-lookup"><span data-stu-id="dcabc-133"><strong>FPNWResourcesCollection</strong></span></span></td>
<td><span data-ttu-id="dcabc-134">Ein ADSI-Objekt, das eine Auflistung von Ressourcen darstellt.</span><span class="sxs-lookup"><span data-stu-id="dcabc-134">An ADSI object that represents a collection of resources.</span></span></td>
<td><span data-ttu-id="dcabc-135"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>Iadscollection</strong></a></span><span class="sxs-lookup"><span data-stu-id="dcabc-135"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dcabc-136"><strong>Fpnwsession</strong></span><span class="sxs-lookup"><span data-stu-id="dcabc-136"><strong>FPNWSession</strong></span></span></td>
<td><span data-ttu-id="dcabc-137">Ein ADSI-Objekt, das eine Sitzung darstellt.</span><span class="sxs-lookup"><span data-stu-id="dcabc-137">An ADSI object that represents a session.</span></span></td>
<td><dl> <span data-ttu-id="dcabc-138"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadssession"><strong>iadssession</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="dcabc-138"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadssession"><strong>IADsSession</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dcabc-139"><strong>Fpnwsessionscollection</strong></span><span class="sxs-lookup"><span data-stu-id="dcabc-139"><strong>FPNWSessionsCollection</strong></span></span></td>
<td><span data-ttu-id="dcabc-140">Ein ADSI-Objekt, das eine Auflistung von Sitzungen darstellt.</span><span class="sxs-lookup"><span data-stu-id="dcabc-140">An ADSI object that represents a collection of sessions.</span></span></td>
<td><span data-ttu-id="dcabc-141"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>Iadscollection</strong></a></span><span class="sxs-lookup"><span data-stu-id="dcabc-141"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dcabc-142"><strong>Gruppieren</strong></span><span class="sxs-lookup"><span data-stu-id="dcabc-142"><strong>Group</strong></span></span></td>
<td><span data-ttu-id="dcabc-143">Ein ADSI-Objekt, das eine Gruppe darstellt.</span><span class="sxs-lookup"><span data-stu-id="dcabc-143">An ADSI object that represents a group.</span></span></td>
<td><dl> <span data-ttu-id="dcabc-144"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsgroup"><strong>IADsGroup</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="dcabc-144"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsgroup"><strong>IADsGroup</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl>
<blockquote>
[!Note]<br />
<span data-ttu-id="dcabc-145">GetInfo kann nicht für Gruppen verwendet werden, die Mitglieder mit bekannten Sicherheits Prinzipalen im WinNT-Bereich enthalten.</span><span class="sxs-lookup"><span data-stu-id="dcabc-145">GetInfo cannot be used for groups that contain members that are wellKnown security principals in the WinNT scope.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dcabc-146"><strong>GroupCollection</strong></span><span class="sxs-lookup"><span data-stu-id="dcabc-146"><strong>GroupCollection</strong></span></span></td>
<td><span data-ttu-id="dcabc-147">Ein ADSI-Objekt, das eine Auflistung von Gruppen darstellt.</span><span class="sxs-lookup"><span data-stu-id="dcabc-147">An ADSI object that represents a collection of groups.</span></span></td>
<td><dl> <span data-ttu-id="dcabc-148"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"> <strong>iadsmembers</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="dcabc-148"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"><strong>IADsMembers</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dcabc-149"><strong>LocalGroup</strong></span><span class="sxs-lookup"><span data-stu-id="dcabc-149"><strong>LocalGroup</strong></span></span></td>
<td><span data-ttu-id="dcabc-150">Ein ADSI-Objekt, das eine lokale Gruppe darstellt.</span><span class="sxs-lookup"><span data-stu-id="dcabc-150">An ADSI object that represents a local group.</span></span></td>
<td><dl> <span data-ttu-id="dcabc-151"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsgroup"><strong>IADsGroup</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="dcabc-151"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsgroup"><strong>IADsGroup</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dcabc-152"><strong>Localgroupcollection</strong></span><span class="sxs-lookup"><span data-stu-id="dcabc-152"><strong>LocalgroupCollection</strong></span></span></td>
<td><span data-ttu-id="dcabc-153">Ein ADSI-Objekt, das eine Auflistung von lokalen Gruppen darstellt.</span><span class="sxs-lookup"><span data-stu-id="dcabc-153">An ADSI object that represents a collection of local groups.</span></span></td>
<td><dl> <span data-ttu-id="dcabc-154"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"> <strong>iadsmembers</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="dcabc-154"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"><strong>IADsMembers</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dcabc-155"><strong>Namespace</strong></span><span class="sxs-lookup"><span data-stu-id="dcabc-155"><strong>Namespace</strong></span></span></td>
<td><span data-ttu-id="dcabc-156">Ein ADSI-Objekt, das den WinNT-Namespace darstellt.</span><span class="sxs-lookup"><span data-stu-id="dcabc-156">An ADSI object that represents the WinNT namespace.</span></span></td>
<td><dl> <span data-ttu-id="dcabc-157"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsopendsobject"><strong>iadsopendsobject</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="dcabc-157"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsopendsobject"><strong>IADsOpenDSObject</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dcabc-158"><strong>PrintJob</strong></span><span class="sxs-lookup"><span data-stu-id="dcabc-158"><strong>PrintJob</strong></span></span></td>
<td><span data-ttu-id="dcabc-159">Ein ADSI-Objekt, das einen Druckauftrag darstellt.</span><span class="sxs-lookup"><span data-stu-id="dcabc-159">An ADSI object that represents a print job.</span></span></td>
<td><dl> <span data-ttu-id="dcabc-160"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintjob"><strong>iadsprintjob</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations"><strong>iadsprintjoboperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="dcabc-160"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintjob"><strong>IADsPrintJob</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations"><strong>IADsPrintJobOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dcabc-161"><strong>Printjobscollection</strong></span><span class="sxs-lookup"><span data-stu-id="dcabc-161"><strong>PrintJobsCollection</strong></span></span></td>
<td><span data-ttu-id="dcabc-162">Ein ADSI-Objekt, das eine Auflistung von Druckaufträgen darstellt.</span><span class="sxs-lookup"><span data-stu-id="dcabc-162">An ADSI object that represents a collection of print jobs.</span></span></td>
<td><span data-ttu-id="dcabc-163"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>Iadscollection</strong></a></span><span class="sxs-lookup"><span data-stu-id="dcabc-163"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dcabc-164"><strong>PrintQueue</strong></span><span class="sxs-lookup"><span data-stu-id="dcabc-164"><strong>PrintQueue</strong></span></span></td>
<td><span data-ttu-id="dcabc-165">Ein ADSI-Objekt, das eine Druck Warteschlange darstellt.</span><span class="sxs-lookup"><span data-stu-id="dcabc-165">An ADSI object that represents a print queue.</span></span></td>
<td><dl> <span data-ttu-id="dcabc-166"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintqueue"><strong>iadsprintqueue</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations"><strong>iadsprintqueueoperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="dcabc-166"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintqueue"><strong>IADsPrintQueue</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations"><strong>IADsPrintQueueOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dcabc-167"><strong>Eigenschaft</strong></span><span class="sxs-lookup"><span data-stu-id="dcabc-167"><strong>Property</strong></span></span></td>
<td><span data-ttu-id="dcabc-168">Ein ADSI-Objekt, das eine Attribut Definition darstellt.</span><span class="sxs-lookup"><span data-stu-id="dcabc-168">An ADSI object that represents an attribute definition.</span></span></td>
<td><dl> <span data-ttu-id="dcabc-169"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadsproperty"> <strong>iadsproperty</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="dcabc-169"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsproperty"><strong>IADsProperty</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dcabc-170"><strong>Ressource</strong></span><span class="sxs-lookup"><span data-stu-id="dcabc-170"><strong>Resource</strong></span></span></td>
<td><span data-ttu-id="dcabc-171">Ein ADSI-Objekt, das eine Ressource darstellt.</span><span class="sxs-lookup"><span data-stu-id="dcabc-171">An ADSI object that represents a resource.</span></span></td>
<td><dl> <span data-ttu-id="dcabc-172"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsresource"><strong>iadsresource</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="dcabc-172"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsresource"><strong>IADsResource</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dcabc-173"><strong>Resourcescollection</strong></span><span class="sxs-lookup"><span data-stu-id="dcabc-173"><strong>ResourcesCollection</strong></span></span></td>
<td><span data-ttu-id="dcabc-174">Ein ADSI-Objekt, das eine Auflistung von Ressourcen darstellt.</span><span class="sxs-lookup"><span data-stu-id="dcabc-174">An ADSI object that represents a collection of resources.</span></span></td>
<td><span data-ttu-id="dcabc-175"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>Iadscollection</strong></a></span><span class="sxs-lookup"><span data-stu-id="dcabc-175"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dcabc-176"><strong>Schema</strong></span><span class="sxs-lookup"><span data-stu-id="dcabc-176"><strong>Schema</strong></span></span></td>
<td><span data-ttu-id="dcabc-177">Ein ADSI-Objekt, das den Schema Container darstellt.</span><span class="sxs-lookup"><span data-stu-id="dcabc-177">An ADSI object that represents the schema container.</span></span></td>
<td><dl> <span data-ttu-id="dcabc-178"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"> <strong>IADsContainer</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="dcabc-178"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dcabc-179"><strong>Service</strong></span><span class="sxs-lookup"><span data-stu-id="dcabc-179"><strong>Service</strong></span></span></td>
<td><span data-ttu-id="dcabc-180">Ein ADSI-Objekt, das einen Dienst darstellt.</span><span class="sxs-lookup"><span data-stu-id="dcabc-180">An ADSI object that represents a service.</span></span></td>
<td><dl> <span data-ttu-id="dcabc-181"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsservice"><strong>iadsservice</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsserviceoperations"><strong>iadsserviceoperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="dcabc-181"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsservice"><strong>IADsService</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsserviceoperations"><strong>IADsServiceOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dcabc-182"><strong>Sitzung</strong></span><span class="sxs-lookup"><span data-stu-id="dcabc-182"><strong>Session</strong></span></span></td>
<td><span data-ttu-id="dcabc-183">Ein ADSI-Objekt, das eine Sitzung darstellt.</span><span class="sxs-lookup"><span data-stu-id="dcabc-183">An ADSI object that represents a session.</span></span></td>
<td><dl> <span data-ttu-id="dcabc-184"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadssession"><strong>iadssession</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="dcabc-184"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadssession"><strong>IADsSession</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dcabc-185"><strong>Sessionscollection</strong></span><span class="sxs-lookup"><span data-stu-id="dcabc-185"><strong>SessionsCollection</strong></span></span></td>
<td><span data-ttu-id="dcabc-186">Ein ADSI-Objekt, das eine Auflistung von Sitzungen darstellt.</span><span class="sxs-lookup"><span data-stu-id="dcabc-186">An ADSI object that represents a collection of sessions.</span></span></td>
<td><span data-ttu-id="dcabc-187"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>Iadscollection</strong></a></span><span class="sxs-lookup"><span data-stu-id="dcabc-187"><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dcabc-188"><strong>Syntax</strong></span><span class="sxs-lookup"><span data-stu-id="dcabc-188"><strong>Syntax</strong></span></span></td>
<td><span data-ttu-id="dcabc-189">Ein ADSI-Objekt, das die Syntax eines Attributs darstellt.</span><span class="sxs-lookup"><span data-stu-id="dcabc-189">An ADSI object that represents the syntax of an attribute.</span></span></td>
<td><dl> <span data-ttu-id="dcabc-190"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadssyntax"> <strong>iadssyntax</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="dcabc-190"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadssyntax"><strong>IADsSyntax</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dcabc-191"><strong>Benutzer</strong></span><span class="sxs-lookup"><span data-stu-id="dcabc-191"><strong>User</strong></span></span></td>
<td><span data-ttu-id="dcabc-192">Ein ADSI-Objekt, das ein Benutzerkonto darstellt.</span><span class="sxs-lookup"><span data-stu-id="dcabc-192">An ADSI object that represents a user account.</span></span></td>
<td><dl> <span data-ttu-id="dcabc-193"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsuser"><strong>IADsUser</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span><span class="sxs-lookup"><span data-stu-id="dcabc-193"><dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsuser"><strong>IADsUser</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </span></span></dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dcabc-194"><strong>Usergroupcollection</strong></span><span class="sxs-lookup"><span data-stu-id="dcabc-194"><strong>UserGroupCollection</strong></span></span></td>
<td><span data-ttu-id="dcabc-195">Ein ADSI-Objekt, das eine Auflistung von Benutzergruppen darstellt.</span><span class="sxs-lookup"><span data-stu-id="dcabc-195">An ADSI object that represents a collection of user groups.</span></span></td>
<td><span data-ttu-id="dcabc-196"><a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"><strong>Iadsmembers</strong></a></span><span class="sxs-lookup"><span data-stu-id="dcabc-196"><a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"><strong>IADsMembers</strong></a></span></span></td>
</tr>
</tbody>
</table>



 

 

 





