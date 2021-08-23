---
description: Listet die Anforderungen auf, die von Systemverwaltungstools für sichere Kennwörter erzwungen werden.
ms.assetid: a84f83b2-181b-4f65-82bd-bc7f0689aad3
title: Sichere Kennworterzwingung und Passfilt.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c3e34e77b15ca9797240ce5647aa58decf3efa05f04cd431b3d723b148bf406
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004896"
---
# <a name="strong-password-enforcement-and-passfiltdll"></a>Sichere Kennworterzwingung und Passfilt.dll

Sichere Kennworterzwingung kann mithilfe der Systemverwaltungstools aktiviert werden. Wenn die Systemverwaltungsrichtlinie aktiviert ist, müssen Kennwörter die folgenden Mindestanforderungen erfüllen, wenn sie erstellt oder geändert werden:

-   Kennwörter dürfen nicht den Wert „SamAccountName“ (Kontoname) oder den gesamten Wert „DisplayName“ (vollständiger Name) des Benutzers enthalten. Beide Prüfungen unterscheiden nicht zwischen Groß-und Kleinschreibung.
-   „SamAccountName“ wird nur vollständig geprüft, um auszuschließen, dass der Wert Teil des Kennworts ist. Wenn „SamAccountName“ weniger als drei Zeichen umfasst, wird diese Überprüfung übersprungen.
-   „DisplayName“ wird auf Trennzeichen hin analysiert: Kommas, Punkte, Gedanken- oder Bindestriche, Unterstriche, Leerzeichen, Nummernzeichen und Tabstopps. Falls diese Trennzeichen gefunden werden, wird „DisplayName“ geteilt, und für alle analysierten Abschnitte (Token) wird sichergestellt, dass sie nicht im Kennwort enthalten sind. Token, die weniger als drei Zeichen umfassen, werden ignoriert, und Teilzeichenfolgen der Token werden nicht geprüft. Beispielsweise wird der Name „Erin M. Hagens“ in drei Token unterteilt: „Erin“, „M“ und „Hagens“. Da das zweite Token nur aus einem Zeichen besteht, wird es ignoriert. Somit kann dieser Benutzer kein Kennwort festgelegt, das „Erin“ oder „Hagens“ als Teilzeichenfolge an einer beliebigen Stelle im Kennwort enthält.
-   Kennwörter müssen Zeichen aus drei der fünf folgenden Kategorien enthalten.



| Zeichenkategorien                                                                                                                                                      | Beispiele                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| Großbuchstaben europäischer Sprachen (A bis Z, mit diakritischen Zeichen, griechische und kyrillische Zeichen)<br/>                                                     | A, B, C, Z<br/>                |
| Kleinbuchstaben europäischer Sprachen (a bis z, ß, mit diakritischen Zeichen, griechische und kyrillische Zeichen)<br/>                                            | a, b, c, z<br/>                |
| 10 Grundziffern (0 - 9)<br/>                                                                                                                                   | 0, 1, 2, 9<br/>                |
| Nicht alphanumerische Zeichen (Sonderzeichen)<br/>                                                                                                               | $,!,%,^,() {} \[ \] ;:<>?<br/> |
| Alle Unicode-Zeichen, die als Zeichen des Alphabets kategorisiert sind, die aber nicht Groß- oder Kleinbuchstaben sind. Dazu zählen Unicode-Zeichen asiatischer Sprachen.<br/> |                                        |



 

**So aktivieren Sie die sichere Kennworterzwingung**

1.  Suchen Sie in der Verwaltungskonsole **nach Lokale Sicherheitsrichtlinie.**
2.  Wählen Sie **Kontorichtlinie** und dann **Kennwortrichtlinie** aus.
3.  Aktivieren Sie die Einstellung **Kennwörter müssen Komplexitätsanforderungen erfüllen.**

> [!Note]  
> Ein bestimmtes Zeichen kann nur eine Kategorie erfüllen. Die [GetStringTypeW-Funktion](/windows/win32/api/stringapiset/nf-stringapiset-getstringtypew) wird verwendet, um zu testen, ob jedes Zeichen im Kennwort groß, klein oder alphanumerisch ist.

 

 

