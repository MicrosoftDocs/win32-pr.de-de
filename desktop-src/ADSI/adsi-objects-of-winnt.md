---
title: ADSI Objects of WinNT
description: Der ADSI WinNT-Anbieter implementiert die folgenden COM-Objekte, um Features und Dienste verschiedener ADSI-Schnittstellen zu unterstützen.
ms.assetid: ce6f8638-aa9e-4036-b597-077da4c3c534
ms.tgt_platform: multiple
keywords:
- WinNT-Dienstanbieter ADSI , ADSI-Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93332a2b0501c9c7c4140d83ff7358f18ae68adc50f9f9f3b689765d947ef01c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118180584"
---
# <a name="adsi-objects-of-winnt"></a>ADSI Objects of WinNT

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
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadsclass"> <strong>IADsClass</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>Computer</strong></td>
<td>Ein ADSI-Objekt, das einen Computer darstellt.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscomputer"><strong>IADsComputer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscomputeroperations"><strong>IADsComputerOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>Domain</strong></td>
<td>Ein ADSI-Objekt, das eine Domäne über das Netzwerk darstellt.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsdomain"><strong>IADsDomain</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>FileService</strong></td>
<td>Ein ADSI-Objekt, das einen Dateidienst darstellt.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileservice"><strong>IADsFileService</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations"><strong>IADsFileServiceOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>FileShare</strong></td>
<td>Ein ADSI-Objekt, das eine Dateifreigabe darstellt.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileshare"><strong>IADsFileShare</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>FPNWFileService</strong></td>
<td>Ein ADSI-Objekt, das einen Dateidienst darstellt.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileservice"><strong>IADsFileService</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations"><strong>IADsFileServiceOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>FPNWFileShare</strong></td>
<td>Ein ADSI-Objekt, das eine Dateifreigabe darstellt.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsfileshare"><strong>IADsFileShare</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>FPNWResource</strong></td>
<td>Ein ADSI-Objekt, das eine Ressource darstellt.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsresource"><strong>IADsRessourcen-IADsPropertyList</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong></strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>FPNWResourcesCollection</strong></td>
<td>Ein ADSI-Objekt, das eine Auflistung von Ressourcen darstellt.</td>
<td><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></td>
</tr>
<tr class="even">
<td><strong>FPNWSession</strong></td>
<td>Ein ADSI-Objekt, das eine Sitzung darstellt.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadssession"><strong>IADsSession</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>FPNWSessionsCollection</strong></td>
<td>Ein ADSI-Objekt, das eine Auflistung von Sitzungen darstellt.</td>
<td><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></td>
</tr>
<tr class="even">
<td><strong>Gruppe</strong></td>
<td>Ein ADSI-Objekt, das eine Gruppe darstellt.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsgroup"><strong>IADsGroup</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl>
<blockquote>
[!Note]<br />
GetInfo kann nicht für Gruppen verwendet werden, die Mitglieder enthalten, die bekannte Sicherheitsprinzipale im WinNT-Bereich sind.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><strong>Groupcollection</strong></td>
<td>Ein ADSI-Objekt, das eine Auflistung von Gruppen darstellt.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"> <strong>IADsMembers</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>Localgroup</strong></td>
<td>Ein ADSI-Objekt, das eine lokale Gruppe darstellt.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsgroup"><strong>IADsGroup</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>LocalgroupCollection</strong></td>
<td>Ein ADSI-Objekt, das eine Auflistung lokaler Gruppen darstellt.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"> <strong>IADsMembers</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>Namespace</strong></td>
<td>Ein ADSI-Objekt, das den WinNT-Namespace darstellt.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"><strong>IADsContainer</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsopendsobject"><strong>IADsOpenDSObject</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>Printjob</strong></td>
<td>Ein ADSI-Objekt, das einen Druckauftrag darstellt.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintjob"><strong>IADsPrintJob</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations"><strong>IADsPrintJobOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>PrintJobsCollection</strong></td>
<td>Ein ADSI-Objekt, das eine Auflistung von Druckaufträgen darstellt.</td>
<td><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></td>
</tr>
<tr class="odd">
<td><strong>PrintQueue</strong></td>
<td>Ein ADSI-Objekt, das eine Druckwarteschlange darstellt.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintqueue"><strong>IADsPrintQueue</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations"><strong>IADsPrintQueueOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>Eigenschaft</strong></td>
<td>Ein ADSI-Objekt, das eine Attributdefinition darstellt.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadsproperty"> <strong>IADsProperty</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>Ressource</strong></td>
<td>Ein ADSI-Objekt, das eine Ressource darstellt.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsresource"><strong>IADsRessourcen-IADsPropertyList</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong></strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>ResourcesCollection</strong></td>
<td>Ein ADSI-Objekt, das eine Auflistung von Ressourcen darstellt.</td>
<td><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></td>
</tr>
<tr class="odd">
<td><strong>Schema</strong></td>
<td>Ein ADSI-Objekt, das den Schemacontainer darstellt.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadscontainer"> <strong>IADsContainer</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>Service</strong></td>
<td>Ein ADSI-Objekt, das einen Dienst darstellt.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsservice"><strong>IADsService</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsserviceoperations"><strong>IADsServiceOperations</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>Sitzungskonsistenz</strong></td>
<td>Ein ADSI-Objekt, das eine Sitzung darstellt.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadssession"><strong>IADsSession</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>SessionsCollection</strong></td>
<td>Ein ADSI-Objekt, das eine Auflistung von Sitzungen darstellt.</td>
<td><a href="/windows/desktop/api/Iads/nn-iads-iadscollection"><strong>IADsCollection</strong></a></td>
</tr>
<tr class="odd">
<td><strong>Syntax</strong></td>
<td>Ein ADSI-Objekt, das die Syntax eines Attributs darstellt.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt> <a href="/windows/desktop/api/Iads/nn-iads-iadssyntax"> <strong>IADsSyntax</strong></a></dt> </dl></td>
</tr>
<tr class="even">
<td><strong>Benutzer</strong></td>
<td>Ein ADSI-Objekt, das ein Benutzerkonto darstellt.</td>
<td><dl> <dt><a href="/windows/desktop/api/Iads/nn-iads-iads"><strong>IADs</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadsuser"><strong>IADsUser</strong></a></dt> <dt><a href="/windows/desktop/api/Iads/nn-iads-iadspropertylist"><strong>IADsPropertyList</strong></a></dt> </dl></td>
</tr>
<tr class="odd">
<td><strong>UserGroupCollection</strong></td>
<td>Ein ADSI-Objekt, das eine Auflistung von Benutzergruppen darstellt.</td>
<td><a href="/windows/desktop/api/Iads/nn-iads-iadsmembers"><strong>IADsMembers</strong></a></td>
</tr>
</tbody>
</table>



 

 

 





