---
description: Es folgen zwei Beispiele für binäre Vorlagen Definitionen und ein Beispiel für ein binäres Datenobjekt.
ms.assetid: vs|directx_sdk|~\examples.htm
title: Beispiele (Direct3D 9-Grafiken)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d26fbb8cbe45881243e17f80fd302c0fb4640685
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124490"
---
# <a name="examples-direct3d-9-graphics"></a><span data-ttu-id="7e311-103">Beispiele (Direct3D 9-Grafiken)</span><span class="sxs-lookup"><span data-stu-id="7e311-103">Examples (Direct3D 9 Graphics)</span></span>

<span data-ttu-id="7e311-104">Es folgen zwei Beispiele für binäre Vorlagen Definitionen und ein Beispiel für ein binäres Datenobjekt.</span><span class="sxs-lookup"><span data-stu-id="7e311-104">Two example binary template definitions and an example of a binary data object follow.</span></span>

> [!Note]  
> <span data-ttu-id="7e311-105">Die Daten werden im Little-Endian-Format gespeichert, das in diesen Beispielen nicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="7e311-105">Data is stored in little-endian format, which is not shown in these examples.</span></span>

 

<span data-ttu-id="7e311-106">Die geschlossene Vorlage RGB wird durch die UUID {55b6d780-37ec-11D0-ab39-0020af71e433} identifiziert und verfügt über die drei Member-r, g und b-jeweils den Typ float.</span><span class="sxs-lookup"><span data-stu-id="7e311-106">The closed template RGB is identified by the UUID {55b6d780-37ec-11d0-ab39-0020af71e433} and has three members - r, g, and b - each of type float.</span></span>


```
TOKEN_TEMPLATE, TOKEN_NAME, 3, 'R', 'G', 'B', TOKEN_OBRACE,
TOKEN_GUID, 55b6d780, 37ec, 11d0, ab, 39, 00, 20, af, 71, e4, 33,
TOKEN_FLOAT, TOKEN_NAME, 1, 'r', TOKEN_SEMICOLON,
TOKEN_FLOAT, TOKEN_NAME, 1, 'g', TOKEN_SEMICOLON,
TOKEN_FLOAT, TOKEN_NAME, 1, 'b', TOKEN_SEMICOLON,
TOKEN_CBRACE
```



<span data-ttu-id="7e311-107">Die geschlossene Vorlage Matrix4x4 wird von der UUID {55b6d781-37ec-11D0-ab39-0020af71e433} identifiziert und verfügt über einen Member, d. h. ein zweidimensionales Array mit dem Namen "Matrix" vom Typ "float".</span><span class="sxs-lookup"><span data-stu-id="7e311-107">The closed template Matrix4x4 is identified by the UUID {55b6d781-37ec-11d0-ab39-0020af71e433} and has one member - a two-dimensional array named matrix - of type float.</span></span>


```
TOKEN_TEMPLATE, TOKEN_NAME, 9, 'M', 'a', 't', 'r', 'i', 'x', '4', 'x', '4', TOKEN_OBRACE,
TOKEN_GUID, 55b6d781, 37ec, 11d0, ab, 39, 00, 20, af, 71, e4, 33,
TOKEN_ARRAY, TOKEN_FLOAT, TOKEN_NAME, 6, 'm', 'a', 't', 'r', 'i', 'x',
TOKEN_OBRACKET, TOKEN_INTEGER, 4, TOKEN_CBRACKET,
TOKEN_OBRACKET, TOKEN_INTEGER, 4, TOKEN_CBRACKET,
TOKEN_CBRACE
```



<span data-ttu-id="7e311-108">Das folgende binäre Datenobjekt zeigt eine Instanz der RGB-Vorlage an, die zuvor definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="7e311-108">The binary data object that follows shows an instance of the RGB template defined earlier.</span></span> <span data-ttu-id="7e311-109">Das Beispiel Objekt hat den Namen Blue und seine drei Member-r, g und b-besitzen die Werte 0,0, 0,0 und 1,0.</span><span class="sxs-lookup"><span data-stu-id="7e311-109">The example object is named blue, and its three members - r, g, and b - have the values 0.0, 0.0, and 1.0, respectively.</span></span>


```
TOKEN_NAME, 3, 'R', 'G', 'B', TOKEN_NAME, 4, 'b', 'l', 'u', 'e', TOKEN_OBRACE,
TOKEN_FLOAT_LIST, 3, 0.0, 0.0, 1.0, TOKEN_CBRACE
```



## <a name="related-topics"></a><span data-ttu-id="7e311-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7e311-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e311-111">Binärcodierung</span><span class="sxs-lookup"><span data-stu-id="7e311-111">Binary Encoding</span></span>](binary-encoding.md)
</dt> </dl>

 

 



