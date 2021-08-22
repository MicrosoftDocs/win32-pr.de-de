---
description: Die WriteIniValues-Aktion schreibt die .ini Dateiinformationen, die die Anwendung benötigt, in ihre .ini Dateien geschrieben werden.
ms.assetid: ec54db54-293c-4db3-81af-6e8669f27310
title: WriteIniValues-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce2551725e7b12a697e35b08b403011044bbd631b3ff5bf3d0a5923ecb4c99e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942098"
---
# <a name="writeinivalues-action"></a>WriteIniValues-Aktion

Die WriteIniValues-Aktion schreibt die .ini Dateiinformationen, die die Anwendung benötigt, in ihre .ini Dateien geschrieben werden. Das Schreiben dieser Informationen wird durch die [Component-Tabelle](component-table.md)geschlossen. Ein .ini Wert wird geschrieben, wenn die entsprechende Komponente entweder lokal installiert oder von der Quelle ausgeführt wurde.

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Die InstallValidate-Aktion muss vor der WriteIniValues-Aktion erfolgen. Wenn die Sequenz eine [RemoveIniValues-Aktion](removeinivalues-action.md) enthält, muss sie vor der WriteIniValues-Aktion stehen.

## <a name="actiondata-messages"></a>ActionData-Nachrichten



| Feld | Beschreibung der Aktionsdaten              |
|-------|-----------------------------------------|
| \[1\] | Bezeichner .ini Datei.                |
| \[2\] | .ini Dateischlüssel im folgenden Abschnitt. |
| \[3\] | Aus .ini Datei entferntes Element.            |
| \[4\] | Aus .ini Datei entfernter Wert.           |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IniFile-Tabelle](inifile-table.md)
</dt> </dl>

 

 



