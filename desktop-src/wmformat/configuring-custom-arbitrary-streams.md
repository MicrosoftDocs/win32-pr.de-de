---
title: Konfigurieren benutzerdefinierter Streams
description: Konfigurieren benutzerdefinierter Streams
ms.assetid: 09b28fd3-a0a3-44d9-b664-7421290abf02
keywords:
- Streams,Konfigurieren benutzerdefinierter beliebiger Streams
- Codecs,Konfigurieren benutzerdefinierter beliebiger Streams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b9b98b25ae9f973682ee3987ed8b590d485288e72e0b5ef7977eb7f3da0d1da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809810"
---
# <a name="configuring-custom-arbitrary-streams"></a>Konfigurieren benutzerdefinierter Streams

Wenn Sie Einen eigenen beliebigen Datentyp verwenden, müssen Sie einen GUID-Wert erstellen, der als Hauptbezeichner für den Medientyp dient. Wenn der Writer auf einen Stream in einem Profil mit einem Haupttyp trifft, der nicht erkannt wird, wird davon ausgegangen, dass es sich bei dem Stream um benutzerdefinierte beliebige Daten handelt. Sie akzeptiert Ihre Beispiele, paketiert sie und kombiniert sie mit Beispielen aus den anderen Datenströmen in der Datei, ohne die Daten in irgendeiner Weise zu überprüfen.

Sie können auch eigene GUID-Untertypbezeichner erstellen, um Unterkategorien Ihrer benutzerdefinierten Daten zu definieren. Der Writer ignoriert diese Untertypen vollständig, sie werden jedoch im Headerabschnitt der ASF-Datei beibehalten, sodass Ihre Leseanwendung sie abrufen und basierend auf ihnen Entscheidungen treffen kann.

Ein beliebiger Stream erfordert eine Bitrate und ein Pufferfenster und muss über eine [**WM \_ MEDIA \_ TYPE-Struktur**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) mit den werten verfügen, die mit Ausnahme des Hauptmedientyps und -untertyps (bei Verwendung eines ) klar sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Configuration Common to All Streams**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Konfigurieren beliebiger Streamtypen**](configuring-arbitrary-stream-types.md)
</dt> <dt>

[**Benutzerdefinierte beliebige Streams**](custom-arbitrary-data-streams.md)
</dt> </dl>

 

 




