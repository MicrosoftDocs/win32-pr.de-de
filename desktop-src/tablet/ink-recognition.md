---
description: Nicht alle Anwendungen erfordern die Verwendung der Erkennung, aber da die meisten Anwendungen mit Text als primärer Datentyp entworfen wurden, ist die Möglichkeit, frei Hand Eingaben in Text umzuwandeln, sehr wertvoll.
ms.assetid: 70d25839-6ddd-40db-8891-92da074d17b0
title: Frei Handerkennung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ca4ec6f897c797d86df96c5d9c2cfd5d80f16c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104568895"
---
# <a name="ink-recognition"></a><span data-ttu-id="22476-103">Frei Handerkennung</span><span class="sxs-lookup"><span data-stu-id="22476-103">Ink Recognition</span></span>

<span data-ttu-id="22476-104">Nicht alle Anwendungen erfordern die Verwendung der Erkennung, aber da die meisten Anwendungen mit Text als primärer Datentyp entworfen wurden, ist die Möglichkeit, frei Hand Eingaben in Text umzuwandeln, sehr wertvoll.</span><span class="sxs-lookup"><span data-stu-id="22476-104">Not all applications require the use of recognition, but because most applications were designed with text as their primary data type, the ability to convert ink into text is very valuable.</span></span> <span data-ttu-id="22476-105">Mithilfe der Erkennungs Features der Tablet PC Platform-API können Sie Informationen zu den verfügbaren Erkennungs Modulen Abfragen, z. b. welche Sprachen Sie erkennen.</span><span class="sxs-lookup"><span data-stu-id="22476-105">You can use the recognition features of the Tablet PC platform API to query for information about the recognition engines that are available, such as what languages they recognize.</span></span> <span data-ttu-id="22476-106">Sie können dann eine [**Striche**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung von einem frei Hand Objekt an eine Erkennungs-Engine senden und ein [**erkentionresult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) [**-Objekt zurück**](inkdisp-class.md) geben lassen.</span><span class="sxs-lookup"><span data-stu-id="22476-106">You can then send a [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection from an [**Ink**](inkdisp-class.md) object to a recognition engine and have it return a [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) object.</span></span>

## <a name="recognizercontext-object"></a><span data-ttu-id="22476-107">Erkenzercontext-Objekt</span><span class="sxs-lookup"><span data-stu-id="22476-107">RecognizerContext Object</span></span>

<span data-ttu-id="22476-108">Ein [**erkenzercontext**](inkrecognizercontext-class.md) -Objekt ist die Instanziierung einer angegebenen Erkennung.</span><span class="sxs-lookup"><span data-stu-id="22476-108">A [**RecognizerContext**](inkrecognizercontext-class.md) object is the instantiation of a given recognizer.</span></span> <span data-ttu-id="22476-109">Das **erkenzercontext** -Objekt ermöglicht es Ihnen, eine angegebene Auflistung von Strichen synchron oder asynchron zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="22476-109">The **RecognizerContext** object enables you to recognize a given collection of strokes synchronously or asynchronously.</span></span> <span data-ttu-id="22476-110">Beim asynchronen erkennen gibt das **erkenzercontext** -Objekt das [**erkentionresult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) -Objekt in einem Ereignis Rückruf an die Anwendung zurück.</span><span class="sxs-lookup"><span data-stu-id="22476-110">When recognizing asynchronously, the **RecognizerContext** object returns the [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) object in an event callback to the application.</span></span>

## <a name="recognizers-and-recognizer-objects"></a><span data-ttu-id="22476-111">Erkenzer und Erkennungs Objekte</span><span class="sxs-lookup"><span data-stu-id="22476-111">Recognizers and Recognizer Objects</span></span>

<span data-ttu-id="22476-112">Auf einem einzelnen Tablet PC ist möglicherweise mindestens ein Erkennungs Modul verfügbar.</span><span class="sxs-lookup"><span data-stu-id="22476-112">A single Tablet PC may have one or more recognizers available.</span></span> <span data-ttu-id="22476-113">Sie können die Auflistung der Erkennungs Modul Abfragen, um zu bestimmen, welche Erkennungsfunktion verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="22476-113">You can query the recognizer's collection to determine which recognizer to use.</span></span> <span data-ttu-id="22476-114">Eine Erkennung stellt spezifische Informationen über ihre Funktionen bereit, z. b. die erkannte Sprache und den Hersteller.</span><span class="sxs-lookup"><span data-stu-id="22476-114">A recognizer provides specific information about its capabilities such as the language it can recognize and the manufacturer.</span></span>

<span data-ttu-id="22476-115">Um zu ermitteln, ob mindestens eine Erkennung installiert ist, instanziieren Sie ein [**inkrecognizercontext**](inkrecognizercontext-class.md) -Objekt, wie in den folgenden C++-und C- \# Codebeispielen gezeigt.</span><span class="sxs-lookup"><span data-stu-id="22476-115">To determine whether at least one recognizer is installed, instantiate an [**InkRecognizerContext**](inkrecognizercontext-class.md) object as shown in the following C++ and C\# code examples.</span></span> <span data-ttu-id="22476-116">Wenn eine Erkennung nicht vorhanden ist, schlägt dieser [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Befehl fehl.</span><span class="sxs-lookup"><span data-stu-id="22476-116">If a recognizer is not present, this call to [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) fails.</span></span>


```C++
CComPtr<IInkRecognizerContext> g_pIInkRecoContext;
hr = CoCreateInstance(CLSID_InkRecognizerContext, 
      NULL, CLSCTX_INPROC_SERVER,
      IID_IInkRecognizerContext, 
(void **) &g_pIInkRecoContext);
if (FAILED(hr)) 
{
      ::MessageBox(NULL, TEXT("No recognizers installed.\nExiting."), 
      gc_szAppName, MB_ICONERROR);
      return -1;
}
```




```CSharp
try
{
  Recognizers recos = new Recognizers();//Check for recognizer.
  Recognizer defReco = recos.GetDefaultRecognizer();
  recoContext = defReco.CreateRecognizerContext();
}
catch
{
  MessageBox.Show("No recognizers installed.");
}
```



## <a name="recognitionresult-and-recognitionalternate-objects"></a><span data-ttu-id="22476-117">Erkennungs Ergebnis und erkenntionalternate-Objekte</span><span class="sxs-lookup"><span data-stu-id="22476-117">RecognitionResult and RecognitionAlternate Objects</span></span>

<span data-ttu-id="22476-118">Die Ergebnisse der Erkennung werden in einem [**erkentionresult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) -Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="22476-118">The results of the recognition are returned in a [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) object.</span></span> <span data-ttu-id="22476-119">Die Ergebnisse enthalten eine beste Ergebnis Zeichenfolge in der [TopString](/previous-versions/ms829602(v=msdn.10)) -Eigenschaft sowie eine Auflistung alternativer Ergebnisse in einer " [**erkenntionalternativen**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates) "-Auflistung.</span><span class="sxs-lookup"><span data-stu-id="22476-119">The results contain a best result string in the [TopString](/previous-versions/ms829602(v=msdn.10)) property, as well as a collection of alternative results in a [**RecognitionAlternates**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates) collection.</span></span> <span data-ttu-id="22476-120">Das **erkentionresult** -Objekt kann mit der ursprünglichen [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung persistent gespeichert werden, aus der es generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="22476-120">The **RecognitionResult** object can be persisted with the original [**Strokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection from which it was generated.</span></span>

## <a name="recognizerguide-structure"></a><span data-ttu-id="22476-121">Erkenn-Guide-Struktur</span><span class="sxs-lookup"><span data-stu-id="22476-121">RecognizerGuide Structure</span></span>

<span data-ttu-id="22476-122">Das Erkennungs Handbuch kann aus Zeilen und Spalten bestehen und ermöglicht der Erkennung einen besseren Kontext, in dem die Erkennung durchgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="22476-122">The recognizer guide can consist of rows and columns, and gives the recognizer a better context in which to perform recognition.</span></span> <span data-ttu-id="22476-123">Sie können z. b. horizontale Linien auf dem Bildschirm eines Benutzers zeichnen, ähnlich wie ein gezeichnetes Papier Stück, das anzeigt, wo die Handschrift auftreten soll (dieser Richtlinientyp würde nur aus Zeilen bestehen und keine Spalten).</span><span class="sxs-lookup"><span data-stu-id="22476-123">For example, you can draw horizontal lines on a user's screen, almost like a ruled piece of paper, that show where handwriting should occur (this type of guide would consist only of rows, and no columns).</span></span> <span data-ttu-id="22476-124">Wenn ein Benutzer anstelle eines beliebigen Speicherplatzes in den Zeilen schreibt, verbessert sich die Erkennungsgenauigkeit.</span><span class="sxs-lookup"><span data-stu-id="22476-124">If a user writes on the lines, instead of some arbitrary space, recognition accuracy improves.</span></span>

<span data-ttu-id="22476-125">Die folgende Abbildung zeigt eine [**Erkennungs Leit Faden**](inkrecognizerguide-class.md) Struktur mit zwei Zeilen für die Eingabe.</span><span class="sxs-lookup"><span data-stu-id="22476-125">The following illustration shows a [**RecognizerGuide**](inkrecognizerguide-class.md) structure with two lines for input.</span></span>

![Abbildung der zweizeiligen Erkennungs Leit Faden](images/9791100b-8279-4dd0-823f-0a38a0308a74.jpg)

<span data-ttu-id="22476-127">Die folgende Abbildung zeigt eine [**Erkennungs Leit Faden**](inkrecognizerguide-class.md) Struktur mit vier Spalten und drei Zeilen.</span><span class="sxs-lookup"><span data-stu-id="22476-127">The following illustration shows a [**RecognizerGuide**](inkrecognizerguide-class.md) structure with four columns and three rows.</span></span>

![Abbildung der drei-bis vier Erkennungs Leit Faden](images/d1bbf2d3-9653-49d7-bf48-c1b26645074c.jpg)

<span data-ttu-id="22476-129">Weitere Informationen zum Verwenden der [**Erkennungs Leit Faden**](inkrecognizerguide-class.md) Struktur finden Sie im Thema zur **Erkennungs** -und Erkennungs Anleitung.</span><span class="sxs-lookup"><span data-stu-id="22476-129">For more information about using the [**RecognizerGuide**](inkrecognizerguide-class.md) structure, see the **RecognizerGuide** reference topic.</span></span>

 

 
