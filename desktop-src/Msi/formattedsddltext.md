---
description: Ein Datenbankfeld des formattedsddltext-Datentyps enthält eine Text Zeichenfolge, die eine Sicherheits Beschreibung mithilfe der gültigen SDDL (Security Deskriptor Definition Language) beschreibt. Dieser Datentyp wird vom sddltext-Feld der msilockpermissionsex-Tabelle zum Sichern eines ausgewählten Objekts verwendet. Beachten Sie, dass das Feld "sddltext" der Tabelle "msilockpermissionsex" keine privaten oder öffentlichen Eigenschaften unterstützt.
ms.assetid: a36e257d-ef3c-45db-a50e-94d7fd4e09e2
title: Formattedsddltext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06ddfeac55f05ebea5f1603def6adcbac32aa9d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353194"
---
# <a name="formattedsddltext"></a>Formattedsddltext

Ein Datenbankfeld des **formattedsddltext** -Datentyps enthält eine Text Zeichenfolge, die eine Sicherheits Beschreibung mithilfe der gültigen SDDL ( [Security Deskriptor Definition Language](../secauthz/security-descriptor-definition-language.md) ) beschreibt. Dieser Datentyp wird vom sddltext-Feld der [msilockpermissionsex-Tabelle](msilockpermissionsex-table.md) zum Sichern eines ausgewählten Objekts verwendet. Beachten Sie, dass das Feld "sddltext" der Tabelle "msilockpermissionsex" keine privaten oder öffentlichen Eigenschaften unterstützt.

**[Windows Installer 4,5 oder früher](not-supported-in-windows-installer-4-5.md):** Nicht unterstützt. Dieser Datentyp ist ab Windows Installer 5,0 verfügbar.

Der **formattedsddltext** -Datentyp kann eine SDDL-Zeichenfolge enthalten, die im gültigen [Zeichen folgen Format der Sicherheits Beschreibung](../secauthz/security-descriptor-string-format.md)geschrieben ist. Weitere Informationen zu SDDL finden Sie im Abschnitt [Access Control](../secauthz/access-control.md) des [Microsoft Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads/windows-10-sdk/). Außerdem kann eine **formattedsddltext** -Text Zeichenfolge eckige Klammern (<>) verwenden, die die Domäne und den Benutzernamen des Benutzers enthalten, dessen Konto-SID bestimmt werden soll.

Wenn der Benutzer mit dem Benutzernamen *sampleuser* zu einer Domäne namens *sampledomain* gehört, kann der Wert von **formattedsddltext** anhand der SID-Zeichenfolge, mit dem Benutzernamen und dem Domänen Namen oder den Windows-Umgebungsvariablen identifiziert werden. Die folgenden Zeichen folgen sind z. b. möglich.

<dl> O:*Besitzer- \_ sid- \_ Zeichenfolge* g:Bad: (D; oici; GA;;; BG) (A; oici; grgwgx;;; *Besitzer- \_ sid- \_ Zeichenfolge*) (A; oici; GA;;; BA) s:Arai (au; Safa, FA;;; Zel  
O: <*sampledomain \\ sampleuser*>g:Bad: (D; oici; GA;;; BG) (A; oici; grgwgx;;; <*sampledomain \\ sampleuser*>) (A; oici; GA;;; BA) s:Arai (au; Safa, FA;;; Zel  
O: <\[ % User Domain \] \\ \[ % username \]>g:Bad: (D; oici; GA;;; BG) (A; oici; grgwgx;;; <\[ % User Domain \] \\ \[ % username \]>) (A; oici; GA;;; BA) s:Arai (au; Safa, FA;;; Zel
</dl>

 

 
