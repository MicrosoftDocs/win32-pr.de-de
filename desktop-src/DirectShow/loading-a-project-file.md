---
description: Laden einer Projektdatei
ms.assetid: f8d142bd-e51d-4714-893b-8e3d02506891
title: Laden einer Projektdatei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f9a710795a29481740bf85390cc7122cc801a22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213901"
---
# <a name="loading-a-project-file"></a><span data-ttu-id="6a9ec-103">Laden einer Projektdatei</span><span class="sxs-lookup"><span data-stu-id="6a9ec-103">Loading a Project File</span></span>

<span data-ttu-id="6a9ec-104">\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]</span><span class="sxs-lookup"><span data-stu-id="6a9ec-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="6a9ec-105">Zum Laden einer Projektdatei benötigen Sie zwei Komponenten: den XML-Parser und eine leere Zeitachse.</span><span class="sxs-lookup"><span data-stu-id="6a9ec-105">To load a project file, you need two components: the XML parser and an empty timeline.</span></span> <span data-ttu-id="6a9ec-106">Der XML-Parser liest eine XML-Projektdatei und erstellt jedes Objekt, das in der Datei definiert ist.</span><span class="sxs-lookup"><span data-stu-id="6a9ec-106">The XML parser reads an XML project file and creates each object defined in the file.</span></span> <span data-ttu-id="6a9ec-107">Anschließend werden die Objekte in die Zeitachse eingefügt, und es werden alle Zeitachsen Attribute festgelegt, z. b. die Standard Frame Rate</span><span class="sxs-lookup"><span data-stu-id="6a9ec-107">Then it inserts the objects into the timeline and sets any timeline attributes, such as the default frame rate.</span></span> <span data-ttu-id="6a9ec-108">Im folgenden Codebeispiel wird eine Datei geladen.</span><span class="sxs-lookup"><span data-stu-id="6a9ec-108">The following code example loads a file.</span></span>


```C++
HRESULT         hr;
IAMTimeline     *pTL = NULL;
IXml2Dex        *pXML = NULL; 
hr = CoCreateInstance(CLSID_AMTimeline, NULL, CLSCTX_INPROC_SERVER, 
            IID_IAMTimeline, (void**)&pTL);
hr = CoCreateInstance(CLSID_Xml2Dex, NULL, CLSCTX_INPROC_SERVER, 
            IID_IXml2Dex, (void**)&pXML);
BSTR bstrFile = SysAllocStringLen(OLESTR("C:\\example.xtl"), 15);
hr = pXML->ReadXMLFile(pTL, bstrFile); 
SysFreeString(bstrFile);
pXML->Release();
```



<span data-ttu-id="6a9ec-109">Der Parser macht die [**IXml2Dex**](ixml2dex.md) -Schnittstelle verfügbar, die Methoden zum Laden und Speichern von Projektdateien enthält.</span><span class="sxs-lookup"><span data-stu-id="6a9ec-109">The parser exposes the [**IXml2Dex**](ixml2dex.md) interface, which contains methods for loading and saving project files.</span></span> <span data-ttu-id="6a9ec-110">Die Zeitachse macht die [**iamtimeline**](iamtimeline.md) -Schnittstelle verfügbar, die Methoden zum Bearbeiten der Zeitachse und Erstellen neuer Zeitachsen Objekte enthält.</span><span class="sxs-lookup"><span data-stu-id="6a9ec-110">The timeline exposes the [**IAMTimeline**](iamtimeline.md) interface, which contains methods for manipulating the timeline and creating new timeline objects.</span></span> <span data-ttu-id="6a9ec-111">Rufen Sie die **cokreateinstance** -Funktion auf, um jede Komponente zu erstellen, wie hier gezeigt.</span><span class="sxs-lookup"><span data-stu-id="6a9ec-111">Call the **CoCreateInstance** function to create each component, as shown.</span></span> <span data-ttu-id="6a9ec-112">Beachten Sie, dass Sie durch das Erstellen einer neuen-Instanz den Verweis Zähler für die-Schnittstelle inkrementieren.</span><span class="sxs-lookup"><span data-stu-id="6a9ec-112">Remember that by creating a new instance, you are incrementing the reference count on the interface.</span></span> <span data-ttu-id="6a9ec-113">Um Speicher Verluste zu vermeiden, geben Sie immer eine Schnittstelle frei, wenn Sie mit der Datei umgehen.</span><span class="sxs-lookup"><span data-stu-id="6a9ec-113">To avoid memory leaks, always release an interface when you are through with it.</span></span> <span data-ttu-id="6a9ec-114">In diesem Beispiel ist der Zeiger auf **IXml2Dex** nicht mehr erforderlich, sodass Sie die-Schnittstelle freigeben können.</span><span class="sxs-lookup"><span data-stu-id="6a9ec-114">In this example, the pointer to **IXml2Dex** is not needed for anything more, so you can release the interface.</span></span> <span data-ttu-id="6a9ec-115">Der Zeiger auf **iamtimeline** ist nach wie vor für die Vorschau der Zeitachse erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6a9ec-115">The pointer to **IAMTimeline** is still needed for previewing the timeline.</span></span>

