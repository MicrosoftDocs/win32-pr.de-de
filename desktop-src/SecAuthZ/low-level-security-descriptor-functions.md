---
description: Funktionen zum Festlegen und Abrufen eines Sicherheits Deskriptors für Objekte.
ms.assetid: 22bf0d6b-3ec6-4c28-ace4-49e48714f4bf
title: 'Sicherheitsbeschreibungsfunktionen auf niedriger Eben '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72406dc2481e4671d8d535327f416a2d003c3a89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363004"
---
# <a name="low-level-security-descriptor-functions"></a>Sicherheitsbeschreibungsfunktionen auf niedriger Eben 

Es gibt mehrere Paare von Low-Level-Funktionen zum Festlegen und Abrufen der [*Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly)eines Objekts. Jedes dieser Paare funktioniert nur mit einem begrenzten Satz von Windows-Objekten. Beispielsweise funktioniert ein paar mit Datei Objekten, und ein anderes funktioniert mit Registrierungs Schlüsseln. In der folgenden Tabelle werden die Funktionen auf niedriger Ebene angezeigt, die mit den verschiedenen Typen von Sicherungs fähigen Objekten verwendet werden können.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Objekttyp</th>
<th>Low-Level-Funktionen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><a href="/windows/desktop/FileIO/file-security-and-access-rights">Dateien</a></li>
<li><a href="/windows/desktop/FileIO/file-security-and-access-rights">Verzeichnisse</a></li>
<li>Postslots</li>
<li><a href="/windows/desktop/ipc/named-pipe-security-and-access-rights">Named Pipes</a></li>
</ul></td>
<td>Verwenden Sie die Funktionen <a href="/windows/desktop/api/Winbase/nf-winbase-getfilesecuritya"><strong>getfilesecurity</strong></a> und <a href="/windows/desktop/api/Winbase/nf-winbase-setfilesecuritya"><strong>setfilesecurity</strong></a> . Diese Funktionen verwenden Zeichen folgen, um das Sicherungs fähige Objekt zu identifizieren, anstatt Handles zu verwenden.</td>
</tr>
<tr class="even">
<td><ul>
<li><a href="/windows/desktop/ProcThread/process-security-and-access-rights">Prozesse</a></li>
<li><a href="/windows/desktop/ProcThread/thread-security-and-access-rights">Threads</a></li>
<li><a href="access-rights-for-access-token-objects.md">Zugriffstoken</a></li>
<li><a href="/windows/desktop/Memory/file-mapping-security-and-access-rights">Datei Zuordnung von Objekten</a></li>
<li><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Semaphoren</a></li>
<li><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Ereignisse</a></li>
<li><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Mutexe</a></li>
<li><a href="/windows/desktop/Sync/synchronization-object-security-and-access-rights">Wanutzbare Timer</a></li>
</ul></td>
<td>Verwenden Sie die Funktionen <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getkernelobjectsecurity"><strong>getkernelobjectsecurity</strong></a> und <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setkernelobjectsecurity"><strong>setkernelobjectsecurity</strong></a> .</td>
</tr>
<tr class="odd">
<td><ul>
<li><a href="/windows/desktop/winstation/window-station-security-and-access-rights">Fenster Stationen</a></li>
<li><a href="/windows/desktop/winstation/desktop-security-and-access-rights">Desktops</a></li>
</ul></td>
<td>Verwenden Sie die Funktionen <a href="/windows/desktop/api/Winuser/nf-winuser-getuserobjectsecurity"><strong>getuserobjectsecurity</strong></a> und <a href="/windows/desktop/api/Winuser/nf-winuser-setuserobjectsecurity"><strong>setuserobjectsecurity</strong></a> .</td>
</tr>
<tr class="even">
<td><ul>
<li><a href="/windows/desktop/SysInfo/registry-key-security-and-access-rights">Registrierungsschlüssel</a></li>
</ul></td>
<td>Verwenden Sie die Funktionen <a href="/windows/desktop/api/Winreg/nf-winreg-reggetkeysecurity"><strong>reggetkeysecurity</strong></a> und <a href="/windows/desktop/api/Winreg/nf-winreg-regsetkeysecurity"><strong>regsetkeysecurity</strong></a> .</td>
</tr>
<tr class="odd">
<td><ul>
<li><a href="/windows/desktop/Services/service-security-and-access-rights">Windows-Dienst Objekte</a></li>
</ul></td>
<td>Verwenden Sie die Funktionen <a href="/windows/desktop/api/Winsvc/nf-winsvc-queryserviceobjectsecurity"><strong>QueryServiceObjectSecurity</strong></a> und <a href="/windows/desktop/api/Winsvc/nf-winsvc-setserviceobjectsecurity"><strong>SetServiceObjectSecurity</strong></a> .</td>
</tr>
<tr class="even">
<td><ul>
<li>Drucker Objekte</li>
</ul></td>
<td>Verwenden Sie die <a href="/windows/desktop/printdocs/printer-info-2"><strong>PRINTER_INFO_2</strong></a> -Struktur mit den Funktionen " <a href="/windows/desktop/printdocs/getprinter"><strong>GetPrinter</strong></a> " und " <a href="/windows/desktop/printdocs/setprinter"><strong>SetPrinter</strong></a> ".</td>
</tr>
<tr class="odd">
<td><ul>
<li><a href="/windows/desktop/NetMgmt/security-requirements-for-the-network-management-functions">Netzwerkfreigaben</a></li>
</ul></td>
<td>Verwenden Sie Level 502 mit den Funktionen <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharegetinfo"><strong>NetShareGetInfo</strong></a> und <a href="/windows/desktop/api/lmshare/nf-lmshare-netsharesetinfo"><strong>NetShareSetInfo</strong></a> .</td>
</tr>
<tr class="even">
<td><ul>
<li><a href="acl-based-access-control.md">Private Objekte (Objekte, die für die Erstellungsanwendung privat sind)</a></li>
</ul></td>
<td>Verwenden Sie die Funktionen " <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity"><strong>kreateprivateobjectsecurity</strong></a>", " <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-destroyprivateobjectsecurity"><strong>DestroyPrivateObjectSecurity</strong></a>", " <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getprivateobjectsecurity"><strong>GetPrivateObjectSecurity</strong></a> " und " <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-setprivateobjectsecurity"><strong>setprivateobjectsecurity</strong></a> ".</td>
</tr>
</tbody>
</table>



 

 

 
