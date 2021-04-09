---
description: In den folgenden Abschnitten wird beschrieben, wie die integrierten Installer-Eigenschaften und zusätzlichen Eigenschaften, die vom Paket Autor definiert werden, verwendet werden.
ms.assetid: 5a2f1cd4-2bbd-414a-a814-8b9fdab434b4
title: Verwenden von Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edab44953f6ccd210d5baa3c446363a1131dc745
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129360"
---
# <a name="using-properties"></a>Verwenden von Eigenschaften

In den folgenden Abschnitten wird beschrieben, wie die integrierten Installer-Eigenschaften und zusätzlichen Eigenschaften, die vom Paket Autor definiert werden, verwendet werden. Eigenschaften können entweder [öffentliche Eigenschaften](public-properties.md) oder [private Eigenschaften](private-properties.md)sein. Jede Eigenschaft, die bei der Initialisierung des Installers definiert werden muss, muss den Namen und den Anfangswert in der [Eigenschaften Tabelle](property-table.md)auflisten. Eigenschaften, die einen NULL-Wert haben, sind nicht in der Eigenschaften Tabelle aufgeführt. Sie können Eigenschaften aus Programmen und benutzerdefinierten Aktionen erhalten oder festlegen und öffentliche Eigenschaften über die Befehlszeile festlegen. Der Installationsvorgang kann mithilfe von Eigenschaften in bedingten Anweisungen geändert werden.

[Einschränkungen für Eigenschaftsnamen](restrictions-on-property-names.md)

[Initialisierung von Eigenschafts Werten](initialization-of-property-values.md)

[Eigenschaften werden erhalten und festgelegt](getting-and-setting-properties.md)

[Verwenden von Eigenschaften in Bedingungs Anweisungen](using-properties-in-conditional-statements.md)

[Verwenden einer Verzeichnis Eigenschaft in einem Pfad](using-a-directory-property-in-a-path.md)

> [!Note]  
> Verwenden Sie keine Eigenschaften für Kenn Wörter oder andere Informationen, die sicher bleiben müssen. Das Installationsprogramm kann den Wert einer Eigenschaft, die in die Eigenschaften Tabelle geschrieben oder zur Laufzeit erstellt wurde, in ein Protokoll oder die Systemregistrierung schreiben.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu Eigenschaften](about-properties.md)
</dt> <dt>

[Eigenschafts Verweis](property-reference.md)
</dt> </dl>

 

 



