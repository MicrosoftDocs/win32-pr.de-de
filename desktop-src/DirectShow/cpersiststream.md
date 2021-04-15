---
description: Cpersiststream ist die Basisklasse für persistente Eigenschaften von Filtern (d. h. Filtereigenschaften in gespeicherten Diagrammen).
ms.assetid: 8073e2be-aaf9-4b01-a7d5-bab5c1dcc19b
title: Cpersiststream-Klasse
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
ms.openlocfilehash: 690a0f45fab7c3612d215a859798460abc81728e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520784"
---
# <a name="cpersiststream-class"></a>Cpersiststream-Klasse

![cpersiststream-Klassenhierarchie](images/pstrm01.png)

`CPersistStream` ist die Basisklasse für persistente Eigenschaften von Filtern (d. h. Filtereigenschaften in gespeicherten Diagrammen).

Die einfachste Möglichkeit zur Verwendung `CPersistStream` von ist:

1.  Ordnen Sie den Filter an, um diese Klasse zu erben.
2.  Implementieren Sie " [**Write-to-Stream**](cpersiststream-writetostream.md) " und "read [**FromStream**](cpersiststream-readfromstream.md) " in ihrer Klasse. Diese Funktionen überschreiben hier die Funktionen, die nur als Platzhalter fungieren.
3.  Ändern Sie die **nondelegatingqueryinterface** so, dass **IPersistStream** verarbeitet wird.
4.  Implementieren Sie [**sizemax**](cpersiststream-sizemax.md) , um eine obere Grenze für die Anzahl der Daten Bytes zurückzugeben, die Sie speichern.

    Wenn Sie Unicode-™ Daten speichern, denken Sie daran, dass es sich bei WCHAR um 2 Bytes handelt.

5.  Wenn sich die Daten ändern, müssen Sie [**SetDirty**](cpersiststream-setdirty.md)aufrufen.

## <a name="version-numbers"></a>Versionsnummern

An einem bestimmten Punkt können Sie sich entscheiden, das Format der Daten zu ändern oder zu erweitern. Sie haben dann die Möglichkeit, eine Versionsnummer in allen alten gespeicherten Streams zu haben, damit Sie feststellen können, ob Sie das alte oder neue Formular darstellen. Zur Unterstützung dieser Klasse wird eine Versionsnummer geschrieben und gelesen. Beim Schreiben wird [**getsoftwareversion**](cpersiststream-getsoftwareversion.md) aufgerufen, um die Version der derzeit verwendeten Software zu übermitteln. (Dies ist tatsächlich eine Versionsnummer des Daten Layouts in der Datei.) Dies wird als erstes in den Daten geschrieben. Wenn Sie die Version ändern möchten, implementieren Sie " **getsoftwareversion**" (außer Kraft setzen). Vor dem Aufrufen von [**readfromstream**](cpersiststream-readfromstream.md)liest Sie die Versionsnummer aus der Datei in **mPS \_ dwfileversion** , sodass Sie in **readfromstream** die **MPS \_ dwfileversion** überprüfen können, um festzustellen, ob Sie eine alte Versionsdatei lesen. Normalerweise sollten Sie Dateien akzeptieren, deren Version nicht neuer ist als die Softwareversion, die Sie liest.

**Cpersiststream** implementiert [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream). Weitere Implementierungs Informationen finden Sie in der com-Referenz im Microsoft Platform SDK.



| Geschützte Datenmember                                          | BESCHREIBUNG                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------|
| mPS \_ dwfileversion                                              | Versionsnummer der Datei.                                                   |
| mPS-fehlerhaft \_                                                     | Die Daten für diesen Stream müssen gespeichert werden.                                           |
| Elementfunktionen                                                | BESCHREIBUNG                                                                   |
| [**Cpersiststream**](cpersiststream-cpersiststream.md)         | Erstellt ein **cpersiststream** -Objekt.                                       |
| [**SetDirty**](cpersiststream-setdirty.md)                     | Gibt an, dass das Objekt im Stream gespeichert werden muss.                        |
| Über schreibbare Member-Funktionen                                    | BESCHREIBUNG                                                                   |
| [**GetClassID**](cpersiststream-getclassid.md)                 | Ruft den Klassen Bezeichner dieses Streams ab.                                |
| [**Getsoftwareversion**](cpersiststream-getsoftwareversion.md) | Ruft die Versionsnummer für dieses Dateiformat ab.                            |
| [**"Read FromStream"**](cpersiststream-readfromstream.md)         | Liest die Filterdaten aus dem Datenstrom.                                      |
| [**Sizemax**](cpersiststream-sizemax.md)                       | Ruft die Anzahl der Bytes ab, die für Daten benötigt werden (nicht einschließlich der Versionsnummer). |
| [**Schreiben von Datenstrom**](cpersiststream-writetostream.md)           | Schreibt die Filterdaten in den Stream.                                       |
| IPersistStream-Methoden                                          | BESCHREIBUNG                                                                   |
| [**GetSizeMax**](cpersiststream-getsizemax.md)                 | Ruft die Anzahl der Bytes ab, die für Daten benötigt werden (einschließlich der Versionsnummer).     |
| [**IsDirty**](cpersiststream-isdirty.md)                       | Überprüft, ob das Objekt gespeichert werden muss.                                           |
| [**Laden**](cpersiststream-load.md)                             | Lädt die Daten aus dem Stream in den Arbeitsspeicher.                                   |
| [**Speichern**](cpersiststream-save.md)                             | Speichert die Daten aus dem Arbeitsspeicher in den Stream.                                     |



 

 

 
