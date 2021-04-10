---
title: Isrresgraphex und IAttribute
description: Isrresgraphex und IAttribute
ms.assetid: 6eb37da1-5252-4c41-891c-c19cca6fb7d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 659d7d4723bfc5145fb8abcc77043031a0e48e8b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038818"
---
# <a name="isrresgraphex-and-iattributes"></a>Isrresgraphex und IAttribute

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Die von der Engine zurückgegebenen Ergebnis Objekte müssen die isrresgraphex-Schnittstelle und die IAttribute-Schnittstelle unterstützen. Nur die Unterstützung der isrresgraphex-Schnittstelle ist ausreichend, damit der Sound-Editor Informationen zu Wort Umbruch bereitstellen kann, aber nicht die erforderliche Unterstützung für Phonem-Informationen bietet.

Der Sound-Editor erfordert, dass Engines auch ein spezielles DWORD-Attribut unterstützen, **z. b. srattr \_ Phones.** Der Editor fragt die Engines ab, um die IAttribute-Schnittstelle anzuzeigen, und versucht, den **srattr \_** -Wert auf 1 festzulegen. Wenn der Befehl erfolgreich ausgeführt wird, geht der Sound-Editor davon aus, dass die Ergebnisse der Engine das Sammeln von Phoneme-Segmentierungs Informationen aus dem Ergebnis Objekt unterstützen.

`#define    SRATTR_PHONESEG    MAKELONG (1, SRVEN_MICROSOFT)`

Wenn ein results-Objekt an den Sound-Editor übertragen wird, fragt es das Objekt nach seiner Implementierung von isrresgraphex ab. Isrresgraphex enthält eine Member-Funktion, DataGet, mit Typsignatur.

`HRESULT  DataGet  (DWord, dwID, GUID gAttrib, SDATA *psData)`

Wenn **dwID** der Bezeichner des Graph-Objekts ist, ist **gatpub** eine GUID, die dem gesuchten Attribut entspricht, und **psdata** ist ein Zeiger auf ein sdata-Objekt, das die zurückgegebenen Daten enthält. Die Engine ist für die Zuordnung der in **psdata** gespeicherten Daten über [**cotaskmemzugc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc)zuständig. Die aufrufende Anwendung (in diesem Fall der Sound-Editor) ist dafür zuständig, Sie durch [**CoTaskMemFree frei**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) zugeben, wenn Sie abgeschlossen ist.

DataGet ist erforderlich, um drei vordefinierte GUIDs zu erkennen, die in der SAPI-Dokumentation aufgeführt sind. Ein Modul, das einen Erfolgs Code an den dwordset-Aufruf zurückgibt **(srattr \_ phonesz, 1)** , ist auch erforderlich, um eine bestimmte GUID, **srgarc \_ phonemesegmentation**, zu erkennen, wenn Sie mit einem **dwID** aufgerufen wird, das einem Edge im Diagramm entspricht.

`DEFINE_GUID(SRGARC_PHONMESEGMENTATION, 0xd05405b0, 0x1db1, 0x11d2, 0x94, 0x2, 0x0, 0xc0, 0x4f, 0x8e, 0xf4, 0x8f);`

Wenn der-Rückruf zurückgegeben wird, sollte **psdata** auf ein Array mit einer DWORD-ausgerichteten Struktur vom Typ **phoneseg** verweisen, die durch definiert wird:

``` syntax
typedef struct tagSRPHONESEG {
   DWORD   dwSize;       // Size of the SRPHONESEG structure + phone data
   QWORD   qwStartTime;  // SAPI timestamp of the start of the seqment
   …QWORD   qwEndTime;    // SAPI timestamp of the end of the seqment
   int      nScore;      // The segment's score
   WCHAR   aPhones[0];   // Array of phone(s) making up the segment
} SRPHONESEG,  *PSRPHONESEG;
```

Dabei zeigen **qwstarttime** und **qwendtime** auf den Anfang und das Ende der einzelnen Phonem, die das von Edge abgedeckte Wort bilden, und **aphones** ist ein Array von Unicode-Zeichen, die der IPA-Darstellung des Telefons entsprechen, die in diesem Segment erstellt wurden. (In einigen Sprachen gibt es Phoneme, die mit mehr als einem IPA-Phoneme geschrieben sind. In englischer Sprache ist beispielsweise der Sound "Long I" im Wort "Live" tatsächlich ein Diphthong, der aus zwei einfacheren, verketteten Phoneme besteht.) Das **aphones** -Array sollte NULL enden und am Ende aufgefüllt werden, damit jede **srphonesz** -Struktur im Array ein gleich Vielfaches von vier Bytes lang ist.

Nehmen wir beispielsweise an, dass das Wort, das in Bogen 4 gesprochen wird, "Made" lautet. Dann der DataGet-DataGet-DataGet (4 **srgarc \_ phonemesegmentation**, &SD) gibt möglicherweise ein Array von drei Phonem-Segmenten zurück,/m/wird von **qwstarttime**= 328434 Bytes auf **qwendtime**= 330354 Bytes ausgeführt,/1E/wird von **qwstarttime**= 330354 Bytes auf **qwendtime**= 344114 Bytes ausgeführt, und/d/wird von **qwstarttime**= 344114 Bytes auf **qwendtime**= 347314 Diese werden als gepacktes Array von drei **srphonesz** -Strukturen, z. b. 28, 32 bzw. 28 bytes, dargestellt. Beachten Sie, dass am Ende der "Middle **srphones"** -Struktur ein Auffüll Zeichen steht, sodass das nächste Element im Array an einer 4-Byte-Grenze beginnt.

Das SAPI 4,0 SDK enthält ein Tool (srfunc) zum Testen der Konformität mit der SAPI 4,0-Spezifikation. In diesem Tool ist ein Test für die Konformität mit diesem Satz von Schnittstellen enthalten. Der Quellcode für dieses Tool ist ein guter Ausgangspunkt, um zu verstehen, wie diese Schnittstellen mit dem Sound-Editor interagieren und die Schnittstellen während der Entwicklung Debuggen.

 

 