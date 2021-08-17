---
description: Um die Codepage einer Datenbank zu bestimmen, rufen Sie MsiDatabaseExport auf, während hDatabase auf das Handle der Datenbank und szTableName auf \_ ForceCodepage festgelegt ist.
ms.assetid: afa3fbd9-9f54-4f72-ab5d-cb0dbbd9946c
title: Bestimmen der Codepage einer Installationsdatenbank
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89825c99e0652c0ef324c99f8906281f3c87ed58bef099886220faa6a9311583
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118637849"
---
# <a name="determining-an-installation-databases-code-page"></a>Bestimmen der Codepage einer Installationsdatenbank

Um die Codepage einer Datenbank zu bestimmen, rufen Sie [**MsiDatabaseExport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) auf, während *hDatabase* auf das Handle der Datenbank und *szTableName* auf \_ ForceCodepage festgelegt ist. Dadurch wird eine Textdatei mit der Erweiterung .idt exportiert. Die ersten beiden Zeilen dieser Datei sind leer. Die dritte Zeile ist die Nummer der ANSI-Codepage, gefolgt von einer Registerkarte, gefolgt vom Namen \_ ForceCodepage. Siehe auch [Codepagebehandlung für importierte und exportierte Tabellen.](code-page-handling-of-imported-and-exported-tables.md)

Ein Beispiel für die Bestimmung der Codepage mithilfe der [**Export-Methode**](database-export.md) finden Sie im Windows Installer SDK als Teil des Hilfsprogramms WiLangId.vbs. Weitere Informationen zur Verwendung von WiLangId.vbs finden Sie im Thema Verwalten [von Sprache und Codepage.](manage-language-and-codepage.md)

 

 



