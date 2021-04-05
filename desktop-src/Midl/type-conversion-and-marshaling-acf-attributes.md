---
title: Type-Conversion und Marshalling von ACF-Attributen
description: Verwenden Sie diese Attribute, um zu steuern, wie Ihre Daten über das Netzwerk übertragen werden.
ms.assetid: 6af635f6-eeee-4fa6-85db-5d60434a1235
keywords:
- ACF-Mittell, Attribute, Typkonvertierung und Marshalling
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14367be3df97cc1185fca64e46aafe1d342f3526
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947963"
---
# <a name="type-conversion-and-marshaling-acf-attributes"></a><span data-ttu-id="7fa78-104">Type-Conversion und Marshalling von ACF-Attributen</span><span class="sxs-lookup"><span data-stu-id="7fa78-104">Type-Conversion and Marshaling ACF Attributes</span></span>

<span data-ttu-id="7fa78-105">Verwenden Sie diese Attribute, um zu steuern, wie Ihre Daten über das Netzwerk übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="7fa78-105">Use these attributes to control how your data is transmitted over the network.</span></span>



| <span data-ttu-id="7fa78-106">Attribut</span><span class="sxs-lookup"><span data-stu-id="7fa78-106">Attribute</span></span>                                        | <span data-ttu-id="7fa78-107">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="7fa78-107">Usage</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fa78-108">[](encode.md)[**decodieren**](decode.md)</span><span class="sxs-lookup"><span data-stu-id="7fa78-108">[**encode**](encode.md)[**decode**](decode.md)</span></span> | <span data-ttu-id="7fa78-109">Weist die Mittell an, die Routinen für den Typ oder die Prozedur-Serialisierung (Pickup) verfügbar zu machen, die für die stubräume generiert werden</span><span class="sxs-lookup"><span data-stu-id="7fa78-109">Instructs MIDL to expose the type or procedure serialization (pickling) routines it generates for the stubs.</span></span> <span data-ttu-id="7fa78-110">Die Client Anwendung kann diese Routinen aufrufen, um Daten nach Wert zu Mars Hallen.</span><span class="sxs-lookup"><span data-stu-id="7fa78-110">Your client application can call those routines to marshal data by value.</span></span>                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="7fa78-111">**Darstellung \_ als**</span><span class="sxs-lookup"><span data-stu-id="7fa78-111">**represent\_as**</span></span>](represent-as.md)            | <span data-ttu-id="7fa78-112">Gibt an, wie ein Datentyp bei der Übertragung dargestellt wird, wenn die genaue Natur eines Client Datentyps für den Server unerheblich ist (weil er nur die Daten selbst und nicht die tatsächliche Struktur benötigt), oder wenn der tatsächliche Clienttyp zur Kompilierzeit nicht der Mitte unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="7fa78-112">Specifies how a data type will be represented on the wire, when the exact nature of a client's data type is unimportant to the server (because it only needs the data itself and not the actual structure), or the actual client type is unknown to MIDL at compile time.</span></span> <span data-ttu-id="7fa78-113">Wenn Ihre Client Anwendung z. b. eine verknüpfte Liste von Gleit Komma Zahlen verwendet, können Sie angeben, dass die Wire-Darstellung dieser Liste ein Array vom Typ " [**float**](float.md)" sein soll.</span><span class="sxs-lookup"><span data-stu-id="7fa78-113">For example, if your client application uses a linked list of floating-point numbers, you could specify that the wire-representation of that list be an array of type [**float**](float.md).</span></span> |
| [<span data-ttu-id="7fa78-114">**Benutzer \_ Mars Hall**</span><span class="sxs-lookup"><span data-stu-id="7fa78-114">**user\_marshal**</span></span>](user-marshal.md)            | <span data-ttu-id="7fa78-115">Steuert, wie Daten über das Netzwerk übertragen werden, indem ihre eigenen Marshallingroutinen implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="7fa78-115">Controls how data is transmitted over the wire by implementing your own marshaling routines.</span></span> <span data-ttu-id="7fa78-116">Dieses Attribut ist nützlich, wenn Sie einen Datentyp haben, der in der mittleren l unbekannt ist, oder wenn Sie Informationen zwischen Big-Endian-und Little-Endian-Plattformen übergeben.</span><span class="sxs-lookup"><span data-stu-id="7fa78-116">This attribute is useful if you have a data type that is unknown to MIDL or if you are passing information between big-endian and little-endian platforms.</span></span>                                                                                                                                                                                                                 |



 

<span data-ttu-id="7fa78-117">Das DCE-Marshalling von Attributen [**in \_ Zeile**](in-line.md) und [**außerhalb \_ der \_ Zeile**](out-of-line.md) ist nicht in Microsoft RPC implementiert.</span><span class="sxs-lookup"><span data-stu-id="7fa78-117">The DCE marshaling attributes [**in\_line**](in-line.md) and [**out\_of\_line**](out-of-line.md) are not implemented in Microsoft RPC.</span></span> <span data-ttu-id="7fa78-118">Der mittlerer l-Compiler marshaut komplexe Datentypen automatisch out-of-Line.</span><span class="sxs-lookup"><span data-stu-id="7fa78-118">The MIDL compiler automatically marshals complex data types out-of-line.</span></span>

 

 




