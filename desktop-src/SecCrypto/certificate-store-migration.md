---
description: Während eines Computer Upgrades oder einer Computer-zu-Computer-Migration werden die Zertifikate in bestimmten Zertifikat speichern migriert.
ms.assetid: fe81d578-f2f6-41f0-9ebf-e7bd5532bed9
title: Zertifikat Speicher Migration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a31b42b83718aa1cab786ad79cc2df754b8fd9b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050273"
---
# <a name="certificate-store-migration"></a>Zertifikat Speicher Migration

Während eines Computer Upgrades oder einer Computer-zu-Computer-Migration werden die Zertifikate in bestimmten Zertifikat speichern migriert. In der folgenden Tabelle sind die Zertifikat Speicher aufgelistet, die standardmäßig migriert werden. Für den automatischen Speicher der Zertifikat Anforderungs Einstellungen (ACRS) werden nur die [*Zertifikat Vertrauens Listen*](../secgloss/c-gly.md) (CTLs) migriert. Für alle anderen unten aufgeführten Geschäfte werden nur die Zertifikate migriert.

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
<td>$ {ROWSPAN8} $System $ {Remove} $<br />
</td>
<td>ROOT</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>System Zertifikate</strong> \ <strong></strong> Stamm \ <strong>Zertifikate</strong><br/></td>
</tr>
<tr class="even">
<td>MY</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>System Zertifikate</strong> \ <strong>Meine</strong> \ <strong>Zertifikate</strong><br/></td>

</tr>
<tr class="odd">
<td>ANFORDERUNG</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>System Zertifikate</strong> \ <strong>Anforderung</strong> \ <strong>Zertifikate</strong><br/></td>

</tr>
<tr class="even">
<td>TrustedPublisher</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>System Zertifikate</strong> \ <strong>Treuhänder Publisher</strong> \ <strong>Zertifikate</strong><br/></td>

</tr>
<tr class="odd">
<td>TrustedPeople</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>System Zertifikate</strong> \ <strong>Treuhänder</strong> \ <strong>Zertifikate</strong><br/></td>

</tr>
<tr class="even">
<td>Unzulässig</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>System Zertifikate</strong> \ Nicht <strong>zulässig</strong> \ <strong>Zertifikate</strong><br/></td>

</tr>
<tr class="odd">
<td>CA</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>System Zertifikate</strong> \ Zertifizierungsstelle <strong></strong> \ <strong>Zertifikate</strong><br/></td>

</tr>
<tr class="even">
<td>ACRS</td>
<td><strong>HKEY_LOCAL_MACHINE</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>System Zertifikate</strong> \ <strong>ACRS</strong> \ <strong>CTLs</strong><br/></td>

</tr>
<tr class="odd">
<td rowspan="7">Benutzer $ {Remove} $<br />
</td>
<td>ROOT</td>
<td><strong>HKEY_CURRENT_USER</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>System Zertifikate</strong> \ <strong></strong> Stamm \ <strong>Zertifikate</strong><br/></td>
</tr>
<tr class="even">
<td>MY</td>
<td>Datei: \\ %AppData%\microsoft\systemcertifieres\my\zertifikate</td>

</tr>
<tr class="odd">
<td>ANFORDERUNG</td>
<td>Datei: \\ %AppData%\microsoft\systemcertifieres\request\zertifikate</td>

</tr>
<tr class="even">
<td>TrustedPublisher</td>
<td><strong>HKEY_CURRENT_USER</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>System Zertifikate</strong> \ <strong>Treuhänder Publisher</strong> \ <strong>Zertifikate</strong><br/></td>

</tr>
<tr class="odd">
<td>TrustedPeople</td>
<td><strong>HKEY_CURRENT_USER</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>System Zertifikate</strong> \ <strong>Treuhänder</strong> \ <strong>Zertifikate</strong><br/></td>

</tr>
<tr class="even">
<td>Unzulässig</td>
<td><strong>HKEY_CURRENT_USER</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>System Zertifikate</strong> \ Nicht <strong>zulässig</strong> \ <strong>Zertifikate</strong><br/></td>

</tr>
<tr class="odd">
<td>CA</td>
<td><strong>HKEY_CURRENT_USER</strong> \ <strong>Software</strong> \ <strong>Microsoft</strong> \ <strong>System Zertifikate</strong> \ Zertifizierungsstelle <strong></strong> \ <strong>Zertifikate</strong><br/></td>

</tr>
</tbody>
</table>



 

Andere von Anwendungen erstellte Zertifikat Speicher werden standardmäßig nicht migriert. Anwendungen, die ihre eigenen Speicher erstellen, sind für die Migration der von Ihnen erstellten Filialen verantwortlich. Zum Erstellen von Stores empfiehlt es sich, einen Registrierungsschlüssel in den Anwendungseinstellungen zu definieren und in den Registrierungs Einstellungen einen Speicher zu erstellen, indem Sie den Speicher Anbieter für den **Zertifikat \_ Speicher \_ Prov \_ reg** verwenden. Weitere Informationen zum Migrieren von Anwendungseinstellungen finden Sie im Thema *Erstellen einer benutzerdefinierten XML-Datei* im Leitfaden *using US MT 3,0* unter [Migrationstool für den Benutzerstatus 3,0](https://www.microsoft.com/technet/windowsvista/library/91f62fc4-621f-4537-b311-1307df010561.mspx). (Diese Ressource ist möglicherweise in einigen Sprachen und Ländern oder Regionen nicht verfügbar.)

 

 
