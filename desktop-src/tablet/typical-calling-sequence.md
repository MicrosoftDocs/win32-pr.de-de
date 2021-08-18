---
description: 'Die Methoden, die Sie implementieren müssen, um eine Ink-Recognizer-Funktion zu erstellen, werden von den Tablet PC-Plattform-APIs und nicht direkt von einer Ink-fähigen Anwendung aufgerufen. Die folgenden Schritte stellen eine typische Aufrufsequenz für die Implementierung dieser Methoden dar: Die DLL wird geladen. Ein&\# 160; Das HRECOGNIZER-Handle wird erstellt. Ein&\# 160; Das HRECOCONTEXT-Handle wird erstellt. Für diesen Kontext werden Optionen und Modi für die Wiedererkennung festgelegt. Den Ink-Daten werden Striche hinzugefügt. Die Eingabe wurde beendet. Die Ink-Datei wird erkannt. Die Erkennungsergebnisse werden zurückgegeben. Das HRECOCONTEXT-Handle wird zerstört. Das HRECOGNIZER-Handle wird zerstört. Die aufrufende Sequenz wird auch in der folgenden Codegliederung veranschaulicht: C++CreateRecognizer(CLSID, &hrec); while (weitere Teile von Ink, um ... zu erkennen) { { / Erstellen Sie einen Kontext, sobald pro Teil der Ink-Funktion erkannt werden soll hrc = CreateContext(hrec, &hrc); / Funktionen zum Einrichten von Optionen und Modi für diesen Kontext SetGuide(hrc, pGuide, 0); SetFactoid(hrc, 5, PHONE); nur, wenn in der Anwendung mit Formularen SetFlags(hrc, RECOFLAG WORDMODE); selten, nur wenn der Wortmodus, kein Out-of-Dictionary oder eine einzelne Segmentierung SetWordList(hrc, hwl) verwendet werden soll; / Alle Striche in diesem Teil der Ink-Datei hinzufügen, während (mehr Striche \_ ... ) { AddStroke(hrc, NULL, 800, pPacket, pXForm); { ein Aufruf pro Strich } EndInkInput(hrc); Dadurch wird der als Ink erkannte Prozess (hrc) erkannt. Wenn es sich um eine einfache Anwendung handelt, wird dies für eine einfache Antwort GetBestResultString(hrc, length, buffer) aufgerufen. Wenn es sich um eine komplexe Anwendung handelt, wird dies für eine vollständige Antwort GetLatticePtr(hrc, &pLattice) bezeichnet. Destroy the context DestroyContext(hrc); } { Wird aufgerufen, kurz bevor die Anwendung DestroyRecognizer(hrec) heruntergefahren hat;'
ms.assetid: 484ba140-788f-4b71-9cc7-9baa919d9936
title: Typische Aufrufsequenz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94506d320d2ac0dca31fcc44714d0fd9ed089a2dda479020d860b0fbe5bfae5a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119708220"
---
# <a name="typical-calling-sequence"></a>Typische Aufrufsequenz

Die Methoden, die Sie implementieren müssen, um eine Ink-Recognizer-Funktion zu erstellen, werden von den Tablet PC-Plattform-APIs und nicht direkt von einer Ink-fähigen Anwendung aufgerufen.

Die folgenden Schritte stellen eine typische Aufrufsequenz für die Implementierung dieser Methoden dar:

1.  Die DLL wird geladen.
2.  Ein [HRECOGNIZER-Handle](hrecognizer-handle.md) wird erstellt.
3.  Ein [HRECOCONTEXT-Handle](hrecocontext-handle.md) wird erstellt.
4.  Für diesen Kontext werden Optionen und Modi für die Wiedererkennung festgelegt.
5.  Den Ink-Daten werden Striche hinzugefügt.
6.  Die Eingabe wurde beendet.
7.  Die Ink-Datei wird erkannt.
8.  Die Erkennungsergebnisse werden zurückgegeben.
9.  Das [HRECOCONTEXT-Handle](hrecocontext-handle.md) wird zerstört.
10. Das [HRECOGNIZER-Handle](hrecognizer-handle.md) wird zerstört.

Die aufrufende Sequenz wird auch in der folgenden Codegliederung veranschaulicht:


```C++
CreateRecognizer(CLSID, &hrec);
while (more pieces of ink to recognize ... )
{
  // Create a context, once per piece of ink to be recognized
  hrc = CreateContext(hrec, &hrc);

  // Functions to set up options and modes for this context
  SetGuide(hrc, pGuide, 0);
  SetFactoid(hrc, 5, PHONE); // only if in application with forms
  SetFlags(hrc, RECOFLAG_WORDMODE); // rare, only if wanting word mode, no out-of-dictionary, or single segmentation
  SetWordList(hrc, hwl);

  // Adding all the strokes in this piece of ink
  while (more strokes ... )
  {
    AddStroke(hrc, NULL, 800, pPacket, pXForm);  // one call per stroke
  }
  EndInkInput(hrc);

  // This gets the ink recognized
  Process(hrc);

  // If this is a simple application, it calls this for a simple answer
  GetBestResultString(hrc, length, buffer);

  // If this is a complex application, it calls this for a complete answer
  GetLatticePtr(hrc, &pLattice);

  // Destroy the context
  DestroyContext(hrc);
}
// Called just before the application shuts down
DestroyRecognizer(hrec);
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Recognizer-APIs](recognizer-apis.md)
</dt> <dt>

[Architektur der Erkennungs-API](recognition-api-architecture.md)
</dt> </dl>

 

 



