---
description: Die fourccmap-Klasse ermöglicht die Konvertierung zwischen Untertypen von GUID-Medien und herkömmlichen viercc-32-Bit-Medien Tags.
ms.assetid: f77f1da9-34f6-44a0-9f1a-7db2e5a26268
title: Fourccmap-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FOURCCMap
api_type:
- COM
api_location: ''
ms.openlocfilehash: fd30a0f04d98b4c6ba4b7716a1a72d527873dbff
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124550"
---
# <a name="fourccmap-class"></a>Fourccmap-Klasse

![fourccmap-Klassenhierarchie](images/fourcc01.png)

Die **fourccmap** -Klasse ermöglicht die Konvertierung zwischen Untertypen von **GUID** -Medien und herkömmlichen **viercc** -32-Bit-Medien Tags. In den ursprünglichen Windows-Multimedia-APIs wurden Medientypen mit 32-Bit-Werten gekennzeichnet, die aus 4 8-Bit-Zeichen erstellt wurden und als **FourCC** s bezeichnet wurden. DirectShow-Medientypen haben **GUID** s für den Untertyp, da diese einfacher zu erstellen sind (die Erstellung einer neuen **FourCC** erfordert die Registrierung bei Microsoft). Da **FourCC** s eindeutig sind, wurde eine eins-zu-Eins-Zuordnung ermöglicht, indem ein Bereich von 4 Milliarden **GUID** s zugeordnet wurde, die **FourCC** s darstellen. Bei diesem Bereich handelt es sich um alle **GUID**-Werte der folgenden Form:

`XXXXXXXX-0000-0010-8000-00AA00389B71`

Diese Klasse vereinfacht die Konvertierung zwischen **GUID** s und **FourCC** s. Dies dient nur zur Kompatibilität. Es wird empfohlen, dass alle neuen Medien Untertypen durch **GUID** s dargestellt werden, die von Guidgen.exe oder einem ähnlichen Tool erstellt werden, und nicht durch Zuordnung von **FourCC** s.

Das-Objekt wird von einer **GUID**, ohne zusätzliche Datenmember, abgeleitet und kann in eine **GUID** umgewandelt werden. An das Objekt kann ein **FourCC** zur Konstruktionszeit übermittelt werden. Der Standardkonstruktor initialisiert den **FourCC** -Wert mit 0 (null).

Die Methoden [**getfourcc**](fourccmap-getfourcc.md) und [**setfourcc**](fourccmap-setfourcc.md) überprüfen nicht, ob die festgelegten Teile der **GUID** dem **FourCC** -Bereich entsprechen. Wenn Sie einen Zeiger auf eine **GUID** in einen Zeiger auf ein **FourCC** umwandeln und dann das Feld " **FourCC** " festlegen oder festlegen, müssen Sie auch separat überprüfen, ob die **GUID** im Bereich " **FourCC** " liegt.

## <a name="member-functions"></a>Elementfunktionen



|                                          |                                                          |
|------------------------------------------|----------------------------------------------------------|
| [**Fourccmap**](fourccmap-fourccmap.md) | Konstruktormethode.                                      |
| [**Getfourcc**](fourccmap-getfourcc.md) | Ruft den **FourCC** von einem **fourccmap** -Objekt ab.    |
| [**Setfourcc**](fourccmap-setfourcc.md) | Legt den **FourCC** -Teil des **fourccmap** -Objekts fest. |



 

 

 



