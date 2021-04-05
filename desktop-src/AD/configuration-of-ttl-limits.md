---
title: Konfiguration von TTL-Limits
description: Ein Client kann einen TTL-Wert für einen Eintrag im Bereich von 1 bis 31557600 (d. h. von 1 Sekunde bis 1 Jahr) anfordern.
ms.assetid: 4009702c-7992-4e20-9d37-384f8137ba8f
ms.tgt_platform: multiple
keywords:
- Konfiguration der TTL-Grenzwerte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2cb3617bd59667f0284c4e383da54752adfbe25
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707194"
---
# <a name="configuration-of-ttl-limits"></a><span data-ttu-id="0cd5c-104">Konfiguration von TTL-Limits</span><span class="sxs-lookup"><span data-stu-id="0cd5c-104">Configuration of TTL Limits</span></span>

<span data-ttu-id="0cd5c-105">Ein Client kann einen TTL-Wert für einen Eintrag im Bereich von 1 bis 31557600 (d. h. von 1 Sekunde bis 1 Jahr) anfordern.</span><span class="sxs-lookup"><span data-stu-id="0cd5c-105">A client can request a TTL value for an entry ranging between 1 and 31557600 (that is, from 1 second to 1 year).</span></span> <span data-ttu-id="0cd5c-106">Dieser Attributwerte Bereich wird von den **rangeLower** -und **rangeUpper** -Attributwerten in der **attributeSchema** -Definition für das **entryttl** -Attribut erzwungen.</span><span class="sxs-lookup"><span data-stu-id="0cd5c-106">This attribute value range will be enforced by the **rangeLower** and **rangeUpper** attribute values in the **attributeSchema** definition for the **entryTTL** attribute.</span></span> <span data-ttu-id="0cd5c-107">Gemäß RFC 2589 müssen Verzeichnisserver diesen Wert nicht akzeptieren, und es wird möglicherweise ein anderer TTL-Wert an den Client zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0cd5c-107">As per RFC 2589, directory servers are not required to accept this value and might return a different TTL value to the client.</span></span> <span data-ttu-id="0cd5c-108">Clients müssen diesen vom Server vorgegebenen Wert als Client Aktualisierungs Zeitraum (CRP) verwenden können, mit dem bestimmt wird, wie oft der Client den Aktualisierungs Vorgang für den dynamischen Eintrag ausführen muss.</span><span class="sxs-lookup"><span data-stu-id="0cd5c-108">Clients must be able to use this server-dictated value as their client refresh period (CRP) which will govern how often the client will need to perform the refresh operation on the dynamic entry.</span></span>

<span data-ttu-id="0cd5c-109">Active Directory Domain Services Administratoren die Möglichkeit bieten, die Standard-und die minimalen TTL-Werte für eine Gesamtstruktur zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="0cd5c-109">Active Directory Domain Services provide administrators with the ability to configure the default and minimum TTL values for a forest.</span></span> <span data-ttu-id="0cd5c-110">Der Standardwert für die Gültigkeitsdauer wird einem neu erstellten dynamischen Eintrag zugewiesen, wenn eine Gültigkeitsdauer nicht explizit angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0cd5c-110">The default TTL value is what will be assigned to a newly created dynamic entry if a TTL is not explicitly specified.</span></span> <span data-ttu-id="0cd5c-111">Die minimale Gültigkeitsdauer überschreibt jeden vom Client angegebenen TTL-Wert, der niedriger ist als der konfigurierte Mindestwert.</span><span class="sxs-lookup"><span data-stu-id="0cd5c-111">The minimum TTL will override any client specified TTL value that is lower than the configured minimum.</span></span> <span data-ttu-id="0cd5c-112">Es muss kein konfigurierbarer maximaler TTL-Wert angegeben werden, da ein Maximum durch den Wert des **rangeUpper** -Attributs im **attributeSchema** -Objekt festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="0cd5c-112">No configurable maximum TTL value needs to be provided because a maximum will be imposed by the **rangeUpper** attribute value in the **attributeSchema** object.</span></span> <span data-ttu-id="0cd5c-113">Wenn Sie zulassen, dass Administratoren diese Werte konfigurieren, können Sie TTL-Werte festlegen, die einen niedrigen Aktualisierungs Datenverkehr erzwingen, oder auf der anderen Seite ein hoch aktuellste Verzeichnis bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="0cd5c-113">Allowing administrators to configure these values will enable them to set TTL values which will enforce a low refresh traffic or, at the other extreme, provide a highly up-to-date directory.</span></span>

<span data-ttu-id="0cd5c-114">Die Standardwerte für die zwei konfigurierbaren TTL-Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="0cd5c-114">The default values for the two configurable TTL parameters will be as follows:</span></span>

-   <span data-ttu-id="0cd5c-115">Standardmäßiger TTL-Wert = 86400 Sekunden (1 Tag)</span><span class="sxs-lookup"><span data-stu-id="0cd5c-115">Default TTL value = 86400 seconds (1 day)</span></span>
-   <span data-ttu-id="0cd5c-116">Minimaler TTL-Wert = 900 Sekunden (15 Minuten)</span><span class="sxs-lookup"><span data-stu-id="0cd5c-116">Minimum TTL value = 900 seconds (15 minutes)</span></span>

<span data-ttu-id="0cd5c-117">Die konfigurierbaren TTL-Parameter werden als AVA-Einträge (Attribut Wert Assertionen) in der Form "<-Wertname>=" gespeichert.</span><span class="sxs-lookup"><span data-stu-id="0cd5c-117">The configurable TTL parameters will be stored as AVA (attribute value assertion) entries of the form "<value-name>=</span></span><value><span data-ttu-id="0cd5c-118">"im Attribut **ms-DS-Other-Settings** des NTDS-Service Objekts, das durch den folgenden DN in der Konfigurations Partition angegeben wird:</span><span class="sxs-lookup"><span data-stu-id="0cd5c-118">" in the attribute **ms-DS-Other-Settings** of the NTDS-Service object given by the following DN in the Configuration partition:</span></span>


```C++
CN=Directory Service,CN=Windows NT,CN=Services,CN=Configuration,DC=...
```



<span data-ttu-id="0cd5c-119">Die exakte AVA-Syntax für die zwei konfigurierbaren TTL-Parameter ist wie folgt, wobei nnnn in Sekunden ausgedrückt wird:</span><span class="sxs-lookup"><span data-stu-id="0cd5c-119">The exact AVA syntax, for the two configurable TTL parameters, is as follows where NNNN is expressed in seconds:</span></span>


```C++
DynamicObjectDefaultTTLSeconds=NNNN
```




```C++
DynamicObjectMinTTLSeconds=NNNN
```



<span data-ttu-id="0cd5c-120">Diese Werte können von einem Administrator über das Befehlszeilen-Hilfsprogramm Ntdsutil festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="0cd5c-120">These values can be set by an administrator through the command-line utility ntdsutil.</span></span>

 

 




