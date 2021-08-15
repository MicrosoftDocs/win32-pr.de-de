---
title: Eigenschaftensatz "Zusammenfassungsinformationen"
description: COM definiert einen allgemeinen Standardeigenschaftssatz zum Speichern von Zusammenfassungsinformationen zu Dokumenten.
ms.assetid: ceed6d66-7327-4781-a5dc-9058e671138a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a54f942d0c7f6c7d1ebc37feda80d55420ea6c8aaf896f4df15df2a5b7e7c0ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118886826"
---
# <a name="the-summary-information-property-set"></a>Eigenschaftensatz "Zusammenfassungsinformationen"

COM definiert einen allgemeinen Standardeigenschaftssatz zum Speichern von Zusammenfassungsinformationen zu Dokumenten. Der Eigenschaftensatz Zusammenfassungsinformationen muss in einem Streamobjekt gespeichert werden. Das heißt, dieser Eigenschaftensatz muss als einfacher Eigenschaftensatz gespeichert werden. Weitere Informationen finden Sie unter [Storage und Stream-Objekte für einen Eigenschaftensatz.](storage-vs--stream-for-a-property-set.md)

Um beispielsweise einen einfachen ANSI-Eigenschaftensatz zu erstellen, würden Sie [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) aufrufen, um den Eigenschaftensatz zu erstellen. Geben Sie **PROPSETFLAG \_ ANSI** an (einfach ist der Standardtyp des Eigenschaftensatzes), und schreiben Sie dann mit einem Aufruf von [**IPropertyStorage::WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple)in diesen. Um den Eigenschaftensatz zu lesen, würden Sie [**IPropertyStorage::ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple)aufrufen.

Alle freigegebenen Eigenschaftensätze werden durch einen Stream- oder Speichernamen mit dem Präfix \\ "005" (oder 0x05) identifiziert, um anzuzeigen, dass es sich um einen Eigenschaftensatz handelt, der von Anwendungen gemeinsam genutzt werden kann. Der Eigenschaftensatz Zusammenfassungsinformationen ist keine Ausnahme. Der Name des Streams, der den Eigenschaftensatz Zusammenfassungsinformationen enthält, lautet **: " \\ 005SummaryInformation"**

Es ist nicht erforderlich, den Streamnamen des Eigenschaftensatzes zu kennen, wenn Sie über die [**Create-**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) oder [**Open-Methoden**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) der [**IPropertySetStorage-Schnittstelle**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) darauf zugreifen. In diesem Fall muss nur der Formatbezeichner (FMTID) bekannt sein. Die FMTID für den Eigenschaftensatz Zusammenfassungsinformationen lautet: **F29F85E0-4FF9-1068-AB91-08002B27B3D9**

Die Deklaration für diesen Wert ist in der Headerdatei als **FMTID \_ SummaryInformation** verfügbar. Weitere Informationen finden Sie unter FMTIDS in den [vordefinierten Formatbezeichnern für Eigenschaftensatz.](predefined-property-set-format-identifiers.md)

In der folgenden Tabelle sind die Zeichenfolgeneigenschaftennamen für den Eigenschaftensatz Zusammenfassungsinformationen zusammen mit den entsprechenden Eigenschaftenbezeichnern und Variablentypindikatoren (VT) aufgeführt. Die Namen werden in der Regel nicht im Eigenschaftensatz gespeichert, sondern aus dem Eigenschafts-ID-Wert abgeleitet. Die hier gezeigten Einträge der Eigenschaften-ID-Zeichenfolge entsprechen Definitionen in den Headerdateien.

| Name | Eigenschaften-ID-Zeichenfolge | Eigenschafts-ID | VT-Typ |
|------|--------------------|-------------|---------|
| Titel | PIDSI \_ TITLE | 0x00000002 | VT \_ LPSTR  |
| Gegenstand | PIDSI \_ SUBJECT | 0x00000003 | VT \_ LPSTR |
| Autor | PIDSI \_ AUTHOR | 0x00000004 | VT \_ LPSTR |
| Keywords | PIDSI \_ KEYWORDS | 0x00000005 | VT \_ LPSTR |
| Kommentare | PIDSI \_ COMMENTS | 0x00000006 | VT \_ LPSTR |
| Vorlage | \_PIDSI-VORLAGE | 0x00000007 | VT \_ LPSTR |
| Zuletzt gespeichert von | PIDSI \_ LASTAUTHOR | 0x00000008 | VT \_ LPSTR |
| Revision Number | PIDSI \_ REVNUMBER | 0x00000009 | VT \_ LPSTR |
| Gesamtbearbeitungszeit | PIDSI \_ EDITTIME | 0x0000000A | VT \_ FILETIME (UTC) |
| Zuletzt gedruckt | PIDSI \_ LASTPRINTED | 0x0000000B | VT \_ FILETIME (UTC) |
| Erstellungszeit/-datum (siehe Hinweis unten) | PIDSI \_ CREATE \_ PIC | 0x0000000C | VT \_ FILETIME (UTC) |
| Zeitpunkt/Datum des letzten Gespeicherten (siehe Hinweis unten) | PIDSI \_ LASTSAVE \_ PIC | 0x0000000D | VT \_ FILETIME (UTC) |
| Anzahl der Seiten | PIDSI \_ PAGECOUNT | 0x0000000E | VT \_ I4 |
| Anzahl von Wörtern | PIDSI \_ WORDCOUNT | 0x0000000F | VT \_ I4 |
| Anzahl von Zeichen | PIDSI \_ CHARCOUNT | 0x00000010 | VT \_ I4 |
| Miniaturansicht | PIDSI \_ THUMBNAIL | 0x00000011 | VT \_ CF |
| Name der Anwendung wird erstellt. | PIDSI \_ APPNAME | 0x00000012 | VT \_ LPSTR |
| Sicherheit | PIDSI \_ SECURITY | 0x00000013 | VT \_ I4 |

> [!NOTE]
> Für **"Create Time/Date"** und **"Last saved Time/Date"**(Uhrzeit/Datum des letzten Speicherns) verwalten einige Methoden der Dateiübertragung, z. B. ein Download von einem BBS, die Dateisystemversion dieser Informationen nicht ordnungsgemäß.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Implementieren des Eigenschaftensatzes für Zusammenfassungsinformationen](implementing-the-summary-information-property-set.md)
</dt> </dl>

 

 




