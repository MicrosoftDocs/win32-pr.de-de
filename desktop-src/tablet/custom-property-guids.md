---
description: Die folgenden global eindeutigen Bezeichner (GUIDs) werden von Windows Journal verwendet, um benutzerdefinierte Eigenschaften für Striche oder Zeichnungs Attribute zu identifizieren.
ms.assetid: a7488c26-b61f-47d8-a19b-d630a8c00875
title: GUIDs der benutzerdefinierten Eigenschaft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eb1d9069f2c655f658752a6ae3891910ff68103
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362642"
---
# <a name="custom-property-guids"></a>GUIDs der benutzerdefinierten Eigenschaft

Die folgenden global eindeutigen Bezeichner (GUIDs) werden von Windows Journal verwendet, um benutzerdefinierte Eigenschaften für Striche oder Zeichnungs Attribute zu identifizieren.

## <a name="guid_stroke_timestamp"></a>GUID- \_ Strich \_ Zeitstempel


```C++
GUID_STROKE_TIMESTAMP = {4EA66C4-F33A-461B-B8FE-68070D9C7575}
```



Dies ist eine [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) -Struktur, die die Uhrzeit angibt, zu der der Strich erstellt oder dem Dokument hinzugefügt wurde.


```C++
typedef struct _FILETIME {
    DWORD dwLowDateTime;
    DWORD dwHighDateTime;
} FILETIME, *PFILETIME;
```



## <a name="guid_stroke_timeid"></a>GUID \_ \_ -Strich-TimeID


```C++
GUID_STROKE_TIMEID = {50B6BC8-3B7D-4816-8C61-BC7E905B2132}
```



Dies ist eine **TimeID-** Struktur. Sie ermöglicht die Beibehaltung der Stroke-Reihenfolge über Einfüge-und Löschvorgänge. Ohne die **TimeID-** Struktur ist der Zeitstempel für alle [**IInkStrokeDisp-Schnittstellen**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) Objekte, die in einer [inkstrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung ausgeschnitten und eingefügt werden, identisch.


```C++
typedef struct tagTIMEID {
    FILETIME  tmFiletime;
    ULONG     uiOrder;
} TIMEID;
```



## <a name="guid_highlighter"></a>GUID- \_ highheller

Dies ist ein **boolescher** Wert, bei dem **true**= highheller Ink, **false**= reguläre Freihand ist. Dies wird auf Zeichnungs Attribute angewendet.


```C++
GUID_HIGHLIGHTER = {9B6267B8-3968-4048-AB74-F490406A2DFA}
```



## <a name="guid_ink_style_bold"></a>GUID- \_ Ink- \_ Stil \_ Fett

Dabei handelt es sich um einen **booleschen** Wert, bei dem **true**= Bold Ink, **false**= normal ist. Dies wird auf Zeichnungs Attribute angewendet.


```C++
GUID_INK_STYLE_BOLD = {E02FB5C1-9693-4312-A434-00DE7F3AD493}
```



## <a name="guid_ink_style_italics"></a>GUID-Freihand- \_ \_ \_ stilkursiv

Dabei handelt es sich um einen **booleschen** Wert ( **true**= Italicized Ink, **false**= normal). Dies wird auf Zeichnungs Attribute angewendet.


```C++
GUID_INK_STYLE_ITALICS = {05253B51-49C6-4A04-8993-64DD9ABD842A}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Ijournalreader-Schnittstelle**](ijournalreader.md)
</dt> </dl>

 

 
