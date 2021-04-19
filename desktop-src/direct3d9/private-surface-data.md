---
description: Sie können beliebige Arten von anwendungsspezifischen Daten mit einer-Oberfläche speichern. Beispielsweise kann eine Oberfläche, die eine Karte in einem Spiel darstellt, Informationen über das Gelände enthalten.
ms.assetid: a66fe0b9-1ccd-4cbd-a3e7-78081047e378
title: Private Oberflächendaten (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66eabd8ce8b5cb93508d3ca8197970fb5d52d96a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106342971"
---
# <a name="private-surface-data-direct3d-9"></a><span data-ttu-id="c5af7-104">Private Oberflächendaten (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="c5af7-104">Private Surface Data (Direct3D 9)</span></span>

<span data-ttu-id="c5af7-105">Sie können beliebige Arten von anwendungsspezifischen Daten mit einer-Oberfläche speichern.</span><span class="sxs-lookup"><span data-stu-id="c5af7-105">You can store any kind of application-specific data with a surface.</span></span> <span data-ttu-id="c5af7-106">Beispielsweise kann eine Oberfläche, die eine Karte in einem Spiel darstellt, Informationen über das Gelände enthalten.</span><span class="sxs-lookup"><span data-stu-id="c5af7-106">For example, a surface representing a map in a game might contain information about terrain.</span></span>

<span data-ttu-id="c5af7-107">Eine Oberfläche kann über mehr als einen privaten Datenpuffer verfügen.</span><span class="sxs-lookup"><span data-stu-id="c5af7-107">A surface can have more than one private data buffer.</span></span> <span data-ttu-id="c5af7-108">Jeder Puffer wird durch eine GUID identifiziert, die Sie angeben, wenn die Daten an die-Oberfläche angefügt werden.</span><span class="sxs-lookup"><span data-stu-id="c5af7-108">Each buffer is identified by a GUID that you supply when attaching the data to the surface.</span></span>

<span data-ttu-id="c5af7-109">Verwenden Sie zum Speichern privater Oberflächendaten setprivatedata, und übergeben Sie einen Zeiger auf den Quell Puffer, die Größe der Daten und eine von der Anwendung definierte GUID für die Daten.</span><span class="sxs-lookup"><span data-stu-id="c5af7-109">To store private surface data, use SetPrivateData, passing a pointer to the source buffer, the size of the data, and an application-defined GUID for the data.</span></span> <span data-ttu-id="c5af7-110">Optional können die Quelldaten in Form eines COM-Objekts vorhanden sein. in diesem Fall übergeben Sie einen Zeiger an den [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstellen Zeiger des Objekts und legen das Flag D3DSPD \_ iunknownpointer fest.</span><span class="sxs-lookup"><span data-stu-id="c5af7-110">Optionally, the source data can exist in the form of a COM object; in this case, you pass a pointer to the object's [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface pointer and you set the D3DSPD\_IUNKNOWNPOINTER flag.</span></span>

<span data-ttu-id="c5af7-111">Setprivatedata ordnet einen internen Puffer für die Daten zu und kopiert ihn.</span><span class="sxs-lookup"><span data-stu-id="c5af7-111">SetPrivateData allocates an internal buffer for the data and copies it.</span></span> <span data-ttu-id="c5af7-112">Anschließend können Sie den Quell Puffer oder das Objekt sicher freigeben.</span><span class="sxs-lookup"><span data-stu-id="c5af7-112">You can then safely free the source buffer or object.</span></span> <span data-ttu-id="c5af7-113">Der interne Puffer-oder Schnittstellen Verweis wird freigegeben, wenn "freprivatedata" aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c5af7-113">The internal buffer or interface reference is released when FreePrivateData is called.</span></span> <span data-ttu-id="c5af7-114">Dies geschieht automatisch, wenn die Oberfläche freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c5af7-114">This happens automatically when the surface is freed.</span></span>

<span data-ttu-id="c5af7-115">Zum Abrufen privater Daten für eine Oberfläche müssen Sie einen Puffer mit der richtigen Größe zuordnen und dann die getprivatedata-Methode aufrufen und dabei die GUID übergeben, die den Daten zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="c5af7-115">To retrieve private data for a surface, you must allocate a buffer of the correct size and then call the GetPrivateData method, passing the GUID that was assigned to the data.</span></span> <span data-ttu-id="c5af7-116">Sie sind dafür verantwortlich, den dynamischen Arbeitsspeicher freizugeben, den Sie für diesen Puffer verwenden.</span><span class="sxs-lookup"><span data-stu-id="c5af7-116">You are responsible for freeing any dynamic memory you use for this buffer.</span></span> <span data-ttu-id="c5af7-117">Wenn es sich bei den Daten um ein COM-Objekt handelt, ruft diese Methode den [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Zeiger ab.</span><span class="sxs-lookup"><span data-stu-id="c5af7-117">If the data is a COM object, this method retrieves the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) pointer.</span></span>

<span data-ttu-id="c5af7-118">Wenn Sie nicht wissen, wie groß ein Puffer ist, müssen Sie zuerst getprivatedata mit 0 (null) in psizeofdata aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c5af7-118">If you don't know how big a buffer to allocate, first call GetPrivateData with zero in pSizeOfData.</span></span> <span data-ttu-id="c5af7-119">Wenn die Methode mit D3DERR \_ MoreData fehlschlägt, wird die erforderliche Anzahl von Bytes für den Puffer zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c5af7-119">If the method fails with D3DERR\_MOREDATA, it returns the necessary number of bytes for the buffer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c5af7-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c5af7-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5af7-121">Direct3D-Oberflächen</span><span class="sxs-lookup"><span data-stu-id="c5af7-121">Direct3D Surfaces</span></span>](direct3d-surfaces.md)
</dt> </dl>

 

 
