---
title: Sicherheit und Zugriffsrechte für Die Fensterstation
description: Mit der Sicherheit können Sie den Zugriff auf Fensterstationsobjekte steuern. Weitere Informationen zur Sicherheit finden Sie unter Access-Control Model.
ms.assetid: b132da61-26b7-4457-9433-4894ca0e640a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04e3b6871fe0e465b4394e871537fbb8ca07f6439577833d61a7fe0c3106685f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118435995"
---
# <a name="window-station-security-and-access-rights"></a>Sicherheit und Zugriffsrechte für Die Fensterstation

Mit der Sicherheit können Sie den Zugriff auf Fensterstationsobjekte steuern. Weitere Informationen zur Sicherheit finden Sie unter [Access-Control Model](/windows/desktop/SecAuthZ/access-control-model).

Sie können einen [Sicherheitsdeskriptor für](/windows/desktop/SecAuthZ/security-descriptors) ein Fensterstationsobjekt angeben, wenn Sie die [**CreateWindowStation-Funktion**](/windows/win32/api/winuser/nf-winuser-createwindowstationa) aufrufen. Wenn Sie NULL angeben, erhält die Fensterstation einen Standardsicherheitsdeskriptor. Die ACLs in der Standardsicherheitsbeschreibung für eine Fensterstation stammen aus dem primären Token oder Identitätswechseltoken des Erstellers.

Rufen Sie die Funktionen [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) und [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) auf, um die Sicherheitsbeschreibung eines Fensterstationsobjekts zu erhalten oder festlegen.

Wenn Sie die [**OpenWindowStation-Funktion**](/windows/win32/api/winuser/nf-winuser-openwindowstationa) aufrufen, überprüft das System die angeforderten Zugriffsrechte mit dem Sicherheitsdeskriptor des Objekts.

Die gültigen Zugriffsrechte für Fensterstationsobjekte umfassen [die Standardzugriffsrechte](/windows/desktop/SecAuthZ/standard-access-rights) und einige objektspezifische Zugriffsrechte. In der folgenden Tabelle sind die Standardzugriffsrechte aufgeführt, die von allen -Objekten verwendet werden.

| Wert                       | Bedeutung                                                                                                                                                                                                                                                                              |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DELETE (0x00010000L)        | Erforderlich, um das Objekt zu löschen.                                                                                                                                                                                                                                                       |
| READ \_ CONTROL (0x00020000L) | Erforderlich, um Informationen in der Sicherheitsbeschreibung für das Objekt zu lesen, nicht die Informationen in der SACL. Zum Lesen oder Schreiben der SACL müssen Sie das Zugriffsrecht ACCESS \_ SYSTEM \_ SECURITY anfordern. Weitere Informationen finden Sie unter [SACL Access Right](/windows/desktop/SecAuthZ/sacl-access-right). |
| SYNCHRONIZE (0x00100000L)   | Wird für Fensterstationsobjekte nicht unterstützt.                                                                                                                                                                                                                                            |
| WRITE \_ DAC (0x00040000L)    | Erforderlich, um die DACL in der Sicherheitsbeschreibung für das Objekt zu ändern.                                                                                                                                                                                                               |
| WRITE \_ OWNER (0x00080000L)  | Erforderlich, um den Besitzer in der Sicherheitsbeschreibung für das Objekt zu ändern.                                                                                                                                                                                                              |



 

In der folgenden Tabelle sind die objektspezifischen Zugriffsrechte aufgeführt.



| Zugriffsrechte                        | Beschreibung                                                                                                                                                                                                                                                                   |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WINSTA \_ ALL \_ ACCESS (0x37F)         | Alle möglichen Zugriffsrechte für die Fensterstation.                                                                                                                                                                                                                            |
| WINSTA \_ ACCESSCLIPBOARD (0x0004L)   | Erforderlich, um die Zwischenablage zu verwenden.                                                                                                                                                                                                                                                |
| WINSTA \_ ACCESSGLOBALATOMS (0x0020L) | Erforderlich, um globale Atome zu bearbeiten.                                                                                                                                                                                                                                          |
| WINSTA \_ CREATEDESKTOP (0x0008L)     | Erforderlich, um neue Desktopobjekte auf der Fensterstation zu erstellen.                                                                                                                                                                                                                 |
| WINSTA \_ ENUMDESKTOPS (0x0001L)      | Erforderlich zum Aufzählen vorhandener Desktopobjekte.                                                                                                                                                                                                                               |
| WINSTA \_ ENUMERATE (0x0100L)         | Erforderlich, damit die Fensterstation aufzählt werden kann.                                                                                                                                                                                                                             |
| WINSTA \_ EXITWINDOWS (0x0040L)       | Erforderlich, um die [**ExitWindows- oder**](/windows/desktop/api/winuser/nf-winuser-exitwindows) [**ExitWindowsEx-Funktion erfolgreich aufrufen zu**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) können. Fensterstationen können von Benutzern gemeinsam genutzt werden, und dieser Zugriffstyp kann verhindern, dass sich andere Benutzer einer Fensterstation vom Besitzer der Fensterstation abmelden. |
| WINSTA \_ READATTRIBUTES (0x0002L)    | Erforderlich, um die Attribute eines Fensterstationsobjekts zu lesen. Dieses Attribut enthält Farbeinstellungen und andere globale Fensterstationseigenschaften.                                                                                                                                |
| WINSTA \_ READSCREEN (0x0200L)        | Erforderlich für den Zugriff auf Bildschirminhalte.                                                                                                                                                                                                                                           |
| WINSTA \_ WRITEATTRIBUTES (0x0010L)   | Erforderlich, um die Attribute eines Fensterstationsobjekts zu ändern. Zu den Attributen gehören Farbeinstellungen und andere globale Fensterstationseigenschaften.                                                                                                                               |



 

Im Folgenden finden Sie die generischen [Zugriffsrechte](/windows/desktop/SecAuthZ/generic-access-rights) für das interaktive Fensterstationsobjekt, bei dem es sich um die Fensterstation handelt, die der Anmeldesitzung des interaktiven Benutzers zugewiesen ist.



<table>
<thead>
<tr class="header">
<th>Zugriffsrechte</th>
<th>Beschreibung</th>
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



 

Im Folgenden finden Sie [die generischen Zugriffsrechte für](/windows/desktop/SecAuthZ/generic-access-rights) ein nichtinteraktives Fensterstationsobjekt. Das System weist allen Anmeldesitzungen außer der des interaktiven Benutzers nicht interaktive Fensterstationen zu.



<table>
<thead>
<tr class="header">
<th>Zugriffsrechte</th>
<th>Beschreibung</th>
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



 

Sie können das Zugriffsrecht ACCESS \_ SYSTEM SECURITY auf ein \_ Fensterstationsobjekt anfordern, wenn Sie die SACL des Objekts lesen oder schreiben möchten. Weitere Informationen finden Sie unter [Zugriffssteuerungslisten (ACLs)](/windows/desktop/SecAuthZ/access-control-lists) und [SACL-Zugriffsrecht.](/windows/desktop/SecAuthZ/sacl-access-right)

 

 