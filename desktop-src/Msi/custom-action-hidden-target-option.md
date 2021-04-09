---
description: Verwenden Sie die folgenden Optionsflags, um anzugeben, dass das Installationsprogramm den Wert, der in das Zielfeld der CustomAction-Tabelle eingegeben wurde, nicht in das Protokoll schreibt. Legen Sie zum Festlegen der Option den Wert in dieser Tabelle dem Wert im type-Feld der CustomAction-Tabelle hinzu.
ms.assetid: b0f99851-a774-4804-8c85-f94943c2d2b0
title: Option "ausgeblendetes Ziel"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acca69e4c3efc2b43302bf926a56bc53b2bf5e7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042399"
---
# <a name="custom-action-hidden-target-option"></a>Option "ausgeblendetes Ziel"

Verwenden Sie die folgenden Optionsflags, um anzugeben, dass das Installationsprogramm den Wert, der in das Zielfeld der [CustomAction-Tabelle](customaction-table.md) eingegeben wurde, nicht in das Protokoll schreibt. Legen Sie zum Festlegen der Option den Wert in dieser Tabelle dem Wert im type-Feld der CustomAction-Tabelle hinzu.



| Konstante                            | Hexadezimal | Decimal | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------|-------------|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| (none)                              | 0x0000      | 0       | Der Installer kann den Wert in der Ziel Spalte der CustomAction-Tabelle in die Protokolldatei schreiben.                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| **msidbcustomaktiontypehidetarget** | 0x2000      | 8192    | Das Installationsprogramm wird daran gehindert, den Wert in der Ziel Spalte der [CustomAction-Tabelle](customaction-table.md) in die Protokolldatei zu schreiben. Die CustomAction Data-Eigenschaft wird auch nicht protokolliert, wenn das Installationsprogramm die benutzerdefinierte Aktion ausführt.<br/> Da das Installationsprogramm den Wert von CustomAction Data aus einer Eigenschaft mit demselben Namen wie die benutzerdefinierte Aktion festlegt, muss diese Eigenschaft in der Eigenschaft [**msihiddenproperties**](msihiddenproperties.md) aufgeführt werden, um zu verhindern, dass der Wert im Protokoll angezeigt wird.<br/> |



 

Weitere Informationen finden Sie unter [verhindern, dass vertrauliche Informationen in die Protokolldatei geschrieben werden](preventing-confidential-information-from-being-written-into-the-log-file.md) .

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Referenz zu benutzerdefinierten Aktionen](custom-action-reference.md)
</dt> <dt>

[Informationen zu benutzerdefinierten Aktionen](about-custom-actions.md)
</dt> <dt>

[Verwenden von benutzerdefinierten Aktionen](using-custom-actions.md)
</dt> </dl>

 

 




