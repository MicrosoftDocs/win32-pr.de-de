---
description: 'Das System speichert Benutzerprofil Informationen in einem bestimmten Verzeichnis, das in verschiedenen Versionen von Windows unterschiedliche Namen hat: &\# 0034; Dokumente und Einstellungen&\# 0034; in Windows XP und &\# 0034; Benutzer&\# 0034; in Windows Vista und höher.'
title: Profile-Verzeichnis
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 41056f40-fa1a-488a-b213-49cbdd8d4fdf
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 3eb310434e5665dd8f28a661785403d72c4c1e46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979952"
---
# <a name="profiles-directory"></a>Profile-Verzeichnis

Das System speichert Benutzerprofil Informationen in einem bestimmten Verzeichnis, das in verschiedenen Versionen von Windows unterschiedliche Namen hat: "Dokumente und Einstellungen" in Windows XP und "Benutzer" in Windows Vista und höher. Verwenden Sie zum Abrufen des Pfads für das Verzeichnis "Profile" die Funktion " [**GetProfilesDirectory**](/windows/desktop/api/Userenv/nf-userenv-getprofilesdirectorya) ".

Das Verzeichnis "Profile" enthält die folgenden Unterverzeichnisse für Benutzerprofile.



| Verzeichnis                                      | BESCHREIBUNG                                                                                                                                |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| ProgramData (Windows Vista oder höher)/all Benutzer | Programminformationen, die für alle Benutzer gelten. Das Verzeichnis "alle Benutzer" ist in Windows Vista oder höher für die Abwärtskompatibilität weiterhin vorhanden. |
| Standard                                        | Profilinformationen, die für den Standardbenutzer gelten.                                                                                      |
| *Benutzer*                                         | Profilinformationen, die für den angegebenen Benutzer gelten. Jeder Benutzer verfügt über ein eigenes Profil Unterverzeichnis.                                      |



 

Rufen Sie die [**getallusersprofiledirectory**](/windows/desktop/api/Userenv/nf-userenv-getallusersprofiledirectorya) -Funktion auf, um den Speicherort des Verzeichnisses ProgramData/all users zu erhalten. Dieses Verzeichnis enthält die folgenden Unterverzeichnisse:



| Verzeichnis  | BESCHREIBUNG                          |
|------------|--------------------------------------|
| Desktop    | Verknüpfungen, die auf dem Desktop angezeigt werden sollen. |
| Startmenü | Menü Elemente für das **Startmenü** .   |



 

Um den Speicherort des Standardbenutzer Verzeichnisses abzurufen, rufen Sie die [**GetDefaultUserProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getdefaultuserprofiledirectorya) -Funktion auf. Um den Speicherort des Verzeichnisses eines bestimmten Benutzers abzurufen, rufen Sie die [**getuserprofiledirectory**](/windows/desktop/api/Userenv/nf-userenv-getuserprofiledirectorya) -Funktion auf. Sowohl der Standardbenutzer als auch bestimmte Benutzerverzeichnisse enthalten die folgenden Unterverzeichnisse. Kursiv formatiertes Verzeichnis geben Verzeichnisse an, die standardmäßig ausgeblendet sind. Sie können diese Verzeichnisse anzeigen, indem Sie die Option Ausgeblendete **Dateien, Ordner und Laufwerke anzeigen** im System Steuerungselement **Ordneroptionen** auswählen.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Verzeichnis</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Anwendungsdaten</td>
<td>Anwendungsspezifische Daten.</td>
</tr>
<tr class="even">
<td>Cookies</td>
<td>Windows Internet Explorer-Cookies.</td>
</tr>
<tr class="odd">
<td>Desktop</td>
<td>Verknüpfungen, die auf dem Desktop angezeigt werden sollen.</td>
</tr>
<tr class="even">
<td>Favoriten</td>
<td>Links zu bevorzugten Websites.</td>
</tr>
<tr class="odd">
<td>Lokale Einstellungen</td>
<td>Anwendungseinstellungen und Daten, die nicht mit dem Profil wechseln. In der Regel sind die Einstellungen oder Daten in diesem Verzeichnis Computer spezifisch, oder Sie sind zu groß, um effektiv zu wechseln. Dieses Verzeichnis enthält die folgenden Unterordner:
<ul>
<li>Anwendungsdaten</li>
<li>Verlauf</li>
<li>Temp</li>
<li>Temporäre Internetdateien</li>
</ul></td>
</tr>
<tr class="even">
<td>Meine Dokumente</td>
<td>Der Standard Speicherort für Dokumente, die der Benutzer erstellt. Anwendungen sollten Dokument Dateien standardmäßig in diesem Verzeichnis speichern.</td>
</tr>
<tr class="odd">
<td><em>Nicht mehr</em></td>
<td>Verknüpfungen zu Netzwerk-Nachbarschafts Elementen.</td>
</tr>
<tr class="even">
<td><em>Printhood</em></td>
<td>Verknüpfungen zu Drucker Ordner Elementen.</td>
</tr>
<tr class="odd">
<td><em>Zuletzt verwendete</em></td>
<td>Verknüpfungen zu den zuletzt verwendeten Dokumenten.</td>
</tr>
<tr class="even">
<td>SendTo</td>
<td>Verknüpfungen zu Speicherorten, an die der Benutzer häufig Dateien sendet.</td>
</tr>
<tr class="odd">
<td>Startmenü</td>
<td>Menü Elemente für das <strong>Startmenü</strong> .</td>
</tr>
<tr class="even">
<td><em>Vorlagen</em></td>
<td>Verknüpfungen zu Vorlagen Elementen.</td>
</tr>
</tbody>
</table>



 

Wenn Sie den Speicherort der Unterverzeichnisse dieser Verzeichnisse abrufen möchten, verwenden Sie die Funktionen " [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) " oder " [**shgetknownfolderpath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) ".

 

 



