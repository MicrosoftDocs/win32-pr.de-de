---
Description: Die KNOWNFOLDERID-Konstanten stellen GUIDs dar, die Standardordner identifizieren, die beim System als Bekannte Ordner registriert sind.
ms.assetid: f2c08ade-3083-44e4-82b0-dde45f0e3094
title: KNOWNFOLDERID (Knownfolders.h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 3d27f8831e4a68b6fb5bb95d7f4a6c34fe361db5
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626376"
---
# <a name="knownfolderid"></a>KNOWNFOLDERID

Die **KNOWNFOLDERID-Konstanten** stellen GUIDs dar, die Standardordner identifizieren, die beim System als Bekannte Ordner registriert [sind.](known-folders.md) Diese Ordner werden mit Windows Vista und späteren Betriebssystemen installiert, und auf einem Computer werden nur Ordner installiert, die für ihn geeignet sind. Beschreibungen dieser Ordner finden Sie unter [**CSIDL**](csidl.md).

## <a name="example"></a>Beispiel

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

Beispiel aus [Windows klassischen Beispielen](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/winui/shell/appplatform/ExplorerBrowserCustomContents/ExplorerBrowserCustomContents.cpp) zu GitHub.

## <a name="constants"></a>Konstanten



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th >Konstante</th>
<th >Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td ><span id="FOLDERID_AccountPictures"></span><span id="folderid_accountpictures"></span><span id="FOLDERID_ACCOUNTPICTURES"></span><dl> <dt><strong>FOLDERID_AccountPictures</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{008ca0b1-55b4-4c56-b8a8-4de4b299d3be}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Kontobilder</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>SOLLSER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%APPDATA%\Microsoft\Windows\AccountPictures</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows 8 eingeführter Wert</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacystandardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_AddNewPrograms"></span><span id="folderid_addnewprograms"></span><span id="FOLDERID_ADDNEWPROGRAMS"></span><dl> <dt><strong>FOLDERID_AddNewPrograms</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{de61d971-5ebc-4f02-a3a9-6c82895e5c04}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Abrufen von Programmen</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>VIRTUELLEN</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>Nicht zutreffend – virtueller Ordner</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>Keine</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Neue Programme hinzufügen (finden Sie im Systemsteuerung im Element <strong>Programme hinzufügen oder entfernen)</strong></td>
</tr>
<tr class="odd">
<td>Legacystandardpfad</td>
<td>Nicht zutreffend – virtueller Ordner</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_AdminTools"></span><span id="folderid_admintools"></span><span id="FOLDERID_ADMINTOOLS"></span><dl> <dt><strong>FOLDERID_AdminTools</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{724EF170-A42D-4FEF-9F26-B60E846FBA4F}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Verwaltung</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>SOLLSER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%APPDATA%\Microsoft\Windows\Startmenü\Programme\Verwaltungstools</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_ADMINTOOLS</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Verwaltung</td>
</tr>
<tr class="odd">
<td>Legacystandardpfad</td>
<td>%USERPROFILE%\Startmenü\Programme\Administrative Tools</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_AppDataDesktop"></span><span id="folderid_appdatadesktop"></span><span id="FOLDERID_APPDATADESKTOP"></span><dl> <dt><strong>FOLDERID_AppDataDesktop</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{B2C5E279-7ADD-439F-B28C-C41FE1BBF672}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>AppDataDesktop</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>SOLLSER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%LOCALAPPDATA%\Desktop</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows 10, Version 1709 eingeführter Wert</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacystandardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p>
<p>Diese FOLDERID wird intern von .NET-Anwendungen verwendet, um plattformübergreifende App-Funktionen zu ermöglichen. Sie ist nicht für die direkte Verwendung aus einer Anwendung vorgesehen.</p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_AppDataDocuments"></span><span id="folderid_appdatadocuments"></span><span id="FOLDERID_APPDATADOCUMENTS"></span><dl> <dt><strong>FOLDERID_AppDataDocuments</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{7BE16610-1F7F-44AC-BFF0-83E15F2FFCA1}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>AppDataDocuments</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>SOLLSER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%LOCALAPPDATA%\Documents</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows 10, Version 1709 eingeführter Wert</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacystandardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p>
<p>Diese FOLDERID wird intern von .NET-Anwendungen verwendet, um plattformübergreifende App-Funktionen zu ermöglichen. Sie ist nicht für die direkte Verwendung aus einer Anwendung vorgesehen.</p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_AppDataFavorites"></span><span id="folderid_appdatafavorites"></span><span id="FOLDERID_APPDATAFAVORITES"></span><dl> <dt><strong>FOLDERID_AppDataFavorites</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{7CFBEFBC-DE1F-45AA-B843-A542AC536CC9}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>AppDataFavorites</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>SOLLSER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%LOCALAPPDATA%\Favoriten</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, value introduced in Windows 10, Version 1709</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p>
<p>Diese FOLDERID wird intern von .NET-Anwendungen verwendet, um plattformübergreifende App-Funktionen zu aktivieren. Sie ist nicht für die direkte Verwendung aus einer Anwendung vorgesehen.</p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_AppDataProgramData"></span><span id="folderid_appdataprogramdata"></span><span id="FOLDERID_APPDATAPROGRAMDATA"></span><dl> <dt><strong>FOLDERID_AppDataProgramData</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{559D40A3-A036-40FA-AF61-84CB430A4D34}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>AppDataProgramData</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>BESER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%LOCALAPPDATA%\ProgramData</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, value introduced in Windows 10, Version 1709</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p>
<p>Diese FOLDERID wird intern von .NET-Anwendungen verwendet, um plattformübergreifende App-Funktionen zu aktivieren. Sie ist nicht für die direkte Verwendung aus einer Anwendung vorgesehen.</p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_ApplicationShortcuts"></span><span id="folderid_applicationshortcuts"></span><span id="FOLDERID_APPLICATIONSHORTCUTS"></span><dl> <dt><strong>FOLDERID_ApplicationShortcuts</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{A3918781-E5F2-4890-B3D9-A7E54332328C}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Anwendungsverknüpfungen</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>BESER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%LOCALAPPDATA%\Microsoft\Windows\Anwendungsverknüpfungen</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, value introduced in Windows 8</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_AppsFolder"></span><span id="folderid_appsfolder"></span><span id="FOLDERID_APPSFOLDER"></span><dl> <dt><strong>FOLDERID_AppsFolder</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{1e87508d-89c2-42f0-8a7e-645a0f50ca58}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Applications</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>VIRTUELLEN</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>Nicht zutreffend – virtueller Ordner</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, value introduced in Windows 8</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_AppUpdates"></span><span id="folderid_appupdates"></span><span id="FOLDERID_APPUPDATES"></span><dl> <dt><strong>FOLDERID_AppUpdates</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{a305ce99-f527-492b-8b1a-7e76fa98d6e4}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Installierte Updates</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>VIRTUELLEN</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>Nicht zutreffend – virtueller Ordner</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>Keine</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>None, value introduced in Windows Vista. In früheren Versionen von Windows die Informationen auf dieser Seite <strong>im</strong> Feld <strong></strong> Programme hinzufügen oder entfernen enthalten, wenn das Kontrollkästchen Updates anzeigen aktivieren war.</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_CameraRoll"></span><span id="folderid_cameraroll"></span><span id="FOLDERID_CAMERAROLL"></span><dl> <dt><strong>FOLDERID_CameraRoll</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{AB5FB87B-7CE2-4F83-915D-550846C9537B}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Kameraroll</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>BESER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%USERPROFILE%\Pictures\Camera Roll</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, value introduced in Windows 8.1</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_CDBurning"></span><span id="folderid_cdburning"></span><span id="FOLDERID_CDBURNING"></span><dl> <dt><strong>FOLDERID_CDBurning</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{9E52AB10-F80D-49DF-ACB8-4330F5687855}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Temporärer Burn-Ordner</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>BESER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%LOCALAPPDATA%\Microsoft\Windows\Burn\Burn</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_CDBURN_AREA</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>CD-2016</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>%USERPROFILE%\Local Einstellungen\Application Data\Microsoft\CD</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_ChangeRemovePrograms"></span><span id="folderid_changeremoveprograms"></span><span id="FOLDERID_CHANGEREMOVEPROGRAMS"></span><dl> <dt><strong>FOLDERID_ChangeRemovePrograms</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{df7266ac-9274-4867-8d55-3bd661de872d}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Programme und Features</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>VIRTUELLEN</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>Nicht zutreffend – virtueller Ordner</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>Keine</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Software</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>Nicht zutreffend – virtueller Ordner</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_CommonAdminTools"></span><span id="folderid_commonadmintools"></span><span id="FOLDERID_COMMONADMINTOOLS"></span><dl> <dt><strong>FOLDERID_CommonAdminTools</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{D0384E7D-BAC3-4797-8F14-CBA229B392B5}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Verwaltung</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>GEMEINSAM</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%ALLUSERSPROFILE%\Microsoft\Windows\Startmenü\Programme\Verwaltung</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_COMMON_ADMINTOOLS</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Verwaltung</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>%ALLUSERSPROFILE%\Start menu\Programs\Administrative Tools</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_CommonOEMLinks"></span><span id="folderid_commonoemlinks"></span><span id="FOLDERID_COMMONOEMLINKS"></span><dl> <dt><strong>FOLDERID_CommonOEMLinks</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{C1BAE2D0-10DF-4334-BEDD-7AA20B227A9D}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>OEM-Links</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>GEMEINSAM</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%ALLUSERSPROFILE%\OEM-Links</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_COMMON_OEM_LINKS</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>OEM-Links</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>%ALLUSERSPROFILE%\OEM-Links</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_CommonPrograms"></span><span id="folderid_commonprograms"></span><span id="FOLDERID_COMMONPROGRAMS"></span><dl> <dt><strong>FOLDERID_CommonPrograms</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{0139D44E-6AFE-49F2-8690-3DAFCAE6FFB8}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Programme</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>GEMEINSAM</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%ALLUSERSPROFILE%\Microsoft\Windows\Startmenü\Programme</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_COMMON_PROGRAMS</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Programme</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>%ALLUSERSPROFILE%\Start menu\Programs</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_CommonStartMenu"></span><span id="folderid_commonstartmenu"></span><span id="FOLDERID_COMMONSTARTMENU"></span><dl> <dt><strong>FOLDERID_CommonStartMenu</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{A4115719-D62E-491D-AA7C-E74B8BE3B067}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Startmenü</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>GEMEINSAM</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%ALLUSERSPROFILE%\Microsoft\Windows\Startmenü</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_COMMON_STARTMENU</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Startmenü</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>%ALLUSERSPROFILE%\Startmenü</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_CommonStartup"></span><span id="folderid_commonstartup"></span><span id="FOLDERID_COMMONSTARTUP"></span><dl> <dt><strong>FOLDERID_CommonStartup</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{82A5EA35-D9CD-47C5-9629-E15D2F714E6E}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Start</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>GEMEINSAM</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%ALLUSERSPROFILE%\Microsoft\Windows\Startmenü\Programme\StartUp</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_COMMON_STARTUP, CSIDL_COMMON_ALTSTARTUP</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Start</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>%ALLUSERSPROFILE%\Start menu\Programs\StartUp</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_CommonTemplates"></span><span id="folderid_commontemplates"></span><span id="FOLDERID_COMMONTEMPLATES"></span><dl> <dt><strong>FOLDERID_CommonTemplates</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{B94237E7-57AC-4347-9151-B08C6C32D1F7}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Vorlagen</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>GEMEINSAM</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%ALLUSERSPROFILE%\Microsoft\Windows\Templates</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_COMMON_TEMPLATES</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Vorlagen</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>%ALLUSERSPROFILE%\Templates</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_ComputerFolder"></span><span id="folderid_computerfolder"></span><span id="FOLDERID_COMPUTERFOLDER"></span><dl> <dt><strong>FOLDERID_ComputerFolder</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{0AC0837C-BBF8-452A-850D-79D08E667CA7}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Computer</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>VIRTUELLEN</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>Nicht zutreffend – virtueller Ordner</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_DRIVES</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Arbeitsplatz</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>Nicht zutreffend – virtueller Ordner</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_ConflictFolder"></span><span id="folderid_conflictfolder"></span><span id="FOLDERID_CONFLICTFOLDER"></span><dl> <dt><strong>FOLDERID_ConflictFolder</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{4bfefb45-347d-4006-a5be-ac0cb0567192}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Konflikte</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>VIRTUELLEN</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>Nicht zutreffend – virtueller Ordner</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, value introduced in Windows Vista</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend Diese <strong>KNOWNFOLDERID</strong> bezieht sich auf den Windows Vista Synchronization Manager. Es handelt sich nicht um den Ordner, auf den der ältere <a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictfolder"><strong>ISyncMgrConflictFolder verweist.</strong></a></td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_ConnectionsFolder"></span><span id="folderid_connectionsfolder"></span><span id="FOLDERID_CONNECTIONSFOLDER"></span><dl> <dt><strong>FOLDERID_ConnectionsFolder</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{6F0CD92B-2E97-45D1-88FF-B0D186B8DEDD}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Netzwerkverbindungen</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>VIRTUELLEN</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>Nicht zutreffend – virtueller Ordner</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_CONNECTIONS</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Netzwerkverbindungen</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>Nicht zutreffend – virtueller Ordner</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_Contacts"></span><span id="folderid_contacts"></span><span id="FOLDERID_CONTACTS"></span><dl> <dt><strong>FOLDERID_Contacts</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{56784854-C6CB-462b-8169-88E350ACB882}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Kontakte</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>BESER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%USERPROFILE%\Contacts</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, value introduced in Windows Vista</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_ControlPanelFolder"></span><span id="folderid_controlpanelfolder"></span><span id="FOLDERID_CONTROLPANELFOLDER"></span><dl> <dt><strong>FOLDERID_ControlPanelFolder</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{82A74AEB-AEB4-465C-A014-D097EE346D63}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Systemsteuerung</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>VIRTUELLEN</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>Nicht zutreffend – virtueller Ordner</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_CONTROLS</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Systemsteuerung</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>Nicht zutreffend – virtueller Ordner</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_Cookies"></span><span id="folderid_cookies"></span><span id="FOLDERID_COOKIES"></span><dl> <dt><strong>FOLDERID_Cookies</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{2B0F765D-C0E9-4171-908E-08A611B84FF6}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Cookies</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>BESER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%APPDATA%\Microsoft\Windows\Cookies</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_COOKIES</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Cookies</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>%USERPROFILE%\Cookies</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_Desktop"></span><span id="folderid_desktop"></span><span id="FOLDERID_DESKTOP"></span><dl> <dt><strong>FOLDERID_Desktop</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{B4BFCC3A-DB2C-424C-B029-7FE99A87C641}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Desktop</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>BESER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%USERPROFILE%\Desktop</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_DESKTOP, CSIDL_DESKTOPDIRECTORY</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Desktop</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>%USERPROFILE%\Desktop</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_DeviceMetadataStore"></span><span id="folderid_devicemetadatastore"></span><span id="FOLDERID_DEVICEMETADATASTORE"></span><dl> <dt><strong>FOLDERID_DeviceMetadataStore</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{5CE4A5E9-E4EB-479D-B89F-130C02886155}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>DeviceMetadataStore</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>GEMEINSAM</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%ALLUSERSPROFILE%\Microsoft\Windows\DeviceMetadataStore</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, value introduced in Windows 7</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_Documents"></span><span id="folderid_documents"></span><span id="FOLDERID_DOCUMENTS"></span><dl> <dt><strong>FOLDERID_Documents</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{FDD39AD0-238F-46AF-ADB4-6C85480369C7}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Dokumente</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>BESER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%USERPROFILE%\Documents</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechungen</td>
<td>CSIDL_MYDOCUMENTS, CSIDL_PERSONAL</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Meine Dokumente</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>%USERPROFILE%\Eigene Dokumente</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_DocumentsLibrary"></span><span id="folderid_documentslibrary"></span><span id="FOLDERID_DOCUMENTSLIBRARY"></span><dl> <dt><strong>FOLDERID_DocumentsLibrary</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{7B0DB17D-9CD2-4A93-9733-46CC89022E7C}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Dokumente</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>BESER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%APPDATA%\Microsoft\Windows\Libraries\Documents.library-ms</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, value introduced in Windows 7</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_Downloads"></span><span id="folderid_downloads"></span><span id="FOLDERID_DOWNLOADS"></span><dl> <dt><strong>FOLDERID_Downloads</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{374DE290-123F-4565-9164-39C4925E467B}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Downloads</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>BESER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%USERPROFILE%\Downloads</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>Keine</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_Favorites"></span><span id="folderid_favorites"></span><span id="FOLDERID_FAVORITES"></span><dl> <dt><strong>FOLDERID_Favorites</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{1777F761-68AD-4D8A-87BD-30B759FA33DD}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Favoriten</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>BESER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%USERPROFILE%\Favoriten</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_FAVORITES, CSIDL_COMMON_FAVORITES</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Favoriten</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>%USERPROFILE%\Favoriten</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_Fonts"></span><span id="folderid_fonts"></span><span id="FOLDERID_FONTS"></span><dl> <dt><strong>FOLDERID_Fonts</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{FD228CB7-AE11-4AE3-864C-16F3910AB8FE}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Schriftarten</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>FIXED</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%windir%\Schriftarten</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_FONTS</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Schriftarten</td>
</tr>
<tr class="odd">
<td>Legacystandardpfad</td>
<td>%windir%\Fonts</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_Games"></span><span id="folderid_games"></span><span id="FOLDERID_GAMES"></span><dl> <dt><strong>FOLDERID_Games</strong></dt> </dl></td>
<td ><div class="alert">
<blockquote>
[!Note]<br />
Diese FOLDERID ist in Windows 10, Version 1803 und höher, veraltet. In diesen Versionen wird 0x80070057 zurückgegeben– <strong>E_INVALIDARG</strong>
</blockquote>
</div>
<div>
 
</div>

<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{CAC52C1A-B53D-4edc-92D7-6B2E8AC19434}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Spiele</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>VIRTUELLEN</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>Nicht zutreffend – virtueller Ordner</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>Keine</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacystandardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_GameTasks"></span><span id="folderid_gametasks"></span><span id="FOLDERID_GAMETASKS"></span><dl> <dt><strong>FOLDERID_GameTasks</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{054FAE61-4DD8-4787-80B6-090220C4B700}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>GameExplorer</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>SOLLSER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%LOCALAPPDATA%\Microsoft\Windows\GameExplorer</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows Vista eingeführter Wert</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacystandardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_History"></span><span id="folderid_history"></span><span id="FOLDERID_HISTORY"></span><dl> <dt><strong>FOLDERID_History</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{D9DC8A3B-B784-432E-A781-5A1130A75963}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Verlauf</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>SOLLSER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%LOCALAPPDATA%\Microsoft\Windows\History</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_HISTORY</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Verlauf</td>
</tr>
<tr class="odd">
<td>Legacystandardpfad</td>
<td>%USERPROFILE%\Local Einstellungen\History</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_HomeGroup"></span><span id="folderid_homegroup"></span><span id="FOLDERID_HOMEGROUP"></span><dl> <dt><strong>FOLDERID_HomeGroup</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{52528A6B-B9E3-4ADD-B60D-588C2DBA842D}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Heimnetzgruppe</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>VIRTUELLEN</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>Nicht zutreffend – virtueller Ordner</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows 7 eingeführter Wert</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacystandardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_HomeGroupCurrentUser"></span><span id="folderid_homegroupcurrentuser"></span><span id="FOLDERID_HOMEGROUPCURRENTUSER"></span><dl> <dt><strong>FOLDERID_HomeGroupCurrentUser</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{9B74B6A3-0DFD-4f11-9E78-5F7800F2E772}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Der Benutzername des Benutzers (%USERNAME%)</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>VIRTUELLEN</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>Nicht zutreffend – virtueller Ordner</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows 8 eingeführter Wert</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacystandardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_ImplicitAppShortcuts"></span><span id="folderid_implicitappshortcuts"></span><span id="FOLDERID_IMPLICITAPPSHORTCUTS"></span><dl> <dt><strong>FOLDERID_ImplicitAppShortcuts</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{BCB5256F-79F6-4CEE-B725-DC34E402FD46}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>ImplicitAppShortcuts</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>SOLLSER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%APPDATA%\Microsoft\Internet Explorer\Schnellstart\User Pinned\ImplicitAppShortcuts</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows 7 eingeführter Wert</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacystandardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_InternetCache"></span><span id="folderid_internetcache"></span><span id="FOLDERID_INTERNETCACHE"></span><dl> <dt><strong>FOLDERID_InternetCache</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{352481E8-33BE-4251-BA85-6007CAEDCF9D}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Temporäre Internetdateien</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>SOLLSER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%LOCALAPPDATA%\Microsoft\Windows\Temporary Internet Files</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_INTERNET_CACHE</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Temporäre Internetdateien</td>
</tr>
<tr class="odd">
<td>Legacystandardpfad</td>
<td>%USERPROFILE%\Local Einstellungen\Temporary Internet Files</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_InternetFolder"></span><span id="folderid_internetfolder"></span><span id="FOLDERID_INTERNETFOLDER"></span><dl> <dt><strong>FOLDERID_InternetFolder</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{4D9F7874-4E0C-4904-967B-40B0D20C3E4B}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Das Internet</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>VIRTUELLEN</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>Nicht zutreffend – virtueller Ordner</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_INTERNET</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Internet Explorer</td>
</tr>
<tr class="odd">
<td>Legacystandardpfad</td>
<td>Nicht zutreffend – virtueller Ordner</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_Libraries"></span><span id="folderid_libraries"></span><span id="FOLDERID_LIBRARIES"></span><dl> <dt><strong>FOLDERID_Libraries</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{1B3EA5DC-B587-4786-B4EF-BD1DC332AEAE}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Bibliotheken</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>SOLLSER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%APPDATA%\Microsoft\Windows\Libraries</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows 7 eingeführter Wert</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacystandardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_Links"></span><span id="folderid_links"></span><span id="FOLDERID_LINKS"></span><dl> <dt><strong>FOLDERID_Links</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{bfb9d5e0-c6a9-404c-b2b2-ae6db6af4968}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Links</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>SOLLSER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%USERPROFILE%\Links</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>Keine</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacystandardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_LocalAppData"></span><span id="folderid_localappdata"></span><span id="FOLDERID_LOCALAPPDATA"></span><dl> <dt><strong>FOLDERID_LocalAppData</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{F1B32785-6FBA-4FCF-9D55-7B8E7F157091}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Lokales Gerät</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>SOLLSER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%LOCALAPPDATA% (%USERPROFILE%\AppData\Local)</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_LOCAL_APPDATA</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Anwendungsdaten</td>
</tr>
<tr class="odd">
<td>Legacystandardpfad</td>
<td>%USERPROFILE%\Local Einstellungen\Application Data</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_LocalAppDataLow"></span><span id="folderid_localappdatalow"></span><span id="FOLDERID_LOCALAPPDATALOW"></span><dl> <dt><strong>FOLDERID_LocalAppDataLow</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{A520A1A4-1780-4FF6-BD18-167343C5AF16}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>LocalLow</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>SOLLSER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%USERPROFILE%\AppData\LocalLow</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>Keine</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacystandardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_LocalizedResourcesDir"></span><span id="folderid_localizedresourcesdir"></span><span id="FOLDERID_LOCALIZEDRESOURCESDIR"></span><dl> <dt><strong>FOLDERID_LocalizedResourcesDir</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{2A00375E-224C-49DE-B8D1-440DF7EF3DDC}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Keine</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>FIXED</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%windir%\resources\0409 (Codepage)</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_RESOURCES_LOCALIZED</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Keine</td>
</tr>
<tr class="odd">
<td>Legacystandardpfad</td>
<td>%windir%\resources\0409 (Codepage)</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_Music"></span><span id="folderid_music"></span><span id="FOLDERID_MUSIC"></span><dl> <dt><strong>FOLDERID_Music</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{4BD8D571-6D19-48D3-BE97-422220080E43}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Musik</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>SOLLSER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%USERPROFILE%\Musik</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_MYMUSIC</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Eigene Musik</td>
</tr>
<tr class="odd">
<td>Legacystandardpfad</td>
<td>%USERPROFILE%\Eigene Dokumente\My Musik</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_MusicLibrary"></span><span id="folderid_musiclibrary"></span><span id="FOLDERID_MUSICLIBRARY"></span><dl> <dt><strong>FOLDERID_MusicLibrary</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{2112AB0A-C86A-4FFE-A368-0DE96E47012E}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Musik</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>SOLLSER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%APPDATA%\Microsoft\Windows\Libraries\Musik.library-ms</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows 7 eingeführter Wert</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacystandardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_NetHood"></span><span id="folderid_nethood"></span><span id="FOLDERID_NETHOOD"></span><dl> <dt><strong>FOLDERID_NetHood</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{C5ABBF53-E17F-4121-8900-86626FC2C973}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Netzwerkverknüpfungen</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>SOLLSER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%APPDATA%\Microsoft\Windows\Netzwerkverknüpfungen</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_NETHOOD</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>NetHood</td>
</tr>
<tr class="odd">
<td>Legacystandardpfad</td>
<td>%USERPROFILE%\NetHood</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_NetworkFolder"></span><span id="folderid_networkfolder"></span><span id="FOLDERID_NETWORKFOLDER"></span><dl> <dt><strong>FOLDERID_NetworkFolder</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{D20BEEC4-5CA8-4905-AE3B-BF251EA09B53}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Netzwerk</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>VIRTUELLEN</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>Nicht zutreffend – virtueller Ordner</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_NETWORK, CSIDL_COMPUTERSNEARME</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Meine Netzwerkorte</td>
</tr>
<tr class="odd">
<td>Legacystandardpfad</td>
<td>Nicht zutreffend – virtueller Ordner</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_Objects3D"></span><span id="folderid_objects3d"></span><span id="FOLDERID_OBJECTS3D"></span><dl> <dt><strong>FOLDERID_Objects3D</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{31C0DD25-9439-4F12-BF41-7FF4EDA38722}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>3D-Objekte</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>SOLLSER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%USERPROFILE%\3D-Objekte</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows 10, Version 1703 eingeführter Wert</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacystandardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_OriginalImages"></span><span id="folderid_originalimages"></span><span id="FOLDERID_ORIGINALIMAGES"></span><dl> <dt><strong>FOLDERID_OriginalImages</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{2C36C0AA-5812-4b87-BFD0-4CD0DFB19B39}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Originalbilder</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>SOLLSER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%LOCALAPPDATA%\Microsoft\Windows Fotogalerie\Originalimages</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows Vista eingeführter Wert</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacystandardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_PhotoAlbums"></span><span id="folderid_photoalbums"></span><span id="FOLDERID_PHOTOALBUMS"></span><dl> <dt><strong>FOLDERID_PhotoAlbums</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{69D2CF90-FC33-4FB7-9A0C-EBB0F0FCB43C}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Diashows</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>SOLLSER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%USERPROFILE%\Pictures\Slide Shows</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows Vista eingeführter Wert</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_PicturesLibrary"></span><span id="folderid_pictureslibrary"></span><span id="FOLDERID_PICTURESLIBRARY"></span><dl> <dt><strong>FOLDERID_PicturesLibrary</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{A990AE9F-A03B-4E80-94BC-9912D7504104}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Bilder</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>BESER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%APPDATA%\Microsoft\Windows\Libraries\Pictures.library-ms</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, value introduced in Windows 7</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_Pictures"></span><span id="folderid_pictures"></span><span id="FOLDERID_PICTURES"></span><dl> <dt><strong>FOLDERID_Pictures</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{33E28130-4E1E-4676-835A-98395C3BC3BB}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Bilder</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>BESER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%USERPROFILE%\Pictures</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_MYPICTURES</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Eigene Bilder</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>%USERPROFILE%\Eigene Dokumente\Meine Bilder</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_Playlists"></span><span id="folderid_playlists"></span><span id="FOLDERID_PLAYLISTS"></span><dl> <dt><strong>FOLDERID_Playlists</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{DE92C1C7-837F-4F69-A3BB-86E631204A23}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Wiedergabelisten</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>BESER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%USERPROFILE%\Musik\Playlists</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>Keine</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_PrintersFolder"></span><span id="folderid_printersfolder"></span><span id="FOLDERID_PRINTERSFOLDER"></span><dl> <dt><strong>FOLDERID_PrintersFolder</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{76FC4E2D-D6AD-4519-A663-37BD56068185}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Drucker</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>VIRTUELLEN</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>Nicht zutreffend – virtueller Ordner</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_PRINTERS</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Drucker und Faxe</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>Nicht zutreffend – virtueller Ordner</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_PrintHood"></span><span id="folderid_printhood"></span><span id="FOLDERID_PRINTHOOD"></span><dl> <dt><strong>FOLDERID_PrintHood</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{9274BD8D-CFD1-41C3-B35E-B13F55A758F4}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Druckerverknüpfungen</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>BESER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%APPDATA%\Microsoft\Windows\Druckerverknüpfungen</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_PRINTHOOD</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>PrintHood</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>%USERPROFILE%\PrintHood</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_Profile"></span><span id="folderid_profile"></span><span id="FOLDERID_PROFILE"></span><dl> <dt><strong>FOLDERID_Profile</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{5E6C858F-0E22-4760-9AFE-EA3317B67173}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Benutzername des Benutzers (%USERNAME%)</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>FIXED</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%USERPROFILE% (%SystemDrive%\BenutzerBENUTZERBENUTZERNAME%) \%</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_PROFILE</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Benutzername des Benutzers (%USERNAME%)</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>%USERPROFILE% (%SystemDrive%\Documents und Einstellungen \% USERNAME%)</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_ProgramData"></span><span id="folderid_programdata"></span><span id="FOLDERID_PROGRAMDATA"></span><dl> <dt><strong>FOLDERID_ProgramData</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{62AB5D82-FDC1-4DC3-A9DD-070D1D495D97}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>ProgramData</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>FIXED</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%ALLUSERSPROFILE% (%ProgramData%, %SystemDrive%\ProgramData)</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_COMMON_APPDATA</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Anwendungsdaten</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>%ALLUSERSPROFILE%\Anwendungsdaten</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_ProgramFiles"></span><span id="folderid_programfiles"></span><span id="FOLDERID_PROGRAMFILES"></span><dl> <dt><strong>FOLDERID_ProgramFiles</strong></dt> </dl></td>
<td ><p>Weitere Informationen finden Sie unter Hinweise.</p>

<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{905e63b6-c1bf-494e-b29c-65b732d3d21a}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Programme</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>FIXED</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%ProgramFiles% (%SystemDrive%\Programme)</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_PROGRAM_FILES</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Programme</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>%ProgramFiles% (%SystemDrive%\Programme)</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_ProgramFilesX64"></span><span id="folderid_programfilesx64"></span><span id="FOLDERID_PROGRAMFILESX64"></span><dl> <dt><strong>FOLDERID_ProgramFilesX64</strong></dt> </dl></td>
<td ><p>Dieser Wert wird unter 32-Bit-Betriebssystemen nicht unterstützt. Es wird auch nicht für 32-Bit-Anwendungen unterstützt, die unter 64-Bit-Betriebssystemen ausgeführt werden. Der Versuch, FOLDERID_ProgramFilesX64 in beiden Situation zu verwenden, führt zu einem Fehler. Weitere Informationen finden Sie unter Hinweise.</p>

<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{6D809377-6AF0-444b-8957-A3773F02200E}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Programme</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>FIXED</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%ProgramFiles% (%SystemDrive%\Programme)</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>Keine</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Programme</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>%ProgramFiles% (%SystemDrive%\Programme)</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_ProgramFilesX86"></span><span id="folderid_programfilesx86"></span><span id="FOLDERID_PROGRAMFILESX86"></span><dl> <dt><strong>FOLDERID_ProgramFilesX86</strong></dt> </dl></td>
<td ><p>Weitere Informationen finden Sie unter Hinweise.</p>

<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{7C5A40EF-A0FB-4BFC-874A-C0F2E0B9FA8E}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Programme</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>FIXED</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%ProgramFiles% (%SystemDrive%\Programme)</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_PROGRAM_FILESX86</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Programme</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>%ProgramFiles% (%SystemDrive%\Programme)</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_ProgramFilesCommon"></span><span id="folderid_programfilescommon"></span><span id="FOLDERID_PROGRAMFILESCOMMON"></span><dl> <dt><strong>FOLDERID_ProgramFilesCommon</strong></dt> </dl></td>
<td ><p>Weitere Informationen finden Sie unter Hinweise.</p>

<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{F7F1ED05-9F6D-47A2-AAAE-29D317C6F066}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Allgemeine Dateien</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>FIXED</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%ProgramFiles%\Common Files</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_PROGRAM_FILES_COMMON</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Allgemeine Dateien</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>%ProgramFiles%\Common Files</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_ProgramFilesCommonX64"></span><span id="folderid_programfilescommonx64"></span><span id="FOLDERID_PROGRAMFILESCOMMONX64"></span><dl> <dt><strong>FOLDERID_ProgramFilesCommonX64</strong></dt> </dl></td>
<td ><p>Weitere Informationen finden Sie unter Hinweise.</p>

<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{6365D5A7-0F0D-45E5-87F6-0DA56B6A4F7D}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Allgemeine Dateien</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>FIXED</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%ProgramFiles%\Common Files</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>Keine</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Allgemeine Dateien</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>%ProgramFiles%\Common Files</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_ProgramFilesCommonX86"></span><span id="folderid_programfilescommonx86"></span><span id="FOLDERID_PROGRAMFILESCOMMONX86"></span><dl> <dt><strong>FOLDERID_ProgramFilesCommonX86</strong></dt> </dl></td>
<td ><p>Weitere Informationen finden Sie unter Hinweise.</p>

<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{DE974D24-D9C6-4D3E-BF91-F4455120B917}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Allgemeine Dateien</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>FIXED</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%ProgramFiles%\Common Files</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_PROGRAM_FILES_COMMONX86</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Allgemeine Dateien</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>%ProgramFiles%\Common Files</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_Programs"></span><span id="folderid_programs"></span><span id="FOLDERID_PROGRAMS"></span><dl> <dt><strong>FOLDERID_Programs</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{A77F5D77-2E2B-44C3-A6A2-ABA601054A51}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Programme</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>BESER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%APPDATA%\Microsoft\Windows\Startmenü\Programme</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_PROGRAMS</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Programme</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>%USERPROFILE%\Startmenü\Programme</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_Public"></span><span id="folderid_public"></span><span id="FOLDERID_PUBLIC"></span><dl> <dt><strong>FOLDERID_Public</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{DFDF76A2-C82A-4D63-906A-5644AC457385}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Öffentlich</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>FIXED</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%PUBLIC% (%SystemDrive%\Users\Public)</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>Keine, neu für Windows Vista</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_PublicDesktop"></span><span id="folderid_publicdesktop"></span><span id="FOLDERID_PUBLICDESKTOP"></span><dl> <dt><strong>FOLDERID_PublicDesktop</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{C4AA340D-F20F-4863-AFEF-F87EF2E6BA25}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Öffentlicher Desktop</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>GEMEINSAM</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%PUBLIC%\Desktop</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_COMMON_DESKTOPDIRECTORY</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Desktop</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>%ALLUSERSPROFILE%\Desktop</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_PublicDocuments"></span><span id="folderid_publicdocuments"></span><span id="FOLDERID_PUBLICDOCUMENTS"></span><dl> <dt><strong>FOLDERID_PublicDocuments</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{ED4824AF-DCE4-45A8-81E2-FC7965083634}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Öffentliche Dokumente</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>GEMEINSAM</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%PUBLIC%\Documents</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_COMMON_DOCUMENTS</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Freigegebene Dokumente</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>%ALLUSERSPROFILE%\Documents</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_PublicDownloads"></span><span id="folderid_publicdownloads"></span><span id="FOLDERID_PUBLICDOWNLOADS"></span><dl> <dt><strong>FOLDERID_PublicDownloads</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{3D644C9B-1FB8-4f30-9B45-F670235F79C0}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Öffentliche Downloads</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>GEMEINSAM</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%PUBLIC%\Downloads</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, value introduced in Windows Vista</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_PublicGameTasks"></span><span id="folderid_publicgametasks"></span><span id="FOLDERID_PUBLICGAMETASKS"></span><dl> <dt><strong>FOLDERID_PublicGameTasks</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{DEBF2536-E1A8-4c59-B6A2-414586476AEA}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>GameExplorer</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>GEMEINSAM</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%ALLUSERSPROFILE%\Microsoft\Windows\GameExplorer</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, value introduced in Windows Vista</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_PublicLibraries"></span><span id="folderid_publiclibraries"></span><span id="FOLDERID_PUBLICLIBRARIES"></span><dl> <dt><strong>FOLDERID_PublicLibraries</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{48DAF80B-E6CF-4F4E-B800-0E69D84EE384}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Bibliotheken</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>GEMEINSAM</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%ALLUSERSPROFILE%\Microsoft\Windows\Libraries</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows 7 eingeführter Wert</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacystandardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_PublicMusic"></span><span id="folderid_publicmusic"></span><span id="FOLDERID_PUBLICMUSIC"></span><dl> <dt><strong>FOLDERID_PublicMusic</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{3214FAB5-9757-4298-BB61-92A9DEAA44FF}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Öffentliche Musik</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>GEMEINSAM</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%PUBLIC%\Musik</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_COMMON_MUSIC</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Freigegebene Musik</td>
</tr>
<tr class="odd">
<td>Legacystandardpfad</td>
<td>%ALLUSERSPROFILE%\Documents\My Musik</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_PublicPictures"></span><span id="folderid_publicpictures"></span><span id="FOLDERID_PUBLICPICTURES"></span><dl> <dt><strong>FOLDERID_PublicPictures</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{B6EBFB86-6907-413C-9AF7-4FC2ABF07CC5}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Öffentliche Bilder</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>GEMEINSAM</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%PUBLIC%\Pictures</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_COMMON_PICTURES</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Freigegebene Bilder</td>
</tr>
<tr class="odd">
<td>Legacystandardpfad</td>
<td>%ALLUSERSPROFILE%\Documents\My Pictures</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_PublicRingtones"></span><span id="folderid_publicringtones"></span><span id="FOLDERID_PUBLICRINGTONES"></span><dl> <dt><strong>FOLDERID_PublicRingtones</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{E555AB60-153B-4D17-9F04-A5FE99FC15EC}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Klingeltöne</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>GEMEINSAM</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%ALLUSERSPROFILE%\Microsoft\Windows\Ringtones</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows 7 eingeführter Wert</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacystandardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_PublicUserTiles"></span><span id="folderid_publicusertiles"></span><span id="FOLDERID_PUBLICUSERTILES"></span><dl> <dt><strong>FOLDERID_PublicUserTiles</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{0482af6c-08f1-4c34-8c90-e17ec98b1e17}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Bilder für öffentliche Konten</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>GEMEINSAM</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%PUBLIC%\AccountPictures</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows 8 eingeführter Wert</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacystandardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_PublicVideos"></span><span id="folderid_publicvideos"></span><span id="FOLDERID_PUBLICVIDEOS"></span><dl> <dt><strong>FOLDERID_PublicVideos</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{2400183A-6185-49FB-A2D8-4A392A602BA3}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Öffentliche Videos</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>GEMEINSAM</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%PUBLIC%\Videos</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_COMMON_VIDEO</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Freigegebenes Video</td>
</tr>
<tr class="odd">
<td>Legacystandardpfad</td>
<td>%ALLUSERSPROFILE%\Documents\My Videos</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_QuickLaunch"></span><span id="folderid_quicklaunch"></span><span id="FOLDERID_QUICKLAUNCH"></span><dl> <dt><strong>FOLDERID_QuickLaunch</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{52a4f021-7b75-48a9-9f6b-4b87a210bc8f}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Schnellstart</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>SOLLSER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%APPDATA%\Microsoft\Internet Explorer\Schnellstart</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>Keine</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Schnellstart</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>%APPDATA%\Microsoft\Internet Explorer\Schnellstart</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_Recent"></span><span id="folderid_recent"></span><span id="FOLDERID_RECENT"></span><dl> <dt><strong>FOLDERID_Recent</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{AE50C081-EBD2-438A-8655-8A092E34987A}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Zuletzt verwendete Elemente</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>BESER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%APPDATA%\Microsoft\Windows\Recent</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_RECENT</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Meine letzten Dokumente</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>%USERPROFILE%\Recent</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_RecordedTV"></span><span id="folderid_recordedtv"></span><span id="FOLDERID_RECORDEDTV"></span><dl> <dt><strong>FOLDERID_RecordedTV</strong></dt> </dl></td>
<td ><p>Nicht verwendet. Dieser Wert ist ab 7 Windows definiert.</p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_RecordedTVLibrary"></span><span id="folderid_recordedtvlibrary"></span><span id="FOLDERID_RECORDEDTVLIBRARY"></span><dl> <dt><strong>FOLDERID_RecordedTVLibrary</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{1A6FDBA2-F42D-4358-A798-B74D745926C5}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>TV-Aufzeichnungen</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>GEMEINSAM</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%PUBLIC%\RecordedTV.library-ms</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, value introduced in Windows 7</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_RecycleBinFolder"></span><span id="folderid_recyclebinfolder"></span><span id="FOLDERID_RECYCLEBINFOLDER"></span><dl> <dt><strong>FOLDERID_RecycleBinFolder</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{B7534046-3ECB-4C18-BE4E-64CD4CB7D6AC}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Papierkorb</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>VIRTUELLEN</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>Nicht zutreffend – virtueller Ordner</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_BITBUCKET</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Papierkorb</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>Nicht zutreffend – virtueller Ordner</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_ResourceDir"></span><span id="folderid_resourcedir"></span><span id="FOLDERID_RESOURCEDIR"></span><dl> <dt><strong>FOLDERID_ResourceDir</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{8AD10C31-2ADB-4296-A8F7-E4701232C972}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Ressourcen</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>FIXED</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%windir%\Resources</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_RESOURCES</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Ressourcen</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>%windir%\Resources</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_Ringtones"></span><span id="folderid_ringtones"></span><span id="FOLDERID_RINGTONES"></span><dl> <dt><strong>FOLDERID_Ringtones</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{C870044B-F49E-4126-A9C3-B52A1FF411E8}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Klingeltöne</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>BESER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%LOCALAPPDATA%\Microsoft\Windows\Ringtones</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, value introduced in Windows 7</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_RoamingAppData"></span><span id="folderid_roamingappdata"></span><span id="FOLDERID_ROAMINGAPPDATA"></span><dl> <dt><strong>FOLDERID_RoamingAppData</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{3EB685DB-65F9-4CF6-A03A-E3EF65729F3D}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Roaming</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>BESER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%APPDATA% (%USERPROFILE%\AppData\Roaming)</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_APPDATA</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Anwendungsdaten</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>%APPDATA% (%USERPROFILE%\Anwendungsdaten)</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_RoamedTileImages"></span><span id="folderid_roamedtileimages"></span><span id="FOLDERID_ROAMEDTILEIMAGES"></span><dl> <dt><strong>FOLDERID_RoamedTileImages</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{AAA8D5A5-F1D6-4259-BAA8-78E7EF60835E}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>RoamedTileImages</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>BESER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%LOCALAPPDATA%\Microsoft\Windows\RoamedTileImages</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, value introduced in Windows 8</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_RoamingTiles"></span><span id="folderid_roamingtiles"></span><span id="FOLDERID_ROAMINGTILES"></span><dl> <dt><strong>FOLDERID_RoamingTiles</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{00BCFC5A-ED94-4e48-96A1-3F6217F21990}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>RoamingTiles</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>BESER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%LOCALAPPDATA%\Microsoft\Windows\RoamingTiles</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, value introduced in Windows 8</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_SampleMusic"></span><span id="folderid_samplemusic"></span><span id="FOLDERID_SAMPLEMUSIC"></span><dl> <dt><strong>FOLDERID_SampleMusic</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{B250C668-F57D-4EE1-A63C-290EE7D1AA1F}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Beispiel Musik</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>GEMEINSAM</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%PUBLIC%\Musik\Beispiel Musik</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>Keine</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Beispiel Musik</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>%ALLUSERSPROFILE%\Documents\My Musik\Sample Musik</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_SamplePictures"></span><span id="folderid_samplepictures"></span><span id="FOLDERID_SAMPLEPICTURES"></span><dl> <dt><strong>FOLDERID_SamplePictures</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{C4900540-2379-4C75-844B-64E6FAF8716B}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Beispielbilder</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>GEMEINSAM</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%PUBLIC%\Pictures\Sample Pictures</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>Keine</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Beispielbilder</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>%ALLUSERSPROFILE%\Documents\My Pictures\Sample Pictures</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_SamplePlaylists"></span><span id="folderid_sampleplaylists"></span><span id="FOLDERID_SAMPLEPLAYLISTS"></span><dl> <dt><strong>FOLDERID_SamplePlaylists</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{15CA69B3-30EE-49C1-ACE1-6B5EC372AFB5}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Beispielwiedergabelisten</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>GEMEINSAM</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%PUBLIC%\Musik\Beispielwiedergabelisten</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, value introduced in Windows Vista</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_SampleVideos"></span><span id="folderid_samplevideos"></span><span id="FOLDERID_SAMPLEVIDEOS"></span><dl> <dt><strong>FOLDERID_SampleVideos</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{859EAD94-2E85-48AD-A71A-0969CB56A6CD}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Beispielvideos</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>GEMEINSAM</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%PUBLIC%\Videos\Beispielvideos</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>Keine</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_SavedGames"></span><span id="folderid_savedgames"></span><span id="FOLDERID_SAVEDGAMES"></span><dl> <dt><strong>FOLDERID_SavedGames</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{4C5C32FF-BB9D-43b0-B5B4-2D72E54EAAA4}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Gespeicherte Spiele</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>BESER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%USERPROFILE%\Saved Games</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, value introduced in Windows Vista</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_SavedPictures"></span><span id="folderid_savedpictures"></span><span id="FOLDERID_SAVEDPICTURES"></span><dl> <dt><strong>FOLDERID_SavedPictures</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{3B193882-D3AD-4eab-965A-69829D1FB59F}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Gespeicherte Bilder</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>BESER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%USERPROFILE%\Pictures\Saved Pictures</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>Keine</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_SavedPicturesLibrary"></span><span id="folderid_savedpictureslibrary"></span><span id="FOLDERID_SAVEDPICTURESLIBRARY"></span><dl> <dt><strong>FOLDERID_SavedPicturesLibrary</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{E25B5812-BE88-4bd9-94B0-29233477B6C3}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Saved Pictures Library</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>BESER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%APPDATA%\Microsoft\Windows\Libraries\SavedPictures.library-ms</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>Keine</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_SavedSearches"></span><span id="folderid_savedsearches"></span><span id="FOLDERID_SAVEDSEARCHES"></span><dl> <dt><strong>FOLDERID_SavedSearches</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{7d1d3a04-debb-4115-95cf-2f29da2920da}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Suchvorgänge</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>BESER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%USERPROFILE%\Searches</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>Keine</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_Screenshots"></span><span id="folderid_screenshots"></span><span id="FOLDERID_SCREENSHOTS"></span><dl> <dt><strong>FOLDERID_Screenshots</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{b7bede81-df94-4682-a7d8-57a52620b86f}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Screenshots</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>BESER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%USERPROFILE%\Pictures\Screenshots</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, value introduced in Windows 8</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_SEARCH_CSC"></span><span id="folderid_search_csc"></span><dl> <dt><strong>FOLDERID_SEARCH_CSC</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{ee32e446-31ca-4aba-814f-a5ebd2fd6d5e}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Offlinedateien</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>VIRTUELLEN</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>Nicht zutreffend – virtueller Ordner</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>Keine</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_SearchHistory"></span><span id="folderid_searchhistory"></span><span id="FOLDERID_SEARCHHISTORY"></span><dl> <dt><strong>FOLDERID_SearchHistory</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{0D4C3DB6-03A3-462F-A0E6-08924C41B5D4}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Verlauf</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>BESER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%LOCALAPPDATA%\Microsoft\Windows\ConnectedSearch\History</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, value introduced in Windows 8.1</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_SearchHome"></span><span id="folderid_searchhome"></span><span id="FOLDERID_SEARCHHOME"></span><dl> <dt><strong>FOLDERID_SearchHome</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{190337d1-b8ca-4121-a639-6d472d16972a}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Suchergebnisse</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>VIRTUELLEN</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>Nicht zutreffend – virtueller Ordner</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>Keine</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacystandardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_SEARCH_MAPI"></span><span id="folderid_search_mapi"></span><dl> <dt><strong>FOLDERID_SEARCH_MAPI</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{98ec0e18-2098-4d44-8644-66979315a281}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Microsoft Office Outlook</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>VIRTUELLEN</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>Nicht zutreffend – virtueller Ordner</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>Keine</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacystandardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_SearchTemplates"></span><span id="folderid_searchtemplates"></span><span id="FOLDERID_SEARCHTEMPLATES"></span><dl> <dt><strong>FOLDERID_SearchTemplates</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{7E636BFE-DFA9-4D5E-B456-D7B39851D8A9}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Vorlagen</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>SOLLSER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%LOCALAPPDATA%\Microsoft\Windows\ConnectedSearch\Templates</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows 8.1 eingeführter Wert</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacystandardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_SendTo"></span><span id="folderid_sendto"></span><span id="FOLDERID_SENDTO"></span><dl> <dt><strong>FOLDERID_SendTo</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{8983036C-27C0-404B-8F08-102D10DCFD74}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Sendto</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>SOLLSER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%APPDATA%\Microsoft\Windows\SendTo</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_SENDTO</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Sendto</td>
</tr>
<tr class="odd">
<td>Legacystandardpfad</td>
<td>%USERPROFILE%\SendTo</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_SidebarDefaultParts"></span><span id="folderid_sidebardefaultparts"></span><span id="FOLDERID_SIDEBARDEFAULTPARTS"></span><dl> <dt><strong>FOLDERID_SidebarDefaultParts</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{7B396E54-9EC5-4300-BE0A-2482EBAE1A26}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Gadgets</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>GEMEINSAM</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%ProgramFiles%\Windows Randleiste\Gadgets</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>Keine, neu für Windows 7</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacystandardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_SidebarParts"></span><span id="folderid_sidebarparts"></span><span id="FOLDERID_SIDEBARPARTS"></span><dl> <dt><strong>FOLDERID_SidebarParts</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{A75D362E-50FC-4fb7-AC2C-A8BEAA314493}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Gadgets</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>SOLLSER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%LOCALAPPDATA%\Microsoft\Windows Randleiste\Gadgets</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>Keine, neu für Windows 7</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacystandardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_SkyDrive"></span><span id="folderid_skydrive"></span><span id="FOLDERID_SKYDRIVE"></span><dl> <dt><strong>FOLDERID_SkyDrive</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{A52BBA46-E9E1-435f-B3D9-28DAA648C0F6}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>OneDrive</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>SOLLSER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%USERPROFILE%\OneDrive</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows 8.1 eingeführter Wert</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacystandardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_SkyDriveCameraRoll"></span><span id="folderid_skydrivecameraroll"></span><span id="FOLDERID_SKYDRIVECAMERAROLL"></span><dl> <dt><strong>FOLDERID_SkyDriveCameraRoll</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{767E6811-49CB-4273-87C2-20F355E1085B}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Kameraroll</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>SOLLSER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%USERPROFILE%\OneDrive\Pictures\Camera Roll</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows 8.1 eingeführter Wert</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacystandardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_SkyDriveDocuments"></span><span id="folderid_skydrivedocuments"></span><span id="FOLDERID_SKYDRIVEDOCUMENTS"></span><dl> <dt><strong>FOLDERID_SkyDriveDocuments</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{24D89E24-2F19-4534-9DDE-6A6671FBB8FE}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Dokumente</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>SOLLSER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%USERPROFILE%\OneDrive\Documents</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows 8.1 eingeführter Wert</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacystandardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_SkyDrivePictures"></span><span id="folderid_skydrivepictures"></span><span id="FOLDERID_SKYDRIVEPICTURES"></span><dl> <dt><strong>FOLDERID_SkyDrivePictures</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{339719B5-8C47-4894-94C2-D8F77ADD44A6}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Bilder</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>SOLLSER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%USERPROFILE%\OneDrive\Pictures</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows 8.1 eingeführter Wert</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacystandardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_StartMenu"></span><span id="folderid_startmenu"></span><span id="FOLDERID_STARTMENU"></span><dl> <dt><strong>FOLDERID_StartMenu</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{625B53C3-AB48-4EC1-BA1F-A1EF4146FC19}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Startmenü</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>SOLLSER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%APPDATA%\Microsoft\Windows\Startmenü</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_STARTMENU</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Startmenü</td>
</tr>
<tr class="odd">
<td>Legacystandardpfad</td>
<td>%USERPROFILE%\Startmenü</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_Startup"></span><span id="folderid_startup"></span><span id="FOLDERID_STARTUP"></span><dl> <dt><strong>FOLDERID_Startup</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{B97D20BB-F46A-4C97-BA10-5E3608430854}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Start</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>SOLLSER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%APPDATA%\Microsoft\Windows\Startmenü\Programme\StartUp</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_STARTUP, CSIDL_ALTSTARTUP</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Start</td>
</tr>
<tr class="odd">
<td>Legacystandardpfad</td>
<td>%USERPROFILE%\Startmenü\Programme\StartUp</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_SyncManagerFolder"></span><span id="folderid_syncmanagerfolder"></span><span id="FOLDERID_SYNCMANAGERFOLDER"></span><dl> <dt><strong>FOLDERID_SyncManagerFolder</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{43668BF8-C14E-49B2-97C9-747784D784B7}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Synchronisierungscenter</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>VIRTUELLEN</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>Nicht zutreffend – virtueller Ordner</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows Vista eingeführter Wert</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacystandardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_SyncResultsFolder"></span><span id="folderid_syncresultsfolder"></span><span id="FOLDERID_SYNCRESULTSFOLDER"></span><dl> <dt><strong>FOLDERID_SyncResultsFolder</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{289a9a43-be44-4057-a41b-587a76d7e7f9}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Synchronisierungsergebnisse</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>VIRTUELLEN</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>Nicht zutreffend – virtueller Ordner</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows Vista eingeführter Wert</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacystandardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_SyncSetupFolder"></span><span id="folderid_syncsetupfolder"></span><span id="FOLDERID_SYNCSETUPFOLDER"></span><dl> <dt><strong>FOLDERID_SyncSetupFolder</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{0F214138-B1D3-4a90-BBA9-27CBC0C5389A}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Setup für die Synchronisierung</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>VIRTUELLEN</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>Nicht zutreffend – virtueller Ordner</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, value introduced in Windows Vista</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_System"></span><span id="folderid_system"></span><span id="FOLDERID_SYSTEM"></span><dl> <dt><strong>FOLDERID_System</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{1AC14E77-02E7-4E5D-B744-2EB1AE5198B7}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>System32</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>FIXED</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%windir%\system32</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_SYSTEM</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>system32</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>%windir%\system32</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_SystemX86"></span><span id="folderid_systemx86"></span><span id="FOLDERID_SYSTEMX86"></span><dl> <dt><strong>FOLDERID_SystemX86</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{D65231B0-B2F1-4857-A4CE-A8E7C6EA7D27}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>System32</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>FIXED</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%windir%\system32</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_SYSTEMX86</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>system32</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>%windir%\system32</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_Templates"></span><span id="folderid_templates"></span><span id="FOLDERID_TEMPLATES"></span><dl> <dt><strong>FOLDERID_Templates</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{A63293E8-664E-48DB-A079-DF759E0509F7}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Vorlagen</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>BESER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%APPDATA%\Microsoft\Windows\Templates</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_TEMPLATES</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Vorlagen</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>%USERPROFILE%\Templates</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_TreeProperties"></span><span id="folderid_treeproperties"></span><span id="FOLDERID_TREEPROPERTIES"></span><dl> <dt><strong>FOLDERID_TreeProperties</strong></dt> </dl></td>
<td ><p>Wird nicht in Windows Vista verwendet. Ab Version Windows 7 nicht mehr unterstützt.</p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_UserPinned"></span><span id="folderid_userpinned"></span><span id="FOLDERID_USERPINNED"></span><dl> <dt><strong>FOLDERID_UserPinned</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{9E3995AB-1F9C-4F13-B827-48B24B6C7174}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Benutzer angeheftet</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>BESER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%APPDATA%\Microsoft\Internet Explorer\Schnellstart\Benutzer angeheftet</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, value introduced in Windows 7</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_UserProfiles"></span><span id="folderid_userprofiles"></span><span id="FOLDERID_USERPROFILES"></span><dl> <dt><strong>FOLDERID_UserProfiles</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{0762D272-C50A-4BB0-A382-697DCD729B80}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Benutzer</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>FIXED</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%SystemDrive%\Users</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>Keine, neu für Windows Vista</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacy-Standardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_UserProgramFiles"></span><span id="folderid_userprogramfiles"></span><span id="FOLDERID_USERPROGRAMFILES"></span><dl> <dt><strong>FOLDERID_UserProgramFiles</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{5CD7AEE2-2219-4A67-B85D-6C9CE15660CB}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Programme</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>SOLLSER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%LOCALAPPDATA%\Programs</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows 7 eingeführter Wert</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacystandardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_UserProgramFilesCommon"></span><span id="folderid_userprogramfilescommon"></span><span id="FOLDERID_USERPROGRAMFILESCOMMON"></span><dl> <dt><strong>FOLDERID_UserProgramFilesCommon</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{BCBD3057-CA5C-4622-B42D-BC56DB0AE516}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Programme</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>SOLLSER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%LOCALAPPDATA%\Programs\Common</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows 7 eingeführter Wert</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacystandardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_UsersFiles"></span><span id="folderid_usersfiles"></span><span id="FOLDERID_USERSFILES"></span><dl> <dt><strong>FOLDERID_UsersFiles</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{f3ce0f7c-4901-4acc-8648-d5d44b04ef8f}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Beim Erstellen des Benutzerkontos wurde der vollständige Name des Benutzers eingegeben (z. B. Benutzerkontenbehälter).</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>VIRTUELLEN</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>Nicht zutreffend – virtueller Ordner</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>Keine</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacystandardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_UsersLibraries"></span><span id="folderid_userslibraries"></span><span id="FOLDERID_USERSLIBRARIES"></span><dl> <dt><strong>FOLDERID_UsersLibraries</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{A302545D-DEFF-464b-ABE8-61C8648D939B}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Bibliotheken</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>VIRTUELLEN</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>Nicht zutreffend – virtueller Ordner</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows 7 eingeführter Wert</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacystandardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_Videos"></span><span id="folderid_videos"></span><span id="FOLDERID_VIDEOS"></span><dl> <dt><strong>FOLDERID_Videos</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{18989B1D-99B5-455B-841C-AB7C74E4DDFC}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Videos</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>SOLLSER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%USERPROFILE%\Videos</td>
</tr>
<tr class="odd">
<td>CSIDL</td>
<td>CSIDL_MYVIDEO</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Meine Videos</td>
</tr>
<tr class="odd">
<td>Legacystandardpfad</td>
<td>%USERPROFILE%\Eigene Dokumente\Meine Videos</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td ><span id="FOLDERID_VideosLibrary"></span><span id="folderid_videoslibrary"></span><span id="FOLDERID_VIDEOSLIBRARY"></span><dl> <dt><strong>FOLDERID_VideosLibrary</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{491E922F-5643-4AF4-A7EB-4E7A138D8174}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Videos</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>SOLLSER</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%APPDATA%\Microsoft\Windows\Libraries\Videos.library-ms</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows 7 eingeführter Wert</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>Nicht zutreffend</td>
</tr>
<tr class="odd">
<td>Legacystandardpfad</td>
<td>Nicht zutreffend</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td ><span id="FOLDERID_Windows"></span><span id="folderid_windows"></span><span id="FOLDERID_WINDOWS"></span><dl> <dt><strong>FOLDERID_Windows</strong></dt> </dl></td>
<td >
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{F38BF404-1D43-42F2-9305-67DE0B28FC23}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Windows</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>FIXED</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%windir%</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_WINDOWS</td>
</tr>
<tr class="even">
<td>Legacyanzeigename</td>
<td>WINDOWS</td>
</tr>
<tr class="odd">
<td>Legacystandardpfad</td>
<td>%windir%</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Hinweise

Die Interpretation bestimmter **KNOWNFOLDERID-Werte** hängt davon ab, ob der Ordner Teil einer 32-Bit- oder 64-Bit-Anwendung ist und ob diese Anwendung unter einem 32-Bit- oder 64-Bit-Betriebssystem ausgeführt wird. Wenn Ihre Anwendung z. B. zwischen **Programmdateien** und **Programmdateien (x86)** unterscheiden muss, müssen Sie für diese Situation die richtige **KNOWNFOLDERID** verwenden.

In den folgenden Tabellen wird die Verwendung **von KNOWNFOLDERID** in diesen Fällen zusammengefasst.


**FOLDERID \_ ProgramFiles** 

| Betriebssystem | Application | KNOWNFOLDERID | Standard Path | CSIDL-Entsprechung |
|------------------|-------------|---------------|--------------|------------------|  
| 32-Bit | 32-Bit | FOLDERID \_ ProgramFiles | %SystemDrive% \\ Programme | \_CSIDL-PROGRAMMDATEIEN \_ |
| 32-Bit | 32-Bit | FOLDERID \_ ProgramFilesX86 | %SystemDrive% \\ Programme | \_ \_ CSIDL-PROGRAMMDATEIENX86 |
| 32-Bit | 32-Bit | FOLDERID \_ ProgramFilesX64 (wird unter 32-Bit-Betriebssystemen nicht unterstützt) | Nicht zutreffend | Nicht zutreffend |
| 64-Bit | 64-Bit | FOLDERID \_ ProgramFiles | %SystemDrive% \\ Programme | \_CSIDL-PROGRAMMDATEIEN \_ |
| 64-Bit | 64-Bit | FOLDERID \_ ProgramFilesX86 | %SystemDrive% \\ Program Files (x86) | \_ \_ CSIDL-PROGRAMMDATEIENX86 |
| 64-Bit | 64-Bit | FOLDERID \_ ProgramFilesX64 | %SystemDrive% \\ Programme | Keine |
| 64-Bit | 32-Bit | FOLDERID \_ ProgramFiles | %SystemDrive% \\ Program Files (x86) | \_CSIDL-PROGRAMMDATEIEN \_ |
| 64-Bit | 32-Bit | FOLDERID \_ ProgramFilesX86 | %SystemDrive% \\ Program Files (x86) | \_ \_ CSIDL-PROGRAMMDATEIENX86 |
| 64-Bit | 32-Bit | FOLDERID \_ ProgramFilesX64 (wird für 32-Bit-Anwendungen nicht unterstützt) | Nicht zutreffend | Nicht zutreffend |


**FOLDERID \_ ProgramFilesCommon**

| Betriebssystem | Application | KNOWNFOLDERID | Standard Path | CSIDL-Entsprechung |
|------------------|-------------|---------------|--------------|------------------|  
| 32-Bit | 32-Bit | FOLDERID \_ ProgramFilesCommon | %ProgramFiles% \\ Common Files | \_ \_ CSIDL-PROGRAMMDATEIEN \_ ( COMMON) |
| 32-Bit | 32-Bit | FOLDERID \_ ProgramFilesCommonX86 | %ProgramFiles% \\ Common Files | \_CSIDL-PROGRAMMDATEIEN \_ \_ COMMONX86 |
| 32-Bit | 32-Bit | FOLDERID \_ ProgramFilesCommonX64 (nicht definiert) | Nicht zutreffend | Nicht zutreffend |
| 64-Bit | 64-Bit | FOLDERID \_ ProgramFilesCommon | %ProgramFiles% \\ Common Files | \_ \_ CSIDL-PROGRAMMDATEIEN \_ ( COMMON) |
| 64-Bit | 64-Bit | FOLDERID \_ ProgramFilesCommonX86 | %ProgramFiles(x86)% \\ Common Files | \_CSIDL-PROGRAMMDATEIEN \_ \_ COMMONX86 |
| 64-Bit | 64-Bit | FOLDERID \_ ProgramFilesCommonX64 | %ProgramFiles% \\ Common Files | Keine |
| 64-Bit | 32-Bit | FOLDERID \_ ProgramFilesCommon | %ProgramFiles(x86)% \\ Common Files | \_ \_ CSIDL-PROGRAMMDATEIEN \_ ( COMMON) |
| 64-Bit | 32-Bit | FOLDERID \_ ProgramFilesCommonX86 | %ProgramFiles(x86)% \\ Common Files | \_CSIDL-PROGRAMMDATEIEN \_ \_ COMMONX86 |
| 64-Bit | 32-Bit | FOLDERID \_ ProgramFilesCommonX64 | %ProgramFiles% \\ Common Files | Keine |


**\_FOLDERID-System**

| Betriebssystem | Application | KNOWNFOLDERID | Standard Path | CSIDL-Entsprechung |
|------------------|-------------|---------------|--------------|------------------|  
| 32-Bit | 32-Bit | \_FOLDERID-System | %windir% \\ system32 | CSIDL \_ SYSTEM |
| 32-Bit | 32-Bit | FOLDERID \_ SystemX86 | %windir% \\ system32 | CSIDL \_ SYSTEMX86 |
| 64-Bit | 64-Bit | \_FOLDERID-System | %windir% \\ system32 | CSIDL \_ SYSTEM |
| 64-Bit | 64-Bit | FOLDERID \_ SystemX86 | %windir% \\ syswow64 | CSIDL \_ SYSTEMX86 |
| 64-Bit | 32-Bit | \_FOLDERID-System | %windir% \\ system32 | CSIDL \_ SYSTEM |
| 64-Bit | 32-Bit | FOLDERID \_ SystemX86 | %windir% \\ syswow64 | CSIDL \_ SYSTEMX86 |


In diesem Thema haben wir Umgebungszeichenfolgen verwendet, um generische Pfade bereitzustellen. Die folgenden Tabellen enthalten Beispiele für die Pfade, die diese Umgebungszeichenfolgen darstellen. In einigen Fällen stimmen diese Pfade möglicherweise nicht mit denen auf einem bestimmten Computer überein, da während der Installation oder späteren Ordnerumleitung Entscheidungen getroffen wurden. Beachten Sie, dass sich einige Pfade für Windows Vista geändert haben.


**Windows Vista und höher**

| Umgebungszeichenfolge | Beispielpfad |
|--------------------|--------------|
| %ALLUSERSPROFILE% | C: \\ ProgramData |
| %APPDATA% | C: \\ \\ *Benutzerbenutzername* \\ AppData \\ Roaming |
| %LOCALAPPDATA% | C: \\ \\ *Benutzerbenutzername* \\ AppData \\ Local |
| %ProgramData% | C: \\ ProgramData |
| %ProgramFiles% | C: \\ Programme |
| %ProgramFiles(x86)% | C: \\ Programme (x86) |
| %PUBLIC% | C: \\ \\ Benutzer öffentlich |
| %SystemDrive% | C: |
| %USERPROFILE% | C: \\ \\ *Benutzername* des Benutzers |
| %windir% | C: \\ Windows |


**Windows XP und früher**

| Umgebungszeichenfolge | Beispielpfad |
|--------------------|--------------|
| %ALLUSERSPROFILE% | C: \\ Dokumente und Einstellungen Alle \\ Benutzer |
| %APPDATA% | C: \\ Dokumente und Einstellungen \\ *Benutzername* \\ Anwendungsdaten |
| %ProgramFiles% | C: \\ Programme |
| %SystemDrive% | C: |
| %USERPROFILE% | C: \\ Dokumente und Einstellungen \\ *Benutzername* |
| %windir% | C: \\ Windows |


## <a name="requirements"></a>Requirements (Anforderungen)


| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Knownfolders.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**CSIDL**](csidl.md)
</dt> <dt>

[Bekannte Ordner](known-folders.md)
</dt> <dt>

[Arbeiten mit bekannten Ordnern in Anwendungen](working-with-known-folders.md)
</dt> <dt>

[Erweitern bekannter Ordner mit benutzerdefinierten Ordnern](how-to-extend-known-folders-with-custom-folders.md)
</dt> <dt>

[Bekannte Ordner (Beispiel)](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))
</dt> </dl>

 

 
