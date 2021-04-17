---
title: Der Eigenschaften Satz für Zusammenfassungs Informationen
description: COM definiert einen allgemeinen Standardeigenschaften Satz zum Speichern von Zusammenfassungs Informationen zu Dokumenten.
ms.assetid: ceed6d66-7327-4781-a5dc-9058e671138a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb318daba7e0ad03ff176853877fe416ddeda799
ms.sourcegitcommit: fc240ac77d4c40a9f3a27714d7b852abbd234774
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/12/2019
ms.locfileid: "104388835"
---
# <a name="the-summary-information-property-set"></a>Der Eigenschaften Satz für Zusammenfassungs Informationen

COM definiert einen allgemeinen Standardeigenschaften Satz zum Speichern von Zusammenfassungs Informationen zu Dokumenten. Der Eigenschaften Satz für Zusammenfassungs Informationen muss in einem Streamobjekt gespeichert werden. Das heißt, dieser Eigenschaften Satz muss als einfacher Eigenschaften Satz gespeichert werden. Weitere Informationen finden Sie unter [Speichern und Streamen von Objekten für einen Eigenschaften Satz](storage-vs--stream-for-a-property-set.md).

Um beispielsweise einen einfachen ANSI-Eigenschafts Satz zu erstellen, würden Sie [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) aufrufen, um den Eigenschaften Satz zu erstellen, indem Sie **propsetflag \_ ANSI** angeben (Simple ist der Standardtyp von Eigenschaften Satz) und dann mit einem [**IPropertyStorage:: Write**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple)-Befehl darauf schreiben. Zum Lesen des Eigenschaften Satzes würden Sie [**IPropertyStorage:: Read Multiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple)aufrufen.

Alle freigegebenen Eigenschaften Sätze werden durch einen Datenstrom-oder Speicher Namen mit dem Präfix " \\ 005" (oder 0x05) identifiziert, um anzuzeigen, dass es sich um einen Eigenschaften Satz handelt, der von den Anwendungen gemeinsam genutzt werden kann. Der Eigenschaften Satz für Zusammenfassungs Informationen ist keine Ausnahme. Der Name des Streams, der den Eigenschaften Satz für Zusammenfassungs Informationen enthält, lautet: **" \\ 005summaryinformation"**

Es ist nicht erforderlich, den Datenstrom Namen des Eigenschaften Satzes zu kennen, wenn er über die [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) -Methode oder die [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) -Methode der [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) -Schnittstelle darauf zugegriffen wird. in diesem Fall muss nur der Format Bezeichner (fmtid) bekannt sein. Die fmtid für den Eigenschaften Satz für Zusammenfassungs Informationen lautet: **F29F85E0-4FF9-1068-AB91-08002B27B3D9**

Die Deklaration für diesen Wert ist in der Header Datei als **fmtid \_ SummaryInformation** verfügbar. Weitere Informationen finden Sie unter den fmtids in den [vordefinierten Eigenschaften Satz-Format Bezeichner.](predefined-property-set-format-identifiers.md)

In der folgenden Tabelle werden die Namen der Zeichen folgen Eigenschaften für den Eigenschaften Satz für Zusammenfassungs Informationen zusammen mit den entsprechenden Eigenschafts bezeichnerbezeichnerindikatoren und den Variablen Typen (VT) aufgelistet. Die Namen werden in der Regel nicht im Eigenschaften Satz gespeichert, sondern aus dem Eigenschafts-ID-Wert abgeleitet. Die hier gezeigten Eigenschaften-ID-Zeichen folgen Einträge entsprechen den in den Header Dateien gefundenen Definitionen.

| Name | ID-Zeichenfolge | Eigenschafts-ID | VT-Typ |
|------|--------------------|-------------|---------|
| Titel | pidsi- \_ Titel | 0x00000002 | VT \_ LPSTR  |
| Subject | pidsi- \_ Betreff | 0x00000003 | VT \_ LPSTR |
| Autor | pidsi- \_ Autor | 0x00000004 | VT \_ LPSTR |
| Keywords | pidsi- \_ Schlüsselwörter | 0x00000005 | VT \_ LPSTR |
| Kommentare | pidsi- \_ Kommentare | 0x00000006 | VT \_ LPSTR |
| Vorlage | pidsi- \_ Vorlage | 0x00000007 | VT \_ LPSTR |
| Zuletzt gespeichert von | pidsi \_ lastauthor | 0x00000008 | VT \_ LPSTR |
| Revision Number | pidsi- \_ revnumber | 0x00000009 | VT \_ LPSTR |
| Bearbeitungszeit Gesamt | pidsi- \_ EditTime | 0x0000000A | VT \_ FILETIME (UTC) |
| Zuletzt gedruckt | pidsi \_ lastprint | 0x0000000b | VT \_ FILETIME (UTC) |
| Create time/date (siehe Hinweis unten) | pidsi \_ Create \_ DTM | 0x0000000c | VT \_ FILETIME (UTC) |
| Letzte gespeicherte Uhrzeit/Datum (siehe Hinweis unten) | pidsi \_ lastsave \_ DTM | 0x0000000d | VT \_ FILETIME (UTC) |
| Anzahl von Seiten | pidsi \_ Page count | 0x0000000e | VT \_ I4 |
| Anzahl von Wörtern | pidsi \_ WordCount | 0x0000000f | VT \_ I4 |
| Anzahl von Zeichen | pidsi \_ charCount | 0x00000010 | VT \_ I4 |
| Miniaturansicht | pidsi- \_ Miniaturansicht | 0x00000011 | VT \_ CF |
| Name der Anwendungs Erstellung | pidsi \_ appname | 0x00000012 | VT \_ LPSTR |
| Sicherheit | pidsi- \_ Sicherheit | 0x00000013 | VT \_ I4 |

> [!NOTE]
> Beim **Erstellen von Datum/** Uhrzeit und Datum der **letzten gespeicherten Uhrzeit**(z. b. bei einem Download von einer BBS) wird die Dateisystem Version dieser Informationen nicht ordnungsgemäß beibehalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Implementieren des Eigenschaften Satzes für Zusammenfassungs Informationen](implementing-the-summary-information-property-set.md)
</dt> </dl>

 

 




