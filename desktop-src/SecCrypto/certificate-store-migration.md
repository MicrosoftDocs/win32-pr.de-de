---
description: Während eines Computerupgrades oder einer Computer-zu-Computer-Migration werden die Zertifikate in bestimmten Zertifikatspeichern migriert.
ms.assetid: fe81d578-f2f6-41f0-9ebf-e7bd5532bed9
title: Migration Store Zertifikaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7de694fc24433ce8db039dd677f52935da70cbf07d0a719b0871bd1e8f4b2d35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771096"
---
# <a name="certificate-store-migration"></a>Migration Store Zertifikaten

Während eines Computerupgrades oder einer Computer-zu-Computer-Migration werden die Zertifikate in bestimmten Zertifikatspeichern migriert. In der folgenden Tabelle sind die Zertifikatspeicher aufgeführt, die standardmäßig migriert werden. Für den AcRS-Speicher (Automatic Certificate Request Einstellungen) werden nur die Zertifikatvertrauenslisten (Certificate [*Trust Lists,*](../secgloss/c-gly.md) CTLs) migriert. Für alle anderen unten aufgeführten Speicher werden nur die Zertifikate migriert.

<table>
<thead>
<tr class="header">
<th>System/Benutzer</th>
<th>Speicher</th>
<th>Speicherort</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>${ROWSPAN8}$System${REMOVE}$<br />
</td>
<td>ROOT</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>SOFTWARE</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>Root</strong> \ <strong>Zertifikate</strong><br/></td>
</tr>
<tr class="even">
<td>MY</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>SOFTWARE</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>My</strong> \ <strong>Zertifikate</strong><br/></td>

</tr>
<tr class="odd">
<td>ANFORDERUNG</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>SOFTWARE</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>Anforderung</strong> \ <strong>Zertifikate</strong><br/></td>

</tr>
<tr class="even">
<td>TrustedPublisher</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>SOFTWARE</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>TrustedPublisher</strong> \ <strong>Zertifikate</strong><br/></td>

</tr>
<tr class="odd">
<td>TrustedPeople</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>SOFTWARE</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>TrustedPeople</strong> \ <strong>Zertifikate</strong><br/></td>

</tr>
<tr class="even">
<td>Unzulässig</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>SOFTWARE</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>Nicht verfügbar</strong> \ <strong>Zertifikate</strong><br/></td>

</tr>
<tr class="odd">
<td>CA</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>SOFTWARE</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>Zertifizierungsstelle</strong> \ <strong>Zertifikate</strong><br/></td>

</tr>
<tr class="even">
<td>ACRS</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>SOFTWARE</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>ACRS</strong> \ <strong>CTLs</strong><br/></td>

</tr>
<tr class="odd">
<td rowspan="7">User${REMOVE}$<br />
</td>
<td>ROOT</td>
<td><strong>HKEY_CURRENT_USER</strong> \ <strong>SOFTWARE</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>Root</strong> \ <strong>Zertifikate</strong><br/></td>
</tr>
<tr class="even">
<td>MY</td>
<td>Datei: \\ %APPDATA%\Microsoft\SystemCertificates\My\Certificates</td>

</tr>
<tr class="odd">
<td>ANFORDERUNG</td>
<td>Datei: \\ %APPDATA%\Microsoft\SystemCertificates\Request\Certificates</td>

</tr>
<tr class="even">
<td>TrustedPublisher</td>
<td><strong>HKEY_CURRENT_USER</strong> \ <strong>SOFTWARE</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>TrustedPublisher</strong> \ <strong>Zertifikate</strong><br/></td>

</tr>
<tr class="odd">
<td>TrustedPeople</td>
<td><strong>HKEY_CURRENT_USER</strong> \ <strong>SOFTWARE</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>TrustedPeople</strong> \ <strong>Zertifikate</strong><br/></td>

</tr>
<tr class="even">
<td>Unzulässig</td>
<td><strong>HKEY_CURRENT_USER</strong> \ <strong>SOFTWARE</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>Nicht verfügbar</strong> \ <strong>Zertifikate</strong><br/></td>

</tr>
<tr class="odd">
<td>CA</td>
<td><strong>HKEY_CURRENT_USER</strong> \ <strong>SOFTWARE</strong> \ <strong>Microsoft</strong> \ <strong>SystemCertificates</strong> \ <strong>Zertifizierungsstelle</strong> \ <strong>Zertifikate</strong><br/></td>

</tr>
</tbody>
</table>



 

Andere von Anwendungen erstellte Zertifikatspeicher werden standardmäßig nicht migriert. Anwendungen, die eigene Filialen erstellen, sind für die Migration der von ihnen erstellten Filialen verantwortlich. Zum Erstellen von Speichern wird empfohlen, einen Registrierungsschlüssel in den Anwendungseinstellungen zu definieren und einen Speicher innerhalb der Registrierungseinstellungen mithilfe des **CERT \_ STORE \_ PROV REG-Speicheranbieters \_** zu erstellen. Weitere Informationen zum Migrieren von Anwendungseinstellungen finden Sie im Thema How To Create a Custom .xml File (Erstellen einer benutzerdefinierten *.xml-Datei)* im Leitfaden *Using USMT 3.0 (Verwenden von USMT 3.0)* unter [Migrationstool für den Benutzerstatus 3.0](https://www.microsoft.com/technet/windowsvista/library/91f62fc4-621f-4537-b311-1307df010561.mspx). (Diese Ressource ist in einigen Sprachen und Ländern oder Regionen möglicherweise nicht verfügbar.)

 

 
