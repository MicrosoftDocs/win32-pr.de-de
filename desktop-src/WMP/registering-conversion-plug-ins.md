---
title: Konvertieren von Konvertierungs-Plug-ins
description: Konvertieren von Konvertierungs-Plug-ins
ms.assetid: d7d6e733-7288-4707-a54a-dcaa71601646
keywords:
- Windows Media Player, Konvertierungs-Plug-ins
- Windows Media Player-Plug-ins, Konvertierung
- Plug-ins, Konvertierung
- Konvertierungs-Plug-ins, registrieren
- Registrierung, Konvertierungs-Plug-ins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 301d24e38cb4672936923cea9edd7fe6b3d2dc5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341228"
---
# <a name="registering-conversion-plug-ins"></a>Konvertieren von Konvertierungs-Plug-ins

Drittanbieter Formate müssen registriert werden, bevor Windows Media Player das Konvertierungs-Plug-in instanziieren und verwenden können. Um die Datei für die Konvertierung zu registrieren, müssen Sie die Dateinamenerweiterung registrieren, die dem Format zugeordnet ist.

Die Liste der registrierten Dateinamen Erweiterungen wird als Satz von Registrierungs Schlüsseln verwaltet. Ausführliche Informationen zum Registrieren von Drittanbieter Formaten finden Sie unter [Registrierungs Einstellungen für Dateinamen Erweiterungen](file-name-extension-registry-settings.md). In der folgenden Tabelle werden die Einstellungen der Registrierungs Werte zum Registrieren eines Drittanbieter Formats für die Konvertierung mithilfe eines Konvertierungs-Plug-Ins aufgelistet.



| Wert                  | Einstellung                                                     |
|------------------------|-------------------------------------------------------------|
| **Laufzeit**            | 13                                                          |
| **Berechtigungen**        | 8 (Berechtigungen für die Bibliothek).                             |
| **Convertpluginclsid** | Die Klassen-ID des Konvertierungs-Plug-ins im Registrierungs Format. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmier Referenz für Konvertierungs-Plug-ins**](conversion-plug-ins-programming-reference.md)
</dt> </dl>

 

 




