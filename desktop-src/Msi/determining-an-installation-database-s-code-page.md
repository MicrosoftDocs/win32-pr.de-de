---
description: Zum Ermitteln der Codepage einer Datenbank müssen Sie msidatabaseexport mit hDataBase auf das Handle der Datenbank und sztablename auf \_ forcecodepage festgelegt haben.
ms.assetid: afa3fbd9-9f54-4f72-ab5d-cb0dbbd9946c
title: Festlegen der Codepage einer Installations Datenbank
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 212978cbce0e73ae495a0ed10ea9070cce6bd374
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866348"
---
# <a name="determining-an-installation-databases-code-page"></a>Festlegen der Codepage einer Installations Datenbank

Zum Ermitteln der Codepage einer Datenbank müssen Sie [**msidatabaseexport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseexporta) mit *hDataBase* auf das Handle der Datenbank und *sztablename* auf \_ forcecodepage festgelegt haben. Dadurch wird eine Textdatei mit der Erweiterung IDT exportiert. Die ersten beiden Zeilen dieser Datei sind leer. Die dritte Zeile ist die ANSI-Code Page Nummer, gefolgt von einer Registerkarte, gefolgt von dem Namen \_ forcecodepage. Siehe auch [Code Page Behandlung importierter und exportierter Tabellen](code-page-handling-of-imported-and-exported-tables.md).

Ein Beispiel für die Bestimmung der Codepage mithilfe der [**Export Methode**](database-export.md) wird im Windows Installer SDK als Teil des Hilfsprogramms WiLangId.vbs bereitgestellt. Weitere Informationen zum Verwenden von WiLangId.vbs finden Sie im Thema zum [Verwalten von Sprache und Codepage](manage-language-and-codepage.md).

 

 



