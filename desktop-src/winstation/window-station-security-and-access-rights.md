---
title: Sicherheit und Zugriffsrechte für die Fenster Station
description: Mithilfe der Sicherheit können Sie den Zugriff auf Fenster Station-Objekte steuern. Weitere Informationen zur Sicherheit finden Sie unter Access-Control Modell.
ms.assetid: b132da61-26b7-4457-9433-4894ca0e640a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c41bfb6d7990c104b60bd9770fde3f45cee0432
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106341524"
---
# <a name="window-station-security-and-access-rights"></a>Sicherheit und Zugriffsrechte für die Fenster Station

Mithilfe der Sicherheit können Sie den Zugriff auf Fenster Station-Objekte steuern. Weitere Informationen zur Sicherheit finden Sie unter [Zugriffs Steuerungsmodell](/windows/desktop/SecAuthZ/access-control-model).

Sie können eine [Sicherheits Beschreibung](/windows/desktop/SecAuthZ/security-descriptors) für ein Fenster Station-Objekt angeben, wenn [**Sie die Funktion**](/windows/win32/api/winuser/nf-winuser-createwindowstationa) "Funktion in der Funktion" aufgerufen haben. Wenn Sie NULL angeben, erhält die Fenster Station eine Standard Sicherheits Beschreibung. Die ACLs in der Standard Sicherheits Beschreibung für eine Fenster Station stammen aus dem primären Token oder dem Identitätswechsel Token des Erstellers.

Zum Abrufen oder Festlegen der Sicherheits Beschreibung eines Fenster Stations Objekts aufrufen Sie die Funktionen [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) und [**setsecurityinfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) .

Wenn Sie die [**openwindowstation**](/windows/win32/api/winuser/nf-winuser-openwindowstationa) -Funktion aufrufen, prüft das System die angeforderten Zugriffsrechte auf die Sicherheits Beschreibung des Objekts.

Zu den gültigen Zugriffsrechten für Fenster Stations Objekte gehören die [Standard Zugriffsrechte](/windows/desktop/SecAuthZ/standard-access-rights) und einige objektspezifische Zugriffsrechte. In der folgenden Tabelle sind die standardmäßigen Zugriffsrechte aufgelistet, die von allen Objekten verwendet werden.

| Wert                       | Bedeutung                                                                                                                                                                                                                                                                              |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Delete (0x00010000l)        | Erforderlich, um das Objekt zu löschen.                                                                                                                                                                                                                                                       |
| Read- \_ Steuerelement (0x00020000l) | Ist erforderlich, um Informationen in der Sicherheits Beschreibung für das-Objekt zu lesen, ohne die Informationen in der SACL zu einschließen. Um die SACL zu lesen oder zu schreiben, müssen Sie das Zugriffs \_ System- \_ Sicherheits Zugriffsrecht anfordern. Weitere Informationen finden Sie unter [SACL-Zugriffsrecht](/windows/desktop/SecAuthZ/sacl-access-right). |
| Synchronisieren (0x00100000l)   | Wird für Fenster Station-Objekte nicht unterstützt.                                                                                                                                                                                                                                            |
| \_DAC schreiben (0x00040000l)    | Erforderlich, um die DACL in der Sicherheits Beschreibung für das-Objekt zu ändern.                                                                                                                                                                                                               |
| Schreib \_ Besitzer (0x00080000l)  | Erforderlich, um den Besitzer in der Sicherheits Beschreibung für das Objekt zu ändern.                                                                                                                                                                                                              |



 

In der folgenden Tabelle sind die Objekt spezifischen Zugriffsrechte aufgeführt.



| Zugriffsrecht                        | BESCHREIBUNG                                                                                                                                                                                                                                                                   |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Winsta \_ All- \_ Zugriff (0x37f)         | Alle möglichen Zugriffsrechte für die Fenster Station.                                                                                                                                                                                                                            |
| Winsta \_ accessclipboard (0x0004l)   | Erforderlich, um die Zwischenablage zu verwenden.                                                                                                                                                                                                                                                |
| Winsta \_ accessglobalatome (0x0020l) | Erforderlich, um globale Atome zu manipulieren.                                                                                                                                                                                                                                          |
| Winsta \_ -kreatedesktop (0x0008l)     | Erforderlich, um neue Desktop Objekte auf der Fenster Station zu erstellen.                                                                                                                                                                                                                 |
| Winsta- \_ EnumDesktops (0x0001l)      | Zum Auflisten vorhandener Desktop Objekte erforderlich.                                                                                                                                                                                                                               |
| Winsta- \_ Enumeration (0x0100l)         | Erforderlich, damit die Fenster Station aufgezählt wird.                                                                                                                                                                                                                             |
| Winsta- \_ exitwindows (0x0040l)       | Erforderlich, um die [**exitwindows**](/windows/desktop/api/winuser/nf-winuser-exitwindows) -oder [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) -Funktion erfolgreich aufzurufen. Fenster Stationen können von Benutzern gemeinsam genutzt werden. mit diesem Zugriffstyp kann verhindert werden, dass andere Benutzer einer Fenster Station sich vom Besitzer der Fenster Station abmelden. |
| Winsta-Read- \_ Attribute (0x0002l)    | Erforderlich, um die Attribute eines Fenster Station-Objekts zu lesen. Dieses Attribut schließt Farbeinstellungen und andere Eigenschaften der globalen Fenster Station ein.                                                                                                                                |
| Winsta- \_ Bildschirm (0x0200l)        | Für den Zugriff auf Bildschirminhalte erforderlich.                                                                                                                                                                                                                                           |
| Winsta- \_ Beschreib teattribute (0x0010l)   | Erforderlich, um die Attribute eines Fenster Station-Objekts zu ändern. Zu den Attributen zählen Farbeinstellungen und andere Eigenschaften der globalen Fenster Station.                                                                                                                               |



 

