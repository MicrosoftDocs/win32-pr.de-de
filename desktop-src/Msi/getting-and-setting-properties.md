---
description: Um Eigenschaften in Ihrer Installation zu verwenden, können Sie Eigenschaftswerte von Programmen mit msiGetProperty und MsiSetProperty erhalten und festlegen und als Teil von Bedingungsanweisungen in die Installationsdatenbank einverhalten.
ms.assetid: 65fe46d7-16b6-46ef-a440-73f954b03105
title: Abrufen und Festlegen von Eigenschaften (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1009fc9370a870c53b3fe5ad471f52dea195648b36bab28dff76fe1271283be1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635950"
---
# <a name="getting-and-setting-properties-windows-installer"></a>Abrufen und Festlegen von Eigenschaften (Windows Installer)

Um [Eigenschaften](properties.md) in Ihrer Installation zu verwenden, können Sie Eigenschaftswerte von Programmen mit [**msiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) und [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya) erhalten und festlegen und als Teil von Bedingungsanweisungen in die Installationsdatenbank einverhalten.

-   Um eine aktuelle Eigenschaft zu erhalten, rufen Sie die [**MsiGetProperty-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) auf.
-   Rufen Sie die [**MsiGetMode-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) auf, um den aktuellen Installationsstatus zu erhalten.
-   Rufen Sie die [**MsiGetLanguage-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msigetlanguage) auf, um die Sprache für die aktuelle Installation zu erhalten.
-   Rufen Sie zum Festlegen einer Eigenschaft die [**MsiSetProperty-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya) auf.
-   Rufen Sie zum Festlegen des Installationsstatus die [**MsiSetMode-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msisetmode) auf.
-   Um eine Eigenschaft zu löschen (indem Sie sie auf NULL festlegen), legen Sie den Wert der Eigenschaft auf eine leere Zeichenfolge fest: "".

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Eigenschaften](using-properties.md)
</dt> <dt>

[Festlegen von öffentlichen Eigenschaftswerten in der Befehlszeile](setting-public-property-values-on-the-command-line.md)
</dt> <dt>

[Löschen einer Installer-Eigenschaft](clearing-an-installer-property.md)
</dt> </dl>

 

 



