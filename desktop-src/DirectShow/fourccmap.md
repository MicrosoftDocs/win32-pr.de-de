---
description: Die FOURCCMap-Klasse ermöglicht die Konvertierung zwischen GUID-Medienuntertypen und 32-Bit-Medientags im alten Format.
ms.assetid: f77f1da9-34f6-44a0-9f1a-7db2e5a26268
title: FOURCCMap-Klasse
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
ms.openlocfilehash: a0ba22ce288535a8d940a5f70275f0152ffa559090d820b77df06ed3d1a9178d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043265"
---
# <a name="fourccmap-class"></a>FOURCCMap-Klasse

![fourccmap-Klassenhierarchie](images/fourcc01.png)

Die **FOURCCMap-Klasse** ermöglicht die Konvertierung zwischen **GUID-Medienuntertypen** und 32-Bit-Medientags im alten Format.  In der ursprünglichen Windows Multimedia-APIs wurden Medientypen mit 32-Bit-Werten markiert, die aus vier 8-Bit-Zeichen erstellt wurden und als **FOURCC** s bezeichnet wurden. DirectShow-Medientypen verfügen über **GUID-S** für den Untertyp, auch weil diese einfacher zu erstellen sind (die Erstellung einer neuen **FOURCC** erfordert die Registrierung bei Microsoft). Da **FOURCC-s** eindeutig sind, wurde eine 1:1-Zuordnung ermöglicht, indem ein Bereich von 4.000 Millionen **GUID-S** zugeordnet wurde, die **FOURCC** s darstellen. Bei diesem Bereich handelt es sich um alle **GUIDs** des Formulars:

`XXXXXXXX-0000-0010-8000-00AA00389B71`

Diese Klasse vereinfacht die Konvertierung zwischen **GUID** s und **FOURCC** s. Dies dient nur zur Kompatibilität. Es wird empfohlen, alle neuen Medienuntertypen durch **GUID-S** darzustellen, die von Guidgen.exe oder einem ähnlichen Tool erstellt wurden, und nicht durch Zuordnung von **FOURCC** s.

Das -Objekt wird von einer **GUID** abgeleitet, ohne zusätzliche Datenmember, und kann in eine **GUID** umgerechnet werden. Dem Objekt kann zur Erstellungszeit eine **FOURCC** übergeben werden. Der Standardkonstruktor initialisiert **FOURCC** auf 0 (null).

Die [**Methoden GetFOURCC**](fourccmap-getfourcc.md) und [**SetFOURCC**](fourccmap-setfourcc.md) überprüfen nicht, ob die festen Teile der **GUID** dem **FOURCC-Bereich** entsprechen. Wenn Sie also einen Zeiger auf eine **GUID** in einen Zeiger auf eine **FOURCC-Datei** umgewandelt und dann das **FELD FOURCC** festlegen oder abrufen, müssen Sie auch separat überprüfen, ob sich die **GUID** innerhalb des **FOURCC-Bereichs** befindet.

## <a name="member-functions"></a>Elementfunktionen



| Bezeichnung | Wert |
|------------------------------------------|----------------------------------------------------------|
| [**FOURCCMap**](fourccmap-fourccmap.md) | Konstruktormethode.                                      |
| [**GetFOURCC**](fourccmap-getfourcc.md) | Ruft die **FOURCC** aus einem **FOURCCMap-Objekt** ab.    |
| [**SetFOURCC**](fourccmap-setfourcc.md) | Legt den **FOURCC-Teil** des **FOURCCMap-Objekts** fest. |



 

 

 



