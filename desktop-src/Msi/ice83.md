---
description: ICE83 überprüft die MsiAssembly-Tabelle.
ms.assetid: dd290c73-6528-482d-8276-ac56d0fec181
title: ICE83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78e8014f8feee76e4d1910fb601e186bec928a0fd6d6d34469ce2c2b201b724d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580750"
---
# <a name="ice83"></a>ICE83

ICE83 überprüft die [MsiAssembly-Tabelle](msiassembly-table.md). Diese benutzerdefinierte ICE-Aktion gibt einen Fehler aus, wenn der Schlüsselpfad für eine Komponente, die eine Win32-Assembly enthält, auf die Manifestdatei festgelegt ist. Der Fehler wird explizit ausgegeben, wenn der in das KeyPath-Feld der [Component-Tabelle](component-table.md) eingegebene Wert dem Wert entspricht, der in das \_ Feld Dateimanifest der MsiAssembly-Tabelle eingegeben wurde. Diese benutzerdefinierte ICE-Aktion sendet einen Fehler, wenn mindestens ein Datensatz in der MsiAssembly-Tabelle vorhanden ist und die [Tabelle InstallExecuteSequence](installexecutesequence-table.md) nicht sowohl die [MsiPublishAssemblies-Aktion](msipublishassemblies-action.md) als auch [die MsiUnpublishAssemblies-Aktion](msiunpublishassemblies-action.md)enthält.

## <a name="result"></a>Ergebnis

ICE83 gibt die folgenden Fehler aus.



| ICE83-Fehler                                                                                                   | Beschreibung                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Der Schlüsselpfad für die Win32-SXS-Assembly (Komponente \_ = \[ \] 1) SOLLTE NICHT die Manifestdatei sein.                       | ICE83 sendet diesen Fehler, wenn das KeyPath-Feld für eine Win32-Assembly auf die Manifestdatei (Component.KeyPath == MsiAssembly.File Manifest) festgelegt \_ ist. \[1 \] ist KeyPath in der Komponententabelle                          |
| Sowohl MsiPublishAssemblies- als auch MsiUnpublishAssemblies-Aktionen MÜSSEN in der Tabelle InstallExecuteSequence vorhanden sein. | ICE83 sendet diesen Fehler, wenn mindestens ein Eintrag in der MsiAssembly-Tabelle vorhanden ist, die Tabelle InstallExecuteSequence jedoch nicht sowohl die MsiAssemblyPublish-Aktion als auch die MsiAssemblyUnpublish-Aktion enthält. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 



