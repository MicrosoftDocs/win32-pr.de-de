---
description: CPersistStream ist die Basisklasse für persistente Eigenschaften von Filtern (d.amp;#160;B. Filtereigenschaften in gespeicherten Diagrammen).
ms.assetid: 8073e2be-aaf9-4b01-a7d5-bab5c1dcc19b
title: CPersistStream-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream
api_type:
- COM
api_location: ''
ms.openlocfilehash: 60a48b35ae1559e9b8dfa718c5bca38689cdf0101ce4a343a907b713c8988de0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073579"
---
# <a name="cpersiststream-class"></a>CPersistStream-Klasse

![cpersiststream-Klassenhierarchie](images/pstrm01.png)

`CPersistStream` ist die Basisklasse für persistente Eigenschaften von Filtern (d. b. Filtereigenschaften in gespeicherten Diagrammen).

Die einfachste Möglichkeit zur Verwendung `CPersistStream` ist Folgendes:

1.  Ordnen Sie an, dass der Filter diese Klasse erbt.
2.  Implementieren Sie [**WriteToStream**](cpersiststream-writetostream.md) und [**ReadFromStream**](cpersiststream-readfromstream.md) in Ihrer Klasse. Diese überschreiben hier die Funktionen, die nur als Platzhalter fungieren.
3.  Ändern Sie **NonDelegatingQueryInterface** so, dass **IPersistStream** behandelt wird.
4.  Implementieren Sie [**SizeMax,**](cpersiststream-sizemax.md) um eine Obergrenze für die Anzahl der von Ihnen gespeicherten Datenbytes zurückzugeben.

    Wenn Sie Unicode™ Daten speichern, denken Sie daran, dass ein WCHAR-Wert 2 Bytes beträgt.

5.  Wenn sich Ihre Daten ändern, rufen [**Sie SetDirty**](cpersiststream-setdirty.md)auf.

## <a name="version-numbers"></a>Versionsnummern

Zu einem bestimmten Zeitpunkt können Sie das Format Ihrer Daten ändern oder erweitern. Sie möchten dann, dass Sie in allen alten gespeicherten Streams eine Versionsnummer haben, damit Sie beim Lesen erkennen können, ob sie das alte oder das neue Formular darstellen. Zur Unterstützung schreibt und liest diese Klasse eine Versionsnummer. Beim Schreiben ruft es [**GetSoftwareVersion**](cpersiststream-getsoftwareversion.md) auf, um nach der Version der software zu fragen, die derzeit verwendet wird. (Dies ist eine Versionsnummer des Datenlayouts in der Datei.) Dies wird als erstes in die Daten geschrieben. Wenn Sie die Version ändern möchten, implementieren Sie **GetSoftwareVersion**(überschreiben). Es liest die Versionsnummer aus der Datei in **mPS \_ dwFileVersion,** bevor [**ReadFromStream**](cpersiststream-readfromstream.md)aufgerufen wird. In **ReadFromStream** können Sie also **mPS \_ dwFileVersion** überprüfen, um festzustellen, ob Sie eine alte Versionsdatei lesen. In der Regel sollten Sie Dateien akzeptieren, deren Version nicht neuer als die Softwareversion ist, die sie liest.

**CPersistStream** implementiert [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream). Weitere Implementierungsinformationen finden Sie in der COM-Referenz im Microsoft Platform SDK.



| Geschützte Datenmember                                          | Beschreibung                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------|
| mPS \_ dwFileVersion                                              | Versionsnummer der Datei.                                                   |
| mPS \_ fDirty                                                     | Daten für diesen Stream müssen gespeichert werden.                                           |
| Elementfunktionen                                                | Beschreibung                                                                   |
| [**CPersistStream**](cpersiststream-cpersiststream.md)         | Erstellt ein **CPersistStream-Objekt.**                                       |
| [**Setdirty**](cpersiststream-setdirty.md)                     | Gibt an, dass das Objekt im Stream gespeichert werden muss.                        |
| Überschreibbare Memberfunktionen                                    | Beschreibung                                                                   |
| [**Getclassid**](cpersiststream-getclassid.md)                 | Ruft den Klassenbezeichner dieses Streams ab.                                |
| [**GetSoftwareVersion**](cpersiststream-getsoftwareversion.md) | Ruft die Versionsnummer für dieses Dateiformat ab.                            |
| [**ReadFromStream**](cpersiststream-readfromstream.md)         | Liest die Daten des Filters aus dem Stream.                                      |
| [**SizeMax**](cpersiststream-sizemax.md)                       | Ruft die Anzahl der Bytes ab, die für Daten benötigt werden (ohne Versionsnummer). |
| [**WriteToStream**](cpersiststream-writetostream.md)           | Schreibt die Daten des Filters in den Stream.                                       |
| IPersistStream-Methoden                                          | Beschreibung                                                                   |
| [**GetSizeMax**](cpersiststream-getsizemax.md)                 | Ruft die Anzahl der Bytes ab, die für Daten benötigt werden (einschließlich Versionsnummer).     |
| [**IsDirty**](cpersiststream-isdirty.md)                       | Überprüft, ob das Objekt gespeichert werden muss.                                           |
| [**Laden**](cpersiststream-load.md)                             | Lädt die Daten aus dem Stream in den Arbeitsspeicher.                                   |
| [**Speichern**](cpersiststream-save.md)                             | Speichert die Daten aus dem Arbeitsspeicher im Stream.                                     |



 

 

 
