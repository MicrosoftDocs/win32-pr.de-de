---
Description: Die KNOWNFOLDERID-Konstanten stellen GUIDs dar, mit denen Standardordner identifiziert werden, die im System als bekannte Ordner registriert sind.
ms.assetid: f2c08ade-3083-44e4-82b0-dde45f0e3094
title: KNOWNFOLDERID (KnownFolders. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 97748d074d6b0982708f51ea679f0629e8abfad6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "104982860"
---
# <a name="knownfolderid"></a><span data-ttu-id="f9a52-103">KNOWNFOLDERID</span><span class="sxs-lookup"><span data-stu-id="f9a52-103">KNOWNFOLDERID</span></span>

<span data-ttu-id="f9a52-104">Die **KNOWNFOLDERID** -Konstanten stellen GUIDs dar, mit denen Standardordner identifiziert werden, die im System als [bekannte Ordner](known-folders.md)registriert sind.</span><span class="sxs-lookup"><span data-stu-id="f9a52-104">The **KNOWNFOLDERID** constants represent GUIDs that identify standard folders registered with the system as [Known Folders](known-folders.md).</span></span> <span data-ttu-id="f9a52-105">Diese Ordner werden mit Windows Vista und höheren Betriebssystemen installiert, und auf einem Computer sind nur geeignete Ordner installiert.</span><span class="sxs-lookup"><span data-stu-id="f9a52-105">These folders are installed with Windows Vista and later operating systems, and a computer will have only folders appropriate to it installed.</span></span> <span data-ttu-id="f9a52-106">Beschreibungen dieser Ordner finden Sie unter [**CSIDL**](csidl.md).</span><span class="sxs-lookup"><span data-stu-id="f9a52-106">For descriptions of these folders, see [**CSIDL**](csidl.md).</span></span>

## <a name="example"></a><span data-ttu-id="f9a52-107">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f9a52-107">Example</span></span>

```c
HRESULT CExplorerBrowserHostDialog::_FillViewWithKnownFolders(IResultsFolder *prf)
{
    IKnownFolderManager *pManager;
    HRESULT hr = CoCreateInstance(CLSID_KnownFolderManager, NULL, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pManager));
    if (SUCCEEDED(hr))
    {
        UINT cCount;
        KNOWNFOLDERID *pkfid;

        hr = pManager->GetFolderIds(&pkfid, &cCount);
        if (SUCCEEDED(hr))
        {
            for (UINT i = 0; i < cCount; i++)
            {
                IKnownFolder *pKnownFolder;
                hr = pManager->GetFolder(pkfid[i], &pKnownFolder);
                if (SUCCEEDED(hr))
                {
                    IShellItem *psi;
                    hr = pKnownFolder->GetShellItem(0, IID_PPV_ARGS(&psi));
                    if (SUCCEEDED(hr))
                    {
                        hr = prf->AddItem(psi);
                        psi->Release();
                    }
                    pKnownFolder->Release();
                }
            }
            CoTaskMemFree(pkfid);
        }
        pManager->Release();
    }
    return hr;
}

```

<span data-ttu-id="f9a52-108">Beispiel aus [klassischen Windows-Beispielen](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/winui/shell/appplatform/ExplorerBrowserCustomContents/ExplorerBrowserCustomContents.cpp) auf GitHub.</span><span class="sxs-lookup"><span data-stu-id="f9a52-108">Example from [Windows classic samples](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/winui/shell/appplatform/ExplorerBrowserCustomContents/ExplorerBrowserCustomContents.cpp) on GitHub.</span></span>

## <a name="constants"></a><span data-ttu-id="f9a52-109">Konstanten</span><span class="sxs-lookup"><span data-stu-id="f9a52-109">Constants</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="f9a52-110">Konstante</span><span class="sxs-lookup"><span data-stu-id="f9a52-110">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="f9a52-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f9a52-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_AccountPictures"></span><span id="folderid_accountpictures"></span><span id="FOLDERID_ACCOUNTPICTURES"></span><dl> <span data-ttu-id="f9a52-112"><dt><strong>FOLDERID_AccountPictures</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-112"><dt><strong>FOLDERID_AccountPictures</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-113">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-113">GUID</span></span></td>
<td><span data-ttu-id="f9a52-114">{008ca0b1-55b4-4c56-b8a8-4de4b299d3be}</span><span class="sxs-lookup"><span data-stu-id="f9a52-114">{008ca0b1-55b4-4c56-b8a8-4de4b299d3be}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-115">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-115">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-116">Konto Bilder</span><span class="sxs-lookup"><span data-stu-id="f9a52-116">Account Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-117">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-117">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-118">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-118">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-119">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-119">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-120">%APPDATA%\microsoft\windows\accountpictures</span><span class="sxs-lookup"><span data-stu-id="f9a52-120">%APPDATA%\Microsoft\Windows\AccountPictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-121">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-121">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-122">None, in Windows 8 eingeführte Wert</span><span class="sxs-lookup"><span data-stu-id="f9a52-122">None, value introduced in Windows 8</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-123">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-123">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-124">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-124">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-125">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-125">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-126">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-126">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_AddNewPrograms"></span><span id="folderid_addnewprograms"></span><span id="FOLDERID_ADDNEWPROGRAMS"></span><dl> <span data-ttu-id="f9a52-127"><dt><strong>FOLDERID_AddNewPrograms</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-127"><dt><strong>FOLDERID_AddNewPrograms</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-128">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-128">GUID</span></span></td>
<td><span data-ttu-id="f9a52-129">{de61d971-5ebc-4f02-a3a9-6c82895e5c04}</span><span class="sxs-lookup"><span data-stu-id="f9a52-129">{de61d971-5ebc-4f02-a3a9-6c82895e5c04}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-130">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-130">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-131">Programme erhalten</span><span class="sxs-lookup"><span data-stu-id="f9a52-131">Get Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-132">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-132">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-133">Virtu</span><span class="sxs-lookup"><span data-stu-id="f9a52-133">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-134">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-134">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-135">Nicht zutreffend – virtueller Ordner</span><span class="sxs-lookup"><span data-stu-id="f9a52-135">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-136">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-136">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-137">Keine</span><span class="sxs-lookup"><span data-stu-id="f9a52-137">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-138">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-138">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-139">Hinzufügen neuer Programme ( <strong>in der System</strong> Steuerung unter "Software" gefunden)</span><span class="sxs-lookup"><span data-stu-id="f9a52-139">Add New Programs (found in the <strong>Add or Remove Programs</strong> item in the Control Panel)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-140">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-140">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-141">Nicht zutreffend – virtueller Ordner</span><span class="sxs-lookup"><span data-stu-id="f9a52-141">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_AdminTools"></span><span id="folderid_admintools"></span><span id="FOLDERID_ADMINTOOLS"></span><dl> <span data-ttu-id="f9a52-142"><dt><strong>FOLDERID_AdminTools</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-142"><dt><strong>FOLDERID_AdminTools</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-143">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-143">GUID</span></span></td>
<td><span data-ttu-id="f9a52-144">{724ef170-a42d-4fef -9F 26-b60e846bba4f}</span><span class="sxs-lookup"><span data-stu-id="f9a52-144">{724EF170-A42D-4FEF-9F26-B60E846FBA4F}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-145">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-145">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-146">Verwaltung</span><span class="sxs-lookup"><span data-stu-id="f9a52-146">Administrative Tools</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-147">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-147">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-148">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-148">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-149">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-149">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-150">%APPDATA%\Microsoft\Windows\Start menu\programs\administrative Tools</span><span class="sxs-lookup"><span data-stu-id="f9a52-150">%APPDATA%\Microsoft\Windows\Start Menu\Programs\Administrative Tools</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-151">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-151">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-152">CSIDL_ADMINTOOLS</span><span class="sxs-lookup"><span data-stu-id="f9a52-152">CSIDL_ADMINTOOLS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-153">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-153">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-154">Verwaltung</span><span class="sxs-lookup"><span data-stu-id="f9a52-154">Administrative Tools</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-155">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-155">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-156">%UserProfile%\Startmenü \ programme\administrative Tools</span><span class="sxs-lookup"><span data-stu-id="f9a52-156">%USERPROFILE%\Start Menu\Programs\Administrative Tools</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_AppDataDesktop"></span><span id="folderid_appdatadesktop"></span><span id="FOLDERID_APPDATADESKTOP"></span><dl> <span data-ttu-id="f9a52-157"><dt><strong>FOLDERID_AppDataDesktop</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-157"><dt><strong>FOLDERID_AppDataDesktop</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-158">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-158">GUID</span></span></td>
<td><span data-ttu-id="f9a52-159">{B2C5E279-7ADD-439F-B28C-C41FE1BBF672}</span><span class="sxs-lookup"><span data-stu-id="f9a52-159">{B2C5E279-7ADD-439F-B28C-C41FE1BBF672}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-160">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-160">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-161">Appdatadesktop</span><span class="sxs-lookup"><span data-stu-id="f9a52-161">AppDataDesktop</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-162">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-162">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-163">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-163">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-164">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-164">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-165">%LocalAppData%\Desktop</span><span class="sxs-lookup"><span data-stu-id="f9a52-165">%LOCALAPPDATA%\Desktop</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-166">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-166">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-167">None, in Windows 10 eingeführte Wert, Version 1709</span><span class="sxs-lookup"><span data-stu-id="f9a52-167">None, value introduced in Windows 10, version 1709</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-168">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-168">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-169">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-169">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-170">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-170">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-171">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-171">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="f9a52-172">Diese folderid wird intern von .NET-Anwendungen verwendet, um plattformübergreifende App-Funktionen zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="f9a52-172">This FOLDERID is used internally by .NET applications to enable cross-platform app functionality.</span></span> <span data-ttu-id="f9a52-173">Sie ist nicht für die direkte Verwendung in einer Anwendung vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="f9a52-173">It is not intended to be used directly from an application.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_AppDataDocuments"></span><span id="folderid_appdatadocuments"></span><span id="FOLDERID_APPDATADOCUMENTS"></span><dl> <span data-ttu-id="f9a52-174"><dt><strong>FOLDERID_AppDataDocuments</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-174"><dt><strong>FOLDERID_AppDataDocuments</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-175">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-175">GUID</span></span></td>
<td><span data-ttu-id="f9a52-176">{7be16610-1f7f-44ac-bff0-83e15f2ffca1}</span><span class="sxs-lookup"><span data-stu-id="f9a52-176">{7BE16610-1F7F-44AC-BFF0-83E15F2FFCA1}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-177">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-177">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-178">Appdatadocals-Elemente</span><span class="sxs-lookup"><span data-stu-id="f9a52-178">AppDataDocuments</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-179">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-179">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-180">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-180">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-181">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-181">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-182">%LocalAppData%\Documents</span><span class="sxs-lookup"><span data-stu-id="f9a52-182">%LOCALAPPDATA%\Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-183">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-183">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-184">None, in Windows 10 eingeführte Wert, Version 1709</span><span class="sxs-lookup"><span data-stu-id="f9a52-184">None, value introduced in Windows 10, version 1709</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-185">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-185">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-186">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-186">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-187">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-187">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-188">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-188">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="f9a52-189">Diese folderid wird intern von .NET-Anwendungen verwendet, um plattformübergreifende App-Funktionen zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="f9a52-189">This FOLDERID is used internally by .NET applications to enable cross-platform app functionality.</span></span> <span data-ttu-id="f9a52-190">Sie ist nicht für die direkte Verwendung in einer Anwendung vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="f9a52-190">It is not intended to be used directly from an application.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_AppDataFavorites"></span><span id="folderid_appdatafavorites"></span><span id="FOLDERID_APPDATAFAVORITES"></span><dl> <span data-ttu-id="f9a52-191"><dt><strong>FOLDERID_AppDataFavorites</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-191"><dt><strong>FOLDERID_AppDataFavorites</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-192">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-192">GUID</span></span></td>
<td><span data-ttu-id="f9a52-193">{7cfbefbc-de1f-45AA-B843-a542ac536cc9}</span><span class="sxs-lookup"><span data-stu-id="f9a52-193">{7CFBEFBC-DE1F-45AA-B843-A542AC536CC9}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-194">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-194">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-195">Appdatafavorites</span><span class="sxs-lookup"><span data-stu-id="f9a52-195">AppDataFavorites</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-196">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-196">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-197">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-197">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-198">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-198">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-199">%LocalAppData%\Favoriten</span><span class="sxs-lookup"><span data-stu-id="f9a52-199">%LOCALAPPDATA%\Favorites</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-200">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-200">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-201">None, in Windows 10 eingeführte Wert, Version 1709</span><span class="sxs-lookup"><span data-stu-id="f9a52-201">None, value introduced in Windows 10, version 1709</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-202">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-202">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-203">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-203">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-204">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-204">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-205">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-205">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="f9a52-206">Diese folderid wird intern von .NET-Anwendungen verwendet, um plattformübergreifende App-Funktionen zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="f9a52-206">This FOLDERID is used internally by .NET applications to enable cross-platform app functionality.</span></span> <span data-ttu-id="f9a52-207">Sie ist nicht für die direkte Verwendung in einer Anwendung vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="f9a52-207">It is not intended to be used directly from an application.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_AppDataProgramData"></span><span id="folderid_appdataprogramdata"></span><span id="FOLDERID_APPDATAPROGRAMDATA"></span><dl> <span data-ttu-id="f9a52-208"><dt><strong>FOLDERID_AppDataProgramData</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-208"><dt><strong>FOLDERID_AppDataProgramData</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-209">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-209">GUID</span></span></td>
<td><span data-ttu-id="f9a52-210">{559d40a3-a036-40fa-af61-84cb430a4d34}</span><span class="sxs-lookup"><span data-stu-id="f9a52-210">{559D40A3-A036-40FA-AF61-84CB430A4D34}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-211">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-211">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-212">Appdataprogramdata</span><span class="sxs-lookup"><span data-stu-id="f9a52-212">AppDataProgramData</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-213">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-213">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-214">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-214">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-215">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-215">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-216">%LocalAppData%\ProgramData</span><span class="sxs-lookup"><span data-stu-id="f9a52-216">%LOCALAPPDATA%\ProgramData</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-217">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-217">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-218">None, in Windows 10 eingeführte Wert, Version 1709</span><span class="sxs-lookup"><span data-stu-id="f9a52-218">None, value introduced in Windows 10, version 1709</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-219">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-219">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-220">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-220">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-221">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-221">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-222">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-222">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="f9a52-223">Diese folderid wird intern von .NET-Anwendungen verwendet, um plattformübergreifende App-Funktionen zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="f9a52-223">This FOLDERID is used internally by .NET applications to enable cross-platform app functionality.</span></span> <span data-ttu-id="f9a52-224">Sie ist nicht für die direkte Verwendung in einer Anwendung vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="f9a52-224">It is not intended to be used directly from an application.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ApplicationShortcuts"></span><span id="folderid_applicationshortcuts"></span><span id="FOLDERID_APPLICATIONSHORTCUTS"></span><dl> <span data-ttu-id="f9a52-225"><dt><strong>FOLDERID_ApplicationShortcuts</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-225"><dt><strong>FOLDERID_ApplicationShortcuts</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-226">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-226">GUID</span></span></td>
<td><span data-ttu-id="f9a52-227">{A3918781-E5F2-4890-B3D9-A7E54332328C}</span><span class="sxs-lookup"><span data-stu-id="f9a52-227">{A3918781-E5F2-4890-B3D9-A7E54332328C}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-228">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-228">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-229">Anwendungs Verknüpfungen</span><span class="sxs-lookup"><span data-stu-id="f9a52-229">Application Shortcuts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-230">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-230">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-231">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-231">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-232">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-232">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-233">%LocalAppData%\microsoft\windows\anwendungstastenkombinationen</span><span class="sxs-lookup"><span data-stu-id="f9a52-233">%LOCALAPPDATA%\Microsoft\Windows\Application Shortcuts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-234">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-234">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-235">None, in Windows 8 eingeführte Wert</span><span class="sxs-lookup"><span data-stu-id="f9a52-235">None, value introduced in Windows 8</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-236">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-236">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-237">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-237">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-238">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-238">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-239">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-239">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_AppsFolder"></span><span id="folderid_appsfolder"></span><span id="FOLDERID_APPSFOLDER"></span><dl> <span data-ttu-id="f9a52-240"><dt><strong>FOLDERID_AppsFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-240"><dt><strong>FOLDERID_AppsFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-241">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-241">GUID</span></span></td>
<td><span data-ttu-id="f9a52-242">{1e87508d-89c2-42f 0-8a7e-645a0l50ca58}</span><span class="sxs-lookup"><span data-stu-id="f9a52-242">{1e87508d-89c2-42f0-8a7e-645a0f50ca58}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-243">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-243">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-244">Anwendungen</span><span class="sxs-lookup"><span data-stu-id="f9a52-244">Applications</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-245">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-245">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-246">Virtu</span><span class="sxs-lookup"><span data-stu-id="f9a52-246">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-247">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-247">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-248">Nicht zutreffend – virtueller Ordner</span><span class="sxs-lookup"><span data-stu-id="f9a52-248">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-249">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-249">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-250">None, in Windows 8 eingeführte Wert</span><span class="sxs-lookup"><span data-stu-id="f9a52-250">None, value introduced in Windows 8</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-251">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-251">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-252">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-252">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-253">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-253">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-254">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-254">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_AppUpdates"></span><span id="folderid_appupdates"></span><span id="FOLDERID_APPUPDATES"></span><dl> <span data-ttu-id="f9a52-255"><dt><strong>FOLDERID_AppUpdates</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-255"><dt><strong>FOLDERID_AppUpdates</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-256">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-256">GUID</span></span></td>
<td><span data-ttu-id="f9a52-257">{a305ce99-f527-492b-8b1a-7e76fa98d6e4}</span><span class="sxs-lookup"><span data-stu-id="f9a52-257">{a305ce99-f527-492b-8b1a-7e76fa98d6e4}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-258">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-258">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-259">Installierte Updates</span><span class="sxs-lookup"><span data-stu-id="f9a52-259">Installed Updates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-260">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-260">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-261">Virtu</span><span class="sxs-lookup"><span data-stu-id="f9a52-261">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-262">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-262">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-263">Nicht zutreffend – virtueller Ordner</span><span class="sxs-lookup"><span data-stu-id="f9a52-263">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-264">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-264">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-265">Keine</span><span class="sxs-lookup"><span data-stu-id="f9a52-265">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-266">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-266">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-267">None, der in Windows Vista eingeführte Wert.</span><span class="sxs-lookup"><span data-stu-id="f9a52-267">None, value introduced in Windows Vista.</span></span> <span data-ttu-id="f9a52-268">In früheren Versionen von Windows waren die Informationen auf dieser Seite in Software enthalten <strong>, wenn das</strong> Kontrollkästchen <strong>Updates anzeigen</strong> aktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="f9a52-268">In earlier versions of Windows, the information on this page was included in <strong>Add or Remove Programs</strong> if the <strong>Show updates</strong> box was checked.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-269">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-269">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-270">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-270">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_CameraRoll"></span><span id="folderid_cameraroll"></span><span id="FOLDERID_CAMERAROLL"></span><dl> <span data-ttu-id="f9a52-271"><dt><strong>FOLDERID_CameraRoll</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-271"><dt><strong>FOLDERID_CameraRoll</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-272">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-272">GUID</span></span></td>
<td><span data-ttu-id="f9a52-273">{AB5FB87B-7CE2-4F83-915D-550846C9537B}</span><span class="sxs-lookup"><span data-stu-id="f9a52-273">{AB5FB87B-7CE2-4F83-915D-550846C9537B}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-274">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-274">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-275">Kamera-Roll</span><span class="sxs-lookup"><span data-stu-id="f9a52-275">Camera Roll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-276">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-276">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-277">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-277">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-278">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-278">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-279">%UserProfile%\pictures\camera Roll</span><span class="sxs-lookup"><span data-stu-id="f9a52-279">%USERPROFILE%\Pictures\Camera Roll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-280">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-280">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-281">None, in Windows 8.1 eingeführte Wert</span><span class="sxs-lookup"><span data-stu-id="f9a52-281">None, value introduced in Windows 8.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-282">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-282">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-283">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-283">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-284">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-284">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-285">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-285">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_CDBurning"></span><span id="folderid_cdburning"></span><span id="FOLDERID_CDBURNING"></span><dl> <span data-ttu-id="f9a52-286"><dt><strong>FOLDERID_CDBurning</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-286"><dt><strong>FOLDERID_CDBurning</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-287">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-287">GUID</span></span></td>
<td><span data-ttu-id="f9a52-288">{9e52ab10-l80d-49df-acb8-4330b5687855}</span><span class="sxs-lookup"><span data-stu-id="f9a52-288">{9E52AB10-F80D-49DF-ACB8-4330F5687855}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-289">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-289">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-290">Temporärer Brenn Ordner</span><span class="sxs-lookup"><span data-stu-id="f9a52-290">Temporary Burn Folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-291">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-291">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-292">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-292">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-293">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-293">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-294">%LocalAppData%\microsoft\windows\burn\burn</span><span class="sxs-lookup"><span data-stu-id="f9a52-294">%LOCALAPPDATA%\Microsoft\Windows\Burn\Burn</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-295">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-295">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-296">CSIDL_CDBURN_AREA</span><span class="sxs-lookup"><span data-stu-id="f9a52-296">CSIDL_CDBURN_AREA</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-297">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-297">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-298">CD-brennen</span><span class="sxs-lookup"><span data-stu-id="f9a52-298">CD Burning</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-299">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-299">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-300">%USERPROFILE%\Local Settings\Application data\microsoft\cd Burning</span><span class="sxs-lookup"><span data-stu-id="f9a52-300">%USERPROFILE%\Local Settings\Application Data\Microsoft\CD Burning</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_ChangeRemovePrograms"></span><span id="folderid_changeremoveprograms"></span><span id="FOLDERID_CHANGEREMOVEPROGRAMS"></span><dl> <span data-ttu-id="f9a52-301"><dt><strong>FOLDERID_ChangeRemovePrograms</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-301"><dt><strong>FOLDERID_ChangeRemovePrograms</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-302">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-302">GUID</span></span></td>
<td><span data-ttu-id="f9a52-303">{df7266ac-9274-4867-8d55-3bd661de872d}</span><span class="sxs-lookup"><span data-stu-id="f9a52-303">{df7266ac-9274-4867-8d55-3bd661de872d}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-304">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-304">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-305">Programme und Funktionen</span><span class="sxs-lookup"><span data-stu-id="f9a52-305">Programs and Features</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-306">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-306">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-307">Virtu</span><span class="sxs-lookup"><span data-stu-id="f9a52-307">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-308">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-308">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-309">Nicht zutreffend – virtueller Ordner</span><span class="sxs-lookup"><span data-stu-id="f9a52-309">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-310">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-310">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-311">Keine</span><span class="sxs-lookup"><span data-stu-id="f9a52-311">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-312">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-312">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-313">Software</span><span class="sxs-lookup"><span data-stu-id="f9a52-313">Add or Remove Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-314">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-314">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-315">Nicht zutreffend – virtueller Ordner</span><span class="sxs-lookup"><span data-stu-id="f9a52-315">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_CommonAdminTools"></span><span id="folderid_commonadmintools"></span><span id="FOLDERID_COMMONADMINTOOLS"></span><dl> <span data-ttu-id="f9a52-316"><dt><strong>FOLDERID_CommonAdminTools</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-316"><dt><strong>FOLDERID_CommonAdminTools</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-317">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-317">GUID</span></span></td>
<td><span data-ttu-id="f9a52-318">{D0384E7D-BAC3-4797-8F14-CBA229B392B5}</span><span class="sxs-lookup"><span data-stu-id="f9a52-318">{D0384E7D-BAC3-4797-8F14-CBA229B392B5}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-319">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-319">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-320">Verwaltung</span><span class="sxs-lookup"><span data-stu-id="f9a52-320">Administrative Tools</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-321">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-321">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-322">Gewöhnliche</span><span class="sxs-lookup"><span data-stu-id="f9a52-322">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-323">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-323">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-324">%ALLUSERSPROFILE%\Microsoft\Windows\Start menu\programs\administrative Tools</span><span class="sxs-lookup"><span data-stu-id="f9a52-324">%ALLUSERSPROFILE%\Microsoft\Windows\Start Menu\Programs\Administrative Tools</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-325">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-325">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-326">CSIDL_COMMON_ADMINTOOLS</span><span class="sxs-lookup"><span data-stu-id="f9a52-326">CSIDL_COMMON_ADMINTOOLS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-327">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-327">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-328">Verwaltung</span><span class="sxs-lookup"><span data-stu-id="f9a52-328">Administrative Tools</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-329">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-329">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-330">%ALLUSERSPROFILE%\Startmenü \ programme\administrative Tools</span><span class="sxs-lookup"><span data-stu-id="f9a52-330">%ALLUSERSPROFILE%\Start Menu\Programs\Administrative Tools</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_CommonOEMLinks"></span><span id="folderid_commonoemlinks"></span><span id="FOLDERID_COMMONOEMLINKS"></span><dl> <span data-ttu-id="f9a52-331"><dt><strong>FOLDERID_CommonOEMLinks</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-331"><dt><strong>FOLDERID_CommonOEMLinks</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-332">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-332">GUID</span></span></td>
<td><span data-ttu-id="f9a52-333">{C1BAE2D0-10df-4334-BEDD-7aa20b227a9d}</span><span class="sxs-lookup"><span data-stu-id="f9a52-333">{C1BAE2D0-10DF-4334-BEDD-7AA20B227A9D}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-334">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-334">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-335">OEM-Links</span><span class="sxs-lookup"><span data-stu-id="f9a52-335">OEM Links</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-336">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-336">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-337">Gewöhnliche</span><span class="sxs-lookup"><span data-stu-id="f9a52-337">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-338">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-338">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-339">%ALLUSERSPROFILE%\oem-Links</span><span class="sxs-lookup"><span data-stu-id="f9a52-339">%ALLUSERSPROFILE%\OEM Links</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-340">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-340">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-341">CSIDL_COMMON_OEM_LINKS</span><span class="sxs-lookup"><span data-stu-id="f9a52-341">CSIDL_COMMON_OEM_LINKS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-342">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-342">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-343">OEM-Links</span><span class="sxs-lookup"><span data-stu-id="f9a52-343">OEM Links</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-344">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-344">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-345">%ALLUSERSPROFILE%\oem-Links</span><span class="sxs-lookup"><span data-stu-id="f9a52-345">%ALLUSERSPROFILE%\OEM Links</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_CommonPrograms"></span><span id="folderid_commonprograms"></span><span id="FOLDERID_COMMONPROGRAMS"></span><dl> <span data-ttu-id="f9a52-346"><dt><strong>FOLDERID_CommonPrograms</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-346"><dt><strong>FOLDERID_CommonPrograms</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-347">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-347">GUID</span></span></td>
<td><span data-ttu-id="f9a52-348">{0139d44e-6afe-49f2-8690-3dafcae6ffb8}</span><span class="sxs-lookup"><span data-stu-id="f9a52-348">{0139D44E-6AFE-49F2-8690-3DAFCAE6FFB8}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-349">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-349">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-350">Programs</span><span class="sxs-lookup"><span data-stu-id="f9a52-350">Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-351">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-351">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-352">Gewöhnliche</span><span class="sxs-lookup"><span data-stu-id="f9a52-352">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-353">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-353">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-354">%ALLUSERSPROFILE%\Microsoft\Windows\Start menu\programme</span><span class="sxs-lookup"><span data-stu-id="f9a52-354">%ALLUSERSPROFILE%\Microsoft\Windows\Start Menu\Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-355">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-355">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-356">CSIDL_COMMON_PROGRAMS</span><span class="sxs-lookup"><span data-stu-id="f9a52-356">CSIDL_COMMON_PROGRAMS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-357">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-357">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-358">Programs</span><span class="sxs-lookup"><span data-stu-id="f9a52-358">Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-359">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-359">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-360">%ALLUSERSPROFILE%\startmenu\programme</span><span class="sxs-lookup"><span data-stu-id="f9a52-360">%ALLUSERSPROFILE%\Start Menu\Programs</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_CommonStartMenu"></span><span id="folderid_commonstartmenu"></span><span id="FOLDERID_COMMONSTARTMENU"></span><dl> <span data-ttu-id="f9a52-361"><dt><strong>FOLDERID_CommonStartMenu</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-361"><dt><strong>FOLDERID_CommonStartMenu</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-362">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-362">GUID</span></span></td>
<td><span data-ttu-id="f9a52-363">{A4115719-D62E-491D-AA7C-E74B8BE3B067}</span><span class="sxs-lookup"><span data-stu-id="f9a52-363">{A4115719-D62E-491D-AA7C-E74B8BE3B067}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-364">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-364">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-365">Startmenü</span><span class="sxs-lookup"><span data-stu-id="f9a52-365">Start Menu</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-366">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-366">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-367">Gewöhnliche</span><span class="sxs-lookup"><span data-stu-id="f9a52-367">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-368">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-368">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-369">%ALLUSERSPROFILE%\microsoft\windows\startmenü</span><span class="sxs-lookup"><span data-stu-id="f9a52-369">%ALLUSERSPROFILE%\Microsoft\Windows\Start Menu</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-370">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-370">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-371">CSIDL_COMMON_STARTMENU</span><span class="sxs-lookup"><span data-stu-id="f9a52-371">CSIDL_COMMON_STARTMENU</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-372">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-372">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-373">Startmenü</span><span class="sxs-lookup"><span data-stu-id="f9a52-373">Start Menu</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-374">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-374">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-375">%ALLUSERSPROFILE%\Startmenü</span><span class="sxs-lookup"><span data-stu-id="f9a52-375">%ALLUSERSPROFILE%\Start Menu</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_CommonStartup"></span><span id="folderid_commonstartup"></span><span id="FOLDERID_COMMONSTARTUP"></span><dl> <span data-ttu-id="f9a52-376"><dt><strong>FOLDERID_CommonStartup</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-376"><dt><strong>FOLDERID_CommonStartup</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-377">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-377">GUID</span></span></td>
<td><span data-ttu-id="f9a52-378">{82a5ea35-d9cd-47c5-9629-e15d2f 714e6e}</span><span class="sxs-lookup"><span data-stu-id="f9a52-378">{82A5EA35-D9CD-47C5-9629-E15D2F714E6E}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-379">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-379">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-380">Start</span><span class="sxs-lookup"><span data-stu-id="f9a52-380">Startup</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-381">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-381">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-382">Gewöhnliche</span><span class="sxs-lookup"><span data-stu-id="f9a52-382">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-383">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-383">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-384">%ALLUSERSPROFILE%\Microsoft\Windows\Start menu\programs\startup</span><span class="sxs-lookup"><span data-stu-id="f9a52-384">%ALLUSERSPROFILE%\Microsoft\Windows\Start Menu\Programs\StartUp</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-385">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-385">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-386">CSIDL_COMMON_STARTUP CSIDL_COMMON_ALTSTARTUP</span><span class="sxs-lookup"><span data-stu-id="f9a52-386">CSIDL_COMMON_STARTUP, CSIDL_COMMON_ALTSTARTUP</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-387">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-387">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-388">Start</span><span class="sxs-lookup"><span data-stu-id="f9a52-388">Startup</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-389">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-389">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-390">%ALLUSERSPROFILE%\Startmenü \ programme\startup</span><span class="sxs-lookup"><span data-stu-id="f9a52-390">%ALLUSERSPROFILE%\Start Menu\Programs\StartUp</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_CommonTemplates"></span><span id="folderid_commontemplates"></span><span id="FOLDERID_COMMONTEMPLATES"></span><dl> <span data-ttu-id="f9a52-391"><dt><strong>FOLDERID_CommonTemplates</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-391"><dt><strong>FOLDERID_CommonTemplates</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-392">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-392">GUID</span></span></td>
<td><span data-ttu-id="f9a52-393">{B94237E7-57ac-4347-9151-B08C6C32D1F7}</span><span class="sxs-lookup"><span data-stu-id="f9a52-393">{B94237E7-57AC-4347-9151-B08C6C32D1F7}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-394">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-394">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-395">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="f9a52-395">Templates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-396">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-396">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-397">Gewöhnliche</span><span class="sxs-lookup"><span data-stu-id="f9a52-397">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-398">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-398">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-399">%ALLUSERSPROFILE%\microsoft\windows\templates</span><span class="sxs-lookup"><span data-stu-id="f9a52-399">%ALLUSERSPROFILE%\Microsoft\Windows\Templates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-400">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-400">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-401">CSIDL_COMMON_TEMPLATES</span><span class="sxs-lookup"><span data-stu-id="f9a52-401">CSIDL_COMMON_TEMPLATES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-402">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-402">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-403">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="f9a52-403">Templates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-404">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-404">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-405">%ALLUSERSPROFILE%\Templates</span><span class="sxs-lookup"><span data-stu-id="f9a52-405">%ALLUSERSPROFILE%\Templates</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ComputerFolder"></span><span id="folderid_computerfolder"></span><span id="FOLDERID_COMPUTERFOLDER"></span><dl> <span data-ttu-id="f9a52-406"><dt><strong>FOLDERID_ComputerFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-406"><dt><strong>FOLDERID_ComputerFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-407">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-407">GUID</span></span></td>
<td><span data-ttu-id="f9a52-408">{0ac0837c-bbf8-452A-850d-79d08e667ca7}</span><span class="sxs-lookup"><span data-stu-id="f9a52-408">{0AC0837C-BBF8-452A-850D-79D08E667CA7}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-409">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-409">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-410">Computer</span><span class="sxs-lookup"><span data-stu-id="f9a52-410">Computer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-411">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-411">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-412">Virtu</span><span class="sxs-lookup"><span data-stu-id="f9a52-412">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-413">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-413">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-414">Nicht zutreffend – virtueller Ordner</span><span class="sxs-lookup"><span data-stu-id="f9a52-414">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-415">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-415">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-416">CSIDL_DRIVES</span><span class="sxs-lookup"><span data-stu-id="f9a52-416">CSIDL_DRIVES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-417">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-417">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-418">Arbeitsplatz</span><span class="sxs-lookup"><span data-stu-id="f9a52-418">My Computer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-419">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-419">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-420">Nicht zutreffend – virtueller Ordner</span><span class="sxs-lookup"><span data-stu-id="f9a52-420">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_ConflictFolder"></span><span id="folderid_conflictfolder"></span><span id="FOLDERID_CONFLICTFOLDER"></span><dl> <span data-ttu-id="f9a52-421"><dt><strong>FOLDERID_ConflictFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-421"><dt><strong>FOLDERID_ConflictFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-422">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-422">GUID</span></span></td>
<td><span data-ttu-id="f9a52-423">{4bfef B45-347d-4006-a5be-ac0cb0567192}</span><span class="sxs-lookup"><span data-stu-id="f9a52-423">{4bfefb45-347d-4006-a5be-ac0cb0567192}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-424">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-424">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-425">Konflikte</span><span class="sxs-lookup"><span data-stu-id="f9a52-425">Conflicts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-426">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-426">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-427">Virtu</span><span class="sxs-lookup"><span data-stu-id="f9a52-427">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-428">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-428">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-429">Nicht zutreffend – virtueller Ordner</span><span class="sxs-lookup"><span data-stu-id="f9a52-429">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-430">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-430">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-431">None, in Windows Vista eingeführte Wert</span><span class="sxs-lookup"><span data-stu-id="f9a52-431">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-432">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-432">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-433">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="f9a52-433">Not applicable.</span></span> <span data-ttu-id="f9a52-434">Diese <strong>KNOWNFOLDERID</strong> bezieht sich auf den Synchronisierungs-Manager von Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f9a52-434">This <strong>KNOWNFOLDERID</strong> refers to the Windows Vista Synchronization Manager.</span></span> <span data-ttu-id="f9a52-435">Dabei handelt es sich nicht um den Ordner, auf den der ältere <a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictfolder"><strong>isyncmgrconflictfolder</strong></a>verweist.</span><span class="sxs-lookup"><span data-stu-id="f9a52-435">It is not the folder referenced by the older <a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictfolder"><strong>ISyncMgrConflictFolder</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-436">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-436">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-437">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-437">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ConnectionsFolder"></span><span id="folderid_connectionsfolder"></span><span id="FOLDERID_CONNECTIONSFOLDER"></span><dl> <span data-ttu-id="f9a52-438"><dt><strong>FOLDERID_ConnectionsFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-438"><dt><strong>FOLDERID_ConnectionsFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-439">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-439">GUID</span></span></td>
<td><span data-ttu-id="f9a52-440">{6f0cd92b-2e97-45D1-88ff-b0d186b8debug}</span><span class="sxs-lookup"><span data-stu-id="f9a52-440">{6F0CD92B-2E97-45D1-88FF-B0D186B8DEDD}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-441">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-441">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-442">Netzwerkverbindungen</span><span class="sxs-lookup"><span data-stu-id="f9a52-442">Network Connections</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-443">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-443">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-444">Virtu</span><span class="sxs-lookup"><span data-stu-id="f9a52-444">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-445">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-445">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-446">Nicht zutreffend – virtueller Ordner</span><span class="sxs-lookup"><span data-stu-id="f9a52-446">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-447">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-447">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-448">CSIDL_CONNECTIONS</span><span class="sxs-lookup"><span data-stu-id="f9a52-448">CSIDL_CONNECTIONS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-449">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-449">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-450">Netzwerkverbindungen</span><span class="sxs-lookup"><span data-stu-id="f9a52-450">Network Connections</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-451">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-451">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-452">Nicht zutreffend – virtueller Ordner</span><span class="sxs-lookup"><span data-stu-id="f9a52-452">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Contacts"></span><span id="folderid_contacts"></span><span id="FOLDERID_CONTACTS"></span><dl> <span data-ttu-id="f9a52-453"><dt><strong>FOLDERID_Contacts</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-453"><dt><strong>FOLDERID_Contacts</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-454">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-454">GUID</span></span></td>
<td><span data-ttu-id="f9a52-455">{56784854-C6CB-462b-8169-88E350ACB882}</span><span class="sxs-lookup"><span data-stu-id="f9a52-455">{56784854-C6CB-462b-8169-88E350ACB882}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-456">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-456">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-457">Kontakte</span><span class="sxs-lookup"><span data-stu-id="f9a52-457">Contacts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-458">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-458">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-459">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-459">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-460">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-460">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-461">%UserProfile%\contacts</span><span class="sxs-lookup"><span data-stu-id="f9a52-461">%USERPROFILE%\Contacts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-462">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-462">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-463">None, in Windows Vista eingeführte Wert</span><span class="sxs-lookup"><span data-stu-id="f9a52-463">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-464">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-464">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-465">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-465">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-466">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-466">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-467">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-467">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ControlPanelFolder"></span><span id="folderid_controlpanelfolder"></span><span id="FOLDERID_CONTROLPANELFOLDER"></span><dl> <span data-ttu-id="f9a52-468"><dt><strong>FOLDERID_ControlPanelFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-468"><dt><strong>FOLDERID_ControlPanelFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-469">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-469">GUID</span></span></td>
<td><span data-ttu-id="f9a52-470">{82a74aeb-aeb4-465c-A014-d097ee346d63}</span><span class="sxs-lookup"><span data-stu-id="f9a52-470">{82A74AEB-AEB4-465C-A014-D097EE346D63}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-471">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-471">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-472">Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="f9a52-472">Control Panel</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-473">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-473">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-474">Virtu</span><span class="sxs-lookup"><span data-stu-id="f9a52-474">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-475">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-475">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-476">Nicht zutreffend – virtueller Ordner</span><span class="sxs-lookup"><span data-stu-id="f9a52-476">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-477">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-477">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-478">CSIDL_CONTROLS</span><span class="sxs-lookup"><span data-stu-id="f9a52-478">CSIDL_CONTROLS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-479">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-479">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-480">Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="f9a52-480">Control Panel</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-481">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-481">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-482">Nicht zutreffend – virtueller Ordner</span><span class="sxs-lookup"><span data-stu-id="f9a52-482">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Cookies"></span><span id="folderid_cookies"></span><span id="FOLDERID_COOKIES"></span><dl> <span data-ttu-id="f9a52-483"><dt><strong>FOLDERID_Cookies</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-483"><dt><strong>FOLDERID_Cookies</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-484">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-484">GUID</span></span></td>
<td><span data-ttu-id="f9a52-485">{2b0f765d-c0e9-4171-908e-08a611b84 FF6}</span><span class="sxs-lookup"><span data-stu-id="f9a52-485">{2B0F765D-C0E9-4171-908E-08A611B84FF6}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-486">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-486">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-487">Cookies</span><span class="sxs-lookup"><span data-stu-id="f9a52-487">Cookies</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-488">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-488">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-489">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-489">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-490">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-490">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-491">%APPDATA%\microsoft\windows\cookies</span><span class="sxs-lookup"><span data-stu-id="f9a52-491">%APPDATA%\Microsoft\Windows\Cookies</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-492">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-492">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-493">CSIDL_COOKIES</span><span class="sxs-lookup"><span data-stu-id="f9a52-493">CSIDL_COOKIES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-494">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-494">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-495">Cookies</span><span class="sxs-lookup"><span data-stu-id="f9a52-495">Cookies</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-496">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-496">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-497">%UserProfile%\Cookies</span><span class="sxs-lookup"><span data-stu-id="f9a52-497">%USERPROFILE%\Cookies</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Desktop"></span><span id="folderid_desktop"></span><span id="FOLDERID_DESKTOP"></span><dl> <span data-ttu-id="f9a52-498"><dt><strong>FOLDERID_Desktop</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-498"><dt><strong>FOLDERID_Desktop</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-499">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-499">GUID</span></span></td>
<td><span data-ttu-id="f9a52-500">{B4BFCC3A-DB2C-424C-B029-7FE99A87C641}</span><span class="sxs-lookup"><span data-stu-id="f9a52-500">{B4BFCC3A-DB2C-424C-B029-7FE99A87C641}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-501">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-501">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-502">Desktop</span><span class="sxs-lookup"><span data-stu-id="f9a52-502">Desktop</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-503">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-503">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-504">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-504">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-505">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-505">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-506">%Userprofile%\desktop</span><span class="sxs-lookup"><span data-stu-id="f9a52-506">%USERPROFILE%\Desktop</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-507">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-507">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-508">CSIDL_DESKTOP CSIDL_DESKTOPDIRECTORY</span><span class="sxs-lookup"><span data-stu-id="f9a52-508">CSIDL_DESKTOP, CSIDL_DESKTOPDIRECTORY</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-509">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-509">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-510">Desktop</span><span class="sxs-lookup"><span data-stu-id="f9a52-510">Desktop</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-511">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-511">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-512">%Userprofile%\desktop</span><span class="sxs-lookup"><span data-stu-id="f9a52-512">%USERPROFILE%\Desktop</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_DeviceMetadataStore"></span><span id="folderid_devicemetadatastore"></span><span id="FOLDERID_DEVICEMETADATASTORE"></span><dl> <span data-ttu-id="f9a52-513"><dt><strong>FOLDERID_DeviceMetadataStore</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-513"><dt><strong>FOLDERID_DeviceMetadataStore</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-514">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-514">GUID</span></span></td>
<td><span data-ttu-id="f9a52-515">{5ce4a5e9-e4eb-479d-B89B-130c02886155}</span><span class="sxs-lookup"><span data-stu-id="f9a52-515">{5CE4A5E9-E4EB-479D-B89F-130C02886155}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-516">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-516">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-517">DeviceMetadataStore</span><span class="sxs-lookup"><span data-stu-id="f9a52-517">DeviceMetadataStore</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-518">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-518">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-519">Gewöhnliche</span><span class="sxs-lookup"><span data-stu-id="f9a52-519">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-520">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-520">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-521">%ALLUSERSPROFILE%\Microsoft\Windows\DeviceMetadataStore</span><span class="sxs-lookup"><span data-stu-id="f9a52-521">%ALLUSERSPROFILE%\Microsoft\Windows\DeviceMetadataStore</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-522">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-522">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-523">None, in Windows 7 eingeführte Wert</span><span class="sxs-lookup"><span data-stu-id="f9a52-523">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-524">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-524">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-525">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-525">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-526">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-526">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-527">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-527">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Documents"></span><span id="folderid_documents"></span><span id="FOLDERID_DOCUMENTS"></span><dl> <span data-ttu-id="f9a52-528"><dt><strong>FOLDERID_Documents</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-528"><dt><strong>FOLDERID_Documents</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-529">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-529">GUID</span></span></td>
<td><span data-ttu-id="f9a52-530">{FDD39AD0-238F-46AF-ADB4-6C85480369C7}</span><span class="sxs-lookup"><span data-stu-id="f9a52-530">{FDD39AD0-238F-46AF-ADB4-6C85480369C7}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-531">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-531">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-532">Dokumente</span><span class="sxs-lookup"><span data-stu-id="f9a52-532">Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-533">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-533">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-534">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-534">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-535">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-535">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-536">%UserProfile%\Documents</span><span class="sxs-lookup"><span data-stu-id="f9a52-536">%USERPROFILE%\Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-537">CSIDL-Entsprechungen</span><span class="sxs-lookup"><span data-stu-id="f9a52-537">CSIDL Equivalents</span></span></td>
<td><span data-ttu-id="f9a52-538">CSIDL_MYDOCUMENTS CSIDL_PERSONAL</span><span class="sxs-lookup"><span data-stu-id="f9a52-538">CSIDL_MYDOCUMENTS, CSIDL_PERSONAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-539">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-539">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-540">Meine Dokumente</span><span class="sxs-lookup"><span data-stu-id="f9a52-540">My Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-541">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-541">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-542">%USERPROFILE%\Eigene Dokumente</span><span class="sxs-lookup"><span data-stu-id="f9a52-542">%USERPROFILE%\My Documents</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_DocumentsLibrary"></span><span id="folderid_documentslibrary"></span><span id="FOLDERID_DOCUMENTSLIBRARY"></span><dl> <span data-ttu-id="f9a52-543"><dt><strong>FOLDERID_DocumentsLibrary</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-543"><dt><strong>FOLDERID_DocumentsLibrary</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-544">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-544">GUID</span></span></td>
<td><span data-ttu-id="f9a52-545">{7b0db17d-9cd2-4A93-9733-46cc89022e7c}</span><span class="sxs-lookup"><span data-stu-id="f9a52-545">{7B0DB17D-9CD2-4A93-9733-46CC89022E7C}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-546">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-546">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-547">Dokumente</span><span class="sxs-lookup"><span data-stu-id="f9a52-547">Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-548">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-548">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-549">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-549">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-550">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-550">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-551">%APPDATA%\microsoft\windows\libraries\documents.Library-MS</span><span class="sxs-lookup"><span data-stu-id="f9a52-551">%APPDATA%\Microsoft\Windows\Libraries\Documents.library-ms</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-552">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-552">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-553">None, in Windows 7 eingeführte Wert</span><span class="sxs-lookup"><span data-stu-id="f9a52-553">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-554">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-554">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-555">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-555">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-556">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-556">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-557">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-557">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Downloads"></span><span id="folderid_downloads"></span><span id="FOLDERID_DOWNLOADS"></span><dl> <span data-ttu-id="f9a52-558"><dt><strong>FOLDERID_Downloads</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-558"><dt><strong>FOLDERID_Downloads</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-559">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-559">GUID</span></span></td>
<td><span data-ttu-id="f9a52-560">{374DE290-123F-4565-9164-39C4925E467B}</span><span class="sxs-lookup"><span data-stu-id="f9a52-560">{374DE290-123F-4565-9164-39C4925E467B}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-561">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-561">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-562">Downloads</span><span class="sxs-lookup"><span data-stu-id="f9a52-562">Downloads</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-563">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-563">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-564">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-564">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-565">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-565">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-566">%UserProfile%\downloads</span><span class="sxs-lookup"><span data-stu-id="f9a52-566">%USERPROFILE%\Downloads</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-567">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-567">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-568">Keine</span><span class="sxs-lookup"><span data-stu-id="f9a52-568">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-569">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-569">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-570">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-570">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-571">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-571">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-572">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-572">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Favorites"></span><span id="folderid_favorites"></span><span id="FOLDERID_FAVORITES"></span><dl> <span data-ttu-id="f9a52-573"><dt><strong>FOLDERID_Favorites</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-573"><dt><strong>FOLDERID_Favorites</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-574">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-574">GUID</span></span></td>
<td><span data-ttu-id="f9a52-575">{1777F761-68AD-4D8A-87BD-30B759FA33DD}</span><span class="sxs-lookup"><span data-stu-id="f9a52-575">{1777F761-68AD-4D8A-87BD-30B759FA33DD}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-576">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-576">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-577">Favoriten</span><span class="sxs-lookup"><span data-stu-id="f9a52-577">Favorites</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-578">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-578">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-579">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-579">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-580">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-580">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-581">%UserProfile%\Favoriten</span><span class="sxs-lookup"><span data-stu-id="f9a52-581">%USERPROFILE%\Favorites</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-582">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-582">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-583">CSIDL_FAVORITES CSIDL_COMMON_FAVORITES</span><span class="sxs-lookup"><span data-stu-id="f9a52-583">CSIDL_FAVORITES, CSIDL_COMMON_FAVORITES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-584">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-584">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-585">Favoriten</span><span class="sxs-lookup"><span data-stu-id="f9a52-585">Favorites</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-586">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-586">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-587">%UserProfile%\Favoriten</span><span class="sxs-lookup"><span data-stu-id="f9a52-587">%USERPROFILE%\Favorites</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Fonts"></span><span id="folderid_fonts"></span><span id="FOLDERID_FONTS"></span><dl> <span data-ttu-id="f9a52-588"><dt><strong>FOLDERID_Fonts</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-588"><dt><strong>FOLDERID_Fonts</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-589">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-589">GUID</span></span></td>
<td><span data-ttu-id="f9a52-590">{FD228CB7-AE11-4AE3-864C-16F3910AB8FE}</span><span class="sxs-lookup"><span data-stu-id="f9a52-590">{FD228CB7-AE11-4AE3-864C-16F3910AB8FE}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-591">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-591">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-592">Schriftarten</span><span class="sxs-lookup"><span data-stu-id="f9a52-592">Fonts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-593">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-593">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-594">FIXED</span><span class="sxs-lookup"><span data-stu-id="f9a52-594">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-595">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-595">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-596">%WINDIR%\fonts</span><span class="sxs-lookup"><span data-stu-id="f9a52-596">%windir%\Fonts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-597">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-597">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-598">CSIDL_FONTS</span><span class="sxs-lookup"><span data-stu-id="f9a52-598">CSIDL_FONTS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-599">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-599">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-600">Schriftarten</span><span class="sxs-lookup"><span data-stu-id="f9a52-600">Fonts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-601">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-601">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-602">%WINDIR%\fonts</span><span class="sxs-lookup"><span data-stu-id="f9a52-602">%windir%\Fonts</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Games"></span><span id="folderid_games"></span><span id="FOLDERID_GAMES"></span><dl> <span data-ttu-id="f9a52-603"><dt><strong>FOLDERID_Games</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-603"><dt><strong>FOLDERID_Games</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="f9a52-604">Diese folderid ist in Windows 10, Version 1803 und höheren Versionen, veraltet.</span><span class="sxs-lookup"><span data-stu-id="f9a52-604">This FOLDERID is deprecated in Windows 10, version 1803 and later versions.</span></span> <span data-ttu-id="f9a52-605">In diesen Versionen wird <strong>0x80070057-E_INVALIDARG</strong> zurückgegeben.
</span><span class="sxs-lookup"><span data-stu-id="f9a52-605">In these versions, it returns <strong>0x80070057 - E_INVALIDARG</strong>
</span></span></blockquote>
</div>
<div>
 
</div>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-606">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-606">GUID</span></span></td>
<td><span data-ttu-id="f9a52-607">{CAC52C1A-B53D-4edc-92D7-6B2E8AC19434}</span><span class="sxs-lookup"><span data-stu-id="f9a52-607">{CAC52C1A-B53D-4edc-92D7-6B2E8AC19434}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-608">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-608">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-609">Spiele</span><span class="sxs-lookup"><span data-stu-id="f9a52-609">Games</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-610">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-610">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-611">Virtu</span><span class="sxs-lookup"><span data-stu-id="f9a52-611">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-612">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-612">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-613">Nicht zutreffend – virtueller Ordner</span><span class="sxs-lookup"><span data-stu-id="f9a52-613">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-614">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-614">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-615">Keine</span><span class="sxs-lookup"><span data-stu-id="f9a52-615">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-616">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-616">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-617">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-617">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-618">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-618">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-619">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-619">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_GameTasks"></span><span id="folderid_gametasks"></span><span id="FOLDERID_GAMETASKS"></span><dl> <span data-ttu-id="f9a52-620"><dt><strong>FOLDERID_GameTasks</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-620"><dt><strong>FOLDERID_GameTasks</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-621">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-621">GUID</span></span></td>
<td><span data-ttu-id="f9a52-622">{054fae61-4dd8-4787-80b6-090220c4b700}</span><span class="sxs-lookup"><span data-stu-id="f9a52-622">{054FAE61-4DD8-4787-80B6-090220C4B700}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-623">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-623">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-624">GameExplorer</span><span class="sxs-lookup"><span data-stu-id="f9a52-624">GameExplorer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-625">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-625">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-626">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-626">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-627">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-627">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-628">%LocalAppData%\microsoft\windows\gameexplorer</span><span class="sxs-lookup"><span data-stu-id="f9a52-628">%LOCALAPPDATA%\Microsoft\Windows\GameExplorer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-629">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-629">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-630">None, in Windows Vista eingeführte Wert</span><span class="sxs-lookup"><span data-stu-id="f9a52-630">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-631">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-631">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-632">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-632">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-633">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-633">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-634">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-634">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_History"></span><span id="folderid_history"></span><span id="FOLDERID_HISTORY"></span><dl> <span data-ttu-id="f9a52-635"><dt><strong>FOLDERID_History</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-635"><dt><strong>FOLDERID_History</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-636">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-636">GUID</span></span></td>
<td><span data-ttu-id="f9a52-637">{D9DC8A3B-B784-432E-A781-5A1130A75963}</span><span class="sxs-lookup"><span data-stu-id="f9a52-637">{D9DC8A3B-B784-432E-A781-5A1130A75963}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-638">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-638">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-639">Verlauf</span><span class="sxs-lookup"><span data-stu-id="f9a52-639">History</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-640">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-640">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-641">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-641">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-642">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-642">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-643">%LocalAppData%\microsoft\windows\history</span><span class="sxs-lookup"><span data-stu-id="f9a52-643">%LOCALAPPDATA%\Microsoft\Windows\History</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-644">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-644">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-645">CSIDL_HISTORY</span><span class="sxs-lookup"><span data-stu-id="f9a52-645">CSIDL_HISTORY</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-646">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-646">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-647">Verlauf</span><span class="sxs-lookup"><span data-stu-id="f9a52-647">History</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-648">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-648">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-649">%USERPROFILE%\Local Settings\History</span><span class="sxs-lookup"><span data-stu-id="f9a52-649">%USERPROFILE%\Local Settings\History</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_HomeGroup"></span><span id="folderid_homegroup"></span><span id="FOLDERID_HOMEGROUP"></span><dl> <span data-ttu-id="f9a52-650"><dt><strong>FOLDERID_HomeGroup</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-650"><dt><strong>FOLDERID_HomeGroup</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-651">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-651">GUID</span></span></td>
<td><span data-ttu-id="f9a52-652">{52528a6b-b9e3-4 Add-b60d-588c2dba842d}</span><span class="sxs-lookup"><span data-stu-id="f9a52-652">{52528A6B-B9E3-4ADD-B60D-588C2DBA842D}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-653">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-653">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-654">Heimnetzgruppe</span><span class="sxs-lookup"><span data-stu-id="f9a52-654">Homegroup</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-655">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-655">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-656">Virtu</span><span class="sxs-lookup"><span data-stu-id="f9a52-656">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-657">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-657">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-658">Nicht zutreffend – virtueller Ordner</span><span class="sxs-lookup"><span data-stu-id="f9a52-658">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-659">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-659">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-660">None, in Windows 7 eingeführte Wert</span><span class="sxs-lookup"><span data-stu-id="f9a52-660">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-661">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-661">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-662">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-662">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-663">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-663">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-664">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-664">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_HomeGroupCurrentUser"></span><span id="folderid_homegroupcurrentuser"></span><span id="FOLDERID_HOMEGROUPCURRENTUSER"></span><dl> <span data-ttu-id="f9a52-665"><dt><strong>FOLDERID_HomeGroupCurrentUser</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-665"><dt><strong>FOLDERID_HomeGroupCurrentUser</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-666">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-666">GUID</span></span></td>
<td><span data-ttu-id="f9a52-667">{9b74b6a3-0dfd-4f 11-9e78-5 f</span><span class="sxs-lookup"><span data-stu-id="f9a52-667">{9B74B6A3-0DFD-4f11-9E78-5F7800F2E772}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-668">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-668">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-669">Der Benutzername des Benutzers (% username%)</span><span class="sxs-lookup"><span data-stu-id="f9a52-669">The user's username (%USERNAME%)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-670">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-670">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-671">Virtu</span><span class="sxs-lookup"><span data-stu-id="f9a52-671">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-672">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-672">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-673">Nicht zutreffend – virtueller Ordner</span><span class="sxs-lookup"><span data-stu-id="f9a52-673">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-674">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-674">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-675">None, in Windows 8 eingeführte Wert</span><span class="sxs-lookup"><span data-stu-id="f9a52-675">None, value introduced in Windows 8</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-676">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-676">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-677">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-677">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-678">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-678">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-679">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-679">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ImplicitAppShortcuts"></span><span id="folderid_implicitappshortcuts"></span><span id="FOLDERID_IMPLICITAPPSHORTCUTS"></span><dl> <span data-ttu-id="f9a52-680"><dt><strong>FOLDERID_ImplicitAppShortcuts</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-680"><dt><strong>FOLDERID_ImplicitAppShortcuts</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-681">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-681">GUID</span></span></td>
<td><span data-ttu-id="f9a52-682">{BCB5256F-79F6-4CEE-B725-DC34E402FD46}</span><span class="sxs-lookup"><span data-stu-id="f9a52-682">{BCB5256F-79F6-4CEE-B725-DC34E402FD46}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-683">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-683">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-684">Implicitappverknüpfungen</span><span class="sxs-lookup"><span data-stu-id="f9a52-684">ImplicitAppShortcuts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-685">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-685">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-686">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-686">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-687">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-687">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-688">%APPDATA%\microsoft\internet Explorer\Quick launch\user pinned\implicitappverknüpfungen</span><span class="sxs-lookup"><span data-stu-id="f9a52-688">%APPDATA%\Microsoft\Internet Explorer\Quick Launch\User Pinned\ImplicitAppShortcuts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-689">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-689">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-690">None, in Windows 7 eingeführte Wert</span><span class="sxs-lookup"><span data-stu-id="f9a52-690">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-691">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-691">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-692">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-692">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-693">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-693">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-694">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-694">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_InternetCache"></span><span id="folderid_internetcache"></span><span id="FOLDERID_INTERNETCACHE"></span><dl> <span data-ttu-id="f9a52-695"><dt><strong>FOLDERID_InternetCache</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-695"><dt><strong>FOLDERID_InternetCache</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-696">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-696">GUID</span></span></td>
<td><span data-ttu-id="f9a52-697">{352481e8-33be-4251-BA85-6007caedcf9d}</span><span class="sxs-lookup"><span data-stu-id="f9a52-697">{352481E8-33BE-4251-BA85-6007CAEDCF9D}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-698">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-698">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-699">Temporäre Internetdateien</span><span class="sxs-lookup"><span data-stu-id="f9a52-699">Temporary Internet Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-700">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-700">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-701">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-701">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-702">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-702">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-703">%LocalAppData%\microsoft\windows\temporäre Internet Dateien</span><span class="sxs-lookup"><span data-stu-id="f9a52-703">%LOCALAPPDATA%\Microsoft\Windows\Temporary Internet Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-704">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-704">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-705">CSIDL_INTERNET_CACHE</span><span class="sxs-lookup"><span data-stu-id="f9a52-705">CSIDL_INTERNET_CACHE</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-706">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-706">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-707">Temporäre Internetdateien</span><span class="sxs-lookup"><span data-stu-id="f9a52-707">Temporary Internet Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-708">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-708">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-709">%USERPROFILE%\Local settings\temporäre Internet Dateien</span><span class="sxs-lookup"><span data-stu-id="f9a52-709">%USERPROFILE%\Local Settings\Temporary Internet Files</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_InternetFolder"></span><span id="folderid_internetfolder"></span><span id="FOLDERID_INTERNETFOLDER"></span><dl> <span data-ttu-id="f9a52-710"><dt><strong>FOLDERID_InternetFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-710"><dt><strong>FOLDERID_InternetFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-711">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-711">GUID</span></span></td>
<td><span data-ttu-id="f9a52-712">{4d9f 7874-4e0c-4904-967b-40b0d20c3e4b}</span><span class="sxs-lookup"><span data-stu-id="f9a52-712">{4D9F7874-4E0C-4904-967B-40B0D20C3E4B}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-713">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-713">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-714">Das Internet</span><span class="sxs-lookup"><span data-stu-id="f9a52-714">The Internet</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-715">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-715">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-716">Virtu</span><span class="sxs-lookup"><span data-stu-id="f9a52-716">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-717">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-717">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-718">Nicht zutreffend – virtueller Ordner</span><span class="sxs-lookup"><span data-stu-id="f9a52-718">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-719">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-719">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-720">CSIDL_INTERNET</span><span class="sxs-lookup"><span data-stu-id="f9a52-720">CSIDL_INTERNET</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-721">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-721">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-722">Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="f9a52-722">Internet Explorer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-723">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-723">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-724">Nicht zutreffend – virtueller Ordner</span><span class="sxs-lookup"><span data-stu-id="f9a52-724">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Libraries"></span><span id="folderid_libraries"></span><span id="FOLDERID_LIBRARIES"></span><dl> <span data-ttu-id="f9a52-725"><dt><strong>FOLDERID_Libraries</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-725"><dt><strong>FOLDERID_Libraries</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-726">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-726">GUID</span></span></td>
<td><span data-ttu-id="f9a52-727">{1b3ea5dc-B587-4786-b4ef-bd1dc332aeae}</span><span class="sxs-lookup"><span data-stu-id="f9a52-727">{1B3EA5DC-B587-4786-B4EF-BD1DC332AEAE}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-728">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-728">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-729">Bibliotheken</span><span class="sxs-lookup"><span data-stu-id="f9a52-729">Libraries</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-730">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-730">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-731">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-731">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-732">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-732">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-733">%Appdata%\microsoft\windows\libraries</span><span class="sxs-lookup"><span data-stu-id="f9a52-733">%APPDATA%\Microsoft\Windows\Libraries</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-734">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-734">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-735">None, in Windows 7 eingeführte Wert</span><span class="sxs-lookup"><span data-stu-id="f9a52-735">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-736">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-736">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-737">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-737">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-738">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-738">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-739">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-739">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Links"></span><span id="folderid_links"></span><span id="FOLDERID_LINKS"></span><dl> <span data-ttu-id="f9a52-740"><dt><strong>FOLDERID_Links</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-740"><dt><strong>FOLDERID_Links</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-741">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-741">GUID</span></span></td>
<td><span data-ttu-id="f9a52-742">{bfb9d5e0-c6a9-404c-b2b2-ae6db6af4968}</span><span class="sxs-lookup"><span data-stu-id="f9a52-742">{bfb9d5e0-c6a9-404c-b2b2-ae6db6af4968}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-743">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-743">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-744">Links</span><span class="sxs-lookup"><span data-stu-id="f9a52-744">Links</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-745">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-745">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-746">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-746">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-747">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-747">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-748">%UserProfile%\links</span><span class="sxs-lookup"><span data-stu-id="f9a52-748">%USERPROFILE%\Links</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-749">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-749">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-750">Keine</span><span class="sxs-lookup"><span data-stu-id="f9a52-750">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-751">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-751">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-752">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-752">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-753">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-753">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-754">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-754">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_LocalAppData"></span><span id="folderid_localappdata"></span><span id="FOLDERID_LOCALAPPDATA"></span><dl> <span data-ttu-id="f9a52-755"><dt><strong>FOLDERID_LocalAppData</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-755"><dt><strong>FOLDERID_LocalAppData</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-756">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-756">GUID</span></span></td>
<td><span data-ttu-id="f9a52-757">{F1B32785-6FBA-4FCF-9D55-7B8E7F157091}</span><span class="sxs-lookup"><span data-stu-id="f9a52-757">{F1B32785-6FBA-4FCF-9D55-7B8E7F157091}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-758">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-758">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-759">Lokal</span><span class="sxs-lookup"><span data-stu-id="f9a52-759">Local</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-760">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-760">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-761">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-761">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-762">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-762">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-763">% LocalAppData% (%userprofile%\AppData\Local)</span><span class="sxs-lookup"><span data-stu-id="f9a52-763">%LOCALAPPDATA% (%USERPROFILE%\AppData\Local)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-764">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-764">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-765">CSIDL_LOCAL_APPDATA</span><span class="sxs-lookup"><span data-stu-id="f9a52-765">CSIDL_LOCAL_APPDATA</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-766">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-766">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-767">Anwendungsdaten</span><span class="sxs-lookup"><span data-stu-id="f9a52-767">Application Data</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-768">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-768">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-769">%Userprofile%\Lokale Einstellungen\Anwendungsdaten</span><span class="sxs-lookup"><span data-stu-id="f9a52-769">%USERPROFILE%\Local Settings\Application Data</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_LocalAppDataLow"></span><span id="folderid_localappdatalow"></span><span id="FOLDERID_LOCALAPPDATALOW"></span><dl> <span data-ttu-id="f9a52-770"><dt><strong>FOLDERID_LocalAppDataLow</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-770"><dt><strong>FOLDERID_LocalAppDataLow</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-771">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-771">GUID</span></span></td>
<td><span data-ttu-id="f9a52-772">{A520A1A4-1780-4FF6-BD18-167343C5AF16}</span><span class="sxs-lookup"><span data-stu-id="f9a52-772">{A520A1A4-1780-4FF6-BD18-167343C5AF16}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-773">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-773">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-774">LocalLow</span><span class="sxs-lookup"><span data-stu-id="f9a52-774">LocalLow</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-775">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-775">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-776">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-776">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-777">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-777">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-778">%UserProfile%\appdata\locallow</span><span class="sxs-lookup"><span data-stu-id="f9a52-778">%USERPROFILE%\AppData\LocalLow</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-779">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-779">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-780">Keine</span><span class="sxs-lookup"><span data-stu-id="f9a52-780">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-781">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-781">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-782">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-782">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-783">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-783">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-784">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-784">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_LocalizedResourcesDir"></span><span id="folderid_localizedresourcesdir"></span><span id="FOLDERID_LOCALIZEDRESOURCESDIR"></span><dl> <span data-ttu-id="f9a52-785"><dt><strong>FOLDERID_LocalizedResourcesDir</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-785"><dt><strong>FOLDERID_LocalizedResourcesDir</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-786">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-786">GUID</span></span></td>
<td><span data-ttu-id="f9a52-787">{2a00375e-224c-49DE-b8d1-440df7ef3ddc}</span><span class="sxs-lookup"><span data-stu-id="f9a52-787">{2A00375E-224C-49DE-B8D1-440DF7EF3DDC}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-788">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-788">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-789">Keine</span><span class="sxs-lookup"><span data-stu-id="f9a52-789">None</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-790">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-790">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-791">FIXED</span><span class="sxs-lookup"><span data-stu-id="f9a52-791">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-792">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-792">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-793">%windir%\resources\0409 (Codepage)</span><span class="sxs-lookup"><span data-stu-id="f9a52-793">%windir%\resources\0409 (code page)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-794">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-794">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-795">CSIDL_RESOURCES_LOCALIZED</span><span class="sxs-lookup"><span data-stu-id="f9a52-795">CSIDL_RESOURCES_LOCALIZED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-796">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-796">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-797">Keine</span><span class="sxs-lookup"><span data-stu-id="f9a52-797">None</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-798">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-798">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-799">%windir%\resources\0409 (Codepage)</span><span class="sxs-lookup"><span data-stu-id="f9a52-799">%windir%\resources\0409 (code page)</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Music"></span><span id="folderid_music"></span><span id="FOLDERID_MUSIC"></span><dl> <span data-ttu-id="f9a52-800"><dt><strong>FOLDERID_Music</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-800"><dt><strong>FOLDERID_Music</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-801">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-801">GUID</span></span></td>
<td><span data-ttu-id="f9a52-802">{4BD8D571-6D19-48D3-BE97-422220080E43}</span><span class="sxs-lookup"><span data-stu-id="f9a52-802">{4BD8D571-6D19-48D3-BE97-422220080E43}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-803">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-803">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-804">Musik</span><span class="sxs-lookup"><span data-stu-id="f9a52-804">Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-805">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-805">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-806">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-806">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-807">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-807">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-808">%UserProfile%\Music</span><span class="sxs-lookup"><span data-stu-id="f9a52-808">%USERPROFILE%\Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-809">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-809">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-810">CSIDL_MYMUSIC</span><span class="sxs-lookup"><span data-stu-id="f9a52-810">CSIDL_MYMUSIC</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-811">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-811">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-812">Meine Musik</span><span class="sxs-lookup"><span data-stu-id="f9a52-812">My Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-813">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-813">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-814">%USERPROFILE%\Eigene Dateien\Eigene Musik</span><span class="sxs-lookup"><span data-stu-id="f9a52-814">%USERPROFILE%\My Documents\My Music</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_MusicLibrary"></span><span id="folderid_musiclibrary"></span><span id="FOLDERID_MUSICLIBRARY"></span><dl> <span data-ttu-id="f9a52-815"><dt><strong>FOLDERID_MusicLibrary</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-815"><dt><strong>FOLDERID_MusicLibrary</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-816">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-816">GUID</span></span></td>
<td><span data-ttu-id="f9a52-817">{2112ab0a-c86a-4ffe-a368-0de96e47012e}</span><span class="sxs-lookup"><span data-stu-id="f9a52-817">{2112AB0A-C86A-4FFE-A368-0DE96E47012E}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-818">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-818">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-819">Musik</span><span class="sxs-lookup"><span data-stu-id="f9a52-819">Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-820">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-820">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-821">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-821">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-822">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-822">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-823">%APPDATA%\microsoft\windows\libraries\music.Library-MS</span><span class="sxs-lookup"><span data-stu-id="f9a52-823">%APPDATA%\Microsoft\Windows\Libraries\Music.library-ms</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-824">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-824">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-825">None, in Windows 7 eingeführte Wert</span><span class="sxs-lookup"><span data-stu-id="f9a52-825">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-826">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-826">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-827">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-827">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-828">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-828">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-829">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-829">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_NetHood"></span><span id="folderid_nethood"></span><span id="FOLDERID_NETHOOD"></span><dl> <span data-ttu-id="f9a52-830"><dt><strong>FOLDERID_NetHood</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-830"><dt><strong>FOLDERID_NetHood</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-831">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-831">GUID</span></span></td>
<td><span data-ttu-id="f9a52-832">{C5ABBF53-E17F-4121-8900-86626FC2C973}</span><span class="sxs-lookup"><span data-stu-id="f9a52-832">{C5ABBF53-E17F-4121-8900-86626FC2C973}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-833">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-833">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-834">Netzwerk Verknüpfungen</span><span class="sxs-lookup"><span data-stu-id="f9a52-834">Network Shortcuts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-835">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-835">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-836">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-836">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-837">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-837">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-838">%APPDATA%\microsoft\windows\network Tastenkombinationen</span><span class="sxs-lookup"><span data-stu-id="f9a52-838">%APPDATA%\Microsoft\Windows\Network Shortcuts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-839">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-839">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-840">CSIDL_NETHOOD</span><span class="sxs-lookup"><span data-stu-id="f9a52-840">CSIDL_NETHOOD</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-841">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-841">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-842">Nicht mehr</span><span class="sxs-lookup"><span data-stu-id="f9a52-842">NetHood</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-843">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-843">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-844">%UserProfile%\netthood</span><span class="sxs-lookup"><span data-stu-id="f9a52-844">%USERPROFILE%\NetHood</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_NetworkFolder"></span><span id="folderid_networkfolder"></span><span id="FOLDERID_NETWORKFOLDER"></span><dl> <span data-ttu-id="f9a52-845"><dt><strong>FOLDERID_NetworkFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-845"><dt><strong>FOLDERID_NetworkFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-846">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-846">GUID</span></span></td>
<td><span data-ttu-id="f9a52-847">{D20BEEC4-5CA8-4905-AE3B-BF251EA09B53}</span><span class="sxs-lookup"><span data-stu-id="f9a52-847">{D20BEEC4-5CA8-4905-AE3B-BF251EA09B53}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-848">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-848">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-849">Netzwerk</span><span class="sxs-lookup"><span data-stu-id="f9a52-849">Network</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-850">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-850">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-851">Virtu</span><span class="sxs-lookup"><span data-stu-id="f9a52-851">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-852">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-852">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-853">Nicht zutreffend – virtueller Ordner</span><span class="sxs-lookup"><span data-stu-id="f9a52-853">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-854">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-854">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-855">CSIDL_NETWORK CSIDL_COMPUTERSNEARME</span><span class="sxs-lookup"><span data-stu-id="f9a52-855">CSIDL_NETWORK, CSIDL_COMPUTERSNEARME</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-856">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-856">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-857">Meine Netzwerk Orte</span><span class="sxs-lookup"><span data-stu-id="f9a52-857">My Network Places</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-858">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-858">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-859">Nicht zutreffend – virtueller Ordner</span><span class="sxs-lookup"><span data-stu-id="f9a52-859">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Objects3D"></span><span id="folderid_objects3d"></span><span id="FOLDERID_OBJECTS3D"></span><dl> <span data-ttu-id="f9a52-860"><dt><strong>FOLDERID_Objects3D</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-860"><dt><strong>FOLDERID_Objects3D</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-861">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-861">GUID</span></span></td>
<td><span data-ttu-id="f9a52-862">{31c0dd25-9439-4f12-bf41-7ff4eda38722}</span><span class="sxs-lookup"><span data-stu-id="f9a52-862">{31C0DD25-9439-4F12-BF41-7FF4EDA38722}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-863">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-863">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-864">3D-Objekte</span><span class="sxs-lookup"><span data-stu-id="f9a52-864">3D Objects</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-865">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-865">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-866">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-866">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-867">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-867">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-868">%UserProfile%\3d-Objekte</span><span class="sxs-lookup"><span data-stu-id="f9a52-868">%USERPROFILE%\3D Objects</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-869">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-869">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-870">None, in Windows 10 eingeführte Wert, Version 1703</span><span class="sxs-lookup"><span data-stu-id="f9a52-870">None, value introduced in Windows 10, version 1703</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-871">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-871">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-872">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-872">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-873">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-873">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-874">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-874">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_OriginalImages"></span><span id="folderid_originalimages"></span><span id="FOLDERID_ORIGINALIMAGES"></span><dl> <span data-ttu-id="f9a52-875"><dt><strong>FOLDERID_OriginalImages</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-875"><dt><strong>FOLDERID_OriginalImages</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-876">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-876">GUID</span></span></td>
<td><span data-ttu-id="f9a52-877">{2c36c0aa-5812-4b87-b bbb0-4cd0dfb19b39}</span><span class="sxs-lookup"><span data-stu-id="f9a52-877">{2C36C0AA-5812-4b87-BFD0-4CD0DFB19B39}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-878">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-878">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-879">Original Bilder</span><span class="sxs-lookup"><span data-stu-id="f9a52-879">Original Images</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-880">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-880">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-881">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-881">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-882">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-882">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-883">%LocalAppData%\Microsoft\Windows Photo gallery\original Images</span><span class="sxs-lookup"><span data-stu-id="f9a52-883">%LOCALAPPDATA%\Microsoft\Windows Photo Gallery\Original Images</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-884">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-884">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-885">None, in Windows Vista eingeführte Wert</span><span class="sxs-lookup"><span data-stu-id="f9a52-885">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-886">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-886">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-887">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-887">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-888">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-888">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-889">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-889">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_PhotoAlbums"></span><span id="folderid_photoalbums"></span><span id="FOLDERID_PHOTOALBUMS"></span><dl> <span data-ttu-id="f9a52-890"><dt><strong>FOLDERID_PhotoAlbums</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-890"><dt><strong>FOLDERID_PhotoAlbums</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-891">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-891">GUID</span></span></td>
<td><span data-ttu-id="f9a52-892">{69d2cf90fc33-4fb7-9a0c-ebb0f0fcb43c}</span><span class="sxs-lookup"><span data-stu-id="f9a52-892">{69D2CF90-FC33-4FB7-9A0C-EBB0F0FCB43C}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-893">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-893">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-894">Folien anzeigen</span><span class="sxs-lookup"><span data-stu-id="f9a52-894">Slide Shows</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-895">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-895">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-896">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-896">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-897">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-897">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-898">%UserProfile%\pictures\folien anzeigen</span><span class="sxs-lookup"><span data-stu-id="f9a52-898">%USERPROFILE%\Pictures\Slide Shows</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-899">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-899">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-900">None, in Windows Vista eingeführte Wert</span><span class="sxs-lookup"><span data-stu-id="f9a52-900">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-901">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-901">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-902">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-902">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-903">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-903">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-904">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-904">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_PicturesLibrary"></span><span id="folderid_pictureslibrary"></span><span id="FOLDERID_PICTURESLIBRARY"></span><dl> <span data-ttu-id="f9a52-905"><dt><strong>FOLDERID_PicturesLibrary</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-905"><dt><strong>FOLDERID_PicturesLibrary</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-906">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-906">GUID</span></span></td>
<td><span data-ttu-id="f9a52-907">{A990AE9F-A03B-4E80-94BC-9912D7504104}</span><span class="sxs-lookup"><span data-stu-id="f9a52-907">{A990AE9F-A03B-4E80-94BC-9912D7504104}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-908">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-908">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-909">Bilder</span><span class="sxs-lookup"><span data-stu-id="f9a52-909">Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-910">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-910">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-911">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-911">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-912">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-912">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-913">%APPDATA%\microsoft\windows\libraries\pictures.Library-MS</span><span class="sxs-lookup"><span data-stu-id="f9a52-913">%APPDATA%\Microsoft\Windows\Libraries\Pictures.library-ms</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-914">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-914">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-915">None, in Windows 7 eingeführte Wert</span><span class="sxs-lookup"><span data-stu-id="f9a52-915">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-916">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-916">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-917">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-917">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-918">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-918">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-919">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-919">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Pictures"></span><span id="folderid_pictures"></span><span id="FOLDERID_PICTURES"></span><dl> <span data-ttu-id="f9a52-920"><dt><strong>FOLDERID_Pictures</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-920"><dt><strong>FOLDERID_Pictures</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-921">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-921">GUID</span></span></td>
<td><span data-ttu-id="f9a52-922">{33E28130-4E1E-4676-835A-98395C3BC3BB}</span><span class="sxs-lookup"><span data-stu-id="f9a52-922">{33E28130-4E1E-4676-835A-98395C3BC3BB}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-923">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-923">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-924">Bilder</span><span class="sxs-lookup"><span data-stu-id="f9a52-924">Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-925">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-925">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-926">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-926">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-927">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-927">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-928">%UserProfile%\Bilder</span><span class="sxs-lookup"><span data-stu-id="f9a52-928">%USERPROFILE%\Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-929">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-929">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-930">CSIDL_MYPICTURES</span><span class="sxs-lookup"><span data-stu-id="f9a52-930">CSIDL_MYPICTURES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-931">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-931">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-932">Meine Bilder</span><span class="sxs-lookup"><span data-stu-id="f9a52-932">My Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-933">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-933">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-934">%USERPROFILE%\Eigene Dateien\Eigene Bilder</span><span class="sxs-lookup"><span data-stu-id="f9a52-934">%USERPROFILE%\My Documents\My Pictures</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Playlists"></span><span id="folderid_playlists"></span><span id="FOLDERID_PLAYLISTS"></span><dl> <span data-ttu-id="f9a52-935"><dt><strong>FOLDERID_Playlists</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-935"><dt><strong>FOLDERID_Playlists</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-936">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-936">GUID</span></span></td>
<td><span data-ttu-id="f9a52-937">{DE92C1C7-837F-4F69-A3BB-86E631204A23}</span><span class="sxs-lookup"><span data-stu-id="f9a52-937">{DE92C1C7-837F-4F69-A3BB-86E631204A23}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-938">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-938">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-939">Wiedergabelisten</span><span class="sxs-lookup"><span data-stu-id="f9a52-939">Playlists</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-940">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-940">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-941">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-941">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-942">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-942">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-943">%UserProfile%\music\playlists</span><span class="sxs-lookup"><span data-stu-id="f9a52-943">%USERPROFILE%\Music\Playlists</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-944">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-944">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-945">Keine</span><span class="sxs-lookup"><span data-stu-id="f9a52-945">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-946">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-946">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-947">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-947">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-948">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-948">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-949">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-949">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_PrintersFolder"></span><span id="folderid_printersfolder"></span><span id="FOLDERID_PRINTERSFOLDER"></span><dl> <span data-ttu-id="f9a52-950"><dt><strong>FOLDERID_PrintersFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-950"><dt><strong>FOLDERID_PrintersFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-951">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-951">GUID</span></span></td>
<td><span data-ttu-id="f9a52-952">{76fc4e2d-D6AD-4519-A663-37bd56068185}</span><span class="sxs-lookup"><span data-stu-id="f9a52-952">{76FC4E2D-D6AD-4519-A663-37BD56068185}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-953">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-953">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-954">Drucker</span><span class="sxs-lookup"><span data-stu-id="f9a52-954">Printers</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-955">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-955">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-956">Virtu</span><span class="sxs-lookup"><span data-stu-id="f9a52-956">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-957">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-957">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-958">Nicht zutreffend – virtueller Ordner</span><span class="sxs-lookup"><span data-stu-id="f9a52-958">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-959">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-959">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-960">CSIDL_PRINTERS</span><span class="sxs-lookup"><span data-stu-id="f9a52-960">CSIDL_PRINTERS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-961">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-961">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-962">Drucker und Faxe</span><span class="sxs-lookup"><span data-stu-id="f9a52-962">Printers and Faxes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-963">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-963">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-964">Nicht zutreffend – virtueller Ordner</span><span class="sxs-lookup"><span data-stu-id="f9a52-964">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_PrintHood"></span><span id="folderid_printhood"></span><span id="FOLDERID_PRINTHOOD"></span><dl> <span data-ttu-id="f9a52-965"><dt><strong>FOLDERID_PrintHood</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-965"><dt><strong>FOLDERID_PrintHood</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-966">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-966">GUID</span></span></td>
<td><span data-ttu-id="f9a52-967">{9274bd8d-CFD1-41c3-b35e-b13f55a758f4}</span><span class="sxs-lookup"><span data-stu-id="f9a52-967">{9274BD8D-CFD1-41C3-B35E-B13F55A758F4}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-968">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-968">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-969">Drucker Verknüpfungen</span><span class="sxs-lookup"><span data-stu-id="f9a52-969">Printer Shortcuts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-970">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-970">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-971">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-971">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-972">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-972">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-973">%APPDATA%\microsoft\windows\druckerkombinationen</span><span class="sxs-lookup"><span data-stu-id="f9a52-973">%APPDATA%\Microsoft\Windows\Printer Shortcuts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-974">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-974">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-975">CSIDL_PRINTHOOD</span><span class="sxs-lookup"><span data-stu-id="f9a52-975">CSIDL_PRINTHOOD</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-976">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-976">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-977">Printhood</span><span class="sxs-lookup"><span data-stu-id="f9a52-977">PrintHood</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-978">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-978">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-979">%UserProfile%\printhood</span><span class="sxs-lookup"><span data-stu-id="f9a52-979">%USERPROFILE%\PrintHood</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Profile"></span><span id="folderid_profile"></span><span id="FOLDERID_PROFILE"></span><dl> <span data-ttu-id="f9a52-980"><dt><strong>FOLDERID_Profile</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-980"><dt><strong>FOLDERID_Profile</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-981">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-981">GUID</span></span></td>
<td><span data-ttu-id="f9a52-982">{5e6c858l-0E22-4760-9afe-ea3317b67173}</span><span class="sxs-lookup"><span data-stu-id="f9a52-982">{5E6C858F-0E22-4760-9AFE-EA3317B67173}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-983">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-983">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-984">Der Benutzername des Benutzers (% username%)</span><span class="sxs-lookup"><span data-stu-id="f9a52-984">The user's username (%USERNAME%)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-985">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-985">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-986">FIXED</span><span class="sxs-lookup"><span data-stu-id="f9a52-986">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-987">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-987">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-988">% User Profile% (%SystemDrive%\Users \% username%)</span><span class="sxs-lookup"><span data-stu-id="f9a52-988">%USERPROFILE% (%SystemDrive%\Users\%USERNAME%)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-989">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-989">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-990">CSIDL_PROFILE</span><span class="sxs-lookup"><span data-stu-id="f9a52-990">CSIDL_PROFILE</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-991">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-991">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-992">Der Benutzername des Benutzers (% username%)</span><span class="sxs-lookup"><span data-stu-id="f9a52-992">The user's username (%USERNAME%)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-993">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-993">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-994">% User Profile% (%systemdrive%\Documents and Settings \% username%)</span><span class="sxs-lookup"><span data-stu-id="f9a52-994">%USERPROFILE% (%SystemDrive%\Documents and Settings\%USERNAME%)</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_ProgramData"></span><span id="folderid_programdata"></span><span id="FOLDERID_PROGRAMDATA"></span><dl> <span data-ttu-id="f9a52-995"><dt><strong>FOLDERID_ProgramData</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-995"><dt><strong>FOLDERID_ProgramData</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-996">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-996">GUID</span></span></td>
<td><span data-ttu-id="f9a52-997">{62ab5d82-f 1-4dc3-a9dd-070d1d495d97}</span><span class="sxs-lookup"><span data-stu-id="f9a52-997">{62AB5D82-FDC1-4DC3-A9DD-070D1D495D97}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-998">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-998">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-999">ProgramData</span><span class="sxs-lookup"><span data-stu-id="f9a52-999">ProgramData</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1000">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1000">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1001">FIXED</span><span class="sxs-lookup"><span data-stu-id="f9a52-1001">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1002">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1002">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1003">% ALLUSERSPROFILE% (% Program Data%,%SystemDrive%\ProgramData)</span><span class="sxs-lookup"><span data-stu-id="f9a52-1003">%ALLUSERSPROFILE% (%ProgramData%, %SystemDrive%\ProgramData)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1004">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1004">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1005">CSIDL_COMMON_APPDATA</span><span class="sxs-lookup"><span data-stu-id="f9a52-1005">CSIDL_COMMON_APPDATA</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1006">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1006">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1007">Anwendungsdaten</span><span class="sxs-lookup"><span data-stu-id="f9a52-1007">Application Data</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1008">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1008">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1009">%ALLUSERSPROFILE%\Anwendungsdaten</span><span class="sxs-lookup"><span data-stu-id="f9a52-1009">%ALLUSERSPROFILE%\Application Data</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ProgramFiles"></span><span id="folderid_programfiles"></span><span id="FOLDERID_PROGRAMFILES"></span><dl> <span data-ttu-id="f9a52-1010"><dt><strong>FOLDERID_ProgramFiles</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1010"><dt><strong>FOLDERID_ProgramFiles</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="f9a52-1011">Weitere Informationen finden Sie unter Hinweise.</span><span class="sxs-lookup"><span data-stu-id="f9a52-1011">See Remarks for more information.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1012">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1012">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1013">{905E63B6-C1BF -494E-B29C-65B732D3D21A}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1013">{905e63b6-c1bf-494e-b29c-65b732d3d21a}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1014">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1014">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1015">Programme</span><span class="sxs-lookup"><span data-stu-id="f9a52-1015">Program Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1016">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1016">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1017">FIXED</span><span class="sxs-lookup"><span data-stu-id="f9a52-1017">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1018">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1018">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1019">% Program Files% (%SystemDrive%\Program Files)</span><span class="sxs-lookup"><span data-stu-id="f9a52-1019">%ProgramFiles% (%SystemDrive%\Program Files)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1020">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1020">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1021">CSIDL_PROGRAM_FILES</span><span class="sxs-lookup"><span data-stu-id="f9a52-1021">CSIDL_PROGRAM_FILES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1022">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1022">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1023">Programme</span><span class="sxs-lookup"><span data-stu-id="f9a52-1023">Program Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1024">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1024">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1025">% Program Files% (%SystemDrive%\Program Files)</span><span class="sxs-lookup"><span data-stu-id="f9a52-1025">%ProgramFiles% (%SystemDrive%\Program Files)</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_ProgramFilesX64"></span><span id="folderid_programfilesx64"></span><span id="FOLDERID_PROGRAMFILESX64"></span><dl> <span data-ttu-id="f9a52-1026"><dt><strong>FOLDERID_ProgramFilesX64</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1026"><dt><strong>FOLDERID_ProgramFilesX64</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="f9a52-1027">Dieser Wert wird auf 32-Bit-Betriebssystemen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f9a52-1027">This value is not supported on 32-bit operating systems.</span></span> <span data-ttu-id="f9a52-1028">Es wird auch nicht für 32-Bit-Anwendungen unterstützt, die auf 64-Bit-Betriebssystemen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f9a52-1028">It also is not supported for 32-bit applications running on 64-bit operating systems.</span></span> <span data-ttu-id="f9a52-1029">Der Versuch, FOLDERID_ProgramFilesX64 in beiden Situationen zu verwenden, führt zu einem Fehler.</span><span class="sxs-lookup"><span data-stu-id="f9a52-1029">Attempting to use FOLDERID_ProgramFilesX64 in either situation results in an error.</span></span> <span data-ttu-id="f9a52-1030">Weitere Informationen finden Sie unter Hinweise.</span><span class="sxs-lookup"><span data-stu-id="f9a52-1030">See Remarks for more information.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1031">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1031">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1032">{6d809377-6af0-444b-8957-A3773F02200E}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1032">{6D809377-6AF0-444b-8957-A3773F02200E}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1033">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1033">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1034">Programme</span><span class="sxs-lookup"><span data-stu-id="f9a52-1034">Program Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1035">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1035">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1036">FIXED</span><span class="sxs-lookup"><span data-stu-id="f9a52-1036">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1037">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1037">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1038">% Program Files% (%SystemDrive%\Program Files)</span><span class="sxs-lookup"><span data-stu-id="f9a52-1038">%ProgramFiles% (%SystemDrive%\Program Files)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1039">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1039">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1040">Keine</span><span class="sxs-lookup"><span data-stu-id="f9a52-1040">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1041">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1041">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1042">Programme</span><span class="sxs-lookup"><span data-stu-id="f9a52-1042">Program Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1043">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1043">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1044">% Program Files% (%SystemDrive%\Program Files)</span><span class="sxs-lookup"><span data-stu-id="f9a52-1044">%ProgramFiles% (%SystemDrive%\Program Files)</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ProgramFilesX86"></span><span id="folderid_programfilesx86"></span><span id="FOLDERID_PROGRAMFILESX86"></span><dl> <span data-ttu-id="f9a52-1045"><dt><strong>FOLDERID_ProgramFilesX86</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1045"><dt><strong>FOLDERID_ProgramFilesX86</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="f9a52-1046">Weitere Informationen finden Sie unter Hinweise.</span><span class="sxs-lookup"><span data-stu-id="f9a52-1046">See Remarks for more information.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1047">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1047">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1048">{7c5a40ef-a0f -4bfc-874a-c0b2e0b9fa8e}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1048">{7C5A40EF-A0FB-4BFC-874A-C0F2E0B9FA8E}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1049">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1049">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1050">Programme</span><span class="sxs-lookup"><span data-stu-id="f9a52-1050">Program Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1051">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1051">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1052">FIXED</span><span class="sxs-lookup"><span data-stu-id="f9a52-1052">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1053">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1053">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1054">% Program Files% (%SystemDrive%\Program Files)</span><span class="sxs-lookup"><span data-stu-id="f9a52-1054">%ProgramFiles% (%SystemDrive%\Program Files)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1055">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1055">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1056">CSIDL_PROGRAM_FILESX86</span><span class="sxs-lookup"><span data-stu-id="f9a52-1056">CSIDL_PROGRAM_FILESX86</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1057">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1057">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1058">Programme</span><span class="sxs-lookup"><span data-stu-id="f9a52-1058">Program Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1059">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1059">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1060">% Program Files% (%SystemDrive%\Program Files)</span><span class="sxs-lookup"><span data-stu-id="f9a52-1060">%ProgramFiles% (%SystemDrive%\Program Files)</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_ProgramFilesCommon"></span><span id="folderid_programfilescommon"></span><span id="FOLDERID_PROGRAMFILESCOMMON"></span><dl> <span data-ttu-id="f9a52-1061"><dt><strong>FOLDERID_ProgramFilesCommon</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1061"><dt><strong>FOLDERID_ProgramFilesCommon</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="f9a52-1062">Weitere Informationen finden Sie unter Hinweise.</span><span class="sxs-lookup"><span data-stu-id="f9a52-1062">See Remarks for more information.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1063">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1063">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1064">{F7F1ED05-9F6D-47A2-AAAE-29D317C6F066}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1064">{F7F1ED05-9F6D-47A2-AAAE-29D317C6F066}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1065">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1065">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1066">Allgemeine Dateien</span><span class="sxs-lookup"><span data-stu-id="f9a52-1066">Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1067">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1067">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1068">FIXED</span><span class="sxs-lookup"><span data-stu-id="f9a52-1068">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1069">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1069">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1070">%ProgramFiles%\Common files</span><span class="sxs-lookup"><span data-stu-id="f9a52-1070">%ProgramFiles%\Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1071">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1071">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1072">CSIDL_PROGRAM_FILES_COMMON</span><span class="sxs-lookup"><span data-stu-id="f9a52-1072">CSIDL_PROGRAM_FILES_COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1073">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1073">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1074">Allgemeine Dateien</span><span class="sxs-lookup"><span data-stu-id="f9a52-1074">Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1075">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1075">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1076">%ProgramFiles%\Common files</span><span class="sxs-lookup"><span data-stu-id="f9a52-1076">%ProgramFiles%\Common Files</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ProgramFilesCommonX64"></span><span id="folderid_programfilescommonx64"></span><span id="FOLDERID_PROGRAMFILESCOMMONX64"></span><dl> <span data-ttu-id="f9a52-1077"><dt><strong>FOLDERID_ProgramFilesCommonX64</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1077"><dt><strong>FOLDERID_ProgramFilesCommonX64</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="f9a52-1078">Weitere Informationen finden Sie unter Hinweise.</span><span class="sxs-lookup"><span data-stu-id="f9a52-1078">See Remarks for more information.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1079">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1079">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1080">{6365d5a7-0F-ID < </UI)</span><span class="sxs-lookup"><span data-stu-id="f9a52-1080">{6365D5A7-0F0D-45E5-87F6-0DA56B6A4F7D}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1081">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1081">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1082">Allgemeine Dateien</span><span class="sxs-lookup"><span data-stu-id="f9a52-1082">Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1083">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1083">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1084">FIXED</span><span class="sxs-lookup"><span data-stu-id="f9a52-1084">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1085">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1085">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1086">%ProgramFiles%\Common files</span><span class="sxs-lookup"><span data-stu-id="f9a52-1086">%ProgramFiles%\Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1087">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1087">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1088">Keine</span><span class="sxs-lookup"><span data-stu-id="f9a52-1088">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1089">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1089">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1090">Allgemeine Dateien</span><span class="sxs-lookup"><span data-stu-id="f9a52-1090">Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1091">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1091">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1092">%ProgramFiles%\Common files</span><span class="sxs-lookup"><span data-stu-id="f9a52-1092">%ProgramFiles%\Common Files</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_ProgramFilesCommonX86"></span><span id="folderid_programfilescommonx86"></span><span id="FOLDERID_PROGRAMFILESCOMMONX86"></span><dl> <span data-ttu-id="f9a52-1093"><dt><strong>FOLDERID_ProgramFilesCommonX86</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1093"><dt><strong>FOLDERID_ProgramFilesCommonX86</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="f9a52-1094">Weitere Informationen finden Sie unter Hinweise.</span><span class="sxs-lookup"><span data-stu-id="f9a52-1094">See Remarks for more information.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1095">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1095">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1096">{DE974D24-D9C6-4D3E-BF91-F4455120B917}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1096">{DE974D24-D9C6-4D3E-BF91-F4455120B917}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1097">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1097">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1098">Allgemeine Dateien</span><span class="sxs-lookup"><span data-stu-id="f9a52-1098">Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1099">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1099">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1100">FIXED</span><span class="sxs-lookup"><span data-stu-id="f9a52-1100">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1101">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1101">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1102">%ProgramFiles%\Common files</span><span class="sxs-lookup"><span data-stu-id="f9a52-1102">%ProgramFiles%\Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1103">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1103">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1104">CSIDL_PROGRAM_FILES_COMMONX86</span><span class="sxs-lookup"><span data-stu-id="f9a52-1104">CSIDL_PROGRAM_FILES_COMMONX86</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1105">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1105">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1106">Allgemeine Dateien</span><span class="sxs-lookup"><span data-stu-id="f9a52-1106">Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1107">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1107">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1108">%ProgramFiles%\Common files</span><span class="sxs-lookup"><span data-stu-id="f9a52-1108">%ProgramFiles%\Common Files</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Programs"></span><span id="folderid_programs"></span><span id="FOLDERID_PROGRAMS"></span><dl> <span data-ttu-id="f9a52-1109"><dt><strong>FOLDERID_Programs</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1109"><dt><strong>FOLDERID_Programs</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1110">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1110">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1111">{A77F5D77-2E2B-44C3-A6A2-ABA601054A51}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1111">{A77F5D77-2E2B-44C3-A6A2-ABA601054A51}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1112">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1112">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1113">Programs</span><span class="sxs-lookup"><span data-stu-id="f9a52-1113">Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1114">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1114">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1115">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-1115">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1116">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1116">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1117">%APPDATA%\Microsoft\Windows\Start menu\programme</span><span class="sxs-lookup"><span data-stu-id="f9a52-1117">%APPDATA%\Microsoft\Windows\Start Menu\Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1118">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1118">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1119">CSIDL_PROGRAMS</span><span class="sxs-lookup"><span data-stu-id="f9a52-1119">CSIDL_PROGRAMS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1120">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1120">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1121">Programs</span><span class="sxs-lookup"><span data-stu-id="f9a52-1121">Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1122">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1122">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1123">%UserProfile%\startmenu\programme</span><span class="sxs-lookup"><span data-stu-id="f9a52-1123">%USERPROFILE%\Start Menu\Programs</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Public"></span><span id="folderid_public"></span><span id="FOLDERID_PUBLIC"></span><dl> <span data-ttu-id="f9a52-1124"><dt><strong>FOLDERID_Public</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1124"><dt><strong>FOLDERID_Public</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1125">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1125">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1126">{DFDF76A2-C82A-4D63-906A-5644AC457385}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1126">{DFDF76A2-C82A-4D63-906A-5644AC457385}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1127">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1127">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1128">Öffentlich</span><span class="sxs-lookup"><span data-stu-id="f9a52-1128">Public</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1129">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1129">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1130">FIXED</span><span class="sxs-lookup"><span data-stu-id="f9a52-1130">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1131">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1131">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1132">% Public% (%SystemDrive%\Users\Public)</span><span class="sxs-lookup"><span data-stu-id="f9a52-1132">%PUBLIC% (%SystemDrive%\Users\Public)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1133">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1133">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1134">Keine, neu für Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f9a52-1134">None, new for Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1135">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1135">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1136">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1136">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1137">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1137">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1138">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1138">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_PublicDesktop"></span><span id="folderid_publicdesktop"></span><span id="FOLDERID_PUBLICDESKTOP"></span><dl> <span data-ttu-id="f9a52-1139"><dt><strong>FOLDERID_PublicDesktop</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1139"><dt><strong>FOLDERID_PublicDesktop</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1140">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1140">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1141">{C4AA340D-F20F-4863-Afef-F87EF2E6BA25}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1141">{C4AA340D-F20F-4863-AFEF-F87EF2E6BA25}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1142">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1142">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1143">Öffentlicher Desktop</span><span class="sxs-lookup"><span data-stu-id="f9a52-1143">Public Desktop</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1144">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1144">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1145">Gewöhnliche</span><span class="sxs-lookup"><span data-stu-id="f9a52-1145">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1146">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1146">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1147">%Public%\Desktop</span><span class="sxs-lookup"><span data-stu-id="f9a52-1147">%PUBLIC%\Desktop</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1148">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1148">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1149">CSIDL_COMMON_DESKTOPDIRECTORY</span><span class="sxs-lookup"><span data-stu-id="f9a52-1149">CSIDL_COMMON_DESKTOPDIRECTORY</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1150">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1150">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1151">Desktop</span><span class="sxs-lookup"><span data-stu-id="f9a52-1151">Desktop</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1152">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1152">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1153">%ALLUSERSPROFILE%\Desktop</span><span class="sxs-lookup"><span data-stu-id="f9a52-1153">%ALLUSERSPROFILE%\Desktop</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_PublicDocuments"></span><span id="folderid_publicdocuments"></span><span id="FOLDERID_PUBLICDOCUMENTS"></span><dl> <span data-ttu-id="f9a52-1154"><dt><strong>FOLDERID_PublicDocuments</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1154"><dt><strong>FOLDERID_PublicDocuments</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1155">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1155">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1156">{ED4824AF-DCE4-45A8-81E2-FC7965083634}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1156">{ED4824AF-DCE4-45A8-81E2-FC7965083634}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1157">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1157">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1158">Öffentliche Dokumente</span><span class="sxs-lookup"><span data-stu-id="f9a52-1158">Public Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1159">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1159">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1160">Gewöhnliche</span><span class="sxs-lookup"><span data-stu-id="f9a52-1160">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1161">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1161">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1162">%PUBLIC%\Documents</span><span class="sxs-lookup"><span data-stu-id="f9a52-1162">%PUBLIC%\Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1163">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1163">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1164">CSIDL_COMMON_DOCUMENTS</span><span class="sxs-lookup"><span data-stu-id="f9a52-1164">CSIDL_COMMON_DOCUMENTS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1165">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1165">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1166">Freigegebene Dokumente</span><span class="sxs-lookup"><span data-stu-id="f9a52-1166">Shared Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1167">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1167">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1168">%ALLUSERSPROFILE%\Documents</span><span class="sxs-lookup"><span data-stu-id="f9a52-1168">%ALLUSERSPROFILE%\Documents</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_PublicDownloads"></span><span id="folderid_publicdownloads"></span><span id="FOLDERID_PUBLICDOWNLOADS"></span><dl> <span data-ttu-id="f9a52-1169"><dt><strong>FOLDERID_PublicDownloads</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1169"><dt><strong>FOLDERID_PublicDownloads</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1170">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1170">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1171">{3d644c9b-1B8-4f 30-9b45-b670235</span><span class="sxs-lookup"><span data-stu-id="f9a52-1171">{3D644C9B-1FB8-4f30-9B45-F670235F79C0}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1172">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1172">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1173">Öffentliche Downloads</span><span class="sxs-lookup"><span data-stu-id="f9a52-1173">Public Downloads</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1174">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1174">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1175">Gewöhnliche</span><span class="sxs-lookup"><span data-stu-id="f9a52-1175">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1176">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1176">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1177">%Public%\downloads</span><span class="sxs-lookup"><span data-stu-id="f9a52-1177">%PUBLIC%\Downloads</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1178">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1178">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1179">None, in Windows Vista eingeführte Wert</span><span class="sxs-lookup"><span data-stu-id="f9a52-1179">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1180">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1180">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1181">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1181">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1182">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1182">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1183">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1183">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_PublicGameTasks"></span><span id="folderid_publicgametasks"></span><span id="FOLDERID_PUBLICGAMETASKS"></span><dl> <span data-ttu-id="f9a52-1184"><dt><strong>FOLDERID_PublicGameTasks</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1184"><dt><strong>FOLDERID_PublicGameTasks</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1185">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1185">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1186">{DEBF2536-E1A8-4c59-B6A2-414586476AEA}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1186">{DEBF2536-E1A8-4c59-B6A2-414586476AEA}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1187">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1187">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1188">GameExplorer</span><span class="sxs-lookup"><span data-stu-id="f9a52-1188">GameExplorer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1189">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1189">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1190">Gewöhnliche</span><span class="sxs-lookup"><span data-stu-id="f9a52-1190">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1191">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1191">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1192">%ALLUSERSPROFILE%\microsoft\windows\gameexplorer</span><span class="sxs-lookup"><span data-stu-id="f9a52-1192">%ALLUSERSPROFILE%\Microsoft\Windows\GameExplorer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1193">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1193">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1194">None, in Windows Vista eingeführte Wert</span><span class="sxs-lookup"><span data-stu-id="f9a52-1194">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1195">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1195">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1196">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1196">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1197">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1197">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1198">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1198">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_PublicLibraries"></span><span id="folderid_publiclibraries"></span><span id="FOLDERID_PUBLICLIBRARIES"></span><dl> <span data-ttu-id="f9a52-1199"><dt><strong>FOLDERID_PublicLibraries</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1199"><dt><strong>FOLDERID_PublicLibraries</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1200">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1200">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1201">{48daf80b-e6cf-4f4e-B800-0e69d84ee384}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1201">{48DAF80B-E6CF-4F4E-B800-0E69D84EE384}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1202">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1202">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1203">Bibliotheken</span><span class="sxs-lookup"><span data-stu-id="f9a52-1203">Libraries</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1204">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1204">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1205">Gewöhnliche</span><span class="sxs-lookup"><span data-stu-id="f9a52-1205">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1206">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1206">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1207">%ALLUSERSPROFILE%\microsoft\windows\libraries</span><span class="sxs-lookup"><span data-stu-id="f9a52-1207">%ALLUSERSPROFILE%\Microsoft\Windows\Libraries</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1208">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1208">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1209">None, in Windows 7 eingeführte Wert</span><span class="sxs-lookup"><span data-stu-id="f9a52-1209">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1210">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1210">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1211">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1211">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1212">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1212">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1213">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1213">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_PublicMusic"></span><span id="folderid_publicmusic"></span><span id="FOLDERID_PUBLICMUSIC"></span><dl> <span data-ttu-id="f9a52-1214"><dt><strong>FOLDERID_PublicMusic</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1214"><dt><strong>FOLDERID_PublicMusic</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1215">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1215">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1216">{3214fab5-9757-4298-bb61-92a9de aa44ff}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1216">{3214FAB5-9757-4298-BB61-92A9DEAA44FF}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1217">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1217">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1218">Öffentliche Musik</span><span class="sxs-lookup"><span data-stu-id="f9a52-1218">Public Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1219">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1219">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1220">Gewöhnliche</span><span class="sxs-lookup"><span data-stu-id="f9a52-1220">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1221">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1221">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1222">%Public%\Music</span><span class="sxs-lookup"><span data-stu-id="f9a52-1222">%PUBLIC%\Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1223">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1223">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1224">CSIDL_COMMON_MUSIC</span><span class="sxs-lookup"><span data-stu-id="f9a52-1224">CSIDL_COMMON_MUSIC</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1225">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1225">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1226">Freigegebene Musik</span><span class="sxs-lookup"><span data-stu-id="f9a52-1226">Shared Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1227">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1227">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1228">%ALLUSERSPROFILE%\documents\meine Musik</span><span class="sxs-lookup"><span data-stu-id="f9a52-1228">%ALLUSERSPROFILE%\Documents\My Music</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_PublicPictures"></span><span id="folderid_publicpictures"></span><span id="FOLDERID_PUBLICPICTURES"></span><dl> <span data-ttu-id="f9a52-1229"><dt><strong>FOLDERID_PublicPictures</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1229"><dt><strong>FOLDERID_PublicPictures</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1230">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1230">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1231">{B6EBFB86-6907-413C-9AF7-4FC2ABF07CC5}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1231">{B6EBFB86-6907-413C-9AF7-4FC2ABF07CC5}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1232">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1232">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1233">Öffentliche Bilder</span><span class="sxs-lookup"><span data-stu-id="f9a52-1233">Public Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1234">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1234">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1235">Gewöhnliche</span><span class="sxs-lookup"><span data-stu-id="f9a52-1235">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1236">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1236">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1237">%Public%\Bilder</span><span class="sxs-lookup"><span data-stu-id="f9a52-1237">%PUBLIC%\Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1238">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1238">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1239">CSIDL_COMMON_PICTURES</span><span class="sxs-lookup"><span data-stu-id="f9a52-1239">CSIDL_COMMON_PICTURES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1240">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1240">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1241">Freigegebene Bilder</span><span class="sxs-lookup"><span data-stu-id="f9a52-1241">Shared Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1242">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1242">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1243">%ALLUSERSPROFILE%\documents\eigene Bilder</span><span class="sxs-lookup"><span data-stu-id="f9a52-1243">%ALLUSERSPROFILE%\Documents\My Pictures</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_PublicRingtones"></span><span id="folderid_publicringtones"></span><span id="FOLDERID_PUBLICRINGTONES"></span><dl> <span data-ttu-id="f9a52-1244"><dt><strong>FOLDERID_PublicRingtones</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1244"><dt><strong>FOLDERID_PublicRingtones</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1245">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1245">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1246">{E555AB60-153B-4D17-9F04-A5FE99FC15EC}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1246">{E555AB60-153B-4D17-9F04-A5FE99FC15EC}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1247">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1247">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1248">Klingeltöne</span><span class="sxs-lookup"><span data-stu-id="f9a52-1248">Ringtones</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1249">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1249">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1250">Gewöhnliche</span><span class="sxs-lookup"><span data-stu-id="f9a52-1250">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1251">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1251">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1252">%ALLUSERSPROFILE%\microsoft\windows\ringtones</span><span class="sxs-lookup"><span data-stu-id="f9a52-1252">%ALLUSERSPROFILE%\Microsoft\Windows\Ringtones</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1253">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1253">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1254">None, in Windows 7 eingeführte Wert</span><span class="sxs-lookup"><span data-stu-id="f9a52-1254">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1255">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1255">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1256">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1256">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1257">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1257">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1258">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1258">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_PublicUserTiles"></span><span id="folderid_publicusertiles"></span><span id="FOLDERID_PUBLICUSERTILES"></span><dl> <span data-ttu-id="f9a52-1259"><dt><strong>FOLDERID_PublicUserTiles</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1259"><dt><strong>FOLDERID_PublicUserTiles</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1260">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1260">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1261">{0482af6c-08b1-4c34-8c90e17ec98b1e17}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1261">{0482af6c-08f1-4c34-8c90-e17ec98b1e17}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1262">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1262">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1263">Öffentliche Konto Bilder</span><span class="sxs-lookup"><span data-stu-id="f9a52-1263">Public Account Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1264">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1264">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1265">Gewöhnliche</span><span class="sxs-lookup"><span data-stu-id="f9a52-1265">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1266">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1266">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1267">%Public%\accountpictures</span><span class="sxs-lookup"><span data-stu-id="f9a52-1267">%PUBLIC%\AccountPictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1268">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1268">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1269">None, in Windows 8 eingeführte Wert</span><span class="sxs-lookup"><span data-stu-id="f9a52-1269">None, value introduced in Windows 8</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1270">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1270">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1271">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1271">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1272">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1272">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1273">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1273">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_PublicVideos"></span><span id="folderid_publicvideos"></span><span id="FOLDERID_PUBLICVIDEOS"></span><dl> <span data-ttu-id="f9a52-1274"><dt><strong>FOLDERID_PublicVideos</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1274"><dt><strong>FOLDERID_PublicVideos</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1275">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1275">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1276">{2400183a-6185-49tb-a2d8-4a392a602ba3}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1276">{2400183A-6185-49FB-A2D8-4A392A602BA3}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1277">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1277">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1278">Öffentliche Videos</span><span class="sxs-lookup"><span data-stu-id="f9a52-1278">Public Videos</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1279">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1279">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1280">Gewöhnliche</span><span class="sxs-lookup"><span data-stu-id="f9a52-1280">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1281">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1281">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1282">%Public%\videos</span><span class="sxs-lookup"><span data-stu-id="f9a52-1282">%PUBLIC%\Videos</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1283">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1283">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1284">CSIDL_COMMON_VIDEO</span><span class="sxs-lookup"><span data-stu-id="f9a52-1284">CSIDL_COMMON_VIDEO</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1285">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1285">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1286">Gemeinsam genutztes Video</span><span class="sxs-lookup"><span data-stu-id="f9a52-1286">Shared Video</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1287">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1287">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1288">%ALLUSERSPROFILE%\Documents\My Videos</span><span class="sxs-lookup"><span data-stu-id="f9a52-1288">%ALLUSERSPROFILE%\Documents\My Videos</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_QuickLaunch"></span><span id="folderid_quicklaunch"></span><span id="FOLDERID_QUICKLAUNCH"></span><dl> <span data-ttu-id="f9a52-1289"><dt><strong>FOLDERID_QuickLaunch</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1289"><dt><strong>FOLDERID_QuickLaunch</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1290">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1290">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1291">{52a4f 021-7b75-48a9-9B a b87b-4b87a210bc8f}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1291">{52a4f021-7b75-48a9-9f6b-4b87a210bc8f}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1292">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1292">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1293">Schnellstart</span><span class="sxs-lookup"><span data-stu-id="f9a52-1293">Quick Launch</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1294">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1294">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1295">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-1295">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1296">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1296">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1297">%APPDATA%\microsoft\internet explorer\schnelllaunch</span><span class="sxs-lookup"><span data-stu-id="f9a52-1297">%APPDATA%\Microsoft\Internet Explorer\Quick Launch</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1298">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1298">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1299">Keine</span><span class="sxs-lookup"><span data-stu-id="f9a52-1299">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1300">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1300">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1301">Schnellstart</span><span class="sxs-lookup"><span data-stu-id="f9a52-1301">Quick Launch</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1302">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1302">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1303">%APPDATA%\microsoft\internet explorer\schnelllaunch</span><span class="sxs-lookup"><span data-stu-id="f9a52-1303">%APPDATA%\Microsoft\Internet Explorer\Quick Launch</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Recent"></span><span id="folderid_recent"></span><span id="FOLDERID_RECENT"></span><dl> <span data-ttu-id="f9a52-1304"><dt><strong>FOLDERID_Recent</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1304"><dt><strong>FOLDERID_Recent</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1305">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1305">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1306">{AE50C081-EBD2-438A-8655-8A092E34987A}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1306">{AE50C081-EBD2-438A-8655-8A092E34987A}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1307">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1307">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1308">Zuletzt verwendete Elemente</span><span class="sxs-lookup"><span data-stu-id="f9a52-1308">Recent Items</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1309">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1309">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1310">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-1310">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1311">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1311">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1312">%APPDATA%\microsoft\windows\recent</span><span class="sxs-lookup"><span data-stu-id="f9a52-1312">%APPDATA%\Microsoft\Windows\Recent</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1313">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1313">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1314">CSIDL_RECENT</span><span class="sxs-lookup"><span data-stu-id="f9a52-1314">CSIDL_RECENT</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1315">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1315">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1316">Meine letzten Dokumente</span><span class="sxs-lookup"><span data-stu-id="f9a52-1316">My Recent Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1317">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1317">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1318">%UserProfile%\recent</span><span class="sxs-lookup"><span data-stu-id="f9a52-1318">%USERPROFILE%\Recent</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_RecordedTV"></span><span id="folderid_recordedtv"></span><span id="FOLDERID_RECORDEDTV"></span><dl> <span data-ttu-id="f9a52-1319"><dt><strong>FOLDERID_RecordedTV</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1319"><dt><strong>FOLDERID_RecordedTV</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="f9a52-1320">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f9a52-1320">Not used.</span></span> <span data-ttu-id="f9a52-1321">Dieser Wert ist ab Windows 7 nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="f9a52-1321">This value is undefined as of Windows 7.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_RecordedTVLibrary"></span><span id="folderid_recordedtvlibrary"></span><span id="FOLDERID_RECORDEDTVLIBRARY"></span><dl> <span data-ttu-id="f9a52-1322"><dt><strong>FOLDERID_RecordedTVLibrary</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1322"><dt><strong>FOLDERID_RecordedTVLibrary</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1323">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1323">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1324">{1a6f dba2-F42D-4358-A798-B74D745926C5}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1324">{1A6FDBA2-F42D-4358-A798-B74D745926C5}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1325">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1325">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1326">TV-Aufzeichnungen</span><span class="sxs-lookup"><span data-stu-id="f9a52-1326">Recorded TV</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1327">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1327">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1328">Gewöhnliche</span><span class="sxs-lookup"><span data-stu-id="f9a52-1328">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1329">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1329">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1330">%Public%\recorddtv.Library-MS</span><span class="sxs-lookup"><span data-stu-id="f9a52-1330">%PUBLIC%\RecordedTV.library-ms</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1331">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1331">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1332">None, in Windows 7 eingeführte Wert</span><span class="sxs-lookup"><span data-stu-id="f9a52-1332">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1333">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1333">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1334">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1334">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1335">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1335">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1336">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1336">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_RecycleBinFolder"></span><span id="folderid_recyclebinfolder"></span><span id="FOLDERID_RECYCLEBINFOLDER"></span><dl> <span data-ttu-id="f9a52-1337"><dt><strong>FOLDERID_RecycleBinFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1337"><dt><strong>FOLDERID_RecycleBinFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1338">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1338">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1339">{B7534046-3ECB-4C18-BE4E-64CD4CB7D6AC}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1339">{B7534046-3ECB-4C18-BE4E-64CD4CB7D6AC}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1340">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1340">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1341">Papierkorb</span><span class="sxs-lookup"><span data-stu-id="f9a52-1341">Recycle Bin</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1342">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1342">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1343">Virtu</span><span class="sxs-lookup"><span data-stu-id="f9a52-1343">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1344">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1344">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1345">Nicht zutreffend – virtueller Ordner</span><span class="sxs-lookup"><span data-stu-id="f9a52-1345">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1346">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1346">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1347">CSIDL_BITBUCKET</span><span class="sxs-lookup"><span data-stu-id="f9a52-1347">CSIDL_BITBUCKET</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1348">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1348">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1349">Papierkorb</span><span class="sxs-lookup"><span data-stu-id="f9a52-1349">Recycle Bin</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1350">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1350">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1351">Nicht zutreffend – virtueller Ordner</span><span class="sxs-lookup"><span data-stu-id="f9a52-1351">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_ResourceDir"></span><span id="folderid_resourcedir"></span><span id="FOLDERID_RESOURCEDIR"></span><dl> <span data-ttu-id="f9a52-1352"><dt><strong>FOLDERID_ResourceDir</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1352"><dt><strong>FOLDERID_ResourceDir</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1353">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1353">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1354">{8ad10c31-2adb-4296-A8F7-E4701232C972}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1354">{8AD10C31-2ADB-4296-A8F7-E4701232C972}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1355">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1355">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1356">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f9a52-1356">Resources</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1357">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1357">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1358">FIXED</span><span class="sxs-lookup"><span data-stu-id="f9a52-1358">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1359">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1359">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1360">%windir%\Resources</span><span class="sxs-lookup"><span data-stu-id="f9a52-1360">%windir%\Resources</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1361">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1361">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1362">CSIDL_RESOURCES</span><span class="sxs-lookup"><span data-stu-id="f9a52-1362">CSIDL_RESOURCES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1363">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1363">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1364">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f9a52-1364">Resources</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1365">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1365">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1366">%windir%\Resources</span><span class="sxs-lookup"><span data-stu-id="f9a52-1366">%windir%\Resources</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Ringtones"></span><span id="folderid_ringtones"></span><span id="FOLDERID_RINGTONES"></span><dl> <span data-ttu-id="f9a52-1367"><dt><strong>FOLDERID_Ringtones</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1367"><dt><strong>FOLDERID_Ringtones</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1368">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1368">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1369">{C870044B-F49E-4126-A9C3-B52A1FF411E8}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1369">{C870044B-F49E-4126-A9C3-B52A1FF411E8}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1370">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1370">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1371">Klingeltöne</span><span class="sxs-lookup"><span data-stu-id="f9a52-1371">Ringtones</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1372">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1372">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1373">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-1373">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1374">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1374">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1375">%LocalAppData%\microsoft\windows\ringtones</span><span class="sxs-lookup"><span data-stu-id="f9a52-1375">%LOCALAPPDATA%\Microsoft\Windows\Ringtones</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1376">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1376">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1377">None, in Windows 7 eingeführte Wert</span><span class="sxs-lookup"><span data-stu-id="f9a52-1377">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1378">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1378">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1379">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1379">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1380">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1380">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1381">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1381">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_RoamingAppData"></span><span id="folderid_roamingappdata"></span><span id="FOLDERID_ROAMINGAPPDATA"></span><dl> <span data-ttu-id="f9a52-1382"><dt><strong>FOLDERID_RoamingAppData</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1382"><dt><strong>FOLDERID_RoamingAppData</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1383">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1383">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1384">{3EB685DB-65F9-4CF6-A03A-E3EF65729F3D}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1384">{3EB685DB-65F9-4CF6-A03A-E3EF65729F3D}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1385">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1385">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1386">Roaming</span><span class="sxs-lookup"><span data-stu-id="f9a52-1386">Roaming</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1387">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1387">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1388">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-1388">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1389">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1389">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1390">% APPDATA% (%USERPROFILE%\appdata\roaming)</span><span class="sxs-lookup"><span data-stu-id="f9a52-1390">%APPDATA% (%USERPROFILE%\AppData\Roaming)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1391">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1391">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1392">CSIDL_APPDATA</span><span class="sxs-lookup"><span data-stu-id="f9a52-1392">CSIDL_APPDATA</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1393">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1393">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1394">Anwendungsdaten</span><span class="sxs-lookup"><span data-stu-id="f9a52-1394">Application Data</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1395">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1395">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1396">% APPDATA% (%USERPROFILE%\Anwendungsdaten)</span><span class="sxs-lookup"><span data-stu-id="f9a52-1396">%APPDATA% (%USERPROFILE%\Application Data)</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_RoamedTileImages"></span><span id="folderid_roamedtileimages"></span><span id="FOLDERID_ROAMEDTILEIMAGES"></span><dl> <span data-ttu-id="f9a52-1397"><dt><strong>FOLDERID_RoamedTileImages</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1397"><dt><strong>FOLDERID_RoamedTileImages</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1398">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1398">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1399">{AAA8D5A5-F1D6-4259-BAA8-78E7EF60835E}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1399">{AAA8D5A5-F1D6-4259-BAA8-78E7EF60835E}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1400">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1400">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1401">Roamedtileimages</span><span class="sxs-lookup"><span data-stu-id="f9a52-1401">RoamedTileImages</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1402">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1402">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1403">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-1403">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1404">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1404">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1405">%LocalAppData%\microsoft\windows\roamedtileimages</span><span class="sxs-lookup"><span data-stu-id="f9a52-1405">%LOCALAPPDATA%\Microsoft\Windows\RoamedTileImages</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1406">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1406">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1407">None, in Windows 8 eingeführte Wert</span><span class="sxs-lookup"><span data-stu-id="f9a52-1407">None, value introduced in Windows 8</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1408">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1408">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1409">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1409">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1410">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1410">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1411">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1411">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_RoamingTiles"></span><span id="folderid_roamingtiles"></span><span id="FOLDERID_ROAMINGTILES"></span><dl> <span data-ttu-id="f9a52-1412"><dt><strong>FOLDERID_RoamingTiles</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1412"><dt><strong>FOLDERID_RoamingTiles</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1413">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1413">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1414">{00bcfc5a-ed94-4e48-96aq1-3 f6217f21990}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1414">{00BCFC5A-ED94-4e48-96A1-3F6217F21990}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1415">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1415">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1416">Roamingtiles</span><span class="sxs-lookup"><span data-stu-id="f9a52-1416">RoamingTiles</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1417">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1417">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1418">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-1418">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1419">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1419">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1420">%LocalAppData%\microsoft\windows\roamingtiles</span><span class="sxs-lookup"><span data-stu-id="f9a52-1420">%LOCALAPPDATA%\Microsoft\Windows\RoamingTiles</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1421">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1421">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1422">None, in Windows 8 eingeführte Wert</span><span class="sxs-lookup"><span data-stu-id="f9a52-1422">None, value introduced in Windows 8</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1423">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1423">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1424">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1424">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1425">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1425">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1426">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1426">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SampleMusic"></span><span id="folderid_samplemusic"></span><span id="FOLDERID_SAMPLEMUSIC"></span><dl> <span data-ttu-id="f9a52-1427"><dt><strong>FOLDERID_SampleMusic</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1427"><dt><strong>FOLDERID_SampleMusic</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1428">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1428">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1429">{B250C668-F57D-4EE1-A63C-290EE7D1AA1F}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1429">{B250C668-F57D-4EE1-A63C-290EE7D1AA1F}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1430">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1430">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1431">Beispiel Musik</span><span class="sxs-lookup"><span data-stu-id="f9a52-1431">Sample Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1432">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1432">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1433">Gewöhnliche</span><span class="sxs-lookup"><span data-stu-id="f9a52-1433">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1434">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1434">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1435">%Public%\music\sample Music</span><span class="sxs-lookup"><span data-stu-id="f9a52-1435">%PUBLIC%\Music\Sample Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1436">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1436">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1437">Keine</span><span class="sxs-lookup"><span data-stu-id="f9a52-1437">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1438">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1438">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1439">Beispiel Musik</span><span class="sxs-lookup"><span data-stu-id="f9a52-1439">Sample Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1440">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1440">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1441">%ALLUSERSPROFILE%\Documents\My music\sample Music</span><span class="sxs-lookup"><span data-stu-id="f9a52-1441">%ALLUSERSPROFILE%\Documents\My Music\Sample Music</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SamplePictures"></span><span id="folderid_samplepictures"></span><span id="FOLDERID_SAMPLEPICTURES"></span><dl> <span data-ttu-id="f9a52-1442"><dt><strong>FOLDERID_SamplePictures</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1442"><dt><strong>FOLDERID_SamplePictures</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1443">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1443">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1444">{C4900540-2379-4C75-844B-64E6FAF8716B}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1444">{C4900540-2379-4C75-844B-64E6FAF8716B}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1445">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1445">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1446">Beispiel Bilder</span><span class="sxs-lookup"><span data-stu-id="f9a52-1446">Sample Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1447">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1447">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1448">Gewöhnliche</span><span class="sxs-lookup"><span data-stu-id="f9a52-1448">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1449">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1449">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1450">%Public%\pictures\beispielbilder</span><span class="sxs-lookup"><span data-stu-id="f9a52-1450">%PUBLIC%\Pictures\Sample Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1451">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1451">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1452">Keine</span><span class="sxs-lookup"><span data-stu-id="f9a52-1452">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1453">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1453">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1454">Beispiel Bilder</span><span class="sxs-lookup"><span data-stu-id="f9a52-1454">Sample Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1455">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1455">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1456">%ALLUSERSPROFILE%\Documents\My Pictures\Sample Pictures</span><span class="sxs-lookup"><span data-stu-id="f9a52-1456">%ALLUSERSPROFILE%\Documents\My Pictures\Sample Pictures</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SamplePlaylists"></span><span id="folderid_sampleplaylists"></span><span id="FOLDERID_SAMPLEPLAYLISTS"></span><dl> <span data-ttu-id="f9a52-1457"><dt><strong>FOLDERID_SamplePlaylists</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1457"><dt><strong>FOLDERID_SamplePlaylists</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1458">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1458">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1459">{15ca69b3-30ee-49c1-ace1-6b5ec372afb5}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1459">{15CA69B3-30EE-49C1-ACE1-6B5EC372AFB5}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1460">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1460">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1461">Beispiel Wiedergabelisten</span><span class="sxs-lookup"><span data-stu-id="f9a52-1461">Sample Playlists</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1462">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1462">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1463">Gewöhnliche</span><span class="sxs-lookup"><span data-stu-id="f9a52-1463">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1464">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1464">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1465">%Public%\music\beispielwiedergabe Listen</span><span class="sxs-lookup"><span data-stu-id="f9a52-1465">%PUBLIC%\Music\Sample Playlists</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1466">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1466">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1467">None, in Windows Vista eingeführte Wert</span><span class="sxs-lookup"><span data-stu-id="f9a52-1467">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1468">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1468">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1469">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1469">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1470">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1470">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1471">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1471">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SampleVideos"></span><span id="folderid_samplevideos"></span><span id="FOLDERID_SAMPLEVIDEOS"></span><dl> <span data-ttu-id="f9a52-1472"><dt><strong>FOLDERID_SampleVideos</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1472"><dt><strong>FOLDERID_SampleVideos</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1473">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1473">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1474">{859ead94-2e85-48ad-A71A-0969cb56a6cd}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1474">{859EAD94-2E85-48AD-A71A-0969CB56A6CD}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1475">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1475">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1476">Beispiel Videos</span><span class="sxs-lookup"><span data-stu-id="f9a52-1476">Sample Videos</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1477">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1477">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1478">Gewöhnliche</span><span class="sxs-lookup"><span data-stu-id="f9a52-1478">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1479">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1479">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1480">%Public%\videos\beispielvideos</span><span class="sxs-lookup"><span data-stu-id="f9a52-1480">%PUBLIC%\Videos\Sample Videos</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1481">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1481">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1482">Keine</span><span class="sxs-lookup"><span data-stu-id="f9a52-1482">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1483">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1483">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1484">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1484">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1485">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1485">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1486">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1486">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SavedGames"></span><span id="folderid_savedgames"></span><span id="FOLDERID_SAVEDGAMES"></span><dl> <span data-ttu-id="f9a52-1487"><dt><strong>FOLDERID_SavedGames</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1487"><dt><strong>FOLDERID_SavedGames</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1488">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1488">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1489">{4c5c32ff-bb9d-43b0-b5b4-2d72e54eaaa4}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1489">{4C5C32FF-BB9D-43b0-B5B4-2D72E54EAAA4}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1490">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1490">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1491">Gespeicherte Spiele</span><span class="sxs-lookup"><span data-stu-id="f9a52-1491">Saved Games</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1492">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1492">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1493">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-1493">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1494">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1494">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1495">%UserProfile%\Gespeicherte Spiele</span><span class="sxs-lookup"><span data-stu-id="f9a52-1495">%USERPROFILE%\Saved Games</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1496">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1496">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1497">None, in Windows Vista eingeführte Wert</span><span class="sxs-lookup"><span data-stu-id="f9a52-1497">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1498">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1498">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1499">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1499">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1500">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1500">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1501">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1501">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SavedPictures"></span><span id="folderid_savedpictures"></span><span id="FOLDERID_SAVEDPICTURES"></span><dl> <span data-ttu-id="f9a52-1502"><dt><strong>FOLDERID_SavedPictures</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1502"><dt><strong>FOLDERID_SavedPictures</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1503">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1503">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1504">{3b193882-D3AD-4eab-965A-69829d1b59f}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1504">{3B193882-D3AD-4eab-965A-69829D1FB59F}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1505">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1505">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1506">Gespeicherte Bilder</span><span class="sxs-lookup"><span data-stu-id="f9a52-1506">Saved Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1507">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1507">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1508">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-1508">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1509">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1509">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1510">%UserProfile%\pictures\gespeicherte Bilder</span><span class="sxs-lookup"><span data-stu-id="f9a52-1510">%USERPROFILE%\Pictures\Saved Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1511">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1511">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1512">Keine</span><span class="sxs-lookup"><span data-stu-id="f9a52-1512">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1513">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1513">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1514">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1514">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1515">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1515">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1516">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1516">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SavedPicturesLibrary"></span><span id="folderid_savedpictureslibrary"></span><span id="FOLDERID_SAVEDPICTURESLIBRARY"></span><dl> <span data-ttu-id="f9a52-1517"><dt><strong>FOLDERID_SavedPicturesLibrary</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1517"><dt><strong>FOLDERID_SavedPicturesLibrary</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1518">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1518">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1519">{E25B5812-BE88-4bd9-94B0-29233477B6C3}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1519">{E25B5812-BE88-4bd9-94B0-29233477B6C3}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1520">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1520">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1521">Gespeicherte Bildbibliothek</span><span class="sxs-lookup"><span data-stu-id="f9a52-1521">Saved Pictures Library</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1522">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1522">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1523">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-1523">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1524">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1524">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1525">%Appdate%\microsoft\windows\libraries\savedpictures.Library-MS</span><span class="sxs-lookup"><span data-stu-id="f9a52-1525">%APPDATE%\Microsoft\Windows\Libraries\SavedPictures.library-ms</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1526">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1526">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1527">Keine</span><span class="sxs-lookup"><span data-stu-id="f9a52-1527">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1528">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1528">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1529">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1529">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1530">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1530">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1531">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1531">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SavedSearches"></span><span id="folderid_savedsearches"></span><span id="FOLDERID_SAVEDSEARCHES"></span><dl> <span data-ttu-id="f9a52-1532"><dt><strong>FOLDERID_SavedSearches</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1532"><dt><strong>FOLDERID_SavedSearches</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1533">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1533">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1534">{7d1d3a04-Debb-4115-95cf-2f29da2920da}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1534">{7d1d3a04-debb-4115-95cf-2f29da2920da}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1535">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1535">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1536">Suchvorgänge</span><span class="sxs-lookup"><span data-stu-id="f9a52-1536">Searches</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1537">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1537">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1538">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-1538">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1539">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1539">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1540">%UserProfile%\suchen</span><span class="sxs-lookup"><span data-stu-id="f9a52-1540">%USERPROFILE%\Searches</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1541">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1541">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1542">Keine</span><span class="sxs-lookup"><span data-stu-id="f9a52-1542">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1543">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1543">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1544">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1544">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1545">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1545">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1546">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1546">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Screenshots"></span><span id="folderid_screenshots"></span><span id="FOLDERID_SCREENSHOTS"></span><dl> <span data-ttu-id="f9a52-1547"><dt><strong>FOLDERID_Screenshots</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1547"><dt><strong>FOLDERID_Screenshots</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1548">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1548">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1549">{b7bede81-df94-4682-a7d8-57a52620b86f}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1549">{b7bede81-df94-4682-a7d8-57a52620b86f}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1550">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1550">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1551">Screenshots</span><span class="sxs-lookup"><span data-stu-id="f9a52-1551">Screenshots</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1552">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1552">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1553">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-1553">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1554">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1554">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1555">%UserProfile%\pictures\screenshots</span><span class="sxs-lookup"><span data-stu-id="f9a52-1555">%USERPROFILE%\Pictures\Screenshots</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1556">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1556">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1557">None, in Windows 8 eingeführte Wert</span><span class="sxs-lookup"><span data-stu-id="f9a52-1557">None, value introduced in Windows 8</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1558">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1558">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1559">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1559">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1560">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1560">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1561">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1561">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SEARCH_CSC"></span><span id="folderid_search_csc"></span><dl> <span data-ttu-id="f9a52-1562"><dt><strong>FOLDERID_SEARCH_CSC</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1562"><dt><strong>FOLDERID_SEARCH_CSC</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1563">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1563">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1564">{ee32e446-31ca-4aba-814f-a5ebd2fd6d5e}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1564">{ee32e446-31ca-4aba-814f-a5ebd2fd6d5e}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1565">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1565">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1566">Offlinedateien</span><span class="sxs-lookup"><span data-stu-id="f9a52-1566">Offline Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1567">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1567">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1568">Virtu</span><span class="sxs-lookup"><span data-stu-id="f9a52-1568">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1569">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1569">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1570">Nicht zutreffend – virtueller Ordner</span><span class="sxs-lookup"><span data-stu-id="f9a52-1570">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1571">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1571">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1572">Keine</span><span class="sxs-lookup"><span data-stu-id="f9a52-1572">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1573">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1573">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1574">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1574">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1575">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1575">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1576">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1576">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SearchHistory"></span><span id="folderid_searchhistory"></span><span id="FOLDERID_SEARCHHISTORY"></span><dl> <span data-ttu-id="f9a52-1577"><dt><strong>FOLDERID_SearchHistory</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1577"><dt><strong>FOLDERID_SearchHistory</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1578">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1578">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1579">{0d4c3db6-03a3-462-a0e6-08924c41b5d4}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1579">{0D4C3DB6-03A3-462F-A0E6-08924C41B5D4}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1580">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1580">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1581">Verlauf</span><span class="sxs-lookup"><span data-stu-id="f9a52-1581">History</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1582">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1582">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1583">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-1583">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1584">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1584">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1585">%LocalAppData%\microsoft\windows\connectedsearch\history</span><span class="sxs-lookup"><span data-stu-id="f9a52-1585">%LOCALAPPDATA%\Microsoft\Windows\ConnectedSearch\History</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1586">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1586">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1587">None, in Windows 8.1 eingeführte Wert</span><span class="sxs-lookup"><span data-stu-id="f9a52-1587">None, value introduced in Windows 8.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1588">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1588">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1589">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1589">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1590">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1590">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1591">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1591">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SearchHome"></span><span id="folderid_searchhome"></span><span id="FOLDERID_SEARCHHOME"></span><dl> <span data-ttu-id="f9a52-1592"><dt><strong>FOLDERID_SearchHome</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1592"><dt><strong>FOLDERID_SearchHome</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1593">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1593">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1594">{190337d1-b8ca-4121-a639-6d472d16972a}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1594">{190337d1-b8ca-4121-a639-6d472d16972a}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1595">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1595">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1596">Suchergebnisse</span><span class="sxs-lookup"><span data-stu-id="f9a52-1596">Search Results</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1597">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1597">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1598">Virtu</span><span class="sxs-lookup"><span data-stu-id="f9a52-1598">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1599">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1599">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1600">Nicht zutreffend – virtueller Ordner</span><span class="sxs-lookup"><span data-stu-id="f9a52-1600">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1601">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1601">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1602">Keine</span><span class="sxs-lookup"><span data-stu-id="f9a52-1602">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1603">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1603">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1604">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1604">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1605">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1605">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1606">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1606">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SEARCH_MAPI"></span><span id="folderid_search_mapi"></span><dl> <span data-ttu-id="f9a52-1607"><dt><strong>FOLDERID_SEARCH_MAPI</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1607"><dt><strong>FOLDERID_SEARCH_MAPI</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1608">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1608">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1609">{98ec0e18-2098-4d44-8644-66979315a281}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1609">{98ec0e18-2098-4d44-8644-66979315a281}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1610">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1610">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1611">Microsoft Office Outlook</span><span class="sxs-lookup"><span data-stu-id="f9a52-1611">Microsoft Office Outlook</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1612">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1612">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1613">Virtu</span><span class="sxs-lookup"><span data-stu-id="f9a52-1613">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1614">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1614">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1615">Nicht zutreffend – virtueller Ordner</span><span class="sxs-lookup"><span data-stu-id="f9a52-1615">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1616">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1616">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1617">Keine</span><span class="sxs-lookup"><span data-stu-id="f9a52-1617">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1618">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1618">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1619">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1619">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1620">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1620">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1621">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1621">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SearchTemplates"></span><span id="folderid_searchtemplates"></span><span id="FOLDERID_SEARCHTEMPLATES"></span><dl> <span data-ttu-id="f9a52-1622"><dt><strong>FOLDERID_SearchTemplates</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1622"><dt><strong>FOLDERID_SearchTemplates</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1623">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1623">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1624">{7e636bfe-dfa9-4d5e-b456-d7b39851d8a9}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1624">{7E636BFE-DFA9-4D5E-B456-D7B39851D8A9}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1625">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1625">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1626">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="f9a52-1626">Templates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1627">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1627">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1628">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-1628">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1629">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1629">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1630">%LocalAppData%\microsoft\windows\connectedsearch\templates</span><span class="sxs-lookup"><span data-stu-id="f9a52-1630">%LOCALAPPDATA%\Microsoft\Windows\ConnectedSearch\Templates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1631">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1631">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1632">None, in Windows 8.1 eingeführte Wert</span><span class="sxs-lookup"><span data-stu-id="f9a52-1632">None, value introduced in Windows 8.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1633">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1633">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1634">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1634">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1635">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1635">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1636">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1636">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SendTo"></span><span id="folderid_sendto"></span><span id="FOLDERID_SENDTO"></span><dl> <span data-ttu-id="f9a52-1637"><dt><strong>FOLDERID_SendTo</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1637"><dt><strong>FOLDERID_SendTo</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1638">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1638">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1639">{8983036c-27c0-404b-8f08-102d10dcfd74}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1639">{8983036C-27C0-404B-8F08-102D10DCFD74}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1640">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1640">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1641">SendTo</span><span class="sxs-lookup"><span data-stu-id="f9a52-1641">SendTo</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1642">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1642">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1643">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-1643">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1644">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1644">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1645">%APPDATA%\microsoft\windows\sendto</span><span class="sxs-lookup"><span data-stu-id="f9a52-1645">%APPDATA%\Microsoft\Windows\SendTo</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1646">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1646">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1647">CSIDL_SENDTO</span><span class="sxs-lookup"><span data-stu-id="f9a52-1647">CSIDL_SENDTO</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1648">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1648">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1649">SendTo</span><span class="sxs-lookup"><span data-stu-id="f9a52-1649">SendTo</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1650">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1650">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1651">%UserProfile%\SendTo</span><span class="sxs-lookup"><span data-stu-id="f9a52-1651">%USERPROFILE%\SendTo</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SidebarDefaultParts"></span><span id="folderid_sidebardefaultparts"></span><span id="FOLDERID_SIDEBARDEFAULTPARTS"></span><dl> <span data-ttu-id="f9a52-1652"><dt><strong>FOLDERID_SidebarDefaultParts</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1652"><dt><strong>FOLDERID_SidebarDefaultParts</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1653">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1653">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1654">{7b396e54-9ec5-4300-be0a-2482ebae1a26}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1654">{7B396E54-9EC5-4300-BE0A-2482EBAE1A26}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1655">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1655">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1656">Geschenken</span><span class="sxs-lookup"><span data-stu-id="f9a52-1656">Gadgets</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1657">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1657">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1658">Gewöhnliche</span><span class="sxs-lookup"><span data-stu-id="f9a52-1658">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1659">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1659">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1660">%ProgramFiles%\Windows sidebar\gadgets</span><span class="sxs-lookup"><span data-stu-id="f9a52-1660">%ProgramFiles%\Windows Sidebar\Gadgets</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1661">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1661">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1662">Keine, neu für Windows 7</span><span class="sxs-lookup"><span data-stu-id="f9a52-1662">None, new for Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1663">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1663">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1664">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1664">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1665">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1665">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1666">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1666">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SidebarParts"></span><span id="folderid_sidebarparts"></span><span id="FOLDERID_SIDEBARPARTS"></span><dl> <span data-ttu-id="f9a52-1667"><dt><strong>FOLDERID_SidebarParts</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1667"><dt><strong>FOLDERID_SidebarParts</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1668">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1668">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1669">{A75D362E-50FC-4fb7-AC2C-A8BEAA314493}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1669">{A75D362E-50FC-4fb7-AC2C-A8BEAA314493}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1670">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1670">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1671">Geschenken</span><span class="sxs-lookup"><span data-stu-id="f9a52-1671">Gadgets</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1672">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1672">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1673">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-1673">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1674">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1674">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1675">%LocalAppData%\Microsoft\Windows sidebar\gadgets</span><span class="sxs-lookup"><span data-stu-id="f9a52-1675">%LOCALAPPDATA%\Microsoft\Windows Sidebar\Gadgets</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1676">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1676">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1677">Keine, neu für Windows 7</span><span class="sxs-lookup"><span data-stu-id="f9a52-1677">None, new for Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1678">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1678">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1679">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1679">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1680">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1680">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1681">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1681">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SkyDrive"></span><span id="folderid_skydrive"></span><span id="FOLDERID_SKYDRIVE"></span><dl> <span data-ttu-id="f9a52-1682"><dt><strong>FOLDERID_SkyDrive</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1682"><dt><strong>FOLDERID_SkyDrive</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1683">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1683">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1684">{A52BBA46-E9E1-435f-B3D9-28DAA648C0F6}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1684">{A52BBA46-E9E1-435f-B3D9-28DAA648C0F6}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1685">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1685">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1686">OneDrive</span><span class="sxs-lookup"><span data-stu-id="f9a52-1686">OneDrive</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1687">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1687">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1688">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-1688">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1689">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1689">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1690">%UserProfile%\onedrive</span><span class="sxs-lookup"><span data-stu-id="f9a52-1690">%USERPROFILE%\OneDrive</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1691">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1691">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1692">None, in Windows 8.1 eingeführte Wert</span><span class="sxs-lookup"><span data-stu-id="f9a52-1692">None, value introduced in Windows 8.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1693">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1693">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1694">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1694">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1695">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1695">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1696">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1696">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SkyDriveCameraRoll"></span><span id="folderid_skydrivecameraroll"></span><span id="FOLDERID_SKYDRIVECAMERAROLL"></span><dl> <span data-ttu-id="f9a52-1697"><dt><strong>FOLDERID_SkyDriveCameraRoll</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1697"><dt><strong>FOLDERID_SkyDriveCameraRoll</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1698">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1698">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1699">{767e6811-49cb-4273-87c2-20s355e1085b}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1699">{767E6811-49CB-4273-87C2-20F355E1085B}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1700">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1700">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1701">Kamera-Roll</span><span class="sxs-lookup"><span data-stu-id="f9a52-1701">Camera Roll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1702">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1702">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1703">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-1703">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1704">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1704">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1705">%UserProfile%\onedrive\pictures\camera Roll</span><span class="sxs-lookup"><span data-stu-id="f9a52-1705">%USERPROFILE%\OneDrive\Pictures\Camera Roll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1706">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1706">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1707">None, in Windows 8.1 eingeführte Wert</span><span class="sxs-lookup"><span data-stu-id="f9a52-1707">None, value introduced in Windows 8.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1708">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1708">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1709">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1709">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1710">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1710">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1711">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1711">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SkyDriveDocuments"></span><span id="folderid_skydrivedocuments"></span><span id="FOLDERID_SKYDRIVEDOCUMENTS"></span><dl> <span data-ttu-id="f9a52-1712"><dt><strong>FOLDERID_SkyDriveDocuments</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1712"><dt><strong>FOLDERID_SkyDriveDocuments</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1713">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1713">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1714">{24d89e24-2f19-4534-9dde -6a6671fbb8fe}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1714">{24D89E24-2F19-4534-9DDE-6A6671FBB8FE}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1715">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1715">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1716">Dokumente</span><span class="sxs-lookup"><span data-stu-id="f9a52-1716">Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1717">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1717">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1718">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-1718">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1719">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1719">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1720">%UserProfile%\onedrive\documents</span><span class="sxs-lookup"><span data-stu-id="f9a52-1720">%USERPROFILE%\OneDrive\Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1721">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1721">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1722">None, in Windows 8.1 eingeführte Wert</span><span class="sxs-lookup"><span data-stu-id="f9a52-1722">None, value introduced in Windows 8.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1723">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1723">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1724">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1724">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1725">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1725">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1726">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1726">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SkyDrivePictures"></span><span id="folderid_skydrivepictures"></span><span id="FOLDERID_SKYDRIVEPICTURES"></span><dl> <span data-ttu-id="f9a52-1727"><dt><strong>FOLDERID_SkyDrivePictures</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1727"><dt><strong>FOLDERID_SkyDrivePictures</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1728">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1728">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1729">{339719b5-8c47-4894-94c2-d8b77add44a6}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1729">{339719B5-8C47-4894-94C2-D8F77ADD44A6}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1730">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1730">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1731">Bilder</span><span class="sxs-lookup"><span data-stu-id="f9a52-1731">Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1732">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1732">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1733">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-1733">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1734">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1734">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1735">%UserProfile%\onedrive\bilder</span><span class="sxs-lookup"><span data-stu-id="f9a52-1735">%USERPROFILE%\OneDrive\Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1736">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1736">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1737">None, in Windows 8.1 eingeführte Wert</span><span class="sxs-lookup"><span data-stu-id="f9a52-1737">None, value introduced in Windows 8.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1738">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1738">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1739">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1739">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1740">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1740">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1741">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1741">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_StartMenu"></span><span id="folderid_startmenu"></span><span id="FOLDERID_STARTMENU"></span><dl> <span data-ttu-id="f9a52-1742"><dt><strong>FOLDERID_StartMenu</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1742"><dt><strong>FOLDERID_StartMenu</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1743">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1743">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1744">{625B53C3-AB48-4EC1-BA1F-A1EF4146FC19}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1744">{625B53C3-AB48-4EC1-BA1F-A1EF4146FC19}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1745">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1745">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1746">Startmenü</span><span class="sxs-lookup"><span data-stu-id="f9a52-1746">Start Menu</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1747">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1747">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1748">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-1748">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1749">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1749">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1750">%APPDATA%\microsoft\windows\startmenü</span><span class="sxs-lookup"><span data-stu-id="f9a52-1750">%APPDATA%\Microsoft\Windows\Start Menu</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1751">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1751">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1752">CSIDL_STARTMENU</span><span class="sxs-lookup"><span data-stu-id="f9a52-1752">CSIDL_STARTMENU</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1753">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1753">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1754">Startmenü</span><span class="sxs-lookup"><span data-stu-id="f9a52-1754">Start Menu</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1755">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1755">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1756">%UserProfile%\Startmenü</span><span class="sxs-lookup"><span data-stu-id="f9a52-1756">%USERPROFILE%\Start Menu</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Startup"></span><span id="folderid_startup"></span><span id="FOLDERID_STARTUP"></span><dl> <span data-ttu-id="f9a52-1757"><dt><strong>FOLDERID_Startup</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1757"><dt><strong>FOLDERID_Startup</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1758">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1758">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1759">{B97D20BB-F46A-4C97-BA10-5E3608430854}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1759">{B97D20BB-F46A-4C97-BA10-5E3608430854}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1760">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1760">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1761">Start</span><span class="sxs-lookup"><span data-stu-id="f9a52-1761">Startup</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1762">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1762">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1763">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-1763">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1764">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1764">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1765">%APPDATA%\Microsoft\Windows\Start menu\programs\startup</span><span class="sxs-lookup"><span data-stu-id="f9a52-1765">%APPDATA%\Microsoft\Windows\Start Menu\Programs\StartUp</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1766">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1766">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1767">CSIDL_STARTUP CSIDL_ALTSTARTUP</span><span class="sxs-lookup"><span data-stu-id="f9a52-1767">CSIDL_STARTUP, CSIDL_ALTSTARTUP</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1768">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1768">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1769">Start</span><span class="sxs-lookup"><span data-stu-id="f9a52-1769">Startup</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1770">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1770">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1771">%UserProfile%\Startmenü \ programme\startup</span><span class="sxs-lookup"><span data-stu-id="f9a52-1771">%USERPROFILE%\Start Menu\Programs\StartUp</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SyncManagerFolder"></span><span id="folderid_syncmanagerfolder"></span><span id="FOLDERID_SYNCMANAGERFOLDER"></span><dl> <span data-ttu-id="f9a52-1772"><dt><strong>FOLDERID_SyncManagerFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1772"><dt><strong>FOLDERID_SyncManagerFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1773">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1773">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1774">{43668bf 8-c14e-49b2-97c9-747784d784b7}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1774">{43668BF8-C14E-49B2-97C9-747784D784B7}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1775">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1775">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1776">Synchronisierungscenter</span><span class="sxs-lookup"><span data-stu-id="f9a52-1776">Sync Center</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1777">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1777">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1778">Virtu</span><span class="sxs-lookup"><span data-stu-id="f9a52-1778">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1779">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1779">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1780">Nicht zutreffend – virtueller Ordner</span><span class="sxs-lookup"><span data-stu-id="f9a52-1780">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1781">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1781">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1782">None, in Windows Vista eingeführte Wert</span><span class="sxs-lookup"><span data-stu-id="f9a52-1782">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1783">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1783">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1784">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1784">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1785">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1785">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1786">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1786">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SyncResultsFolder"></span><span id="folderid_syncresultsfolder"></span><span id="FOLDERID_SYNCRESULTSFOLDER"></span><dl> <span data-ttu-id="f9a52-1787"><dt><strong>FOLDERID_SyncResultsFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1787"><dt><strong>FOLDERID_SyncResultsFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1788">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1788">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1789">{289a9a43-be44-4057-a41b-587a76d7e7f}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1789">{289a9a43-be44-4057-a41b-587a76d7e7f9}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1790">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1790">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1791">Ergebnisse synchronisieren</span><span class="sxs-lookup"><span data-stu-id="f9a52-1791">Sync Results</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1792">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1792">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1793">Virtu</span><span class="sxs-lookup"><span data-stu-id="f9a52-1793">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1794">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1794">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1795">Nicht zutreffend – virtueller Ordner</span><span class="sxs-lookup"><span data-stu-id="f9a52-1795">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1796">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1796">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1797">None, in Windows Vista eingeführte Wert</span><span class="sxs-lookup"><span data-stu-id="f9a52-1797">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1798">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1798">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1799">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1799">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1800">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1800">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1801">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1801">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SyncSetupFolder"></span><span id="folderid_syncsetupfolder"></span><span id="FOLDERID_SYNCSETUPFOLDER"></span><dl> <span data-ttu-id="f9a52-1802"><dt><strong>FOLDERID_SyncSetupFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1802"><dt><strong>FOLDERID_SyncSetupFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1803">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1803">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1804">{0F 214138-b1d3-4 a90bba9-27cbc0c5389a}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1804">{0F214138-B1D3-4a90-BBA9-27CBC0C5389A}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1805">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1805">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1806">Sync-Setup</span><span class="sxs-lookup"><span data-stu-id="f9a52-1806">Sync Setup</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1807">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1807">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1808">Virtu</span><span class="sxs-lookup"><span data-stu-id="f9a52-1808">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1809">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1809">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1810">Nicht zutreffend – virtueller Ordner</span><span class="sxs-lookup"><span data-stu-id="f9a52-1810">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1811">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1811">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1812">None, in Windows Vista eingeführte Wert</span><span class="sxs-lookup"><span data-stu-id="f9a52-1812">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1813">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1813">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1814">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1814">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1815">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1815">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1816">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1816">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_System"></span><span id="folderid_system"></span><span id="FOLDERID_SYSTEM"></span><dl> <span data-ttu-id="f9a52-1817"><dt><strong>FOLDERID_System</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1817"><dt><strong>FOLDERID_System</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1818">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1818">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1819">{1ac14e77-02e7-4e5d-B744-2eb1ae5198b7}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1819">{1AC14E77-02E7-4E5D-B744-2EB1AE5198B7}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1820">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1820">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1821">System32</span><span class="sxs-lookup"><span data-stu-id="f9a52-1821">System32</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1822">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1822">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1823">FIXED</span><span class="sxs-lookup"><span data-stu-id="f9a52-1823">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1824">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1824">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1825">%WINDIR%\System32</span><span class="sxs-lookup"><span data-stu-id="f9a52-1825">%windir%\system32</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1826">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1826">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1827">CSIDL_SYSTEM</span><span class="sxs-lookup"><span data-stu-id="f9a52-1827">CSIDL_SYSTEM</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1828">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1828">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1829">system32</span><span class="sxs-lookup"><span data-stu-id="f9a52-1829">system32</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1830">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1830">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1831">%WINDIR%\System32</span><span class="sxs-lookup"><span data-stu-id="f9a52-1831">%windir%\system32</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SystemX86"></span><span id="folderid_systemx86"></span><span id="FOLDERID_SYSTEMX86"></span><dl> <span data-ttu-id="f9a52-1832"><dt><strong>FOLDERID_SystemX86</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1832"><dt><strong>FOLDERID_SystemX86</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1833">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1833">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1834">{D65231B0-B2F1-4857-A4CE-A8E7C6EA7D27}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1834">{D65231B0-B2F1-4857-A4CE-A8E7C6EA7D27}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1835">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1835">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1836">System32</span><span class="sxs-lookup"><span data-stu-id="f9a52-1836">System32</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1837">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1837">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1838">FIXED</span><span class="sxs-lookup"><span data-stu-id="f9a52-1838">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1839">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1839">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1840">%WINDIR%\System32</span><span class="sxs-lookup"><span data-stu-id="f9a52-1840">%windir%\system32</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1841">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1841">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1842">CSIDL_SYSTEMX86</span><span class="sxs-lookup"><span data-stu-id="f9a52-1842">CSIDL_SYSTEMX86</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1843">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1843">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1844">system32</span><span class="sxs-lookup"><span data-stu-id="f9a52-1844">system32</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1845">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1845">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1846">%WINDIR%\System32</span><span class="sxs-lookup"><span data-stu-id="f9a52-1846">%windir%\system32</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Templates"></span><span id="folderid_templates"></span><span id="FOLDERID_TEMPLATES"></span><dl> <span data-ttu-id="f9a52-1847"><dt><strong>FOLDERID_Templates</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1847"><dt><strong>FOLDERID_Templates</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1848">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1848">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1849">{A63293E8-664E-48DB-A079-DF759E0509F7}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1849">{A63293E8-664E-48DB-A079-DF759E0509F7}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1850">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1850">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1851">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="f9a52-1851">Templates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1852">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1852">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1853">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-1853">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1854">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1854">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1855">%APPDATA%\microsoft\windows\templates</span><span class="sxs-lookup"><span data-stu-id="f9a52-1855">%APPDATA%\Microsoft\Windows\Templates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1856">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1856">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1857">CSIDL_TEMPLATES</span><span class="sxs-lookup"><span data-stu-id="f9a52-1857">CSIDL_TEMPLATES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1858">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1858">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1859">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="f9a52-1859">Templates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1860">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1860">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1861">%UserProfile%\Vorlagen</span><span class="sxs-lookup"><span data-stu-id="f9a52-1861">%USERPROFILE%\Templates</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_TreeProperties"></span><span id="folderid_treeproperties"></span><span id="FOLDERID_TREEPROPERTIES"></span><dl> <span data-ttu-id="f9a52-1862"><dt><strong>FOLDERID_TreeProperties</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1862"><dt><strong>FOLDERID_TreeProperties</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="f9a52-1863">Wird in Windows Vista nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f9a52-1863">Not used in Windows Vista.</span></span> <span data-ttu-id="f9a52-1864">Wird ab Windows 7 nicht mehr unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f9a52-1864">Unsupported as of Windows 7.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_UserPinned"></span><span id="folderid_userpinned"></span><span id="FOLDERID_USERPINNED"></span><dl> <span data-ttu-id="f9a52-1865"><dt><strong>FOLDERID_UserPinned</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1865"><dt><strong>FOLDERID_UserPinned</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1866">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1866">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1867">{9e3995ab-1B-4 b827-48b24b6c7174}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1867">{9E3995AB-1F9C-4F13-B827-48B24B6C7174}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1868">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1868">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1869">Benutzer fixiert</span><span class="sxs-lookup"><span data-stu-id="f9a52-1869">User Pinned</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1870">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1870">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1871">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-1871">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1872">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1872">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1873">%APPDATA%\microsoft\internet Explorer\Quick launch\benutzerpinned</span><span class="sxs-lookup"><span data-stu-id="f9a52-1873">%APPDATA%\Microsoft\Internet Explorer\Quick Launch\User Pinned</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1874">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1874">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1875">None, in Windows 7 eingeführte Wert</span><span class="sxs-lookup"><span data-stu-id="f9a52-1875">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1876">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1876">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1877">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1877">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1878">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1878">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1879">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1879">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_UserProfiles"></span><span id="folderid_userprofiles"></span><span id="FOLDERID_USERPROFILES"></span><dl> <span data-ttu-id="f9a52-1880"><dt><strong>FOLDERID_UserProfiles</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1880"><dt><strong>FOLDERID_UserProfiles</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1881">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1881">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1882">{0762d272-c50a-4bb0-a382-697dcd729b80}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1882">{0762D272-C50A-4BB0-A382-697DCD729B80}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1883">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1883">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1884">Benutzer</span><span class="sxs-lookup"><span data-stu-id="f9a52-1884">Users</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1885">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1885">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1886">FIXED</span><span class="sxs-lookup"><span data-stu-id="f9a52-1886">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1887">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1887">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1888">%SystemDrive%\Users</span><span class="sxs-lookup"><span data-stu-id="f9a52-1888">%SystemDrive%\Users</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1889">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1889">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1890">Keine, neu für Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f9a52-1890">None, new for Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1891">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1891">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1892">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1892">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1893">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1893">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1894">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1894">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_UserProgramFiles"></span><span id="folderid_userprogramfiles"></span><span id="FOLDERID_USERPROGRAMFILES"></span><dl> <span data-ttu-id="f9a52-1895"><dt><strong>FOLDERID_UserProgramFiles</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1895"><dt><strong>FOLDERID_UserProgramFiles</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1896">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1896">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1897">{5cd7aee2-2219-4a67-b85d-6c9ce15660cb}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1897">{5CD7AEE2-2219-4A67-B85D-6C9CE15660CB}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1898">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1898">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1899">Programs</span><span class="sxs-lookup"><span data-stu-id="f9a52-1899">Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1900">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1900">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1901">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-1901">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1902">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1902">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1903">%LocalAppData%\Programme</span><span class="sxs-lookup"><span data-stu-id="f9a52-1903">%LOCALAPPDATA%\Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1904">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1904">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1905">None, in Windows 7 eingeführte Wert</span><span class="sxs-lookup"><span data-stu-id="f9a52-1905">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1906">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1906">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1907">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1907">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1908">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1908">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1909">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1909">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_UserProgramFilesCommon"></span><span id="folderid_userprogramfilescommon"></span><span id="FOLDERID_USERPROGRAMFILESCOMMON"></span><dl> <span data-ttu-id="f9a52-1910"><dt><strong>FOLDERID_UserProgramFilesCommon</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1910"><dt><strong>FOLDERID_UserProgramFilesCommon</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1911">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1911">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1912">{BCBD3057-CA5C-4622-B42D-BC56DB0AE516}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1912">{BCBD3057-CA5C-4622-B42D-BC56DB0AE516}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1913">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1913">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1914">Programs</span><span class="sxs-lookup"><span data-stu-id="f9a52-1914">Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1915">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1915">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1916">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-1916">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1917">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1917">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1918">%LocalAppData%\Programme\Common</span><span class="sxs-lookup"><span data-stu-id="f9a52-1918">%LOCALAPPDATA%\Programs\Common</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1919">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1919">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1920">None, in Windows 7 eingeführte Wert</span><span class="sxs-lookup"><span data-stu-id="f9a52-1920">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1921">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1921">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1922">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1922">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1923">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1923">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1924">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1924">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_UsersFiles"></span><span id="folderid_usersfiles"></span><span id="FOLDERID_USERSFILES"></span><dl> <span data-ttu-id="f9a52-1925"><dt><strong>FOLDERID_UsersFiles</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1925"><dt><strong>FOLDERID_UsersFiles</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1926">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1926">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1927">{f3ce0f7c-4901-4acc-8648-d5d44b04ef8f}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1927">{f3ce0f7c-4901-4acc-8648-d5d44b04ef8f}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1928">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1928">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1929">Der vollständige Name des Benutzers (z.b. Jean Philippe Bagel), der beim Erstellen des Benutzerkontos eingegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="f9a52-1929">The user's full name (for instance, Jean Philippe Bagel) entered when the user account was created.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1930">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1930">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1931">Virtu</span><span class="sxs-lookup"><span data-stu-id="f9a52-1931">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1932">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1932">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1933">Nicht zutreffend – virtueller Ordner</span><span class="sxs-lookup"><span data-stu-id="f9a52-1933">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1934">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1934">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1935">Keine</span><span class="sxs-lookup"><span data-stu-id="f9a52-1935">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1936">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1936">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1937">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1937">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1938">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1938">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1939">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1939">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_UsersLibraries"></span><span id="folderid_userslibraries"></span><span id="FOLDERID_USERSLIBRARIES"></span><dl> <span data-ttu-id="f9a52-1940"><dt><strong>FOLDERID_UsersLibraries</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1940"><dt><strong>FOLDERID_UsersLibraries</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1941">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1941">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1942">{A302545D-DEFF-464b-ABE8-61C8648D939B}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1942">{A302545D-DEFF-464b-ABE8-61C8648D939B}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1943">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1943">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1944">Bibliotheken</span><span class="sxs-lookup"><span data-stu-id="f9a52-1944">Libraries</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1945">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1945">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1946">Virtu</span><span class="sxs-lookup"><span data-stu-id="f9a52-1946">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1947">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1947">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1948">Nicht zutreffend – virtueller Ordner</span><span class="sxs-lookup"><span data-stu-id="f9a52-1948">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1949">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1949">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1950">None, in Windows 7 eingeführte Wert</span><span class="sxs-lookup"><span data-stu-id="f9a52-1950">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1951">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1951">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1952">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1952">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1953">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1953">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1954">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1954">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Videos"></span><span id="folderid_videos"></span><span id="FOLDERID_VIDEOS"></span><dl> <span data-ttu-id="f9a52-1955"><dt><strong>FOLDERID_Videos</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1955"><dt><strong>FOLDERID_Videos</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1956">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1956">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1957">{18989B1D-99B5-455B-841C-AB7C74E4DDFC}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1957">{18989B1D-99B5-455B-841C-AB7C74E4DDFC}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1958">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1958">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1959">Videos</span><span class="sxs-lookup"><span data-stu-id="f9a52-1959">Videos</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1960">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1960">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1961">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-1961">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1962">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1962">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1963">%UserProfile%\videos</span><span class="sxs-lookup"><span data-stu-id="f9a52-1963">%USERPROFILE%\Videos</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1964">CSIDL</span><span class="sxs-lookup"><span data-stu-id="f9a52-1964">CSIDL</span></span></td>
<td><span data-ttu-id="f9a52-1965">CSIDL_MYVIDEO</span><span class="sxs-lookup"><span data-stu-id="f9a52-1965">CSIDL_MYVIDEO</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1966">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1966">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1967">Meine Videos</span><span class="sxs-lookup"><span data-stu-id="f9a52-1967">My Videos</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1968">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1968">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1969">%USERPROFILE%\Eigene Dateien\Eigene Videos</span><span class="sxs-lookup"><span data-stu-id="f9a52-1969">%USERPROFILE%\My Documents\My Videos</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_VideosLibrary"></span><span id="folderid_videoslibrary"></span><span id="FOLDERID_VIDEOSLIBRARY"></span><dl> <span data-ttu-id="f9a52-1970"><dt><strong>FOLDERID_VideosLibrary</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1970"><dt><strong>FOLDERID_VideosLibrary</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1971">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1971">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1972">{491e922f -5643-4af4-A7EB-4e7a138d8174}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1972">{491E922F-5643-4AF4-A7EB-4E7A138D8174}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1973">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1973">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1974">Videos</span><span class="sxs-lookup"><span data-stu-id="f9a52-1974">Videos</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1975">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1975">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1976">Peruser</span><span class="sxs-lookup"><span data-stu-id="f9a52-1976">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1977">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1977">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1978">%APPDATA%\microsoft\windows\libraries\videos.Library-MS</span><span class="sxs-lookup"><span data-stu-id="f9a52-1978">%APPDATA%\Microsoft\Windows\Libraries\Videos.library-ms</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1979">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1979">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1980">None, in Windows 7 eingeführte Wert</span><span class="sxs-lookup"><span data-stu-id="f9a52-1980">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1981">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1981">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1982">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1982">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1983">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1983">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1984">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-1984">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Windows"></span><span id="folderid_windows"></span><span id="FOLDERID_WINDOWS"></span><dl> <span data-ttu-id="f9a52-1985"><dt><strong>FOLDERID_Windows</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="f9a52-1985"><dt><strong>FOLDERID_Windows</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f9a52-1986">GUID</span><span class="sxs-lookup"><span data-stu-id="f9a52-1986">GUID</span></span></td>
<td><span data-ttu-id="f9a52-1987">{F38BF404-1D43-42F2-9305-67DE0B28FC23}</span><span class="sxs-lookup"><span data-stu-id="f9a52-1987">{F38BF404-1D43-42F2-9305-67DE0B28FC23}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1988">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="f9a52-1988">Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1989">Windows</span><span class="sxs-lookup"><span data-stu-id="f9a52-1989">Windows</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1990">Ordnertyp</span><span class="sxs-lookup"><span data-stu-id="f9a52-1990">Folder Type</span></span></td>
<td><span data-ttu-id="f9a52-1991">FIXED</span><span class="sxs-lookup"><span data-stu-id="f9a52-1991">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1992">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-1992">Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1993">%windir%</span><span class="sxs-lookup"><span data-stu-id="f9a52-1993">%windir%</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1994">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-1994">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="f9a52-1995">CSIDL_WINDOWS</span><span class="sxs-lookup"><span data-stu-id="f9a52-1995">CSIDL_WINDOWS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f9a52-1996">Legacy Anzeige Name</span><span class="sxs-lookup"><span data-stu-id="f9a52-1996">Legacy Display Name</span></span></td>
<td><span data-ttu-id="f9a52-1997">WINDOWS</span><span class="sxs-lookup"><span data-stu-id="f9a52-1997">WINDOWS</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f9a52-1998">Standardpfad für Legacy</span><span class="sxs-lookup"><span data-stu-id="f9a52-1998">Legacy Default Path</span></span></td>
<td><span data-ttu-id="f9a52-1999">%windir%</span><span class="sxs-lookup"><span data-stu-id="f9a52-1999">%windir%</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="f9a52-2000">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f9a52-2000">Remarks</span></span>

<span data-ttu-id="f9a52-2001">Die Interpretation bestimmter **KNOWNFOLDERID** -Werte hängt davon ab, ob der Ordner Teil einer 32-Bit-oder einer 64-Bit-Anwendung ist und ob diese Anwendung unter einem 32-Bit-oder 64-Bit-Betriebssystem ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f9a52-2001">The interpretation of certain **KNOWNFOLDERID** values depends on whether the folder is part of a 32-bit or 64-bit application and whether that application is running on a 32-bit or 64-bit operating system.</span></span> <span data-ttu-id="f9a52-2002">Wenn Ihre Anwendung zwischen z. b. **Programmdateien** und **Programmdateien (x86)** unterscheiden muss, müssen Sie die richtige **KNOWNFOLDERID** für die Situation verwenden.</span><span class="sxs-lookup"><span data-stu-id="f9a52-2002">If your application needs to distinguish between, for example, **Program Files** and **Program Files (x86)**, you must use the right **KNOWNFOLDERID** for the situation.</span></span>

<span data-ttu-id="f9a52-2003">In den folgenden Tabellen wird die Verwendung von **KNOWNFOLDERID** in diesen Fällen zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="f9a52-2003">The following tables summarize the **KNOWNFOLDERID** use in those cases.</span></span>


<span data-ttu-id="f9a52-2004">**Folderid- \_ Programmdateien**</span><span class="sxs-lookup"><span data-stu-id="f9a52-2004">**FOLDERID\_ProgramFiles**</span></span> 

| <span data-ttu-id="f9a52-2005">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="f9a52-2005">Operating System</span></span> | <span data-ttu-id="f9a52-2006">Application</span><span class="sxs-lookup"><span data-stu-id="f9a52-2006">Application</span></span> | <span data-ttu-id="f9a52-2007">KNOWNFOLDERID</span><span class="sxs-lookup"><span data-stu-id="f9a52-2007">KNOWNFOLDERID</span></span> | <span data-ttu-id="f9a52-2008">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-2008">Default Path</span></span> | <span data-ttu-id="f9a52-2009">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-2009">CSIDL Equivalent</span></span> |
|------------------|-------------|---------------|--------------|------------------|  
| <span data-ttu-id="f9a52-2010">32-Bit</span><span class="sxs-lookup"><span data-stu-id="f9a52-2010">32 bit</span></span> | <span data-ttu-id="f9a52-2011">32-Bit</span><span class="sxs-lookup"><span data-stu-id="f9a52-2011">32 bit</span></span> | <span data-ttu-id="f9a52-2012">Folderid- \_ Programmdateien</span><span class="sxs-lookup"><span data-stu-id="f9a52-2012">FOLDERID\_ProgramFiles</span></span> | <span data-ttu-id="f9a52-2013">% System Drive%- \\ Programmdateien</span><span class="sxs-lookup"><span data-stu-id="f9a52-2013">%SystemDrive%\\Program Files</span></span> | <span data-ttu-id="f9a52-2014">CSIDL- \_ Programm \_ Dateien</span><span class="sxs-lookup"><span data-stu-id="f9a52-2014">CSIDL\_PROGRAM\_FILES</span></span> |
| <span data-ttu-id="f9a52-2015">32-Bit</span><span class="sxs-lookup"><span data-stu-id="f9a52-2015">32 bit</span></span> | <span data-ttu-id="f9a52-2016">32-Bit</span><span class="sxs-lookup"><span data-stu-id="f9a52-2016">32 bit</span></span> | <span data-ttu-id="f9a52-2017">Folderid \_ ProgramFilesX86</span><span class="sxs-lookup"><span data-stu-id="f9a52-2017">FOLDERID\_ProgramFilesX86</span></span> | <span data-ttu-id="f9a52-2018">% System Drive%- \\ Programmdateien</span><span class="sxs-lookup"><span data-stu-id="f9a52-2018">%SystemDrive%\\Program Files</span></span> | <span data-ttu-id="f9a52-2019">CSIDL- \_ Programm \_ FILESX86</span><span class="sxs-lookup"><span data-stu-id="f9a52-2019">CSIDL\_PROGRAM\_FILESX86</span></span> |
| <span data-ttu-id="f9a52-2020">32-Bit</span><span class="sxs-lookup"><span data-stu-id="f9a52-2020">32 bit</span></span> | <span data-ttu-id="f9a52-2021">32-Bit</span><span class="sxs-lookup"><span data-stu-id="f9a52-2021">32 bit</span></span> | <span data-ttu-id="f9a52-2022">Folderid \_ ProgramFilesX64 (wird unter 32-Bit-Betriebssystemen nicht unterstützt)</span><span class="sxs-lookup"><span data-stu-id="f9a52-2022">FOLDERID\_ProgramFilesX64 (not supported under 32-bit operating systems)</span></span> | <span data-ttu-id="f9a52-2023">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-2023">Not applicable</span></span> | <span data-ttu-id="f9a52-2024">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-2024">Not applicable</span></span> |
| <span data-ttu-id="f9a52-2025">64-Bit</span><span class="sxs-lookup"><span data-stu-id="f9a52-2025">64 bit</span></span> | <span data-ttu-id="f9a52-2026">64-Bit</span><span class="sxs-lookup"><span data-stu-id="f9a52-2026">64 bit</span></span> | <span data-ttu-id="f9a52-2027">Folderid- \_ Programmdateien</span><span class="sxs-lookup"><span data-stu-id="f9a52-2027">FOLDERID\_ProgramFiles</span></span> | <span data-ttu-id="f9a52-2028">% System Drive%- \\ Programmdateien</span><span class="sxs-lookup"><span data-stu-id="f9a52-2028">%SystemDrive%\\Program Files</span></span> | <span data-ttu-id="f9a52-2029">CSIDL- \_ Programm \_ Dateien</span><span class="sxs-lookup"><span data-stu-id="f9a52-2029">CSIDL\_PROGRAM\_FILES</span></span> |
| <span data-ttu-id="f9a52-2030">64-Bit</span><span class="sxs-lookup"><span data-stu-id="f9a52-2030">64 bit</span></span> | <span data-ttu-id="f9a52-2031">64-Bit</span><span class="sxs-lookup"><span data-stu-id="f9a52-2031">64 bit</span></span> | <span data-ttu-id="f9a52-2032">Folderid \_ ProgramFilesX86</span><span class="sxs-lookup"><span data-stu-id="f9a52-2032">FOLDERID\_ProgramFilesX86</span></span> | <span data-ttu-id="f9a52-2033">% System Drive% \\ Program Files (x86)</span><span class="sxs-lookup"><span data-stu-id="f9a52-2033">%SystemDrive%\\Program Files (x86)</span></span> | <span data-ttu-id="f9a52-2034">CSIDL- \_ Programm \_ FILESX86</span><span class="sxs-lookup"><span data-stu-id="f9a52-2034">CSIDL\_PROGRAM\_FILESX86</span></span> |
| <span data-ttu-id="f9a52-2035">64-Bit</span><span class="sxs-lookup"><span data-stu-id="f9a52-2035">64 bit</span></span> | <span data-ttu-id="f9a52-2036">64-Bit</span><span class="sxs-lookup"><span data-stu-id="f9a52-2036">64 bit</span></span> | <span data-ttu-id="f9a52-2037">Folderid \_ ProgramFilesX64</span><span class="sxs-lookup"><span data-stu-id="f9a52-2037">FOLDERID\_ProgramFilesX64</span></span> | <span data-ttu-id="f9a52-2038">% System Drive%- \\ Programmdateien</span><span class="sxs-lookup"><span data-stu-id="f9a52-2038">%SystemDrive%\\Program Files</span></span> | <span data-ttu-id="f9a52-2039">Keine</span><span class="sxs-lookup"><span data-stu-id="f9a52-2039">None</span></span> |
| <span data-ttu-id="f9a52-2040">64-Bit</span><span class="sxs-lookup"><span data-stu-id="f9a52-2040">64 bit</span></span> | <span data-ttu-id="f9a52-2041">32-Bit</span><span class="sxs-lookup"><span data-stu-id="f9a52-2041">32 bit</span></span> | <span data-ttu-id="f9a52-2042">Folderid- \_ Programmdateien</span><span class="sxs-lookup"><span data-stu-id="f9a52-2042">FOLDERID\_ProgramFiles</span></span> | <span data-ttu-id="f9a52-2043">% System Drive% \\ Program Files (x86)</span><span class="sxs-lookup"><span data-stu-id="f9a52-2043">%SystemDrive%\\Program Files (x86)</span></span> | <span data-ttu-id="f9a52-2044">CSIDL- \_ Programm \_ Dateien</span><span class="sxs-lookup"><span data-stu-id="f9a52-2044">CSIDL\_PROGRAM\_FILES</span></span> |
| <span data-ttu-id="f9a52-2045">64-Bit</span><span class="sxs-lookup"><span data-stu-id="f9a52-2045">64 bit</span></span> | <span data-ttu-id="f9a52-2046">32-Bit</span><span class="sxs-lookup"><span data-stu-id="f9a52-2046">32 bit</span></span> | <span data-ttu-id="f9a52-2047">Folderid \_ ProgramFilesX86</span><span class="sxs-lookup"><span data-stu-id="f9a52-2047">FOLDERID\_ProgramFilesX86</span></span> | <span data-ttu-id="f9a52-2048">% System Drive% \\ Program Files (x86)</span><span class="sxs-lookup"><span data-stu-id="f9a52-2048">%SystemDrive%\\Program Files (x86)</span></span> | <span data-ttu-id="f9a52-2049">CSIDL- \_ Programm \_ FILESX86</span><span class="sxs-lookup"><span data-stu-id="f9a52-2049">CSIDL\_PROGRAM\_FILESX86</span></span> |
| <span data-ttu-id="f9a52-2050">64-Bit</span><span class="sxs-lookup"><span data-stu-id="f9a52-2050">64 bit</span></span> | <span data-ttu-id="f9a52-2051">32-Bit</span><span class="sxs-lookup"><span data-stu-id="f9a52-2051">32 bit</span></span> | <span data-ttu-id="f9a52-2052">Folderid \_ ProgramFilesX64 (wird für 32-Bit-Anwendungen nicht unterstützt)</span><span class="sxs-lookup"><span data-stu-id="f9a52-2052">FOLDERID\_ProgramFilesX64 (not supported for 32-bit applications)</span></span> | <span data-ttu-id="f9a52-2053">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-2053">Not applicable</span></span> | <span data-ttu-id="f9a52-2054">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-2054">Not applicable</span></span> |


<span data-ttu-id="f9a52-2055">**Folderid \_ programfilescommon**</span><span class="sxs-lookup"><span data-stu-id="f9a52-2055">**FOLDERID\_ProgramFilesCommon**</span></span>

| <span data-ttu-id="f9a52-2056">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="f9a52-2056">Operating System</span></span> | <span data-ttu-id="f9a52-2057">Application</span><span class="sxs-lookup"><span data-stu-id="f9a52-2057">Application</span></span> | <span data-ttu-id="f9a52-2058">KNOWNFOLDERID</span><span class="sxs-lookup"><span data-stu-id="f9a52-2058">KNOWNFOLDERID</span></span> | <span data-ttu-id="f9a52-2059">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-2059">Default Path</span></span> | <span data-ttu-id="f9a52-2060">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-2060">CSIDL Equivalent</span></span> |
|------------------|-------------|---------------|--------------|------------------|  
| <span data-ttu-id="f9a52-2061">32-Bit</span><span class="sxs-lookup"><span data-stu-id="f9a52-2061">32 bit</span></span> | <span data-ttu-id="f9a52-2062">32-Bit</span><span class="sxs-lookup"><span data-stu-id="f9a52-2062">32 bit</span></span> | <span data-ttu-id="f9a52-2063">Folderid \_ programfilescommon</span><span class="sxs-lookup"><span data-stu-id="f9a52-2063">FOLDERID\_ProgramFilesCommon</span></span> | <span data-ttu-id="f9a52-2064">% Program Files% \\ Allgemeine Dateien</span><span class="sxs-lookup"><span data-stu-id="f9a52-2064">%ProgramFiles%\\Common Files</span></span> | <span data-ttu-id="f9a52-2065">Allgemeine CSIDL- \_ Programm \_ Dateien \_</span><span class="sxs-lookup"><span data-stu-id="f9a52-2065">CSIDL\_PROGRAM\_FILES\_COMMON</span></span> |
| <span data-ttu-id="f9a52-2066">32-Bit</span><span class="sxs-lookup"><span data-stu-id="f9a52-2066">32 bit</span></span> | <span data-ttu-id="f9a52-2067">32-Bit</span><span class="sxs-lookup"><span data-stu-id="f9a52-2067">32 bit</span></span> | <span data-ttu-id="f9a52-2068">Folderid \_ ProgramFilesCommonX86</span><span class="sxs-lookup"><span data-stu-id="f9a52-2068">FOLDERID\_ProgramFilesCommonX86</span></span> | <span data-ttu-id="f9a52-2069">% Program Files% \\ Allgemeine Dateien</span><span class="sxs-lookup"><span data-stu-id="f9a52-2069">%ProgramFiles%\\Common Files</span></span> | <span data-ttu-id="f9a52-2070">CSIDL- \_ Programm \_ Dateien \_ COMMONX86</span><span class="sxs-lookup"><span data-stu-id="f9a52-2070">CSIDL\_PROGRAM\_FILES\_COMMONX86</span></span> |
| <span data-ttu-id="f9a52-2071">32-Bit</span><span class="sxs-lookup"><span data-stu-id="f9a52-2071">32 bit</span></span> | <span data-ttu-id="f9a52-2072">32-Bit</span><span class="sxs-lookup"><span data-stu-id="f9a52-2072">32 bit</span></span> | <span data-ttu-id="f9a52-2073">Folderid \_ ProgramFilesCommonX64 (nicht definiert)</span><span class="sxs-lookup"><span data-stu-id="f9a52-2073">FOLDERID\_ProgramFilesCommonX64 (undefined)</span></span> | <span data-ttu-id="f9a52-2074">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-2074">Not applicable</span></span> | <span data-ttu-id="f9a52-2075">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f9a52-2075">Not applicable</span></span> |
| <span data-ttu-id="f9a52-2076">64-Bit</span><span class="sxs-lookup"><span data-stu-id="f9a52-2076">64 bit</span></span> | <span data-ttu-id="f9a52-2077">64-Bit</span><span class="sxs-lookup"><span data-stu-id="f9a52-2077">64 bit</span></span> | <span data-ttu-id="f9a52-2078">Folderid \_ programfilescommon</span><span class="sxs-lookup"><span data-stu-id="f9a52-2078">FOLDERID\_ProgramFilesCommon</span></span> | <span data-ttu-id="f9a52-2079">% Program Files% \\ Allgemeine Dateien</span><span class="sxs-lookup"><span data-stu-id="f9a52-2079">%ProgramFiles%\\Common Files</span></span> | <span data-ttu-id="f9a52-2080">Allgemeine CSIDL- \_ Programm \_ Dateien \_</span><span class="sxs-lookup"><span data-stu-id="f9a52-2080">CSIDL\_PROGRAM\_FILES\_COMMON</span></span> |
| <span data-ttu-id="f9a52-2081">64-Bit</span><span class="sxs-lookup"><span data-stu-id="f9a52-2081">64 bit</span></span> | <span data-ttu-id="f9a52-2082">64-Bit</span><span class="sxs-lookup"><span data-stu-id="f9a52-2082">64 bit</span></span> | <span data-ttu-id="f9a52-2083">Folderid \_ ProgramFilesCommonX86</span><span class="sxs-lookup"><span data-stu-id="f9a52-2083">FOLDERID\_ProgramFilesCommonX86</span></span> | <span data-ttu-id="f9a52-2084">% Program Files (x86)% \\ Allgemeine Dateien</span><span class="sxs-lookup"><span data-stu-id="f9a52-2084">%ProgramFiles(x86)%\\Common Files</span></span> | <span data-ttu-id="f9a52-2085">CSIDL- \_ Programm \_ Dateien \_ COMMONX86</span><span class="sxs-lookup"><span data-stu-id="f9a52-2085">CSIDL\_PROGRAM\_FILES\_COMMONX86</span></span> |
| <span data-ttu-id="f9a52-2086">64-Bit</span><span class="sxs-lookup"><span data-stu-id="f9a52-2086">64 bit</span></span> | <span data-ttu-id="f9a52-2087">64-Bit</span><span class="sxs-lookup"><span data-stu-id="f9a52-2087">64 bit</span></span> | <span data-ttu-id="f9a52-2088">Folderid \_ ProgramFilesCommonX64</span><span class="sxs-lookup"><span data-stu-id="f9a52-2088">FOLDERID\_ProgramFilesCommonX64</span></span> | <span data-ttu-id="f9a52-2089">% Program Files% \\ Allgemeine Dateien</span><span class="sxs-lookup"><span data-stu-id="f9a52-2089">%ProgramFiles%\\Common Files</span></span> | <span data-ttu-id="f9a52-2090">Keine</span><span class="sxs-lookup"><span data-stu-id="f9a52-2090">None</span></span> |
| <span data-ttu-id="f9a52-2091">64-Bit</span><span class="sxs-lookup"><span data-stu-id="f9a52-2091">64 bit</span></span> | <span data-ttu-id="f9a52-2092">32-Bit</span><span class="sxs-lookup"><span data-stu-id="f9a52-2092">32 bit</span></span> | <span data-ttu-id="f9a52-2093">Folderid \_ programfilescommon</span><span class="sxs-lookup"><span data-stu-id="f9a52-2093">FOLDERID\_ProgramFilesCommon</span></span> | <span data-ttu-id="f9a52-2094">% Program Files (x86)% \\ Allgemeine Dateien</span><span class="sxs-lookup"><span data-stu-id="f9a52-2094">%ProgramFiles(x86)%\\Common Files</span></span> | <span data-ttu-id="f9a52-2095">Allgemeine CSIDL- \_ Programm \_ Dateien \_</span><span class="sxs-lookup"><span data-stu-id="f9a52-2095">CSIDL\_PROGRAM\_FILES\_COMMON</span></span> |
| <span data-ttu-id="f9a52-2096">64-Bit</span><span class="sxs-lookup"><span data-stu-id="f9a52-2096">64 bit</span></span> | <span data-ttu-id="f9a52-2097">32-Bit</span><span class="sxs-lookup"><span data-stu-id="f9a52-2097">32 bit</span></span> | <span data-ttu-id="f9a52-2098">Folderid \_ ProgramFilesCommonX86</span><span class="sxs-lookup"><span data-stu-id="f9a52-2098">FOLDERID\_ProgramFilesCommonX86</span></span> | <span data-ttu-id="f9a52-2099">% Program Files (x86)% \\ Allgemeine Dateien</span><span class="sxs-lookup"><span data-stu-id="f9a52-2099">%ProgramFiles(x86)%\\Common Files</span></span> | <span data-ttu-id="f9a52-2100">CSIDL- \_ Programm \_ Dateien \_ COMMONX86</span><span class="sxs-lookup"><span data-stu-id="f9a52-2100">CSIDL\_PROGRAM\_FILES\_COMMONX86</span></span> |
| <span data-ttu-id="f9a52-2101">64-Bit</span><span class="sxs-lookup"><span data-stu-id="f9a52-2101">64 bit</span></span> | <span data-ttu-id="f9a52-2102">32-Bit</span><span class="sxs-lookup"><span data-stu-id="f9a52-2102">32 bit</span></span> | <span data-ttu-id="f9a52-2103">Folderid \_ ProgramFilesCommonX64</span><span class="sxs-lookup"><span data-stu-id="f9a52-2103">FOLDERID\_ProgramFilesCommonX64</span></span> | <span data-ttu-id="f9a52-2104">% Program Files% \\ Allgemeine Dateien</span><span class="sxs-lookup"><span data-stu-id="f9a52-2104">%ProgramFiles%\\Common Files</span></span> | <span data-ttu-id="f9a52-2105">Keine</span><span class="sxs-lookup"><span data-stu-id="f9a52-2105">None</span></span> |


<span data-ttu-id="f9a52-2106">**Folderid- \_ System**</span><span class="sxs-lookup"><span data-stu-id="f9a52-2106">**FOLDERID\_System**</span></span>

| <span data-ttu-id="f9a52-2107">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="f9a52-2107">Operating System</span></span> | <span data-ttu-id="f9a52-2108">Application</span><span class="sxs-lookup"><span data-stu-id="f9a52-2108">Application</span></span> | <span data-ttu-id="f9a52-2109">KNOWNFOLDERID</span><span class="sxs-lookup"><span data-stu-id="f9a52-2109">KNOWNFOLDERID</span></span> | <span data-ttu-id="f9a52-2110">Standard Path</span><span class="sxs-lookup"><span data-stu-id="f9a52-2110">Default Path</span></span> | <span data-ttu-id="f9a52-2111">CSIDL-Entsprechung</span><span class="sxs-lookup"><span data-stu-id="f9a52-2111">CSIDL Equivalent</span></span> |
|------------------|-------------|---------------|--------------|------------------|  
| <span data-ttu-id="f9a52-2112">32-Bit</span><span class="sxs-lookup"><span data-stu-id="f9a52-2112">32 bit</span></span> | <span data-ttu-id="f9a52-2113">32-Bit</span><span class="sxs-lookup"><span data-stu-id="f9a52-2113">32 bit</span></span> | <span data-ttu-id="f9a52-2114">Folderid- \_ System</span><span class="sxs-lookup"><span data-stu-id="f9a52-2114">FOLDERID\_System</span></span> | <span data-ttu-id="f9a52-2115">% windir% \\ system32</span><span class="sxs-lookup"><span data-stu-id="f9a52-2115">%windir%\\system32</span></span> | <span data-ttu-id="f9a52-2116">CSIDL- \_ System</span><span class="sxs-lookup"><span data-stu-id="f9a52-2116">CSIDL\_SYSTEM</span></span> |
| <span data-ttu-id="f9a52-2117">32-Bit</span><span class="sxs-lookup"><span data-stu-id="f9a52-2117">32 bit</span></span> | <span data-ttu-id="f9a52-2118">32-Bit</span><span class="sxs-lookup"><span data-stu-id="f9a52-2118">32 bit</span></span> | <span data-ttu-id="f9a52-2119">Folderid \_ SystemX86</span><span class="sxs-lookup"><span data-stu-id="f9a52-2119">FOLDERID\_SystemX86</span></span> | <span data-ttu-id="f9a52-2120">% windir% \\ system32</span><span class="sxs-lookup"><span data-stu-id="f9a52-2120">%windir%\\system32</span></span> | <span data-ttu-id="f9a52-2121">CSIDL- \_ SYSTEMX86</span><span class="sxs-lookup"><span data-stu-id="f9a52-2121">CSIDL\_SYSTEMX86</span></span> |
| <span data-ttu-id="f9a52-2122">64-Bit</span><span class="sxs-lookup"><span data-stu-id="f9a52-2122">64 bit</span></span> | <span data-ttu-id="f9a52-2123">64-Bit</span><span class="sxs-lookup"><span data-stu-id="f9a52-2123">64 bit</span></span> | <span data-ttu-id="f9a52-2124">Folderid- \_ System</span><span class="sxs-lookup"><span data-stu-id="f9a52-2124">FOLDERID\_System</span></span> | <span data-ttu-id="f9a52-2125">% windir% \\ system32</span><span class="sxs-lookup"><span data-stu-id="f9a52-2125">%windir%\\system32</span></span> | <span data-ttu-id="f9a52-2126">CSIDL- \_ System</span><span class="sxs-lookup"><span data-stu-id="f9a52-2126">CSIDL\_SYSTEM</span></span> |
| <span data-ttu-id="f9a52-2127">64-Bit</span><span class="sxs-lookup"><span data-stu-id="f9a52-2127">64 bit</span></span> | <span data-ttu-id="f9a52-2128">64-Bit</span><span class="sxs-lookup"><span data-stu-id="f9a52-2128">64 bit</span></span> | <span data-ttu-id="f9a52-2129">Folderid \_ SystemX86</span><span class="sxs-lookup"><span data-stu-id="f9a52-2129">FOLDERID\_SystemX86</span></span> | <span data-ttu-id="f9a52-2130">% windir% \\ syswow64</span><span class="sxs-lookup"><span data-stu-id="f9a52-2130">%windir%\\syswow64</span></span> | <span data-ttu-id="f9a52-2131">CSIDL- \_ SYSTEMX86</span><span class="sxs-lookup"><span data-stu-id="f9a52-2131">CSIDL\_SYSTEMX86</span></span> |
| <span data-ttu-id="f9a52-2132">64-Bit</span><span class="sxs-lookup"><span data-stu-id="f9a52-2132">64 bit</span></span> | <span data-ttu-id="f9a52-2133">32-Bit</span><span class="sxs-lookup"><span data-stu-id="f9a52-2133">32 bit</span></span> | <span data-ttu-id="f9a52-2134">Folderid- \_ System</span><span class="sxs-lookup"><span data-stu-id="f9a52-2134">FOLDERID\_System</span></span> | <span data-ttu-id="f9a52-2135">% windir% \\ system32</span><span class="sxs-lookup"><span data-stu-id="f9a52-2135">%windir%\\system32</span></span> | <span data-ttu-id="f9a52-2136">CSIDL- \_ System</span><span class="sxs-lookup"><span data-stu-id="f9a52-2136">CSIDL\_SYSTEM</span></span> |
| <span data-ttu-id="f9a52-2137">64-Bit</span><span class="sxs-lookup"><span data-stu-id="f9a52-2137">64 bit</span></span> | <span data-ttu-id="f9a52-2138">32-Bit</span><span class="sxs-lookup"><span data-stu-id="f9a52-2138">32 bit</span></span> | <span data-ttu-id="f9a52-2139">Folderid \_ SystemX86</span><span class="sxs-lookup"><span data-stu-id="f9a52-2139">FOLDERID\_SystemX86</span></span> | <span data-ttu-id="f9a52-2140">% windir% \\ syswow64</span><span class="sxs-lookup"><span data-stu-id="f9a52-2140">%windir%\\syswow64</span></span> | <span data-ttu-id="f9a52-2141">CSIDL- \_ SYSTEMX86</span><span class="sxs-lookup"><span data-stu-id="f9a52-2141">CSIDL\_SYSTEMX86</span></span> |


<span data-ttu-id="f9a52-2142">Wir haben Umgebungs Zeichenfolgen verwendet, um generische Pfade in diesem Thema bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="f9a52-2142">We have used environment strings to provide generic paths throughout this topic.</span></span> <span data-ttu-id="f9a52-2143">Die folgenden Tabellen stellen Beispiele für die Pfade dar, die diese Umgebungs Zeichenfolgen darstellen.</span><span class="sxs-lookup"><span data-stu-id="f9a52-2143">The following tables give examples of the paths those environment strings represent.</span></span> <span data-ttu-id="f9a52-2144">In einigen Fällen Stimmen diese Pfade möglicherweise nicht mit denen auf einem bestimmten Computer zu, da Sie während der Installation oder einer späteren Ordner Umleitung ausgewählt wurden.</span><span class="sxs-lookup"><span data-stu-id="f9a52-2144">In some cases, these paths might not match those on a particular computer because of choices made during installation or later folder redirection.</span></span> <span data-ttu-id="f9a52-2145">Beachten Sie, dass einige Pfade für Windows Vista geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="f9a52-2145">Note that some paths have changed for Windows Vista.</span></span>


<span data-ttu-id="f9a52-2146">**Windows Vista und höher**</span><span class="sxs-lookup"><span data-stu-id="f9a52-2146">**Windows Vista and later**</span></span>

| <span data-ttu-id="f9a52-2147">Umgebungs Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f9a52-2147">Environment String</span></span> | <span data-ttu-id="f9a52-2148">Beispiel Pfad</span><span class="sxs-lookup"><span data-stu-id="f9a52-2148">Example Path</span></span> |
|--------------------|--------------|
| <span data-ttu-id="f9a52-2149">%ALLUSERSPROFILE%</span><span class="sxs-lookup"><span data-stu-id="f9a52-2149">%ALLUSERSPROFILE%</span></span> | <span data-ttu-id="f9a52-2150">C: \\ programmdata</span><span class="sxs-lookup"><span data-stu-id="f9a52-2150">C:\\ProgramData</span></span> |
| <span data-ttu-id="f9a52-2151">%APPDATA%</span><span class="sxs-lookup"><span data-stu-id="f9a52-2151">%APPDATA%</span></span> | <span data-ttu-id="f9a52-2152">C: \\ Benutzer \\ *Benutzername* \\ AppData \\ Roaming</span><span class="sxs-lookup"><span data-stu-id="f9a52-2152">C:\\Users\\*username*\\AppData\\Roaming</span></span> |
| <span data-ttu-id="f9a52-2153">LocalAppData</span><span class="sxs-lookup"><span data-stu-id="f9a52-2153">%LOCALAPPDATA%</span></span> | <span data-ttu-id="f9a52-2154">C: \\ Benutzer \\ *Benutzername* \\ AppData \\ local</span><span class="sxs-lookup"><span data-stu-id="f9a52-2154">C:\\Users\\*username*\\AppData\\Local</span></span> |
| <span data-ttu-id="f9a52-2155">%ProgramData%</span><span class="sxs-lookup"><span data-stu-id="f9a52-2155">%ProgramData%</span></span> | <span data-ttu-id="f9a52-2156">C: \\ programmdata</span><span class="sxs-lookup"><span data-stu-id="f9a52-2156">C:\\ProgramData</span></span> |
| <span data-ttu-id="f9a52-2157">%ProgramFiles%</span><span class="sxs-lookup"><span data-stu-id="f9a52-2157">%ProgramFiles%</span></span> | <span data-ttu-id="f9a52-2158">C: \\ Programmdateien</span><span class="sxs-lookup"><span data-stu-id="f9a52-2158">C:\\Program Files</span></span> |
| <span data-ttu-id="f9a52-2159">%ProgramFiles(x86)%</span><span class="sxs-lookup"><span data-stu-id="f9a52-2159">%ProgramFiles(x86)%</span></span> | <span data-ttu-id="f9a52-2160">C: \\ Programmdateien (x86)</span><span class="sxs-lookup"><span data-stu-id="f9a52-2160">C:\\Program Files (x86)</span></span> |
| <span data-ttu-id="f9a52-2161">Publikums</span><span class="sxs-lookup"><span data-stu-id="f9a52-2161">%PUBLIC%</span></span> | <span data-ttu-id="f9a52-2162">C: \\ \\ öffentliche Benutzer</span><span class="sxs-lookup"><span data-stu-id="f9a52-2162">C:\\Users\\Public</span></span> |
| <span data-ttu-id="f9a52-2163">%SystemDrive%</span><span class="sxs-lookup"><span data-stu-id="f9a52-2163">%SystemDrive%</span></span> | <span data-ttu-id="f9a52-2164">C:</span><span class="sxs-lookup"><span data-stu-id="f9a52-2164">C:</span></span> |
| <span data-ttu-id="f9a52-2165">%USERPROFILE%</span><span class="sxs-lookup"><span data-stu-id="f9a52-2165">%USERPROFILE%</span></span> | <span data-ttu-id="f9a52-2166">C: \\ Benutzer \\ *Benutzername*</span><span class="sxs-lookup"><span data-stu-id="f9a52-2166">C:\\Users\\*username*</span></span> |
| <span data-ttu-id="f9a52-2167">%windir%</span><span class="sxs-lookup"><span data-stu-id="f9a52-2167">%windir%</span></span> | <span data-ttu-id="f9a52-2168">C: \\ Windows</span><span class="sxs-lookup"><span data-stu-id="f9a52-2168">C:\\Windows</span></span> |


<span data-ttu-id="f9a52-2169">**Windows XP und früher**</span><span class="sxs-lookup"><span data-stu-id="f9a52-2169">**Windows XP and earlier**</span></span>

| <span data-ttu-id="f9a52-2170">Umgebungs Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="f9a52-2170">Environment String</span></span> | <span data-ttu-id="f9a52-2171">Beispiel Pfad</span><span class="sxs-lookup"><span data-stu-id="f9a52-2171">Example Path</span></span> |
|--------------------|--------------|
| <span data-ttu-id="f9a52-2172">%ALLUSERSPROFILE%</span><span class="sxs-lookup"><span data-stu-id="f9a52-2172">%ALLUSERSPROFILE%</span></span> | <span data-ttu-id="f9a52-2173">C: \\ Dokumente und Einstellungen \\ alle Benutzer</span><span class="sxs-lookup"><span data-stu-id="f9a52-2173">C:\\Documents and Settings\\All Users</span></span> |
| <span data-ttu-id="f9a52-2174">%APPDATA%</span><span class="sxs-lookup"><span data-stu-id="f9a52-2174">%APPDATA%</span></span> | <span data-ttu-id="f9a52-2175">C: \\ Dokumente und Einstellungen \\ *Benutzername* \\ Anwendungsdaten</span><span class="sxs-lookup"><span data-stu-id="f9a52-2175">C:\\Documents and Settings\\*username*\\Application Data</span></span> |
| <span data-ttu-id="f9a52-2176">%ProgramFiles%</span><span class="sxs-lookup"><span data-stu-id="f9a52-2176">%ProgramFiles%</span></span> | <span data-ttu-id="f9a52-2177">C: \\ Programmdateien</span><span class="sxs-lookup"><span data-stu-id="f9a52-2177">C:\\Program Files</span></span> |
| <span data-ttu-id="f9a52-2178">%SystemDrive%</span><span class="sxs-lookup"><span data-stu-id="f9a52-2178">%SystemDrive%</span></span> | <span data-ttu-id="f9a52-2179">C:</span><span class="sxs-lookup"><span data-stu-id="f9a52-2179">C:</span></span> |
| <span data-ttu-id="f9a52-2180">%USERPROFILE%</span><span class="sxs-lookup"><span data-stu-id="f9a52-2180">%USERPROFILE%</span></span> | <span data-ttu-id="f9a52-2181">C: \\ \\ *Benutzername* für Dokumente und Einstellungen</span><span class="sxs-lookup"><span data-stu-id="f9a52-2181">C:\\Documents and Settings\\*username*</span></span> |
| <span data-ttu-id="f9a52-2182">%windir%</span><span class="sxs-lookup"><span data-stu-id="f9a52-2182">%windir%</span></span> | <span data-ttu-id="f9a52-2183">C: \\ Windows</span><span class="sxs-lookup"><span data-stu-id="f9a52-2183">C:\\Windows</span></span> |


## <a name="requirements"></a><span data-ttu-id="f9a52-2184">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="f9a52-2184">Requirements</span></span>


| <span data-ttu-id="f9a52-2185">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f9a52-2185">Requirement</span></span> | <span data-ttu-id="f9a52-2186">Wert</span><span class="sxs-lookup"><span data-stu-id="f9a52-2186">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9a52-2187">Header</span><span class="sxs-lookup"><span data-stu-id="f9a52-2187">Header</span></span><br/> | <dl> <span data-ttu-id="f9a52-2188"><dt>KnownFolders. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9a52-2188"><dt>Knownfolders.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9a52-2189">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f9a52-2189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9a52-2190">**CSIDL**</span><span class="sxs-lookup"><span data-stu-id="f9a52-2190">**CSIDL**</span></span>](csidl.md)
</dt> <dt>

[<span data-ttu-id="f9a52-2191">Bekannte Ordner</span><span class="sxs-lookup"><span data-stu-id="f9a52-2191">Known Folders</span></span>](known-folders.md)
</dt> <dt>

[<span data-ttu-id="f9a52-2192">Arbeiten mit bekannten Ordnern in Anwendungen</span><span class="sxs-lookup"><span data-stu-id="f9a52-2192">Working with Known Folders in Applications</span></span>](working-with-known-folders.md)
</dt> <dt>

[<span data-ttu-id="f9a52-2193">Erweitern bekannter Ordner mit benutzerdefinierten Ordnern</span><span class="sxs-lookup"><span data-stu-id="f9a52-2193">How to Extend Known Folders with Custom Folders</span></span>](how-to-extend-known-folders-with-custom-folders.md)
</dt> <dt>

<span data-ttu-id="f9a52-2194">[Bekannte Ordner (Beispiel)](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f9a52-2194">[Known Folders Sample](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))</span></span>
</dt> </dl>

 

 
