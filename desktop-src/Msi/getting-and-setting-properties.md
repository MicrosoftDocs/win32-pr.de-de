---
description: Wenn Sie Eigenschaften in der-Installation verwenden möchten, können Sie Eigenschaftswerte mithilfe von "MsiGetProperty" und "msisetproperty" aus Programmen aufrufen und festlegen und als Teil von Bedingungs Anweisungen in die-Installations Datenbank einschließen.
ms.assetid: 65fe46d7-16b6-46ef-a440-73f954b03105
title: Festlegen und Festlegen von Eigenschaften (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0154b84af656d295b9fa84ebcca881eab1c288f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866328"
---
# <a name="getting-and-setting-properties-windows-installer"></a>Festlegen und Festlegen von Eigenschaften (Windows Installer)

Wenn Sie [Eigenschaften](properties.md) in der-Installation verwenden möchten, können Sie Eigenschaftswerte mithilfe von " [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) " und " [**msisetproperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya) " aus Programmen aufrufen und festlegen und als Teil von Bedingungs Anweisungen in die-Installations Datenbank einschließen.

-   Rufen Sie zum Abrufen einer aktuellen Eigenschaft die [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) -Funktion auf.
-   Rufen Sie zum Abrufen des aktuellen Installationsstatus die [**msigetmode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) -Funktion auf.
-   Rufen Sie zum Abrufen der Sprache für die aktuelle Installation die [**msigetlanguage**](/windows/desktop/api/Msiquery/nf-msiquery-msigetlanguage) -Funktion auf.
-   Um eine Eigenschaft festzulegen, müssen Sie die [**msisetproperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya) -Funktion aufrufen.
-   Um den Installationsstatus festzulegen, müssen Sie die [**msisetmode**](/windows/desktop/api/Msiquery/nf-msiquery-msisetmode) -Funktion aufrufen.
-   Um eine Eigenschaft zu löschen (auf NULL festzulegen), legen Sie den Wert der Eigenschaft auf eine leere Zeichenfolge fest: "".

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Eigenschaften](using-properties.md)
</dt> <dt>

[Festlegen von Werten für öffentliche Eigenschaften in der Befehlszeile](setting-public-property-values-on-the-command-line.md)
</dt> <dt>

[Löschen einer installereigenschaft](clearing-an-installer-property.md)
</dt> </dl>

 

 