<span data-ttu-id="6a9ec-116">Die [**IXml2Dex:: infoxmlfile**](ixml2dex-readxmlfile.md) -Methode liest die angegebene Datei und füllt die Zeitachse mit den in der Datei definierten Objekten auf.</span><span class="sxs-lookup"><span data-stu-id="6a9ec-116">The [**IXml2Dex::ReadXMLFile**](ixml2dex-readxmlfile.md) method reads the specified file and populates the timeline with the objects defined in the file.</span></span> <span data-ttu-id="6a9ec-117">Der Dateiname wird mit einem **BSTR** -Wert angegeben.</span><span class="sxs-lookup"><span data-stu-id="6a9ec-117">The file name is specified using a **BSTR** value.</span></span> <span data-ttu-id="6a9ec-118">Um das Beispiel zu verkürzen, wird der Dateiname im Beispiel als Literalzeichenfolge angegeben.</span><span class="sxs-lookup"><span data-stu-id="6a9ec-118">To shorten the example, the file name in the example is given as a literal string.</span></span> <span data-ttu-id="6a9ec-119">Normalerweise erhalten Sie diese aus einem geöffneten Datei Dialogfeld oder etwas ähnliches.</span><span class="sxs-lookup"><span data-stu-id="6a9ec-119">Normally, you obtain it from an Open File dialog or something similar.</span></span>

<span data-ttu-id="6a9ec-120">Wenn die Read **XML** -Methode erfolgreich ist, wird ein Erfolgs Code zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6a9ec-120">If the **ReadXML** method is successful, it returns a success code.</span></span> <span data-ttu-id="6a9ec-121">Andernfalls wird ein Fehlercode zurückgegeben, z \_ . b. VFW E \_ ungültiges \_ Datei \_ Format.</span><span class="sxs-lookup"><span data-stu-id="6a9ec-121">Otherwise, it returns an error code such as VFW\_E\_INVALID\_FILE\_FORMAT.</span></span> <span data-ttu-id="6a9ec-122">Überprüfen Sie immer den Rückgabewert, um Fehlerbedingungen ordnungsgemäß zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="6a9ec-122">Always check the return value, in order to handle error conditions gracefully.</span></span> <span data-ttu-id="6a9ec-123">Aus Gründen der Übersichtlichkeit wird im Beispielcode nicht auf Fehler überprüft.</span><span class="sxs-lookup"><span data-stu-id="6a9ec-123">Again for brevity, the example code does not check for errors.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6a9ec-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6a9ec-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a9ec-125">Laden und Anzeigen der Vorschau eines Projekts</span><span class="sxs-lookup"><span data-stu-id="6a9ec-125">Loading and Previewing a Project</span></span>](loading-and-previewing-a-project.md)
</dt> </dl>

 

 



