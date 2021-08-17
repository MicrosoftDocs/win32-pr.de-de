---
title: Desktopsicherheits- und Zugriffsrechte
description: Mit der Sicherheit können Sie den Zugriff auf Desktopobjekte steuern. Weitere Informationen zur Sicherheit finden Sie unter Access-Control-Modell.
ms.assetid: 6512d128-3b0c-4ba7-8709-2fd225389a40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1805a9b5b3db70bf496d467b774dc7c959030b43d6f89d40aabd0336540b7e56
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119346690"
---
# <a name="desktop-security-and-access-rights"></a>Desktopsicherheits- und Zugriffsrechte

Mit der Sicherheit können Sie den Zugriff auf Desktopobjekte steuern. Weitere Informationen zur Sicherheit finden Sie unter [Access-Control Model](/windows/desktop/SecAuthZ/access-control-model).

Sie können eine [Sicherheitsbeschreibung](/windows/desktop/SecAuthZ/security-descriptors) für ein Desktopobjekt angeben, wenn Sie die [**Funktion CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa) oder [**CreateDesktopEx**](/windows/win32/api/winuser/nf-winuser-createdesktopexa) aufrufen. Wenn Sie NULL angeben, ruft der Desktop einen Standardsicherheitsdeskriptor ab. Die ACLs in der Standardsicherheitsbeschreibung für einen Desktop stammen von der übergeordneten Fensterstation.

Um die Sicherheitsbeschreibung eines Fensterstationsobjekts abzurufen oder festzulegen, rufen Sie die Funktionen [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) und [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) auf.

Wenn Sie die [**OpenDesktop-**](/windows/win32/api/winuser/nf-winuser-opendesktopa) oder [**OpenInputDesktop-Funktion**](/windows/win32/api/winuser/nf-winuser-openinputdesktop) aufrufen, überprüft das System die angeforderten Zugriffsrechte anhand des Sicherheitsdeskriptors des Objekts.

Zu den gültigen Zugriffsrechten für Desktopobjekte gehören die [Standardzugriffsrechte](/windows/desktop/SecAuthZ/standard-access-rights) und einige objektspezifische Zugriffsrechte. In der folgenden Tabelle sind die Standardzugriffsrechte aufgeführt, die von allen -Objekten verwendet werden.

| Wert                       | Bedeutung                                                                                                                                                                                                                                                                              |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DELETE (0x00010000L)        | Erforderlich, um das Objekt zu löschen.                                                                                                                                                                                                                                                       |
| READ \_ CONTROL (0x00020000L) | Erforderlich, um Informationen in der Sicherheitsbeschreibung für das Objekt zu lesen, ohne die Informationen in der SACL einzulesen. Zum Lesen oder Schreiben der SACL müssen Sie das Zugriffsrecht ACCESS \_ SYSTEM \_ SECURITY anfordern. Weitere Informationen finden Sie unter [SACL-Zugriffsrecht.](/windows/desktop/SecAuthZ/sacl-access-right) |
| SYNCHRONIZE (0x00100000L)   | Wird für Desktopobjekte nicht unterstützt.                                                                                                                                                                                                                                                   |
| WRITE \_ DAC (0x00040000L)    | Erforderlich, um die DACL in der Sicherheitsbeschreibung für das Objekt zu ändern.                                                                                                                                                                                                               |
| WRITE \_ OWNER (0x00080000L)  | Erforderlich, um den Besitzer in der Sicherheitsbeschreibung für das Objekt zu ändern.                                                                                                                                                                                                              |



 

In der folgenden Tabelle sind die objektspezifischen Zugriffsrechte aufgeführt.



| Zugriffsrecht                       | BESCHREIBUNG                                                                                 |
|------------------------------------|---------------------------------------------------------------------------------------------|
| DESKTOP \_ CREATEMENU (0x0004L)      | Erforderlich, um ein Menü auf dem Desktop zu erstellen.                                                   |
| DESKTOP \_ CREATEWINDOW (0x0002L)    | Erforderlich, um ein Fenster auf dem Desktop zu erstellen.                                                 |
| DESKTOP \_ ENUMERATE (0x0040L)       | Erforderlich, damit der Desktop aufzählt.                                                  |
| DESKTOP \_ HOOKCONTROL (0x0008L)     | Erforderlich, um einen der Fensterhooks einzurichten.                                              |
| DESKTOP \_ JOURNALPLAYBACK (0x0020L) | Erforderlich, um die Journalwiedergabe auf einem Desktop durchzuführen.                                          |
| DESKTOP \_ JOURNALRECORD (0x0010L)   | Erforderlich, um eine Journalaufzeichnung auf einem Desktop durchzuführen.                                         |
| DESKTOP \_ READOBJECTS (0x0001L)     | Erforderlich zum Lesen von Objekten auf dem Desktop.                                                    |
| DESKTOP \_ SWITCHDESKTOP (0x0100L)   | Erforderlich, um den Desktop mithilfe der [**SwitchDesktop-Funktion**](/windows/win32/api/winuser/nf-winuser-switchdesktop) zu aktivieren. |
| DESKTOP \_ WRITEOBJECTS (0x0080L)    | Erforderlich, um Objekte auf dem Desktop zu schreiben.                                                   |



 

Im Folgenden sind die [generischen Zugriffsrechte](/windows/desktop/SecAuthZ/generic-access-rights) für ein Desktopobjekt aufgeführt, das in der interaktiven Fensterstation der Anmeldesitzung des Benutzers enthalten ist.



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
<td><dl> DESKTOP_ENUMERATE<br />
DESKTOP_READOBJECTS<br />
STANDARD_RIGHTS_READ<br />
</dl></td>
</tr>
<tr class="even">
<td>GENERIC_WRITE</td>
<td><dl> DESKTOP_CREATEMENU<br />
DESKTOP_CREATEWINDOW<br />
DESKTOP_HOOKCONTROL<br />
DESKTOP_JOURNALPLAYBACK<br />
DESKTOP_JOURNALRECORD<br />
DESKTOP_WRITEOBJECTS<br />
STANDARD_RIGHTS_WRITE<br />
</dl></td>
</tr>
<tr class="odd">
<td>GENERIC_EXECUTE</td>
<td><dl> DESKTOP_SWITCHDESKTOP<br />
STANDARD_RIGHTS_EXECUTE<br />
</dl></td>
</tr>
<tr class="even">
<td>GENERIC_ALL</td>
<td><dl> DESKTOP_CREATEMENU<br />
DESKTOP_CREATEWINDOW<br />
DESKTOP_ENUMERATE<br />
DESKTOP_HOOKCONTROL<br />
DESKTOP_JOURNALPLAYBACK<br />
DESKTOP_JOURNALRECORD<br />
DESKTOP_READOBJECTS<br />
DESKTOP_SWITCHDESKTOP<br />
DESKTOP_WRITEOBJECTS<br />
STANDARD_RIGHTS_REQUIRED<br />
</dl></td>
</tr>
</tbody>
</table>



 

Sie können das Zugriffsrecht ACCESS \_ SYSTEM SECURITY auf ein \_ Desktopobjekt anfordern, wenn Sie die SACL des Objekts lesen oder schreiben möchten. Weitere Informationen finden Sie unter [Zugriffssteuerungslisten (ACLs)](/windows/desktop/SecAuthZ/access-control-lists) und [SACL-Zugriffsrecht.](/windows/desktop/SecAuthZ/sacl-access-right)

 

 