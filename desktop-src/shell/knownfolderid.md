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
# <a name="knownfolderid"></a>KNOWNFOLDERID

Die **KNOWNFOLDERID** -Konstanten stellen GUIDs dar, mit denen Standardordner identifiziert werden, die im System als [bekannte Ordner](known-folders.md)registriert sind. Diese Ordner werden mit Windows Vista und höheren Betriebssystemen installiert, und auf einem Computer sind nur geeignete Ordner installiert. Beschreibungen dieser Ordner finden Sie unter [**CSIDL**](csidl.md).

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

Beispiel aus [klassischen Windows-Beispielen](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/winui/shell/appplatform/ExplorerBrowserCustomContents/ExplorerBrowserCustomContents.cpp) auf GitHub.

## <a name="constants"></a>Konstanten



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Konstante</th>
<th style="text-align: left;">BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_AccountPictures"></span><span id="folderid_accountpictures"></span><span id="FOLDERID_ACCOUNTPICTURES"></span><dl> <dt><strong>FOLDERID_AccountPictures</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{008ca0b1-55b4-4c56-b8a8-4de4b299d3be}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Konto Bilder</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%APPDATA%\microsoft\windows\accountpictures</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows 8 eingeführte Wert</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_AddNewPrograms"></span><span id="folderid_addnewprograms"></span><span id="FOLDERID_ADDNEWPROGRAMS"></span><dl> <dt><strong>FOLDERID_AddNewPrograms</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{de61d971-5ebc-4f02-a3a9-6c82895e5c04}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Programme erhalten</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Virtu</td>
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
<td>Legacy Anzeige Name</td>
<td>Hinzufügen neuer Programme ( <strong>in der System</strong> Steuerung unter "Software" gefunden)</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht zutreffend – virtueller Ordner</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_AdminTools"></span><span id="folderid_admintools"></span><span id="FOLDERID_ADMINTOOLS"></span><dl> <dt><strong>FOLDERID_AdminTools</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{724ef170-a42d-4fef -9F 26-b60e846bba4f}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Verwaltung</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%APPDATA%\Microsoft\Windows\Start menu\programs\administrative Tools</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_ADMINTOOLS</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Verwaltung</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>%UserProfile%\Startmenü \ programme\administrative Tools</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_AppDataDesktop"></span><span id="folderid_appdatadesktop"></span><span id="FOLDERID_APPDATADESKTOP"></span><dl> <dt><strong>FOLDERID_AppDataDesktop</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{B2C5E279-7ADD-439F-B28C-C41FE1BBF672}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Appdatadesktop</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%LocalAppData%\Desktop</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows 10 eingeführte Wert, Version 1709</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p>
<p>Diese folderid wird intern von .NET-Anwendungen verwendet, um plattformübergreifende App-Funktionen zu aktivieren. Sie ist nicht für die direkte Verwendung in einer Anwendung vorgesehen.</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_AppDataDocuments"></span><span id="folderid_appdatadocuments"></span><span id="FOLDERID_APPDATADOCUMENTS"></span><dl> <dt><strong>FOLDERID_AppDataDocuments</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{7be16610-1f7f-44ac-bff0-83e15f2ffca1}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Appdatadocals-Elemente</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%LocalAppData%\Documents</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows 10 eingeführte Wert, Version 1709</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p>
<p>Diese folderid wird intern von .NET-Anwendungen verwendet, um plattformübergreifende App-Funktionen zu aktivieren. Sie ist nicht für die direkte Verwendung in einer Anwendung vorgesehen.</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_AppDataFavorites"></span><span id="folderid_appdatafavorites"></span><span id="FOLDERID_APPDATAFAVORITES"></span><dl> <dt><strong>FOLDERID_AppDataFavorites</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{7cfbefbc-de1f-45AA-B843-a542ac536cc9}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Appdatafavorites</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%LocalAppData%\Favoriten</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows 10 eingeführte Wert, Version 1709</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p>
<p>Diese folderid wird intern von .NET-Anwendungen verwendet, um plattformübergreifende App-Funktionen zu aktivieren. Sie ist nicht für die direkte Verwendung in einer Anwendung vorgesehen.</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_AppDataProgramData"></span><span id="folderid_appdataprogramdata"></span><span id="FOLDERID_APPDATAPROGRAMDATA"></span><dl> <dt><strong>FOLDERID_AppDataProgramData</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{559d40a3-a036-40fa-af61-84cb430a4d34}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Appdataprogramdata</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%LocalAppData%\ProgramData</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows 10 eingeführte Wert, Version 1709</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p>
<p>Diese folderid wird intern von .NET-Anwendungen verwendet, um plattformübergreifende App-Funktionen zu aktivieren. Sie ist nicht für die direkte Verwendung in einer Anwendung vorgesehen.</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ApplicationShortcuts"></span><span id="folderid_applicationshortcuts"></span><span id="FOLDERID_APPLICATIONSHORTCUTS"></span><dl> <dt><strong>FOLDERID_ApplicationShortcuts</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{A3918781-E5F2-4890-B3D9-A7E54332328C}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Anwendungs Verknüpfungen</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%LocalAppData%\microsoft\windows\anwendungstastenkombinationen</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows 8 eingeführte Wert</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_AppsFolder"></span><span id="folderid_appsfolder"></span><span id="FOLDERID_APPSFOLDER"></span><dl> <dt><strong>FOLDERID_AppsFolder</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{1e87508d-89c2-42f 0-8a7e-645a0l50ca58}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Anwendungen</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Virtu</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>Nicht zutreffend – virtueller Ordner</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows 8 eingeführte Wert</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_AppUpdates"></span><span id="folderid_appupdates"></span><span id="FOLDERID_APPUPDATES"></span><dl> <dt><strong>FOLDERID_AppUpdates</strong></dt> </dl></td>
<td style="text-align: left;">
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
<td>Virtu</td>
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
<td>Legacy Anzeige Name</td>
<td>None, der in Windows Vista eingeführte Wert. In früheren Versionen von Windows waren die Informationen auf dieser Seite in Software enthalten <strong>, wenn das</strong> Kontrollkästchen <strong>Updates anzeigen</strong> aktiviert wurde.</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_CameraRoll"></span><span id="folderid_cameraroll"></span><span id="FOLDERID_CAMERAROLL"></span><dl> <dt><strong>FOLDERID_CameraRoll</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{AB5FB87B-7CE2-4F83-915D-550846C9537B}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Kamera-Roll</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%UserProfile%\pictures\camera Roll</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows 8.1 eingeführte Wert</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_CDBurning"></span><span id="folderid_cdburning"></span><span id="FOLDERID_CDBURNING"></span><dl> <dt><strong>FOLDERID_CDBurning</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{9e52ab10-l80d-49df-acb8-4330b5687855}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Temporärer Brenn Ordner</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%LocalAppData%\microsoft\windows\burn\burn</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_CDBURN_AREA</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>CD-brennen</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>%USERPROFILE%\Local Settings\Application data\microsoft\cd Burning</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_ChangeRemovePrograms"></span><span id="folderid_changeremoveprograms"></span><span id="FOLDERID_CHANGEREMOVEPROGRAMS"></span><dl> <dt><strong>FOLDERID_ChangeRemovePrograms</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{df7266ac-9274-4867-8d55-3bd661de872d}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Programme und Funktionen</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Virtu</td>
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
<td>Legacy Anzeige Name</td>
<td>Software</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht zutreffend – virtueller Ordner</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_CommonAdminTools"></span><span id="folderid_commonadmintools"></span><span id="FOLDERID_COMMONADMINTOOLS"></span><dl> <dt><strong>FOLDERID_CommonAdminTools</strong></dt> </dl></td>
<td style="text-align: left;">
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
<td>Gewöhnliche</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%ALLUSERSPROFILE%\Microsoft\Windows\Start menu\programs\administrative Tools</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_COMMON_ADMINTOOLS</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Verwaltung</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>%ALLUSERSPROFILE%\Startmenü \ programme\administrative Tools</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_CommonOEMLinks"></span><span id="folderid_commonoemlinks"></span><span id="FOLDERID_COMMONOEMLINKS"></span><dl> <dt><strong>FOLDERID_CommonOEMLinks</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{C1BAE2D0-10df-4334-BEDD-7aa20b227a9d}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>OEM-Links</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Gewöhnliche</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%ALLUSERSPROFILE%\oem-Links</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_COMMON_OEM_LINKS</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>OEM-Links</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>%ALLUSERSPROFILE%\oem-Links</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_CommonPrograms"></span><span id="folderid_commonprograms"></span><span id="FOLDERID_COMMONPROGRAMS"></span><dl> <dt><strong>FOLDERID_CommonPrograms</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{0139d44e-6afe-49f2-8690-3dafcae6ffb8}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Programs</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Gewöhnliche</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%ALLUSERSPROFILE%\Microsoft\Windows\Start menu\programme</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_COMMON_PROGRAMS</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Programs</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>%ALLUSERSPROFILE%\startmenu\programme</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_CommonStartMenu"></span><span id="folderid_commonstartmenu"></span><span id="FOLDERID_COMMONSTARTMENU"></span><dl> <dt><strong>FOLDERID_CommonStartMenu</strong></dt> </dl></td>
<td style="text-align: left;">
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
<td>Gewöhnliche</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%ALLUSERSPROFILE%\microsoft\windows\startmenü</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_COMMON_STARTMENU</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Startmenü</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>%ALLUSERSPROFILE%\Startmenü</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_CommonStartup"></span><span id="folderid_commonstartup"></span><span id="FOLDERID_COMMONSTARTUP"></span><dl> <dt><strong>FOLDERID_CommonStartup</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{82a5ea35-d9cd-47c5-9629-e15d2f 714e6e}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Start</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Gewöhnliche</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%ALLUSERSPROFILE%\Microsoft\Windows\Start menu\programs\startup</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_COMMON_STARTUP CSIDL_COMMON_ALTSTARTUP</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Start</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>%ALLUSERSPROFILE%\Startmenü \ programme\startup</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_CommonTemplates"></span><span id="folderid_commontemplates"></span><span id="FOLDERID_COMMONTEMPLATES"></span><dl> <dt><strong>FOLDERID_CommonTemplates</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{B94237E7-57ac-4347-9151-B08C6C32D1F7}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Vorlagen</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Gewöhnliche</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%ALLUSERSPROFILE%\microsoft\windows\templates</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_COMMON_TEMPLATES</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Vorlagen</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>%ALLUSERSPROFILE%\Templates</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ComputerFolder"></span><span id="folderid_computerfolder"></span><span id="FOLDERID_COMPUTERFOLDER"></span><dl> <dt><strong>FOLDERID_ComputerFolder</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{0ac0837c-bbf8-452A-850d-79d08e667ca7}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Computer</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Virtu</td>
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
<td>Legacy Anzeige Name</td>
<td>Arbeitsplatz</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht zutreffend – virtueller Ordner</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_ConflictFolder"></span><span id="folderid_conflictfolder"></span><span id="FOLDERID_CONFLICTFOLDER"></span><dl> <dt><strong>FOLDERID_ConflictFolder</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{4bfef B45-347d-4006-a5be-ac0cb0567192}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Konflikte</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Virtu</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>Nicht zutreffend – virtueller Ordner</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows Vista eingeführte Wert</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht zutreffend Diese <strong>KNOWNFOLDERID</strong> bezieht sich auf den Synchronisierungs-Manager von Windows Vista. Dabei handelt es sich nicht um den Ordner, auf den der ältere <a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictfolder"><strong>isyncmgrconflictfolder</strong></a>verweist.</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ConnectionsFolder"></span><span id="folderid_connectionsfolder"></span><span id="FOLDERID_CONNECTIONSFOLDER"></span><dl> <dt><strong>FOLDERID_ConnectionsFolder</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{6f0cd92b-2e97-45D1-88ff-b0d186b8debug}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Netzwerkverbindungen</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Virtu</td>
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
<td>Legacy Anzeige Name</td>
<td>Netzwerkverbindungen</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht zutreffend – virtueller Ordner</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Contacts"></span><span id="folderid_contacts"></span><span id="FOLDERID_CONTACTS"></span><dl> <dt><strong>FOLDERID_Contacts</strong></dt> </dl></td>
<td style="text-align: left;">
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
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%UserProfile%\contacts</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows Vista eingeführte Wert</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ControlPanelFolder"></span><span id="folderid_controlpanelfolder"></span><span id="FOLDERID_CONTROLPANELFOLDER"></span><dl> <dt><strong>FOLDERID_ControlPanelFolder</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{82a74aeb-aeb4-465c-A014-d097ee346d63}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Systemsteuerung</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Virtu</td>
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
<td>Legacy Anzeige Name</td>
<td>Systemsteuerung</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht zutreffend – virtueller Ordner</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Cookies"></span><span id="folderid_cookies"></span><span id="FOLDERID_COOKIES"></span><dl> <dt><strong>FOLDERID_Cookies</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{2b0f765d-c0e9-4171-908e-08a611b84 FF6}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Cookies</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%APPDATA%\microsoft\windows\cookies</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_COOKIES</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Cookies</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>%UserProfile%\Cookies</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Desktop"></span><span id="folderid_desktop"></span><span id="FOLDERID_DESKTOP"></span><dl> <dt><strong>FOLDERID_Desktop</strong></dt> </dl></td>
<td style="text-align: left;">
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
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%Userprofile%\desktop</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_DESKTOP CSIDL_DESKTOPDIRECTORY</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Desktop</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>%Userprofile%\desktop</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_DeviceMetadataStore"></span><span id="folderid_devicemetadatastore"></span><span id="FOLDERID_DEVICEMETADATASTORE"></span><dl> <dt><strong>FOLDERID_DeviceMetadataStore</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{5ce4a5e9-e4eb-479d-B89B-130c02886155}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>DeviceMetadataStore</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Gewöhnliche</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%ALLUSERSPROFILE%\Microsoft\Windows\DeviceMetadataStore</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows 7 eingeführte Wert</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Documents"></span><span id="folderid_documents"></span><span id="FOLDERID_DOCUMENTS"></span><dl> <dt><strong>FOLDERID_Documents</strong></dt> </dl></td>
<td style="text-align: left;">
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
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%UserProfile%\Documents</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechungen</td>
<td>CSIDL_MYDOCUMENTS CSIDL_PERSONAL</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Meine Dokumente</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>%USERPROFILE%\Eigene Dokumente</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_DocumentsLibrary"></span><span id="folderid_documentslibrary"></span><span id="FOLDERID_DOCUMENTSLIBRARY"></span><dl> <dt><strong>FOLDERID_DocumentsLibrary</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{7b0db17d-9cd2-4A93-9733-46cc89022e7c}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Dokumente</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%APPDATA%\microsoft\windows\libraries\documents.Library-MS</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows 7 eingeführte Wert</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Downloads"></span><span id="folderid_downloads"></span><span id="FOLDERID_DOWNLOADS"></span><dl> <dt><strong>FOLDERID_Downloads</strong></dt> </dl></td>
<td style="text-align: left;">
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
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%UserProfile%\downloads</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>Keine</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Favorites"></span><span id="folderid_favorites"></span><span id="FOLDERID_FAVORITES"></span><dl> <dt><strong>FOLDERID_Favorites</strong></dt> </dl></td>
<td style="text-align: left;">
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
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%UserProfile%\Favoriten</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_FAVORITES CSIDL_COMMON_FAVORITES</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Favoriten</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>%UserProfile%\Favoriten</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Fonts"></span><span id="folderid_fonts"></span><span id="FOLDERID_FONTS"></span><dl> <dt><strong>FOLDERID_Fonts</strong></dt> </dl></td>
<td style="text-align: left;">
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
<td>%WINDIR%\fonts</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_FONTS</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Schriftarten</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>%WINDIR%\fonts</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Games"></span><span id="folderid_games"></span><span id="FOLDERID_GAMES"></span><dl> <dt><strong>FOLDERID_Games</strong></dt> </dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
Diese folderid ist in Windows 10, Version 1803 und höheren Versionen, veraltet. In diesen Versionen wird <strong>0x80070057-E_INVALIDARG</strong> zurückgegeben.
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
<td>Virtu</td>
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
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_GameTasks"></span><span id="folderid_gametasks"></span><span id="FOLDERID_GAMETASKS"></span><dl> <dt><strong>FOLDERID_GameTasks</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{054fae61-4dd8-4787-80b6-090220c4b700}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>GameExplorer</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%LocalAppData%\microsoft\windows\gameexplorer</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows Vista eingeführte Wert</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_History"></span><span id="folderid_history"></span><span id="FOLDERID_HISTORY"></span><dl> <dt><strong>FOLDERID_History</strong></dt> </dl></td>
<td style="text-align: left;">
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
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%LocalAppData%\microsoft\windows\history</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_HISTORY</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Verlauf</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>%USERPROFILE%\Local Settings\History</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_HomeGroup"></span><span id="folderid_homegroup"></span><span id="FOLDERID_HOMEGROUP"></span><dl> <dt><strong>FOLDERID_HomeGroup</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{52528a6b-b9e3-4 Add-b60d-588c2dba842d}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Heimnetzgruppe</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Virtu</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>Nicht zutreffend – virtueller Ordner</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows 7 eingeführte Wert</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_HomeGroupCurrentUser"></span><span id="folderid_homegroupcurrentuser"></span><span id="FOLDERID_HOMEGROUPCURRENTUSER"></span><dl> <dt><strong>FOLDERID_HomeGroupCurrentUser</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{9b74b6a3-0dfd-4f 11-9e78-5 f</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Der Benutzername des Benutzers (% username%)</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Virtu</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>Nicht zutreffend – virtueller Ordner</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows 8 eingeführte Wert</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ImplicitAppShortcuts"></span><span id="folderid_implicitappshortcuts"></span><span id="FOLDERID_IMPLICITAPPSHORTCUTS"></span><dl> <dt><strong>FOLDERID_ImplicitAppShortcuts</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{BCB5256F-79F6-4CEE-B725-DC34E402FD46}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Implicitappverknüpfungen</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%APPDATA%\microsoft\internet Explorer\Quick launch\user pinned\implicitappverknüpfungen</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows 7 eingeführte Wert</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_InternetCache"></span><span id="folderid_internetcache"></span><span id="FOLDERID_INTERNETCACHE"></span><dl> <dt><strong>FOLDERID_InternetCache</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{352481e8-33be-4251-BA85-6007caedcf9d}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Temporäre Internetdateien</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%LocalAppData%\microsoft\windows\temporäre Internet Dateien</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_INTERNET_CACHE</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Temporäre Internetdateien</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>%USERPROFILE%\Local settings\temporäre Internet Dateien</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_InternetFolder"></span><span id="folderid_internetfolder"></span><span id="FOLDERID_INTERNETFOLDER"></span><dl> <dt><strong>FOLDERID_InternetFolder</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{4d9f 7874-4e0c-4904-967b-40b0d20c3e4b}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Das Internet</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Virtu</td>
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
<td>Legacy Anzeige Name</td>
<td>Internet Explorer</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht zutreffend – virtueller Ordner</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Libraries"></span><span id="folderid_libraries"></span><span id="FOLDERID_LIBRARIES"></span><dl> <dt><strong>FOLDERID_Libraries</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{1b3ea5dc-B587-4786-b4ef-bd1dc332aeae}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Bibliotheken</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%Appdata%\microsoft\windows\libraries</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows 7 eingeführte Wert</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Links"></span><span id="folderid_links"></span><span id="FOLDERID_LINKS"></span><dl> <dt><strong>FOLDERID_Links</strong></dt> </dl></td>
<td style="text-align: left;">
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
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%UserProfile%\links</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>Keine</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_LocalAppData"></span><span id="folderid_localappdata"></span><span id="FOLDERID_LOCALAPPDATA"></span><dl> <dt><strong>FOLDERID_LocalAppData</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{F1B32785-6FBA-4FCF-9D55-7B8E7F157091}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Lokal</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>% LocalAppData% (%userprofile%\AppData\Local)</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_LOCAL_APPDATA</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Anwendungsdaten</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>%Userprofile%\Lokale Einstellungen\Anwendungsdaten</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_LocalAppDataLow"></span><span id="folderid_localappdatalow"></span><span id="FOLDERID_LOCALAPPDATALOW"></span><dl> <dt><strong>FOLDERID_LocalAppDataLow</strong></dt> </dl></td>
<td style="text-align: left;">
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
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%UserProfile%\appdata\locallow</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>Keine</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_LocalizedResourcesDir"></span><span id="folderid_localizedresourcesdir"></span><span id="FOLDERID_LOCALIZEDRESOURCESDIR"></span><dl> <dt><strong>FOLDERID_LocalizedResourcesDir</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{2a00375e-224c-49DE-b8d1-440df7ef3ddc}</td>
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
<td>Legacy Anzeige Name</td>
<td>Keine</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>%windir%\resources\0409 (Codepage)</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Music"></span><span id="folderid_music"></span><span id="FOLDERID_MUSIC"></span><dl> <dt><strong>FOLDERID_Music</strong></dt> </dl></td>
<td style="text-align: left;">
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
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%UserProfile%\Music</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_MYMUSIC</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Meine Musik</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>%USERPROFILE%\Eigene Dateien\Eigene Musik</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_MusicLibrary"></span><span id="folderid_musiclibrary"></span><span id="FOLDERID_MUSICLIBRARY"></span><dl> <dt><strong>FOLDERID_MusicLibrary</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{2112ab0a-c86a-4ffe-a368-0de96e47012e}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Musik</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%APPDATA%\microsoft\windows\libraries\music.Library-MS</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows 7 eingeführte Wert</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_NetHood"></span><span id="folderid_nethood"></span><span id="FOLDERID_NETHOOD"></span><dl> <dt><strong>FOLDERID_NetHood</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{C5ABBF53-E17F-4121-8900-86626FC2C973}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Netzwerk Verknüpfungen</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%APPDATA%\microsoft\windows\network Tastenkombinationen</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_NETHOOD</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht mehr</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>%UserProfile%\netthood</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_NetworkFolder"></span><span id="folderid_networkfolder"></span><span id="FOLDERID_NETWORKFOLDER"></span><dl> <dt><strong>FOLDERID_NetworkFolder</strong></dt> </dl></td>
<td style="text-align: left;">
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
<td>Virtu</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>Nicht zutreffend – virtueller Ordner</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_NETWORK CSIDL_COMPUTERSNEARME</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Meine Netzwerk Orte</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht zutreffend – virtueller Ordner</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Objects3D"></span><span id="folderid_objects3d"></span><span id="FOLDERID_OBJECTS3D"></span><dl> <dt><strong>FOLDERID_Objects3D</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{31c0dd25-9439-4f12-bf41-7ff4eda38722}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>3D-Objekte</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%UserProfile%\3d-Objekte</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows 10 eingeführte Wert, Version 1703</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_OriginalImages"></span><span id="folderid_originalimages"></span><span id="FOLDERID_ORIGINALIMAGES"></span><dl> <dt><strong>FOLDERID_OriginalImages</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{2c36c0aa-5812-4b87-b bbb0-4cd0dfb19b39}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Original Bilder</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%LocalAppData%\Microsoft\Windows Photo gallery\original Images</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows Vista eingeführte Wert</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_PhotoAlbums"></span><span id="folderid_photoalbums"></span><span id="FOLDERID_PHOTOALBUMS"></span><dl> <dt><strong>FOLDERID_PhotoAlbums</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{69d2cf90fc33-4fb7-9a0c-ebb0f0fcb43c}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Folien anzeigen</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%UserProfile%\pictures\folien anzeigen</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows Vista eingeführte Wert</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_PicturesLibrary"></span><span id="folderid_pictureslibrary"></span><span id="FOLDERID_PICTURESLIBRARY"></span><dl> <dt><strong>FOLDERID_PicturesLibrary</strong></dt> </dl></td>
<td style="text-align: left;">
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
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%APPDATA%\microsoft\windows\libraries\pictures.Library-MS</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows 7 eingeführte Wert</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Pictures"></span><span id="folderid_pictures"></span><span id="FOLDERID_PICTURES"></span><dl> <dt><strong>FOLDERID_Pictures</strong></dt> </dl></td>
<td style="text-align: left;">
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
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%UserProfile%\Bilder</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_MYPICTURES</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Meine Bilder</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>%USERPROFILE%\Eigene Dateien\Eigene Bilder</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Playlists"></span><span id="folderid_playlists"></span><span id="FOLDERID_PLAYLISTS"></span><dl> <dt><strong>FOLDERID_Playlists</strong></dt> </dl></td>
<td style="text-align: left;">
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
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%UserProfile%\music\playlists</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>Keine</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_PrintersFolder"></span><span id="folderid_printersfolder"></span><span id="FOLDERID_PRINTERSFOLDER"></span><dl> <dt><strong>FOLDERID_PrintersFolder</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{76fc4e2d-D6AD-4519-A663-37bd56068185}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Drucker</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Virtu</td>
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
<td>Legacy Anzeige Name</td>
<td>Drucker und Faxe</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht zutreffend – virtueller Ordner</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_PrintHood"></span><span id="folderid_printhood"></span><span id="FOLDERID_PRINTHOOD"></span><dl> <dt><strong>FOLDERID_PrintHood</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{9274bd8d-CFD1-41c3-b35e-b13f55a758f4}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Drucker Verknüpfungen</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%APPDATA%\microsoft\windows\druckerkombinationen</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_PRINTHOOD</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Printhood</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>%UserProfile%\printhood</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Profile"></span><span id="folderid_profile"></span><span id="FOLDERID_PROFILE"></span><dl> <dt><strong>FOLDERID_Profile</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{5e6c858l-0E22-4760-9afe-ea3317b67173}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Der Benutzername des Benutzers (% username%)</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>FIXED</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>% User Profile% (%SystemDrive%\Users \% username%)</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_PROFILE</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Der Benutzername des Benutzers (% username%)</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>% User Profile% (%systemdrive%\Documents and Settings \% username%)</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_ProgramData"></span><span id="folderid_programdata"></span><span id="FOLDERID_PROGRAMDATA"></span><dl> <dt><strong>FOLDERID_ProgramData</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{62ab5d82-f 1-4dc3-a9dd-070d1d495d97}</td>
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
<td>% ALLUSERSPROFILE% (% Program Data%,%SystemDrive%\ProgramData)</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_COMMON_APPDATA</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Anwendungsdaten</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>%ALLUSERSPROFILE%\Anwendungsdaten</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ProgramFiles"></span><span id="folderid_programfiles"></span><span id="FOLDERID_PROGRAMFILES"></span><dl> <dt><strong>FOLDERID_ProgramFiles</strong></dt> </dl></td>
<td style="text-align: left;"><p>Weitere Informationen finden Sie unter Hinweise.</p>

<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{905E63B6-C1BF -494E-B29C-65B732D3D21A}</td>
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
<td>% Program Files% (%SystemDrive%\Program Files)</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_PROGRAM_FILES</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Programme</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>% Program Files% (%SystemDrive%\Program Files)</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_ProgramFilesX64"></span><span id="folderid_programfilesx64"></span><span id="FOLDERID_PROGRAMFILESX64"></span><dl> <dt><strong>FOLDERID_ProgramFilesX64</strong></dt> </dl></td>
<td style="text-align: left;"><p>Dieser Wert wird auf 32-Bit-Betriebssystemen nicht unterstützt. Es wird auch nicht für 32-Bit-Anwendungen unterstützt, die auf 64-Bit-Betriebssystemen ausgeführt werden. Der Versuch, FOLDERID_ProgramFilesX64 in beiden Situationen zu verwenden, führt zu einem Fehler. Weitere Informationen finden Sie unter Hinweise.</p>

<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{6d809377-6af0-444b-8957-A3773F02200E}</td>
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
<td>% Program Files% (%SystemDrive%\Program Files)</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>Keine</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Programme</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>% Program Files% (%SystemDrive%\Program Files)</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ProgramFilesX86"></span><span id="folderid_programfilesx86"></span><span id="FOLDERID_PROGRAMFILESX86"></span><dl> <dt><strong>FOLDERID_ProgramFilesX86</strong></dt> </dl></td>
<td style="text-align: left;"><p>Weitere Informationen finden Sie unter Hinweise.</p>

<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{7c5a40ef-a0f -4bfc-874a-c0b2e0b9fa8e}</td>
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
<td>% Program Files% (%SystemDrive%\Program Files)</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_PROGRAM_FILESX86</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Programme</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>% Program Files% (%SystemDrive%\Program Files)</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_ProgramFilesCommon"></span><span id="folderid_programfilescommon"></span><span id="FOLDERID_PROGRAMFILESCOMMON"></span><dl> <dt><strong>FOLDERID_ProgramFilesCommon</strong></dt> </dl></td>
<td style="text-align: left;"><p>Weitere Informationen finden Sie unter Hinweise.</p>

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
<td>%ProgramFiles%\Common files</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_PROGRAM_FILES_COMMON</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Allgemeine Dateien</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>%ProgramFiles%\Common files</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ProgramFilesCommonX64"></span><span id="folderid_programfilescommonx64"></span><span id="FOLDERID_PROGRAMFILESCOMMONX64"></span><dl> <dt><strong>FOLDERID_ProgramFilesCommonX64</strong></dt> </dl></td>
<td style="text-align: left;"><p>Weitere Informationen finden Sie unter Hinweise.</p>

<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{6365d5a7-0F-ID < </UI)</td>
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
<td>%ProgramFiles%\Common files</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>Keine</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Allgemeine Dateien</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>%ProgramFiles%\Common files</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_ProgramFilesCommonX86"></span><span id="folderid_programfilescommonx86"></span><span id="FOLDERID_PROGRAMFILESCOMMONX86"></span><dl> <dt><strong>FOLDERID_ProgramFilesCommonX86</strong></dt> </dl></td>
<td style="text-align: left;"><p>Weitere Informationen finden Sie unter Hinweise.</p>

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
<td>%ProgramFiles%\Common files</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_PROGRAM_FILES_COMMONX86</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Allgemeine Dateien</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>%ProgramFiles%\Common files</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Programs"></span><span id="folderid_programs"></span><span id="FOLDERID_PROGRAMS"></span><dl> <dt><strong>FOLDERID_Programs</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{A77F5D77-2E2B-44C3-A6A2-ABA601054A51}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Programs</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%APPDATA%\Microsoft\Windows\Start menu\programme</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_PROGRAMS</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Programs</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>%UserProfile%\startmenu\programme</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Public"></span><span id="folderid_public"></span><span id="FOLDERID_PUBLIC"></span><dl> <dt><strong>FOLDERID_Public</strong></dt> </dl></td>
<td style="text-align: left;">
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
<td>% Public% (%SystemDrive%\Users\Public)</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>Keine, neu für Windows Vista</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_PublicDesktop"></span><span id="folderid_publicdesktop"></span><span id="FOLDERID_PUBLICDESKTOP"></span><dl> <dt><strong>FOLDERID_PublicDesktop</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{C4AA340D-F20F-4863-Afef-F87EF2E6BA25}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Öffentlicher Desktop</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Gewöhnliche</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%Public%\Desktop</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_COMMON_DESKTOPDIRECTORY</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Desktop</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>%ALLUSERSPROFILE%\Desktop</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_PublicDocuments"></span><span id="folderid_publicdocuments"></span><span id="FOLDERID_PUBLICDOCUMENTS"></span><dl> <dt><strong>FOLDERID_PublicDocuments</strong></dt> </dl></td>
<td style="text-align: left;">
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
<td>Gewöhnliche</td>
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
<td>Legacy Anzeige Name</td>
<td>Freigegebene Dokumente</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>%ALLUSERSPROFILE%\Documents</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_PublicDownloads"></span><span id="folderid_publicdownloads"></span><span id="FOLDERID_PUBLICDOWNLOADS"></span><dl> <dt><strong>FOLDERID_PublicDownloads</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{3d644c9b-1B8-4f 30-9b45-b670235</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Öffentliche Downloads</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Gewöhnliche</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%Public%\downloads</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows Vista eingeführte Wert</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_PublicGameTasks"></span><span id="folderid_publicgametasks"></span><span id="FOLDERID_PUBLICGAMETASKS"></span><dl> <dt><strong>FOLDERID_PublicGameTasks</strong></dt> </dl></td>
<td style="text-align: left;">
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
<td>Gewöhnliche</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%ALLUSERSPROFILE%\microsoft\windows\gameexplorer</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows Vista eingeführte Wert</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_PublicLibraries"></span><span id="folderid_publiclibraries"></span><span id="FOLDERID_PUBLICLIBRARIES"></span><dl> <dt><strong>FOLDERID_PublicLibraries</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{48daf80b-e6cf-4f4e-B800-0e69d84ee384}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Bibliotheken</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Gewöhnliche</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%ALLUSERSPROFILE%\microsoft\windows\libraries</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows 7 eingeführte Wert</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_PublicMusic"></span><span id="folderid_publicmusic"></span><span id="FOLDERID_PUBLICMUSIC"></span><dl> <dt><strong>FOLDERID_PublicMusic</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{3214fab5-9757-4298-bb61-92a9de aa44ff}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Öffentliche Musik</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Gewöhnliche</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%Public%\Music</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_COMMON_MUSIC</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Freigegebene Musik</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>%ALLUSERSPROFILE%\documents\meine Musik</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_PublicPictures"></span><span id="folderid_publicpictures"></span><span id="FOLDERID_PUBLICPICTURES"></span><dl> <dt><strong>FOLDERID_PublicPictures</strong></dt> </dl></td>
<td style="text-align: left;">
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
<td>Gewöhnliche</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%Public%\Bilder</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_COMMON_PICTURES</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Freigegebene Bilder</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>%ALLUSERSPROFILE%\documents\eigene Bilder</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_PublicRingtones"></span><span id="folderid_publicringtones"></span><span id="FOLDERID_PUBLICRINGTONES"></span><dl> <dt><strong>FOLDERID_PublicRingtones</strong></dt> </dl></td>
<td style="text-align: left;">
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
<td>Gewöhnliche</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%ALLUSERSPROFILE%\microsoft\windows\ringtones</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows 7 eingeführte Wert</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_PublicUserTiles"></span><span id="folderid_publicusertiles"></span><span id="FOLDERID_PUBLICUSERTILES"></span><dl> <dt><strong>FOLDERID_PublicUserTiles</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{0482af6c-08b1-4c34-8c90e17ec98b1e17}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Öffentliche Konto Bilder</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Gewöhnliche</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%Public%\accountpictures</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows 8 eingeführte Wert</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_PublicVideos"></span><span id="folderid_publicvideos"></span><span id="FOLDERID_PUBLICVIDEOS"></span><dl> <dt><strong>FOLDERID_PublicVideos</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{2400183a-6185-49tb-a2d8-4a392a602ba3}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Öffentliche Videos</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Gewöhnliche</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%Public%\videos</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_COMMON_VIDEO</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Gemeinsam genutztes Video</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>%ALLUSERSPROFILE%\Documents\My Videos</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_QuickLaunch"></span><span id="folderid_quicklaunch"></span><span id="FOLDERID_QUICKLAUNCH"></span><dl> <dt><strong>FOLDERID_QuickLaunch</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{52a4f 021-7b75-48a9-9B a b87b-4b87a210bc8f}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Schnellstart</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%APPDATA%\microsoft\internet explorer\schnelllaunch</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>Keine</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Schnellstart</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>%APPDATA%\microsoft\internet explorer\schnelllaunch</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Recent"></span><span id="folderid_recent"></span><span id="FOLDERID_RECENT"></span><dl> <dt><strong>FOLDERID_Recent</strong></dt> </dl></td>
<td style="text-align: left;">
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
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%APPDATA%\microsoft\windows\recent</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_RECENT</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Meine letzten Dokumente</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>%UserProfile%\recent</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_RecordedTV"></span><span id="folderid_recordedtv"></span><span id="FOLDERID_RECORDEDTV"></span><dl> <dt><strong>FOLDERID_RecordedTV</strong></dt> </dl></td>
<td style="text-align: left;"><p>Nicht verwendet. Dieser Wert ist ab Windows 7 nicht definiert.</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_RecordedTVLibrary"></span><span id="folderid_recordedtvlibrary"></span><span id="FOLDERID_RECORDEDTVLIBRARY"></span><dl> <dt><strong>FOLDERID_RecordedTVLibrary</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{1a6f dba2-F42D-4358-A798-B74D745926C5}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>TV-Aufzeichnungen</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Gewöhnliche</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%Public%\recorddtv.Library-MS</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows 7 eingeführte Wert</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_RecycleBinFolder"></span><span id="folderid_recyclebinfolder"></span><span id="FOLDERID_RECYCLEBINFOLDER"></span><dl> <dt><strong>FOLDERID_RecycleBinFolder</strong></dt> </dl></td>
<td style="text-align: left;">
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
<td>Virtu</td>
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
<td>Legacy Anzeige Name</td>
<td>Papierkorb</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht zutreffend – virtueller Ordner</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_ResourceDir"></span><span id="folderid_resourcedir"></span><span id="FOLDERID_RESOURCEDIR"></span><dl> <dt><strong>FOLDERID_ResourceDir</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{8ad10c31-2adb-4296-A8F7-E4701232C972}</td>
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
<td>Legacy Anzeige Name</td>
<td>Ressourcen</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>%windir%\Resources</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Ringtones"></span><span id="folderid_ringtones"></span><span id="FOLDERID_RINGTONES"></span><dl> <dt><strong>FOLDERID_Ringtones</strong></dt> </dl></td>
<td style="text-align: left;">
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
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%LocalAppData%\microsoft\windows\ringtones</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows 7 eingeführte Wert</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_RoamingAppData"></span><span id="folderid_roamingappdata"></span><span id="FOLDERID_ROAMINGAPPDATA"></span><dl> <dt><strong>FOLDERID_RoamingAppData</strong></dt> </dl></td>
<td style="text-align: left;">
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
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>% APPDATA% (%USERPROFILE%\appdata\roaming)</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_APPDATA</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Anwendungsdaten</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>% APPDATA% (%USERPROFILE%\Anwendungsdaten)</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_RoamedTileImages"></span><span id="folderid_roamedtileimages"></span><span id="FOLDERID_ROAMEDTILEIMAGES"></span><dl> <dt><strong>FOLDERID_RoamedTileImages</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{AAA8D5A5-F1D6-4259-BAA8-78E7EF60835E}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Roamedtileimages</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%LocalAppData%\microsoft\windows\roamedtileimages</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows 8 eingeführte Wert</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_RoamingTiles"></span><span id="folderid_roamingtiles"></span><span id="FOLDERID_ROAMINGTILES"></span><dl> <dt><strong>FOLDERID_RoamingTiles</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{00bcfc5a-ed94-4e48-96aq1-3 f6217f21990}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Roamingtiles</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%LocalAppData%\microsoft\windows\roamingtiles</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows 8 eingeführte Wert</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SampleMusic"></span><span id="folderid_samplemusic"></span><span id="FOLDERID_SAMPLEMUSIC"></span><dl> <dt><strong>FOLDERID_SampleMusic</strong></dt> </dl></td>
<td style="text-align: left;">
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
<td>Gewöhnliche</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%Public%\music\sample Music</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>Keine</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Beispiel Musik</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>%ALLUSERSPROFILE%\Documents\My music\sample Music</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SamplePictures"></span><span id="folderid_samplepictures"></span><span id="FOLDERID_SAMPLEPICTURES"></span><dl> <dt><strong>FOLDERID_SamplePictures</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{C4900540-2379-4C75-844B-64E6FAF8716B}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Beispiel Bilder</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Gewöhnliche</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%Public%\pictures\beispielbilder</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>Keine</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Beispiel Bilder</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>%ALLUSERSPROFILE%\Documents\My Pictures\Sample Pictures</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SamplePlaylists"></span><span id="folderid_sampleplaylists"></span><span id="FOLDERID_SAMPLEPLAYLISTS"></span><dl> <dt><strong>FOLDERID_SamplePlaylists</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{15ca69b3-30ee-49c1-ace1-6b5ec372afb5}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Beispiel Wiedergabelisten</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Gewöhnliche</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%Public%\music\beispielwiedergabe Listen</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows Vista eingeführte Wert</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SampleVideos"></span><span id="folderid_samplevideos"></span><span id="FOLDERID_SAMPLEVIDEOS"></span><dl> <dt><strong>FOLDERID_SampleVideos</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{859ead94-2e85-48ad-A71A-0969cb56a6cd}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Beispiel Videos</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Gewöhnliche</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%Public%\videos\beispielvideos</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>Keine</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SavedGames"></span><span id="folderid_savedgames"></span><span id="FOLDERID_SAVEDGAMES"></span><dl> <dt><strong>FOLDERID_SavedGames</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{4c5c32ff-bb9d-43b0-b5b4-2d72e54eaaa4}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Gespeicherte Spiele</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%UserProfile%\Gespeicherte Spiele</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows Vista eingeführte Wert</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SavedPictures"></span><span id="folderid_savedpictures"></span><span id="FOLDERID_SAVEDPICTURES"></span><dl> <dt><strong>FOLDERID_SavedPictures</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{3b193882-D3AD-4eab-965A-69829d1b59f}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Gespeicherte Bilder</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%UserProfile%\pictures\gespeicherte Bilder</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>Keine</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SavedPicturesLibrary"></span><span id="folderid_savedpictureslibrary"></span><span id="FOLDERID_SAVEDPICTURESLIBRARY"></span><dl> <dt><strong>FOLDERID_SavedPicturesLibrary</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{E25B5812-BE88-4bd9-94B0-29233477B6C3}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Gespeicherte Bildbibliothek</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%Appdate%\microsoft\windows\libraries\savedpictures.Library-MS</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>Keine</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SavedSearches"></span><span id="folderid_savedsearches"></span><span id="FOLDERID_SAVEDSEARCHES"></span><dl> <dt><strong>FOLDERID_SavedSearches</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{7d1d3a04-Debb-4115-95cf-2f29da2920da}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Suchvorgänge</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%UserProfile%\suchen</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>Keine</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Screenshots"></span><span id="folderid_screenshots"></span><span id="FOLDERID_SCREENSHOTS"></span><dl> <dt><strong>FOLDERID_Screenshots</strong></dt> </dl></td>
<td style="text-align: left;">
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
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%UserProfile%\pictures\screenshots</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows 8 eingeführte Wert</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SEARCH_CSC"></span><span id="folderid_search_csc"></span><dl> <dt><strong>FOLDERID_SEARCH_CSC</strong></dt> </dl></td>
<td style="text-align: left;">
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
<td>Virtu</td>
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
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SearchHistory"></span><span id="folderid_searchhistory"></span><span id="FOLDERID_SEARCHHISTORY"></span><dl> <dt><strong>FOLDERID_SearchHistory</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{0d4c3db6-03a3-462-a0e6-08924c41b5d4}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Verlauf</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%LocalAppData%\microsoft\windows\connectedsearch\history</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows 8.1 eingeführte Wert</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SearchHome"></span><span id="folderid_searchhome"></span><span id="FOLDERID_SEARCHHOME"></span><dl> <dt><strong>FOLDERID_SearchHome</strong></dt> </dl></td>
<td style="text-align: left;">
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
<td>Virtu</td>
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
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SEARCH_MAPI"></span><span id="folderid_search_mapi"></span><dl> <dt><strong>FOLDERID_SEARCH_MAPI</strong></dt> </dl></td>
<td style="text-align: left;">
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
<td>Virtu</td>
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
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SearchTemplates"></span><span id="folderid_searchtemplates"></span><span id="FOLDERID_SEARCHTEMPLATES"></span><dl> <dt><strong>FOLDERID_SearchTemplates</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{7e636bfe-dfa9-4d5e-b456-d7b39851d8a9}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Vorlagen</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%LocalAppData%\microsoft\windows\connectedsearch\templates</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows 8.1 eingeführte Wert</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SendTo"></span><span id="folderid_sendto"></span><span id="FOLDERID_SENDTO"></span><dl> <dt><strong>FOLDERID_SendTo</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{8983036c-27c0-404b-8f08-102d10dcfd74}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>SendTo</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%APPDATA%\microsoft\windows\sendto</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_SENDTO</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>SendTo</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>%UserProfile%\SendTo</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SidebarDefaultParts"></span><span id="folderid_sidebardefaultparts"></span><span id="FOLDERID_SIDEBARDEFAULTPARTS"></span><dl> <dt><strong>FOLDERID_SidebarDefaultParts</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{7b396e54-9ec5-4300-be0a-2482ebae1a26}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Geschenken</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Gewöhnliche</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%ProgramFiles%\Windows sidebar\gadgets</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>Keine, neu für Windows 7</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SidebarParts"></span><span id="folderid_sidebarparts"></span><span id="FOLDERID_SIDEBARPARTS"></span><dl> <dt><strong>FOLDERID_SidebarParts</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{A75D362E-50FC-4fb7-AC2C-A8BEAA314493}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Geschenken</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%LocalAppData%\Microsoft\Windows sidebar\gadgets</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>Keine, neu für Windows 7</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SkyDrive"></span><span id="folderid_skydrive"></span><span id="FOLDERID_SKYDRIVE"></span><dl> <dt><strong>FOLDERID_SkyDrive</strong></dt> </dl></td>
<td style="text-align: left;">
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
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%UserProfile%\onedrive</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows 8.1 eingeführte Wert</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SkyDriveCameraRoll"></span><span id="folderid_skydrivecameraroll"></span><span id="FOLDERID_SKYDRIVECAMERAROLL"></span><dl> <dt><strong>FOLDERID_SkyDriveCameraRoll</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{767e6811-49cb-4273-87c2-20s355e1085b}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Kamera-Roll</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%UserProfile%\onedrive\pictures\camera Roll</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows 8.1 eingeführte Wert</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SkyDriveDocuments"></span><span id="folderid_skydrivedocuments"></span><span id="FOLDERID_SKYDRIVEDOCUMENTS"></span><dl> <dt><strong>FOLDERID_SkyDriveDocuments</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{24d89e24-2f19-4534-9dde -6a6671fbb8fe}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Dokumente</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%UserProfile%\onedrive\documents</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows 8.1 eingeführte Wert</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SkyDrivePictures"></span><span id="folderid_skydrivepictures"></span><span id="FOLDERID_SKYDRIVEPICTURES"></span><dl> <dt><strong>FOLDERID_SkyDrivePictures</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{339719b5-8c47-4894-94c2-d8b77add44a6}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Bilder</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%UserProfile%\onedrive\bilder</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows 8.1 eingeführte Wert</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_StartMenu"></span><span id="folderid_startmenu"></span><span id="FOLDERID_STARTMENU"></span><dl> <dt><strong>FOLDERID_StartMenu</strong></dt> </dl></td>
<td style="text-align: left;">
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
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%APPDATA%\microsoft\windows\startmenü</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_STARTMENU</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Startmenü</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>%UserProfile%\Startmenü</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Startup"></span><span id="folderid_startup"></span><span id="FOLDERID_STARTUP"></span><dl> <dt><strong>FOLDERID_Startup</strong></dt> </dl></td>
<td style="text-align: left;">
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
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%APPDATA%\Microsoft\Windows\Start menu\programs\startup</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_STARTUP CSIDL_ALTSTARTUP</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Start</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>%UserProfile%\Startmenü \ programme\startup</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SyncManagerFolder"></span><span id="folderid_syncmanagerfolder"></span><span id="FOLDERID_SYNCMANAGERFOLDER"></span><dl> <dt><strong>FOLDERID_SyncManagerFolder</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{43668bf 8-c14e-49b2-97c9-747784d784b7}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Synchronisierungscenter</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Virtu</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>Nicht zutreffend – virtueller Ordner</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows Vista eingeführte Wert</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SyncResultsFolder"></span><span id="folderid_syncresultsfolder"></span><span id="FOLDERID_SYNCRESULTSFOLDER"></span><dl> <dt><strong>FOLDERID_SyncResultsFolder</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{289a9a43-be44-4057-a41b-587a76d7e7f}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Ergebnisse synchronisieren</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Virtu</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>Nicht zutreffend – virtueller Ordner</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows Vista eingeführte Wert</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SyncSetupFolder"></span><span id="folderid_syncsetupfolder"></span><span id="FOLDERID_SYNCSETUPFOLDER"></span><dl> <dt><strong>FOLDERID_SyncSetupFolder</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{0F 214138-b1d3-4 a90bba9-27cbc0c5389a}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Sync-Setup</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Virtu</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>Nicht zutreffend – virtueller Ordner</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows Vista eingeführte Wert</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_System"></span><span id="folderid_system"></span><span id="FOLDERID_SYSTEM"></span><dl> <dt><strong>FOLDERID_System</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{1ac14e77-02e7-4e5d-B744-2eb1ae5198b7}</td>
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
<td>%WINDIR%\System32</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_SYSTEM</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>system32</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>%WINDIR%\System32</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SystemX86"></span><span id="folderid_systemx86"></span><span id="FOLDERID_SYSTEMX86"></span><dl> <dt><strong>FOLDERID_SystemX86</strong></dt> </dl></td>
<td style="text-align: left;">
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
<td>%WINDIR%\System32</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_SYSTEMX86</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>system32</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>%WINDIR%\System32</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Templates"></span><span id="folderid_templates"></span><span id="FOLDERID_TEMPLATES"></span><dl> <dt><strong>FOLDERID_Templates</strong></dt> </dl></td>
<td style="text-align: left;">
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
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%APPDATA%\microsoft\windows\templates</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>CSIDL_TEMPLATES</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Vorlagen</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>%UserProfile%\Vorlagen</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_TreeProperties"></span><span id="folderid_treeproperties"></span><span id="FOLDERID_TREEPROPERTIES"></span><dl> <dt><strong>FOLDERID_TreeProperties</strong></dt> </dl></td>
<td style="text-align: left;"><p>Wird in Windows Vista nicht verwendet. Wird ab Windows 7 nicht mehr unterstützt.</p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_UserPinned"></span><span id="folderid_userpinned"></span><span id="FOLDERID_USERPINNED"></span><dl> <dt><strong>FOLDERID_UserPinned</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{9e3995ab-1B-4 b827-48b24b6c7174}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Benutzer fixiert</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%APPDATA%\microsoft\internet Explorer\Quick launch\benutzerpinned</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows 7 eingeführte Wert</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_UserProfiles"></span><span id="folderid_userprofiles"></span><span id="FOLDERID_USERPROFILES"></span><dl> <dt><strong>FOLDERID_UserProfiles</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{0762d272-c50a-4bb0-a382-697dcd729b80}</td>
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
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_UserProgramFiles"></span><span id="folderid_userprogramfiles"></span><span id="FOLDERID_USERPROGRAMFILES"></span><dl> <dt><strong>FOLDERID_UserProgramFiles</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{5cd7aee2-2219-4a67-b85d-6c9ce15660cb}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Programs</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%LocalAppData%\Programme</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows 7 eingeführte Wert</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_UserProgramFilesCommon"></span><span id="folderid_userprogramfilescommon"></span><span id="FOLDERID_USERPROGRAMFILESCOMMON"></span><dl> <dt><strong>FOLDERID_UserProgramFilesCommon</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{BCBD3057-CA5C-4622-B42D-BC56DB0AE516}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Programs</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%LocalAppData%\Programme\Common</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows 7 eingeführte Wert</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_UsersFiles"></span><span id="folderid_usersfiles"></span><span id="FOLDERID_USERSFILES"></span><dl> <dt><strong>FOLDERID_UsersFiles</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{f3ce0f7c-4901-4acc-8648-d5d44b04ef8f}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Der vollständige Name des Benutzers (z.b. Jean Philippe Bagel), der beim Erstellen des Benutzerkontos eingegeben wurde.</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Virtu</td>
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
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_UsersLibraries"></span><span id="folderid_userslibraries"></span><span id="FOLDERID_USERSLIBRARIES"></span><dl> <dt><strong>FOLDERID_UsersLibraries</strong></dt> </dl></td>
<td style="text-align: left;">
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
<td>Virtu</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>Nicht zutreffend – virtueller Ordner</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows 7 eingeführte Wert</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Videos"></span><span id="folderid_videos"></span><span id="FOLDERID_VIDEOS"></span><dl> <dt><strong>FOLDERID_Videos</strong></dt> </dl></td>
<td style="text-align: left;">
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
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%UserProfile%\videos</td>
</tr>
<tr class="odd">
<td>CSIDL</td>
<td>CSIDL_MYVIDEO</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Meine Videos</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>%USERPROFILE%\Eigene Dateien\Eigene Videos</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_VideosLibrary"></span><span id="folderid_videoslibrary"></span><span id="FOLDERID_VIDEOSLIBRARY"></span><dl> <dt><strong>FOLDERID_VideosLibrary</strong></dt> </dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td>GUID</td>
<td>{491e922f -5643-4af4-A7EB-4e7a138d8174}</td>
</tr>
<tr class="even">
<td>Anzeigename</td>
<td>Videos</td>
</tr>
<tr class="odd">
<td>Ordnertyp</td>
<td>Peruser</td>
</tr>
<tr class="even">
<td>Standard Path</td>
<td>%APPDATA%\microsoft\windows\libraries\videos.Library-MS</td>
</tr>
<tr class="odd">
<td>CSIDL-Entsprechung</td>
<td>None, in Windows 7 eingeführte Wert</td>
</tr>
<tr class="even">
<td>Legacy Anzeige Name</td>
<td>Nicht verfügbar</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>Nicht verfügbar</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Windows"></span><span id="folderid_windows"></span><span id="FOLDERID_WINDOWS"></span><dl> <dt><strong>FOLDERID_Windows</strong></dt> </dl></td>
<td style="text-align: left;">
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
<td>Legacy Anzeige Name</td>
<td>WINDOWS</td>
</tr>
<tr class="odd">
<td>Standardpfad für Legacy</td>
<td>%windir%</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Bemerkungen

Die Interpretation bestimmter **KNOWNFOLDERID** -Werte hängt davon ab, ob der Ordner Teil einer 32-Bit-oder einer 64-Bit-Anwendung ist und ob diese Anwendung unter einem 32-Bit-oder 64-Bit-Betriebssystem ausgeführt wird. Wenn Ihre Anwendung zwischen z. b. **Programmdateien** und **Programmdateien (x86)** unterscheiden muss, müssen Sie die richtige **KNOWNFOLDERID** für die Situation verwenden.

In den folgenden Tabellen wird die Verwendung von **KNOWNFOLDERID** in diesen Fällen zusammengefasst.


**Folderid- \_ Programmdateien** 

| Betriebssystem | Application | KNOWNFOLDERID | Standard Path | CSIDL-Entsprechung |
|------------------|-------------|---------------|--------------|------------------|  
| 32-Bit | 32-Bit | Folderid- \_ Programmdateien | % System Drive%- \\ Programmdateien | CSIDL- \_ Programm \_ Dateien |
| 32-Bit | 32-Bit | Folderid \_ ProgramFilesX86 | % System Drive%- \\ Programmdateien | CSIDL- \_ Programm \_ FILESX86 |
| 32-Bit | 32-Bit | Folderid \_ ProgramFilesX64 (wird unter 32-Bit-Betriebssystemen nicht unterstützt) | Nicht verfügbar | Nicht verfügbar |
| 64-Bit | 64-Bit | Folderid- \_ Programmdateien | % System Drive%- \\ Programmdateien | CSIDL- \_ Programm \_ Dateien |
| 64-Bit | 64-Bit | Folderid \_ ProgramFilesX86 | % System Drive% \\ Program Files (x86) | CSIDL- \_ Programm \_ FILESX86 |
| 64-Bit | 64-Bit | Folderid \_ ProgramFilesX64 | % System Drive%- \\ Programmdateien | Keine |
| 64-Bit | 32-Bit | Folderid- \_ Programmdateien | % System Drive% \\ Program Files (x86) | CSIDL- \_ Programm \_ Dateien |
| 64-Bit | 32-Bit | Folderid \_ ProgramFilesX86 | % System Drive% \\ Program Files (x86) | CSIDL- \_ Programm \_ FILESX86 |
| 64-Bit | 32-Bit | Folderid \_ ProgramFilesX64 (wird für 32-Bit-Anwendungen nicht unterstützt) | Nicht verfügbar | Nicht verfügbar |


**Folderid \_ programfilescommon**

| Betriebssystem | Application | KNOWNFOLDERID | Standard Path | CSIDL-Entsprechung |
|------------------|-------------|---------------|--------------|------------------|  
| 32-Bit | 32-Bit | Folderid \_ programfilescommon | % Program Files% \\ Allgemeine Dateien | Allgemeine CSIDL- \_ Programm \_ Dateien \_ |
| 32-Bit | 32-Bit | Folderid \_ ProgramFilesCommonX86 | % Program Files% \\ Allgemeine Dateien | CSIDL- \_ Programm \_ Dateien \_ COMMONX86 |
| 32-Bit | 32-Bit | Folderid \_ ProgramFilesCommonX64 (nicht definiert) | Nicht verfügbar | Nicht verfügbar |
| 64-Bit | 64-Bit | Folderid \_ programfilescommon | % Program Files% \\ Allgemeine Dateien | Allgemeine CSIDL- \_ Programm \_ Dateien \_ |
| 64-Bit | 64-Bit | Folderid \_ ProgramFilesCommonX86 | % Program Files (x86)% \\ Allgemeine Dateien | CSIDL- \_ Programm \_ Dateien \_ COMMONX86 |
| 64-Bit | 64-Bit | Folderid \_ ProgramFilesCommonX64 | % Program Files% \\ Allgemeine Dateien | Keine |
| 64-Bit | 32-Bit | Folderid \_ programfilescommon | % Program Files (x86)% \\ Allgemeine Dateien | Allgemeine CSIDL- \_ Programm \_ Dateien \_ |
| 64-Bit | 32-Bit | Folderid \_ ProgramFilesCommonX86 | % Program Files (x86)% \\ Allgemeine Dateien | CSIDL- \_ Programm \_ Dateien \_ COMMONX86 |
| 64-Bit | 32-Bit | Folderid \_ ProgramFilesCommonX64 | % Program Files% \\ Allgemeine Dateien | Keine |


**Folderid- \_ System**

| Betriebssystem | Application | KNOWNFOLDERID | Standard Path | CSIDL-Entsprechung |
|------------------|-------------|---------------|--------------|------------------|  
| 32-Bit | 32-Bit | Folderid- \_ System | % windir% \\ system32 | CSIDL- \_ System |
| 32-Bit | 32-Bit | Folderid \_ SystemX86 | % windir% \\ system32 | CSIDL- \_ SYSTEMX86 |
| 64-Bit | 64-Bit | Folderid- \_ System | % windir% \\ system32 | CSIDL- \_ System |
| 64-Bit | 64-Bit | Folderid \_ SystemX86 | % windir% \\ syswow64 | CSIDL- \_ SYSTEMX86 |
| 64-Bit | 32-Bit | Folderid- \_ System | % windir% \\ system32 | CSIDL- \_ System |
| 64-Bit | 32-Bit | Folderid \_ SystemX86 | % windir% \\ syswow64 | CSIDL- \_ SYSTEMX86 |


Wir haben Umgebungs Zeichenfolgen verwendet, um generische Pfade in diesem Thema bereitzustellen. Die folgenden Tabellen stellen Beispiele für die Pfade dar, die diese Umgebungs Zeichenfolgen darstellen. In einigen Fällen Stimmen diese Pfade möglicherweise nicht mit denen auf einem bestimmten Computer zu, da Sie während der Installation oder einer späteren Ordner Umleitung ausgewählt wurden. Beachten Sie, dass einige Pfade für Windows Vista geändert wurden.


**Windows Vista und höher**

| Umgebungs Zeichenfolge | Beispiel Pfad |
|--------------------|--------------|
| %ALLUSERSPROFILE% | C: \\ programmdata |
| %APPDATA% | C: \\ Benutzer \\ *Benutzername* \\ AppData \\ Roaming |
| LocalAppData | C: \\ Benutzer \\ *Benutzername* \\ AppData \\ local |
| %ProgramData% | C: \\ programmdata |
| %ProgramFiles% | C: \\ Programmdateien |
| %ProgramFiles(x86)% | C: \\ Programmdateien (x86) |
| Publikums | C: \\ \\ öffentliche Benutzer |
| %SystemDrive% | C: |
| %USERPROFILE% | C: \\ Benutzer \\ *Benutzername* |
| %windir% | C: \\ Windows |


**Windows XP und früher**

| Umgebungs Zeichenfolge | Beispiel Pfad |
|--------------------|--------------|
| %ALLUSERSPROFILE% | C: \\ Dokumente und Einstellungen \\ alle Benutzer |
| %APPDATA% | C: \\ Dokumente und Einstellungen \\ *Benutzername* \\ Anwendungsdaten |
| %ProgramFiles% | C: \\ Programmdateien |
| %SystemDrive% | C: |
| %USERPROFILE% | C: \\ \\ *Benutzername* für Dokumente und Einstellungen |
| %windir% | C: \\ Windows |


## <a name="requirements"></a>Requirements (Anforderungen)


| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>KnownFolders. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

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

 

 
