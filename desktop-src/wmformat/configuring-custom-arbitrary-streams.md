---
title: Konfigurieren von benutzerdefinierten beliebigen Streams
description: Konfigurieren von benutzerdefinierten beliebigen Streams
ms.assetid: 09b28fd3-a0a3-44d9-b664-7421290abf02
keywords:
- Streams, Konfigurieren von benutzerdefinierten beliebigen Streams
- Codecs, Konfigurieren von benutzerdefinierten beliebigen Streams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29d5cf3e95a5514ddeede9eb3c25df01ed4cd2ae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710163"
---
# <a name="configuring-custom-arbitrary-streams"></a>Konfigurieren von benutzerdefinierten beliebigen Streams

Wenn Sie Ihren eigenen beliebigen Datentyp verwenden, müssen Sie einen GUID-Wert erstellen, der als Haupt Bezeichner für den Medientyp fungiert. Wenn der Writer einen Stream in einem Profil mit einem Haupttyp findet, der nicht erkannt wird, wird davon ausgegangen, dass es sich bei dem Stream um benutzerdefinierte beliebige Daten handelt. Sie akzeptiert Ihre Beispiele, fügt Sie ein und kombiniert Sie mit Beispielen aus anderen Streams in der Datei, ohne die Daten zu überprüfen.

Sie können auch eigene GUID-Bezeichner für den Untertyp erstellen, um Unterkategorien Ihrer benutzerdefinierten Daten zu definieren. Der Writer ignoriert diese Untertypen vollständig, aber Sie werden im Header Abschnitt der ASF-Datei beibehalten, sodass Ihre Leseanwendung Sie abrufen und Entscheidungen basierend auf diesen treffen kann.

Ein beliebiger Stream erfordert eine Bitrate und ein Puffer Fenster und muss über eine [**WM- \_ \_ Medientyp**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) Struktur mit den Werten verfügen, die mit Ausnahme des Hauptmedien Typs und des Untertyps (bei Verwendung eines) gelöscht werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Allgemeine Konfiguration für alle Streams**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Konfigurieren beliebiger Streamtypen**](configuring-arbitrary-stream-types.md)
</dt> <dt>

[**Benutzerdefinierte beliebige Datenströme**](custom-arbitrary-data-streams.md)
</dt> </dl>

 

 




