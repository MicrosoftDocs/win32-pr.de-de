---
description: Verwenden Sie die folgenden Optionsflags, um anzugeben, dass das Installationsprogramm den in das Feld Ziel der CustomAction-Tabelle eingegebenen Wert nicht in das Protokoll schreibt. Fügen Sie zum Festlegen der Option den Wert in dieser Tabelle dem Wert im Feld Typ der CustomAction-Tabelle hinzu.
ms.assetid: b0f99851-a774-4804-8c85-f94943c2d2b0
title: Option "Ausgeblendetes Ziel für benutzerdefinierte Aktion"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1adc0df477510ac7d5d6bec65025b6fed1bfd7971e6ddf35da3a7e4cbc714690
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118638163"
---
# <a name="custom-action-hidden-target-option"></a>Option "Ausgeblendetes Ziel für benutzerdefinierte Aktion"

Verwenden Sie die folgenden Optionsflags, um anzugeben, dass das Installationsprogramm den in das Feld Ziel der [CustomAction-Tabelle](customaction-table.md) eingegebenen Wert nicht in das Protokoll schreibt. Fügen Sie zum Festlegen der Option den Wert in dieser Tabelle dem Wert im Feld Typ der CustomAction-Tabelle hinzu.



| Konstante                            | Hexadezimal | Decimal | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------|-------------|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| (none)                              | 0x0000      | 0       | Das Installationsprogramm kann den Wert in der Spalte Ziel der CustomAction-Tabelle in die Protokolldatei schreiben.                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **msidbCustomActionTypeHideTarget** | 0x2000      | 8192    | Das Installationsprogramm kann den Wert in der Spalte Ziel der [CustomAction-Tabelle](customaction-table.md) nicht in die Protokolldatei schreiben. Die CustomActionData-Eigenschaft wird auch nicht protokolliert, wenn das Installationsprogramm die benutzerdefinierte Aktion ausgeführt.<br/> Da das Installationsprogramm den Wert von CustomActionData aus einer Eigenschaft mit dem gleichen Namen wie die benutzerdefinierte Aktion legt, muss diese Eigenschaft in der [**MsiHiddenProperties-Eigenschaft**](msihiddenproperties.md) aufgeführt werden, um zu verhindern, dass ihr Wert im Protokoll angezeigt wird.<br/> |



 

Weitere Informationen finden Sie unter [Verhindern, dass vertrauliche Informationen in die Protokolldatei geschrieben werden.](preventing-confidential-information-from-being-written-into-the-log-file.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Referenz zu benutzerdefinierten Aktionen](custom-action-reference.md)
</dt> <dt>

[Informationen zu benutzerdefinierten Aktionen](about-custom-actions.md)
</dt> <dt>

[Verwenden benutzerdefinierter Aktionen](using-custom-actions.md)
</dt> </dl>

 

 




