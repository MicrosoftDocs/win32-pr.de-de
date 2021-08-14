---
title: ISRResGraphEx und IAttributes
description: ISRResGraphEx und IAttributes
ms.assetid: 6eb37da1-5252-4c41-891c-c19cca6fb7d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81f5e08b77b917e4630afcaeb8baed5aac4e13c20a1ed289418681abbbdca20b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118748996"
---
# <a name="isrresgraphex-and-iattributes"></a>ISRResGraphEx und IAttributes

\[Microsoft Agent ist ab Version Windows 7 veraltet und möglicherweise in nachfolgenden Versionen von Windows.\]

Die von der Engine zurückgegebenen Ergebnisobjekte müssen die ISRResGraphEx-Schnittstelle und die IAttributes-Schnittstelle unterstützen. Die reine Unterstützung der ISRResGraphEx-Schnittstelle reicht aus, um dem Sound-Editor die Bereitstellung von Informationen zur Wörterpause zu ermöglichen, bietet jedoch nicht die erforderliche Unterstützung für Phoneminformationen.

Der Sound-Editor erfordert, dass Engines auch das spezielle DWord-Attribut **SRATTR \_ PHONESEG unterstützen.** Der Editor fragt die Engines ab, um die IAttributes-Schnittstelle zu sehen, und versucht, **SRATTR \_ PHONESEG** auf 1 zu setzen. Wenn dieser Aufruf erfolgreich ist, geht der Sound-Editor davon aus, dass die Ergebnisse der Engine das Sammeln von Phonemsegmentierungsinformationen aus dem Ergebnisobjekt unterstützen.

`#define    SRATTR_PHONESEG    MAKELONG (1, SRVEN_MICROSOFT)`

Wenn ein Ergebnisobjekt an den Sound-Editor übertragen wird, fragt es dieses Objekt nach seiner Implementierung von ISRResGraphEx ab. ISRResGraphEx enthält die Memberfunktion DataGet mit Typsignatur.

`HRESULT  DataGet  (DWord, dwID, GUID gAttrib, SDATA *psData)`

Dabei **ist dwID** der Bezeichner des Graphobjekts, **gAttrib** eine GUID, die dem gesuchten Attribut entspricht, und **psData** ist ein Zeiger auf ein SDATA-Objekt, das die zurückgegebenen Daten enthält. Die Engine ist für die Zuordnung der in **psData gespeicherten** Daten über [**CoTaskMemAlloc verantwortlich.**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc) Die aufrufende Anwendung (in diesem Fall der Sound-Editor) ist dafür verantwortlich, sie über [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) frei zu geben, wenn sie abgeschlossen ist.

DataGet ist erforderlich, um drei vordefinierte GUIDs zu erkennen, die in der SAPI-Dokumentation aufgeführt sind. Eine Engine, die einen Erfolgscode an den Aufruf von **DWORDSet(SRATTR \_ PHONESEG, 1) zurückgibt,** ist auch erforderlich, um eine bestimmte GUID, **SRGARC \_ PHONEMESEGMENTATION,** zu erkennen, wenn sie mit einer **dwID** aufgerufen wird, die einem Rand im Diagramm entspricht.

`DEFINE_GUID(SRGARC_PHONMESEGMENTATION, 0xd05405b0, 0x1db1, 0x11d2, 0x94, 0x2, 0x0, 0xc0, 0x4f, 0x8e, 0xf4, 0x8f);`

Wenn der Aufruf zurückgegeben wird, **sollte psData** auf ein Array von DWORD-ausgerichteter Struktur vom Typ **PHONESEG** verweisen, definiert durch:

``` syntax
typedef struct tagSRPHONESEG {
   DWORD   dwSize;       // Size of the SRPHONESEG structure + phone data
   QWORD   qwStartTime;  // SAPI timestamp of the start of the seqment
   …QWORD   qwEndTime;    // SAPI timestamp of the end of the seqment
   int      nScore;      // The segment's score
   WCHAR   aPhones[0];   // Array of phone(s) making up the segment
} SRPHONESEG,  *PSRPHONESEG;
```

Dabei **zeigen qwStartTime** und **qwEndTime** auf den Anfang und das Ende jedes Phonems, aus dem das vom Edge abgedeckte Wort besteht, und **aPhones** ein Array von Unicode-Zeichen, das der IPA-Darstellung des Telefons entspricht, die in diesem Segment erzeugt wurden. (In einigen Sprachen gibt es Phoneme, die mit mehr als einem IPA-Phonem geschrieben sind. Im Englischen ist der "lange I"-Sound im Wort "live" tatsächlich ein Diphthong, der aus zwei einfacheren, miteinander verketteten Phonemen besteht.) Das **aPhones-Array** sollte 0 (null) enden und am Ende aufschlossen sein, damit jede **SRPHONESEG-Struktur** im Array ein gleichmäßiges Vielfaches von vier Bytes lang wird.

Angenommen, das auf Arc 4 gesprochene Wort wurde "made" (gemacht). Anschließend gibt der Aufruf von DataGet(4, **SRGARC \_ PHONEMESEGMENTATION**, &sd) möglicherweise ein Array von drei Phonemsegmenten zurück. /m/running from **qwStartTime**=328434 bytes to **qwEndTime**=330354 bytes, /1e/ running from **qwStartTime**=330354 bytes to **qwEndTime**=344114 bytes, and /d/ running from **qwStartTime**=344114 bytes to **qwEndTime**=347314 bytes. Diese werden als gepacktes Array mit drei **SRPHONESEG-Strukturen** der Größen 28, 32 bzw. 28 Bytes dargestellt. Beachten Sie, dass am Ende der mittleren **SRPHONESEG-Struktur** eine Auf padding-Struktur angezeigt wird, sodass das nächste Element im Array an einer 4-Byte-Grenze beginnt.

Das SAPI 4.0 SDK enthält ein Tool (SRFunc) zum Testen der Konformität mit der SAPI 4.0-Spezifikation. In diesem Tool ist ein Test auf Konformität mit diesem Satz von Schnittstellen enthalten. Der Quellcode für dieses Tool ist ein guter Einstieg, um zu verstehen, wie diese Schnittstellen mit dem Sound-Editor interagieren und die Schnittstellen während der Entwicklung debuggen.

 

 