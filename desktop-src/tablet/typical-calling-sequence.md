---
description: 'Die Methoden, die Sie implementieren müssen, um eine frei Handerkennung zu erstellen, werden von den Tablet PC Platform-APIs und nicht direkt von einer frei Hand fähigen Anwendung aufgerufen. Die folgenden Schritte stellen eine typische Aufruf Sequenz für die Implementierung dieser Methoden dar: die dll wird geladen. Ein&\# 160; Das herkenzer-Handle wird erstellt. Ein&\# 160; Das hrecocontext-Handle wird erstellt. Erkennungs Optionen und-Modi werden für diesen Kontext festgelegt. Zu den frei Hand Daten werden Striche hinzugefügt. Die Eingabe wurde beendet. Die frei Hand Eingaben werden erkannt. Die Erkennungsergebnisse werden zurückgegeben. Das hrecocontext-Handle wird zerstört. Das herkenzer-Handle wird zerstört. Die Aufruf Sequenz wird auch in der folgenden Code Gliederung veranschaulicht: C + + createrecognizer (CLSID, &hrec); während (mehr frei Hand Eingaben erkannt werden...) {//Create a context, Once per Ink, um zu erkennen, dass HRC = kreatecontext (hrec, &HRC);//Funktionen zum Einrichten von Optionen und Modi für diesen Kontext setguide (HRC, pguide, 0); Setfaktoid (HRC, 5, Phone); nur, wenn in der Anwendung mit den Formularen setFlags (HRC, recoflag \_ wordmode),//selten, nur bei Verwendung des Word-Modus, nicht außerhalb des Wörterbuchs oder einzelner Segmentierung setwordlist (HRC, HWL);//Hinzufügen aller Striche in dieser frei Hand Eingabe, während (weitere Striche...) {AddStroke (HRC, NULL, 800, ppacket, pxform);//ein einziger Rückruf pro Strich} Umdinkinput (HRC); Hierdurch wird der frei Hand erkannte Prozess (HRC) abgerufen. Handelt es sich hierbei um eine einfache Anwendung, wird diese für eine einfache Antwort GetBestResultString (HRC, length, Buffer) aufgerufen. Handelt es sich hierbei um eine komplexe Anwendung, wird diese für eine komplette Antwort getlatticeptr (HRC, &plattice) aufgerufen. Zerstören Sie den Kontext destroycontext (HRC); }//Wird aufgerufen, kurz bevor die Anwendung destroyerkenzer (hrec) herunterfährt.'
ms.assetid: 484ba140-788f-4b71-9cc7-9baa919d9936
title: Typische Aufruf Sequenz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 832ea396c1d73748c4636d2cad5e17529b8d54df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347648"
---
# <a name="typical-calling-sequence"></a>Typische Aufruf Sequenz

Die Methoden, die Sie implementieren müssen, um eine frei Handerkennung zu erstellen, werden von den Tablet PC Platform-APIs und nicht direkt von einer frei Hand fähigen Anwendung aufgerufen.

Die folgenden Schritte stellen eine typische Aufruf Sequenz für die Implementierung dieser Methoden dar:

1.  Die dll wird geladen.
2.  Es wird ein [herkenzer](hrecognizer-handle.md) -Handle erstellt.
3.  Es wird ein [hrecocontext](hrecocontext-handle.md) -Handle erstellt.
4.  Erkennungs Optionen und-Modi werden für diesen Kontext festgelegt.
5.  Zu den frei Hand Daten werden Striche hinzugefügt.
6.  Die Eingabe wurde beendet.
7.  Die frei Hand Eingaben werden erkannt.
8.  Die Erkennungsergebnisse werden zurückgegeben.
9.  Das [hrecocontext](hrecocontext-handle.md) -Handle wird zerstört.
10. Das [herkenzer](hrecognizer-handle.md) -Handle wird zerstört.

Die Aufruf Sequenz wird auch in der folgenden Code Gliederung veranschaulicht:


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

[Erkennungs-APIs](recognizer-apis.md)
</dt> <dt>

[Erkennungs-API-Architektur](recognition-api-architecture.md)
</dt> </dl>

 

 



