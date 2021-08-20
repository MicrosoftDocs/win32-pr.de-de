---
description: Ein Datenbankfeld des Datentyps FormattedSDDLText enthält eine Textzeichenfolge, die einen Sicherheitsdeskriptor mithilfe einer gültigen Sicherheitsbeschreibungsdefinitionssprache (SDDL) beschreibt. Dieser Datentyp wird vom SDDLText-Feld der MsiLockPermissionsEx-Tabelle verwendet, um ein ausgewähltes Objekt zu schützen. Beachten Sie, dass das SDDLText-Feld der MsiLockPermissionsEx-Tabelle keine privaten oder öffentlichen Eigenschaften unterstützt.
ms.assetid: a36e257d-ef3c-45db-a50e-94d7fd4e09e2
title: FormattedSDDLText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdfc4446c4362646e8c275ec427f759b8aec6a257d5221926431434688b91c7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142889"
---
# <a name="formattedsddltext"></a>FormattedSDDLText

Ein Datenbankfeld des **Datentyps FormattedSDDLText** enthält eine Textzeichenfolge, die einen Sicherheitsdeskriptor mithilfe einer gültigen Sicherheitsbeschreibungsdefinitionssprache (SDDL) beschreibt. [](../secauthz/security-descriptor-definition-language.md) Dieser Datentyp wird vom SDDLText-Feld der [MsiLockPermissionsEx-Tabelle](msilockpermissionsex-table.md) verwendet, um ein ausgewähltes Objekt zu schützen. Beachten Sie, dass das SDDLText-Feld der MsiLockPermissionsEx-Tabelle keine privaten oder öffentlichen Eigenschaften unterstützt.

**[Windows Installer 4.5 oder früher:](not-supported-in-windows-installer-4-5.md)** Nicht unterstützt. Dieser Datentyp ist ab Windows Installer 5.0 verfügbar.

Der **FormattedSDDLText-Datentyp** kann eine SDDL-Zeichenfolge enthalten, die im [gültigen Sicherheitsbeschreibungszeichenfolgenformat geschrieben ist.](../secauthz/security-descriptor-string-format.md) Weitere Informationen zu SDDL finden Sie im [abschnitt](../secauthz/access-control.md) Access Control des Microsoft Windows Software Development [Kit (SDK).](https://developer.microsoft.com/windows/downloads/windows-10-sdk/) Darüber hinaus kann eine **FormattedSDDLText-Textzeichenfolge** eckige Klammern (<>) verwenden, um die Domäne und den Benutzernamen des Benutzers zu enthalten, dessen Konto-SID bestimmt werden soll.

Wenn der Benutzer mit dem Benutzernamen *SampleUser* zu einer Domäne mit dem Namen *SampleDomain* gehört, kann der **Wert FormattedSDDLText** den Besitzer anhand der SID-Zeichenfolge, des Benutzernamens und Domänennamens oder der Windows-Umgebungsvariablen identifizieren. Beispielsweise sind die folgenden Zeichenfolgen möglich.

<dl> O:*owner \_ sid \_ string* G:BAD:(D;OICI;GA;;; BG)(A;OICI;GRGWGX;;; *owner \_ sid \_ string*)(A;OICI;GA;;; BA)S:ARAI(AU; BESEN;FA;;; WD)  
O:<*SampleDomain \\ SampleUser*>G:BAD:(D;OICI;GA;;; BG)(A;OICI;GRGWGX;;; <*SampleDomain \\ SampleUser*>)(A;OICI;GA;;; BA)S:ARAI(AU; BESEN;FA;;; WD)  
O:<\[ %USERDOMAIN \] \\ \[ %USERNAME \]>G:BAD:(D;OICI;GA;;; BG)(A;OICI;GRGWGX;;; <\[ %USERDOMAIN \] \\ \[ %USERNAME \]>)(A;OICI;GA;;; BA)S:ARAI(AU; BESEN;FA;;; WD)
</dl>

 

 
