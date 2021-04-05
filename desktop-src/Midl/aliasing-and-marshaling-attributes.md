---
title: Aliasing-und Marshallingattribute
description: Verteilte Anwendungen übergeben fast immer Daten zwischen Client-und Serverprogrammen, wenn Sie Schnittstellen Prozeduren aufzurufen.
ms.assetid: 64895c64-f16b-47c4-928d-5149808b0476
keywords:
- IDL-Mittell, Attribute-Mittell, Aliasing und Marshalling
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ac66aa04210a878c67ee6bcf1a50ff21fa1d1d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037543"
---
# <a name="aliasing-and-marshaling-attributes"></a><span data-ttu-id="661a1-104">Aliasing-und Marshallingattribute</span><span class="sxs-lookup"><span data-stu-id="661a1-104">Aliasing and Marshaling Attributes</span></span>

<span data-ttu-id="661a1-105">Verteilte Anwendungen übergeben fast immer Daten zwischen Client-und Serverprogrammen, wenn Sie Schnittstellen Prozeduren aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="661a1-105">Distributed applications almost always pass data between client and server programs when they call interface procedures.</span></span> <span data-ttu-id="661a1-106">Entwickler verwenden die Mittel l, um die Daten zu beschreiben, die von Client-und Serverprogrammen standardmäßig bestanden werden.</span><span class="sxs-lookup"><span data-stu-id="661a1-106">Developers use MIDL to describe the data that client and server programs pass in a standard way.</span></span> <span data-ttu-id="661a1-107">Der mittlerer l-Compiler erstellt anwendungstub-oder Proxy Programme für den Client und den Server, die die Daten in eine standardisierte Form konvertieren, die über ein Netzwerk gesendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="661a1-107">The MIDL compiler creates application stub, or proxy, programs for the client and the server that convert the data into a standardized form that can be sent over a network.</span></span> <span data-ttu-id="661a1-108">Dieses Format, das Format der Netzwerkdaten Darstellung (Network Data Darstellung, NDR), wird häufig als Wire-Format der Daten bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="661a1-108">This format, the Network Data Representation (NDR) format, is often called the wire format of the data.</span></span> <span data-ttu-id="661a1-109">Die Stubdateien müssen Daten aus ihrem systemeigenen Format im Speicherbereich des Programms in den NDR konvertieren.</span><span class="sxs-lookup"><span data-stu-id="661a1-109">The stubs must convert data from its native format in the program's memory space to NDR.</span></span> <span data-ttu-id="661a1-110">Diese Konvertierung wird als Marshalling der Daten bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="661a1-110">This conversion is termed marshaling the data.</span></span> <span data-ttu-id="661a1-111">Wenn ein Client-oder Serverprogramm Daten empfängt, muss es die Daten von der NDR in das systemeigene Format für dieses Programm konvertieren.</span><span class="sxs-lookup"><span data-stu-id="661a1-111">When a client or server program receives data, it must convert the data from NDR to the native format for that program.</span></span> <span data-ttu-id="661a1-112">Dies wird als "Unmarshalling der Daten" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="661a1-112">This is called unmarshaling the data.</span></span>

<span data-ttu-id="661a1-113">Verwenden Sie Aliasing-und Marshallingattribute, um zu steuern, wie Ihre Daten in das NDR-Format gepackt und über das Netzwerk übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="661a1-113">Use aliasing and marshaling attributes to control how your data is packaged into NDR format and transmitted over the network.</span></span>



| <span data-ttu-id="661a1-114">Attribut</span><span class="sxs-lookup"><span data-stu-id="661a1-114">Attribute</span></span>                             | <span data-ttu-id="661a1-115">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="661a1-115">Usage</span></span>                                                                                                                         |
|---------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="661a1-116">**aufzurufen \_ als**</span><span class="sxs-lookup"><span data-stu-id="661a1-116">**call\_as**</span></span>](call-as.md)           | <span data-ttu-id="661a1-117">Ordnet einem Remote Prozedur aufzurufen eine nicht Remote fähige Funktion zu.</span><span class="sxs-lookup"><span data-stu-id="661a1-117">Maps a nonremotable function to a remote procedure call.</span></span>                                                                      |
| [<span data-ttu-id="661a1-118">**IID \_ ist**</span><span class="sxs-lookup"><span data-stu-id="661a1-118">**iid\_is**</span></span>](iid-is.md)             | <span data-ttu-id="661a1-119">Stellt den Schnittstellen Bezeichner der COM-Schnittstelle bereit, die das-Objekt des Zeigers ist.</span><span class="sxs-lookup"><span data-stu-id="661a1-119">Provides the interface identifier of the COM interface that is the object of the pointer.</span></span>                                     |
| [<span data-ttu-id="661a1-120">**übertragen \_ als**</span><span class="sxs-lookup"><span data-stu-id="661a1-120">**transmit\_as**</span></span>](transmit-as.md)   | <span data-ttu-id="661a1-121">Konvertiert einen Datentyp in einen einfacheren Typ für die Übertragung über ein Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="661a1-121">Converts a data type to a simpler type for transmission over a network.</span></span>                                                       |
| [<span data-ttu-id="661a1-122">**Wire \_ Marshal**</span><span class="sxs-lookup"><span data-stu-id="661a1-122">**wire\_marshal**</span></span>](wire-marshal.md) | <span data-ttu-id="661a1-123">Ähnlich wie bei der über [**Tragung \_ als**](transmit-as.md) , aber implementieren Sie die Routinen, um die Daten zu verkleinern, zu Mars Hallen, zu entsperren und freizugeben.</span><span class="sxs-lookup"><span data-stu-id="661a1-123">Similar to [**transmit\_as**](transmit-as.md) but you implement the routines to size, marshal, unmarshal, and free the data.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="661a1-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="661a1-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="661a1-125">Typkonvertierung und Marshalling von ACF-Attributen</span><span class="sxs-lookup"><span data-stu-id="661a1-125">Type Conversion and Marshaling ACF Attributes</span></span>](type-conversion-and-marshaling-acf-attributes.md)
</dt> </dl>

 

 




