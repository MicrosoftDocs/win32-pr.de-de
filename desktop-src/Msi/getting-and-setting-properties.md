---
description: Um Eigenschaften in ihrer Installation zu verwenden, können Sie Eigenschaftswerte aus Programmen abrufen und festlegen, indem Sie MsiGetProperty und MsiSetProperty verwenden und als Teil von bedingten Anweisungen in die Installationsdatenbank einschließen.
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

Um [Eigenschaften](properties.md) in ihrer Installation zu verwenden, können Sie Eigenschaftswerte aus Programmen abrufen und festlegen, indem [**Sie MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) und [**MsiSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya) verwenden und als Teil von bedingten Anweisungen in die Installationsdatenbank einschließen.

-   Um eine aktuelle Eigenschaft abzurufen, rufen Sie die [**MsiGetProperty-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) auf.
-   Rufen Sie die [**MsiGetMode-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) auf, um den aktuellen Installationsstatus abzurufen.
-   Rufen Sie die [**MsiGetLanguage-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msigetlanguage) auf, um die Sprache für die aktuelle Installation abzurufen.
-   Um eine Eigenschaft festzulegen, rufen Sie die [**MsiSetProperty-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msisetpropertya) auf.
-   Um den Installationsstatus festzulegen, rufen Sie die [**MsiSetMode-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msisetmode) auf.
-   Um eine Eigenschaft zu löschen (legen Sie sie auf NULL fest), legen Sie den Wert der Eigenschaft auf eine leere Zeichenfolge fest: "".

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Eigenschaften](using-properties.md)
</dt> <dt>

[Festlegen öffentlicher Eigenschaftswerte in der Befehlszeile](setting-public-property-values-on-the-command-line.md)
</dt> <dt>

[Löschen einer Installer-Eigenschaft](clearing-an-installer-property.md)
</dt> </dl>

 

 



