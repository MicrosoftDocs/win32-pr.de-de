---
title: Der ADSI-Attribut Cache
description: Das ADSI-Objektmodell stellt einen Client seitigen Attribut Cache für jedes ADSI-Objekt bereit.
ms.assetid: 0d2b4117-11f2-4b39-8fe5-3b176e4256f4
ms.tgt_platform: multiple
keywords:
- ADSI-Attribut Cache ADSI
- ADSI ADSI, using, zugreifen auf und Bearbeiten von Daten mit ADSI, Attribut Cache
- Attribute ADSI, Attribut Caching
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df3062ed5862f11e9db5dadd83b80ac624218c81
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707374"
---
# <a name="the-adsi-attribute-cache"></a><span data-ttu-id="577da-106">Der ADSI-Attribut Cache</span><span class="sxs-lookup"><span data-stu-id="577da-106">The ADSI Attribute Cache</span></span>

<span data-ttu-id="577da-107">Das ADSI-Objektmodell stellt einen Client seitigen Attribut Cache für jedes ADSI-Objekt bereit.</span><span class="sxs-lookup"><span data-stu-id="577da-107">The ADSI object model provides a client-side attribute cache for each ADSI object.</span></span> <span data-ttu-id="577da-108">Der Attribut Cache ist mit einer Tabelle im Arbeitsspeicher vergleichbar, die die Namen und Werte der meisten Objekt Attribute enthält, die heruntergeladen wurden.</span><span class="sxs-lookup"><span data-stu-id="577da-108">The attribute cache is comparable to a table in memory that contains the names and values of most object attributes that have been downloaded.</span></span> <span data-ttu-id="577da-109">Einige Attribute, z. b. operative Attribute, werden nicht zwischengespeichert.</span><span class="sxs-lookup"><span data-stu-id="577da-109">Some attributes, such as operational attributes, are not cached.</span></span> <span data-ttu-id="577da-110">ADSI verwendet das Zwischenspeichern von Eigenschaften, um die Leistung der Attribut Manipulation zu verbessern und die Transaktions Funktion für Lese-und Schreibvorgänge von Attributen hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="577da-110">ADSI uses property caching to enhance the performance of attribute manipulation and add transactioning capability for attribute read and write operations.</span></span> <span data-ttu-id="577da-111">Diese Funktion ist wichtig für Clients, die in Sprachen geschrieben wurden, die keinen systemeigenen Batch Verarbeitungs Mechanismus zum Festlegen von Attributen haben, wie z. b. Microsoft Visual Basic Development System.</span><span class="sxs-lookup"><span data-stu-id="577da-111">This capability is critical for clients written in languages that have no native batching mechanism for setting attributes, such as Microsoft Visual Basic development system.</span></span> <span data-ttu-id="577da-112">Ohne den ADSI-Eigenschafts Cache müssten diese Clients immer dann auf den Server zugreifen, wenn ein Attribut gelesen oder geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="577da-112">Without the ADSI property cache, such clients would have to access the server every time an attribute is read or written.</span></span>

<span data-ttu-id="577da-113">Wenn ein Objekt erstellt oder zuerst an gebunden wird, ist der Eigenschafts Cache für das-Objekt leer.</span><span class="sxs-lookup"><span data-stu-id="577da-113">When an object is created or first bound to, the property cache for the object is empty.</span></span> <span data-ttu-id="577da-114">Wenn die [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) -Methode aufgerufen wird, lädt ADSI die angeforderten Attribute für das Objekt aus dem zugrunde liegenden Verzeichnisdienst in den lokalen Cache.</span><span class="sxs-lookup"><span data-stu-id="577da-114">When the [**IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) method is called, ADSI loads the requested attributes for the object from the underlying directory service into the local cache.</span></span> <span data-ttu-id="577da-115">Wenn ein bestimmter Attribut Wert gelesen wird und der Cache leer ist, führt ADSI einen impliziten Rückruf der **IADs:: GetInfo** -Methode aus.</span><span class="sxs-lookup"><span data-stu-id="577da-115">When a specific attribute value is read and the cache is empty, ADSI makes an implicit call to the **IADs::GetInfo** method.</span></span> <span data-ttu-id="577da-116">Wenn der Cache ausgefüllt ist, funktionieren alle Attribut Lesevorgänge nur für den Inhalt des Caches.</span><span class="sxs-lookup"><span data-stu-id="577da-116">When the cache is filled, all attribute read operations work on the contents of the cache only.</span></span>

<span data-ttu-id="577da-117">Wenn ein Attribut Wert geschrieben wird, wird der neue Wert im lokalen Cache gespeichert, bis die [**IADs::**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) \*-Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="577da-117">When an attribute value is written, the new value is stored in the local cache until the [**IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method is called.</span></span> <span data-ttu-id="577da-118">Wenn die **IADs::** \*-Methode aufgerufen wird, werden die Attribute im Cache an den zugrunde liegenden Verzeichnisdienst übertragen.</span><span class="sxs-lookup"><span data-stu-id="577da-118">When the **IADs::SetInfo** method is called, the attributes in the cache are committed to the underlying directory service.</span></span> <span data-ttu-id="577da-119">Nachdem die **IADs::** \*-Methode aufgerufen wurde, verbleiben die Werte im Cache, bis Sie explizit mit einem weiteren Aufruf der [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) -Methode aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="577da-119">After the **IADs::SetInfo** method is called, the values remain in the cache until explicitly refreshed with another call to the [**IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) method.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="577da-120">Die [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) -Methode muss sorgfältig verwendet werden, da diese Methode immer die Attributwerte im Cache vom zugrunde liegenden Verzeichnisdienst überschreibt, auch wenn der zwischengespeicherte Wert geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="577da-120">The [**IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) method must be used carefully because this method will always overwrite the attribute values in the cache from the underlying directory service, even if the cached value has been changed.</span></span> <span data-ttu-id="577da-121">Das heißt, es werden Attributwerte überschrieben, die im Cache geändert wurden, aber nicht mit einem Commit der [**IADs::**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) \*-Methode in den zugrunde liegenden Verzeichnisdienst committet wurden.</span><span class="sxs-lookup"><span data-stu-id="577da-121">That is, it will overwrite attribute values that have been changed in the cache, but not committed to the underlying directory service with a call to the [**IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method.</span></span>

 

<span data-ttu-id="577da-122">Die folgende Abbildung zeigt die verschiedenen Methoden, die für den Cache verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="577da-122">The following figure shows the different methods used to operate on the cache.</span></span>

![ADSI-Attribut Cache](images/ds2propc.png)

 

 




