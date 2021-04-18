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
# <a name="typical-calling-sequence"></a><span data-ttu-id="3de2b-103">Typische Aufruf Sequenz</span><span class="sxs-lookup"><span data-stu-id="3de2b-103">Typical Calling Sequence</span></span>

<span data-ttu-id="3de2b-104">Die Methoden, die Sie implementieren müssen, um eine frei Handerkennung zu erstellen, werden von den Tablet PC Platform-APIs und nicht direkt von einer frei Hand fähigen Anwendung aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="3de2b-104">The methods you must implement to create an ink recognizer are called by the Tablet PC Platform APIs and not directly by an ink-enabled application.</span></span>

<span data-ttu-id="3de2b-105">Die folgenden Schritte stellen eine typische Aufruf Sequenz für die Implementierung dieser Methoden dar:</span><span class="sxs-lookup"><span data-stu-id="3de2b-105">The following steps represent a typical calling sequence for the implementation of these methods:</span></span>

1.  <span data-ttu-id="3de2b-106">Die dll wird geladen.</span><span class="sxs-lookup"><span data-stu-id="3de2b-106">The DLL is loaded.</span></span>
2.  <span data-ttu-id="3de2b-107">Es wird ein [herkenzer](hrecognizer-handle.md) -Handle erstellt.</span><span class="sxs-lookup"><span data-stu-id="3de2b-107">An [HRECOGNIZER](hrecognizer-handle.md) handle is created.</span></span>
3.  <span data-ttu-id="3de2b-108">Es wird ein [hrecocontext](hrecocontext-handle.md) -Handle erstellt.</span><span class="sxs-lookup"><span data-stu-id="3de2b-108">An [HRECOCONTEXT](hrecocontext-handle.md) handle is created.</span></span>
4.  <span data-ttu-id="3de2b-109">Erkennungs Optionen und-Modi werden für diesen Kontext festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3de2b-109">Recognizer options and modes are set for this context.</span></span>
5.  <span data-ttu-id="3de2b-110">Zu den frei Hand Daten werden Striche hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3de2b-110">Strokes are added to the ink data.</span></span>
6.  <span data-ttu-id="3de2b-111">Die Eingabe wurde beendet.</span><span class="sxs-lookup"><span data-stu-id="3de2b-111">Input is ended.</span></span>
7.  <span data-ttu-id="3de2b-112">Die frei Hand Eingaben werden erkannt.</span><span class="sxs-lookup"><span data-stu-id="3de2b-112">The ink is recognized.</span></span>
8.  <span data-ttu-id="3de2b-113">Die Erkennungsergebnisse werden zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3de2b-113">The recognition results are returned.</span></span>
9.  <span data-ttu-id="3de2b-114">Das [hrecocontext](hrecocontext-handle.md) -Handle wird zerstört.</span><span class="sxs-lookup"><span data-stu-id="3de2b-114">The [HRECOCONTEXT](hrecocontext-handle.md) handle is destroyed.</span></span>
10. <span data-ttu-id="3de2b-115">Das [herkenzer](hrecognizer-handle.md) -Handle wird zerstört.</span><span class="sxs-lookup"><span data-stu-id="3de2b-115">The [HRECOGNIZER](hrecognizer-handle.md) handle is destroyed.</span></span>

<span data-ttu-id="3de2b-116">Die Aufruf Sequenz wird auch in der folgenden Code Gliederung veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="3de2b-116">The calling sequence is also illustrated in the following code outline:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="3de2b-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3de2b-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3de2b-118">Erkennungs-APIs</span><span class="sxs-lookup"><span data-stu-id="3de2b-118">Recognizer APIs</span></span>](recognizer-apis.md)
</dt> <dt>

[<span data-ttu-id="3de2b-119">Erkennungs-API-Architektur</span><span class="sxs-lookup"><span data-stu-id="3de2b-119">Recognition API Architecture</span></span>](recognition-api-architecture.md)
</dt> </dl>

 

 



