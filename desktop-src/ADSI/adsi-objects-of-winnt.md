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
# <a name="adsi-objects-of-winnt"></a>ADSI-Objekte von Winnt

Der ADSI WinNT-Anbieter implementiert die folgenden COM-Objekte, um Features und Dienste verschiedener ADSI-Schnittstellen zu unterstützen.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>ADSI-Objekt</th>
<th>BESCHREIBUNG</th>
<th>Unterstützte Schnittstellen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Klasse</strong></td>
<td>Ein ADSI-Objekt, das eine Klassendefinition darstellt.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadsclass"> <strong>iadsclass</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>Computer</strong></td>
<td>Ein ADSI-Objekt, das einen Computer darstellt.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscomputer"><strong>iadscomputer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscomputeroperations"><strong>iadscomputeroperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>Domäne</strong></td>
<td>Ein ADSI-Objekt, das eine Domäne über das Netzwerk darstellt.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsdomain"><strong>iadsdomain</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>File Service</strong></td>
<td>Ein ADSI-Objekt, das einen Datei Dienst darstellt.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileservice"><strong>iadsfileservice</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations"><strong>iadsfileserviceoperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>FileShare</strong></td>
<td>Ein ADSI-Objekt, das eine Dateifreigabe darstellt.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileshare"><strong>iadsfileshare</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>Fpnwfileservice</strong></td>
<td>Ein ADSI-Objekt, das einen Datei Dienst darstellt.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileservice"><strong>iadsfileservice</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations"><strong>iadsfileserviceoperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>Fpnwfileshare</strong></td>
<td>Ein ADSI-Objekt, das eine Dateifreigabe darstellt.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileshare"><strong>iadsfileshare</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>Fpnwresource</strong></td>
<td>Ein ADSI-Objekt, das eine Ressource darstellt.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsresource"><strong>iadsresource</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>Fpnwresourcescollection</strong></td>
<td>Ein ADSI-Objekt, das eine Auflistung von Ressourcen darstellt.</td>
<td><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>Iadscollection</strong></a></td>
</tr>
<tr class="even">
<td><strong>Fpnwsession</strong></td>
<td>Ein ADSI-Objekt, das eine Sitzung darstellt.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadssession"><strong>iadssession</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>Fpnwsessionscollection</strong></td>
<td>Ein ADSI-Objekt, das eine Auflistung von Sitzungen darstellt.</td>
<td><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>Iadscollection</strong></a></td>
</tr>
<tr class="even">
<td><strong>Gruppieren</strong></td>
<td>Ein ADSI-Objekt, das eine Gruppe darstellt.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsgroup"><strong>IADsGroup</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl>
<blockquote>
[!Note]<br />
GetInfo kann nicht für Gruppen verwendet werden, die Mitglieder mit bekannten Sicherheits Prinzipalen im WinNT-Bereich enthalten.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>GroupCollection</strong></td>
<td>Ein ADSI-Objekt, das eine Auflistung von Gruppen darstellt.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"> <strong>iadsmembers</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>LocalGroup</strong></td>
<td>Ein ADSI-Objekt, das eine lokale Gruppe darstellt.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsgroup"><strong>IADsGroup</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>Localgroupcollection</strong></td>
<td>Ein ADSI-Objekt, das eine Auflistung von lokalen Gruppen darstellt.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"> <strong>iadsmembers</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>Namespace</strong></td>
<td>Ein ADSI-Objekt, das den WinNT-Namespace darstellt.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsopendsobject"><strong>iadsopendsobject</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>PrintJob</strong></td>
<td>Ein ADSI-Objekt, das einen Druckauftrag darstellt.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintjob"><strong>iadsprintjob</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations"><strong>iadsprintjoboperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>Printjobscollection</strong></td>
<td>Ein ADSI-Objekt, das eine Auflistung von Druckaufträgen darstellt.</td>
<td><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>Iadscollection</strong></a></td>
</tr>
<tr class="odd">
<td><strong>PrintQueue</strong></td>
<td>Ein ADSI-Objekt, das eine Druck Warteschlange darstellt.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintqueue"><strong>iadsprintqueue</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations"><strong>iadsprintqueueoperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>Eigenschaft</strong></td>
<td>Ein ADSI-Objekt, das eine Attribut Definition darstellt.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadsproperty"> <strong>iadsproperty</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>Ressource</strong></td>
<td>Ein ADSI-Objekt, das eine Ressource darstellt.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsresource"><strong>iadsresource</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>Resourcescollection</strong></td>
<td>Ein ADSI-Objekt, das eine Auflistung von Ressourcen darstellt.</td>
<td><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>Iadscollection</strong></a></td>
</tr>
<tr class="odd">
<td><strong>Schema</strong></td>
<td>Ein ADSI-Objekt, das den Schema Container darstellt.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"> <strong>IADsContainer</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>Service</strong></td>
<td>Ein ADSI-Objekt, das einen Dienst darstellt.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsservice"><strong>iadsservice</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsserviceoperations"><strong>iadsserviceoperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>Sitzung</strong></td>
<td>Ein ADSI-Objekt, das eine Sitzung darstellt.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadssession"><strong>iadssession</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>Sessionscollection</strong></td>
<td>Ein ADSI-Objekt, das eine Auflistung von Sitzungen darstellt.</td>
<td><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>Iadscollection</strong></a></td>
</tr>
<tr class="odd">
<td><strong>Syntax</strong></td>
<td>Ein ADSI-Objekt, das die Syntax eines Attributs darstellt.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadssyntax"> <strong>iadssyntax</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>Benutzer</strong></td>
<td>Ein ADSI-Objekt, das ein Benutzerkonto darstellt.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsuser"><strong>IADsUser</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>Usergroupcollection</strong></td>
<td>Ein ADSI-Objekt, das eine Auflistung von Benutzergruppen darstellt.</td>
<td><a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"><strong>Iadsmembers</strong></a></td>
</tr>
</tbody>
</table>



 

 

 





