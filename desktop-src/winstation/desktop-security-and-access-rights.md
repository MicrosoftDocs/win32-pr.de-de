---
title: Desktop Sicherheit und Zugriffsrechte
description: Sicherheit ermöglicht es Ihnen, den Zugriff auf Desktop Objekte zu steuern. Weitere Informationen zur Sicherheit finden Sie unter Access-Control Modell.
ms.assetid: 6512d128-3b0c-4ba7-8709-2fd225389a40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d18b48e0b80dc39ea1b3f65a77acb615c4cb8c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390639"
---
# <a name="desktop-security-and-access-rights"></a>Desktop Sicherheit und Zugriffsrechte

Sicherheit ermöglicht es Ihnen, den Zugriff auf Desktop Objekte zu steuern. Weitere Informationen zur Sicherheit finden Sie unter [Zugriffs Steuerungsmodell](/windows/desktop/SecAuthZ/access-control-model).

Sie können eine [Sicherheits Beschreibung](/windows/desktop/SecAuthZ/security-descriptors) für ein Desktop Objekt angeben, wenn Sie die Funktion "up [**Desktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa) " oder " [**kreatedesktopex**](/windows/win32/api/winuser/nf-winuser-createdesktopexa) " aufrufen. Wenn Sie NULL angeben, erhält der Desktop eine Standard Sicherheits Beschreibung. Die ACLs in der Standard Sicherheits Beschreibung für einen Desktop stammen aus der übergeordneten Fenster Station.

Zum Abrufen oder Festlegen der Sicherheits Beschreibung eines Fenster Stations Objekts aufrufen Sie die Funktionen [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) und [**setsecurityinfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) .

Wenn Sie die Funktion [**OpenDesktop**](/windows/win32/api/winuser/nf-winuser-opendesktopa) oder [**openinputdesktop**](/windows/win32/api/winuser/nf-winuser-openinputdesktop) aufrufen, prüft das System die angeforderten Zugriffsrechte auf die Sicherheits Beschreibung des Objekts.

Zu den gültigen Zugriffsrechten für Desktop Objekte gehören die [Standard Zugriffsrechte](/windows/desktop/SecAuthZ/standard-access-rights) und einige objektspezifische Zugriffsrechte. In der folgenden Tabelle sind die standardmäßigen Zugriffsrechte aufgelistet, die von allen Objekten verwendet werden.

| Wert                       | Bedeutung                                                                                                                                                                                                                                                                              |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Delete (0x00010000l)        | Erforderlich, um das Objekt zu löschen.                                                                                                                                                                                                                                                       |
| Read- \_ Steuerelement (0x00020000l) | Ist erforderlich, um Informationen in der Sicherheits Beschreibung für das-Objekt zu lesen, ohne die Informationen in der SACL zu einschließen. Um die SACL zu lesen oder zu schreiben, müssen Sie das Zugriffs \_ System- \_ Sicherheits Zugriffsrecht anfordern. Weitere Informationen finden Sie unter [SACL-Zugriffsrecht](/windows/desktop/SecAuthZ/sacl-access-right). |
| Synchronisieren (0x00100000l)   | Wird für Desktop Objekte nicht unterstützt.                                                                                                                                                                                                                                                   |
| \_DAC schreiben (0x00040000l)    | Erforderlich, um die DACL in der Sicherheits Beschreibung für das-Objekt zu ändern.                                                                                                                                                                                                               |
| Schreib \_ Besitzer (0x00080000l)  | Erforderlich, um den Besitzer in der Sicherheits Beschreibung für das Objekt zu ändern.                                                                                                                                                                                                              |



 

In der folgenden Tabelle sind die Objekt spezifischen Zugriffsrechte aufgeführt.



| Zugriffsrecht                       | BESCHREIBUNG                                                                                 |
|------------------------------------|---------------------------------------------------------------------------------------------|
| Desktop " \_ beatemdeu" (0x0004l)      | Erforderlich, um auf dem Desktop ein Menü zu erstellen.                                                   |
| Desktop- \_ kreatewindow (0x0002l)    | Erforderlich, um auf dem Desktop ein Fenster zu erstellen.                                                 |
| Desktop \_ Aufzählung (0x0040l)       | Erforderlich, damit der Desktop aufgezählt wird.                                                  |
| Desktop- \_ Hostingsteuerelement (0x0008l)     | Erforderlich, um einen der Fenster Hooks einzurichten.                                              |
| Desktop \_ journalplayback (0x0020l) | Erforderlich, um die Journal Wiedergabe auf einem Desktop auszuführen.                                          |
| Desktop \_ journalrecord (0x0010l)   | Erforderlich, um die Journal Aufzeichnung auf einem Desktop auszuführen.                                         |
| Desktop-Schreib \_ Objekte (0x0001l)     | Erforderlich zum Lesen von Objekten auf dem Desktop.                                                    |
| Desktop \_ switchdesktop (0x0100l)   | Erforderlich, um den Desktop mithilfe der [**switchdesktop**](/windows/win32/api/winuser/nf-winuser-switchdesktop) -Funktion zu aktivieren. |
| Desktop-Schreib \_ Objekte (0x0080l)    | Erforderlich zum Schreiben von Objekten auf dem Desktop.                                                   |



 

Im folgenden finden Sie die [allgemeinen Zugriffsrechte](/windows/desktop/SecAuthZ/generic-access-rights) für ein Desktop Objekt, das in der interaktiven Fenster Station der Anmelde Sitzung des Benutzers enthalten ist.



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



 

Sie können das Zugriffs \_ System \_ -Sicherheits Zugriffsrecht für ein Desktop Objekt anfordern, wenn Sie die SACL des Objekts lesen oder schreiben möchten. Weitere Informationen finden Sie unter [Zugriffs Steuerungs Listen (Access Control Lists, ACLs)](/windows/desktop/SecAuthZ/access-control-lists) und [SACL-Zugriffsrecht](/windows/desktop/SecAuthZ/sacl-access-right).

 

 