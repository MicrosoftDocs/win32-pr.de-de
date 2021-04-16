---
description: Listet die Anforderungen auf, die durch sichere Kenn Wort System-Verwaltungs Tools erzwungen werden
ms.assetid: a84f83b2-181b-4f65-82bd-bc7f0689aad3
title: Starke Kenn Wort Erzwingung und Passfilt.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63b7be524511d52048e06ae83ab110384c3bf5c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525706"
---
# <a name="strong-password-enforcement-and-passfiltdll"></a>Starke Kenn Wort Erzwingung und Passfilt.dll

Die sichere Kenn Wort Erzwingung kann mithilfe der System Verwaltungs Tools aktiviert werden. Wenn die Richtlinie für die Systemverwaltung aktiviert ist, müssen Kenn Wörter die folgenden Mindestanforderungen erfüllen, wenn Sie erstellt oder geändert werden:

-   Kennwörter dürfen nicht den Wert „SamAccountName“ (Kontoname) oder den gesamten Wert „DisplayName“ (vollständiger Name) des Benutzers enthalten. Beide Prüfungen unterscheiden nicht zwischen Groß-und Kleinschreibung.
-   „SamAccountName“ wird nur vollständig geprüft, um auszuschließen, dass der Wert Teil des Kennworts ist. Wenn „SamAccountName“ weniger als drei Zeichen umfasst, wird diese Überprüfung übersprungen.
-   „DisplayName“ wird auf Trennzeichen hin analysiert: Kommas, Punkte, Gedanken- oder Bindestriche, Unterstriche, Leerzeichen, Nummernzeichen und Tabstopps. Falls diese Trennzeichen gefunden werden, wird „DisplayName“ geteilt, und für alle analysierten Abschnitte (Token) wird sichergestellt, dass sie nicht im Kennwort enthalten sind. Token, die weniger als drei Zeichen umfassen, werden ignoriert, und Teilzeichenfolgen der Token werden nicht geprüft. Beispielsweise wird der Name „Erin M. Hagens“ in drei Token unterteilt: „Erin“, „M“ und „Hagens“. Da das zweite Token nur aus einem Zeichen besteht, wird es ignoriert. Somit kann dieser Benutzer kein Kennwort festgelegt, das „Erin“ oder „Hagens“ als Teilzeichenfolge an einer beliebigen Stelle im Kennwort enthält.
-   Kenn Wörter müssen Zeichen aus drei der fünf folgenden Kategorien enthalten.



| Zeichenkategorien                                                                                                                                                      | Beispiele                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| Großbuchstaben europäischer Sprachen (A bis Z, mit diakritischen Zeichen, griechische und kyrillische Zeichen)<br/>                                                     | a, B, C, Z<br/>                |
| Kleinbuchstaben europäischer Sprachen (a bis z, ß, mit diakritischen Zeichen, griechische und kyrillische Zeichen)<br/>                                            | a, b, c, z<br/>                |
| 10 Grundziffern (0 - 9)<br/>                                                                                                                                   | 0, 1, 2, 9<br/>                |
| Nicht alphanumerische Zeichen (Sonderzeichen)<br/>                                                                                                               | $,!,%, ^, () {} \[ \] ;: <>?<br/> |
| Alle Unicode-Zeichen, die als Zeichen des Alphabets kategorisiert sind, die aber nicht Groß- oder Kleinbuchstaben sind. Dazu zählen Unicode-Zeichen asiatischer Sprachen.<br/> |                                        |



 

**Aktivieren der sicheren Kenn Wort Erzwingung**

1.  Suchen Sie in der-Verwaltungskonsole nach **lokale Sicherheitsrichtlinie**.
2.  Wählen Sie **Konto Richtlinie** aus, und klicken Sie dann auf Kenn **Wort Richtlinie**.
3.  Aktivieren Sie die Einstellung Kenn **Wörter müssen Komplexitäts Anforderungen entsprechen** .

> [!Note]  
> Ein bestimmtes Zeichen kann nur eine Kategorie erfüllen. Die [getstringtypew](/windows/win32/api/stringapiset/nf-stringapiset-getstringtypew) -Funktion wird verwendet, um zu testen, ob die einzelnen Zeichen im Kennwort Großbuchstaben, Kleinbuchstaben oder alphanumerische Zeichen sind.

 

 

