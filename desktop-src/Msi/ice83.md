---
description: ICE83 überprüft die MsiAssembly-Tabelle.
ms.assetid: dd290c73-6528-482d-8276-ac56d0fec181
title: ICE83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5ac38b4455875314c85fa08c1cfdc329e0cb470
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042147"
---
# <a name="ice83"></a>ICE83

ICE83 überprüft die [MsiAssembly-Tabelle](msiassembly-table.md). Diese benutzerdefinierte Ice-Aktion sendet einen Fehler, wenn der Schlüssel Pfad für eine Komponente, die eine Win32-Assembly enthält, auf die Manifest-Datei festgelegt ist. Der Fehler wird explizit ausgegeben, wenn der im KEYPATH-Feld der [Komponenten Tabelle](component-table.md) eingegebene Wert gleich dem Wert ist, der im Feld "Datei \_ Manifest" der Tabelle "MsiAssembly" eingegeben wurde. Diese benutzerdefinierte Ice-Aktion gibt einen Fehler aus, wenn mindestens ein Datensatz in der MsiAssembly-Tabelle vorhanden ist und die [InstallExecuteSequence-Tabelle](installexecutesequence-table.md) nicht sowohl die [msipublishassemblierungsaktion](msipublishassemblies-action.md) als auch die [msiunpublishassemblyaktion](msiunpublishassemblies-action.md)enthält.

## <a name="result"></a>Ergebnis

ICE83 gibt die folgenden Fehler aus.



| ICE83-Fehler                                                                                                   | BESCHREIBUNG                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Der Schlüssel Pfad für die Win32-SxS-Assembly (Komponente \_ = \[ 1 \] ) sollte nicht die Manifest-Datei sein.                       | ICE83 gibt diesen Fehler aus, wenn das KEYPATH-Feld für eine Win32-Assembly auf die zugehörige Manifest-Datei (Component. KEYPATH = = MsiAssembly. File Manifest) festgelegt ist \_ . \[1 \] ist ein KEYPATH in der Component-Tabelle.                          |
| In der InstallExecuteSequence-Tabelle müssen sowohl msipublishassemblys als auch msiunpublishassemblyaktionen vorhanden sein. | ICE83 gibt diesen Fehler aus, wenn mindestens ein Eintrag in der MsiAssembly-Tabelle vorhanden ist, aber die InstallExecuteSequence-Tabelle nicht gleichzeitig die msiassemblypublish-Aktion und die msiassemblyunpublish-Aktion enthält. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