Im folgenden finden Sie die [allgemeinen Zugriffsrechte](/windows/desktop/SecAuthZ/generic-access-rights) für das interaktive Fenster Station-Objekt, bei dem es sich um die der Anmelde Sitzung des interaktiven Benutzers zugewiesene Fenster Station handelt.



<table>
<thead>
<tr class="header">
<th>Zugriffsrecht</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>GENERIC_READ</td>
<td><dl> STANDARD_RIGHTS_READ<br />
WINSTA_ENUMDESKTOPS<br />
WINSTA_ENUMERATE<br />
WINSTA_READATTRIBUTES<br />
WINSTA_READSCREEN<br />
</dl></td>
</tr>
<tr class="even">
<td>GENERIC_WRITE</td>
<td><dl> STANDARD_RIGHTS_WRITE<br />
WINSTA_ACCESSCLIPBOARD<br />
WINSTA_CREATEDESKTOP<br />
WINSTA_WRITEATTRIBUTES<br />
</dl></td>
</tr>
<tr class="odd">
<td>GENERIC_EXECUTE</td>
<td><dl> STANDARD_RIGHTS_EXECUTE<br />
WINSTA_ACCESSGLOBALATOMS<br />
WINSTA_EXITWINDOWS<br />
</dl></td>
</tr>
<tr class="even">
<td>GENERIC_ALL</td>
<td><dl> STANDARD_RIGHTS_REQUIRED<br />
WINSTA_ACCESSCLIPBOARD<br />
WINSTA_ACCESSGLOBALATOMS<br />
WINSTA_CREATEDESKTOP<br />
WINSTA_ENUMDESKTOPS<br />
WINSTA_ENUMERATE<br />
WINSTA_EXITWINDOWS<br />
WINSTA_READATTRIBUTES<br />
WINSTA_READSCREEN<br />
WINSTA_WRITEATTRIBUTES<br />
</dl></td>
</tr>
</tbody>
</table>



 

Im folgenden finden Sie die [allgemeinen Zugriffsrechte](/windows/desktop/SecAuthZ/generic-access-rights) für ein nicht interaktives Fenster Station-Objekt. Das System weist nicht interaktive Fenster Stationen allen anderen Anmelde Sitzungen als der des interaktiven Benutzers zu.



<table>
<thead>
<tr class="header">
<th>Zugriffsrecht</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>GENERIC_READ</td>
<td><dl> STANDARD_RIGHTS_READ<br />
WINSTA_ENUMDESKTOPS<br />
WINSTA_ENUMERATE<br />
WINSTA_READATTRIBUTES<br />
</dl></td>
</tr>
<tr class="even">
<td>GENERIC_WRITE</td>
<td><dl> STANDARD_RIGHTS_WRITE<br />
WINSTA_ACCESSCLIPBOARD<br />
WINSTA_CREATEDESKTOP<br />
</dl></td>
</tr>
<tr class="odd">
<td>GENERIC_EXECUTE</td>
<td><dl> STANDARD_RIGHTS_EXECUTE<br />
WINSTA_ACCESSGLOBALATOMS<br />
WINSTA_EXITWINDOWS<br />
</dl></td>
</tr>
<tr class="even">
<td>GENERIC_ALL</td>
<td><dl> STANDARD_RIGHTS_REQUIRED<br />
WINSTA_ACCESSCLIPBOARD<br />
WINSTA_ACCESSGLOBALATOMS<br />
WINSTA_CREATEDESKTOP<br />
WINSTA_ENUMDESKTOPS<br />
WINSTA_ENUMERATE<br />
WINSTA_EXITWINDOWS<br />
WINSTA_READATTRIBUTES<br />
</dl></td>
</tr>
</tbody>
</table>



 

Sie können das Zugriffs \_ System \_ -Sicherheits Zugriffsrecht auf ein Fenster Station-Objekt anfordern, wenn Sie die SACL des Objekts lesen oder schreiben möchten. Weitere Informationen finden Sie unter [Zugriffs Steuerungs Listen (Access Control Lists, ACLs)](/windows/desktop/SecAuthZ/access-control-lists) und [SACL-Zugriffsrecht](/windows/desktop/SecAuthZ/sacl-access-right).

 

 