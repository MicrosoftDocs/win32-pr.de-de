---
description: Netzwerkmonitor stellt eine PropertyInfo-Struktur zum Definieren der Eigenschaften eines Protokolls und eine propertyinst-Struktur sowie eine propertyinstex-Struktur zum Definieren einer Instanz einer Eigenschaft bereit.
ms.assetid: d1e29bd6-c04a-48f1-9727-96b9450e256f
title: Eigenschafts Definition und eigenschafteninstanzstrukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55aa67efb5054d93184b56c53f84f9fac0893abf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756209"
---
# <a name="property-definition-and-property-instance-structures"></a><span data-ttu-id="4d550-103">Eigenschafts Definition und eigenschafteninstanzstrukturen</span><span class="sxs-lookup"><span data-stu-id="4d550-103">Property Definition and Property Instance Structures</span></span>

<span data-ttu-id="4d550-104">Netzwerkmonitor stellt eine [**PropertyInfo**](propertyinfo.md) -Struktur zum Definieren der Eigenschaften eines Protokolls und eine [**propertyinst**](propertyinst.md)-Struktur sowie eine [**propertyinstex**](propertyinstex.md) -Struktur zum Definieren einer Instanz einer Eigenschaft bereit.</span><span class="sxs-lookup"><span data-stu-id="4d550-104">Network Monitor provides a [**PROPERTYINFO**](propertyinfo.md) structure to define the properties of a protocol, and a [**PROPERTYINST**](propertyinst.md), and [**PROPERTYINSTEX**](propertyinstex.md) structure to define an instance of a property.</span></span>

![Netzwerkmonitor Strukturen](images/property1.png)

<span data-ttu-id="4d550-106">Der Parser weist die [**PropertyInfo**](propertyinfo.md) -Struktur für alle Eigenschaften zu, die ein Protokoll unterstützt, und füllt diese aus.</span><span class="sxs-lookup"><span data-stu-id="4d550-106">The parser allocates and fills-in the [**PROPERTYINFO**](propertyinfo.md) structure for all the properties that a protocol supports.</span></span> <span data-ttu-id="4d550-107">Der Parser übergibt die Struktur an Netzwerkmonitor, wo die Struktur der Protokoll [*Eigenschaften Datenbank*](p.md)hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="4d550-107">The parser passes the structure to Network Monitor where the structure is added to the protocol [*property database*](p.md).</span></span> <span data-ttu-id="4d550-108">Die Informationen in der **PropertyInfo** -Struktur werden beim Auswerten einer Instanz einer Eigenschaft und beim Formatieren der Daten verwendet, die in der Netzwerkmonitor-Benutzeroberfläche angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="4d550-108">The information in the **PROPERTYINFO** structure is used when parsing an instance of a property, and when formatting the data that is displayed in the Network Monitor UI.</span></span>

<span data-ttu-id="4d550-109">Netzwerkmonitor ordnet die Strukturen [**propertyinst**](propertyinst.md) und [**propertyinstex**](propertyinstex.md) zu, wenn der Parser eine Eigenschafts Definition an eine Instanz einer Eigenschaft anfügt.</span><span class="sxs-lookup"><span data-stu-id="4d550-109">Network Monitor allocates the [**PROPERTYINST**](propertyinst.md) and [**PROPERTYINSTEX**](propertyinstex.md) structures when the parser attaches a property definition to an instance of a property.</span></span>

<span data-ttu-id="4d550-110">Im folgenden Verfahren werden die Schritte beschrieben, die zum Anfügen einer Eigenschafts Definition erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="4d550-110">The following procedure identifies the steps necessary to attach a property definition.</span></span>

<span data-ttu-id="4d550-111">**So fügen Sie eine Eigenschaften Definition an**</span><span class="sxs-lookup"><span data-stu-id="4d550-111">**To attach a property definition**</span></span>

1.  <span data-ttu-id="4d550-112">Identifizieren Sie jede Eigenschaft, die in einer Instanz des Protokolls vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="4d550-112">Identify each property that exists in an instance of the protocol.</span></span> <span data-ttu-id="4d550-113">Beim Anfügen einer Definition übergibt Netzwerkmonitor die erfassten Daten an den Parser.</span><span class="sxs-lookup"><span data-stu-id="4d550-113">When attaching a definition, Network Monitor passes the captured data to the parser.</span></span> <span data-ttu-id="4d550-114">Die Daten werden auf der Basis einer Protokoll Instanz übermittelt.</span><span class="sxs-lookup"><span data-stu-id="4d550-114">The data is passed on a protocol instance basis.</span></span>
2.  <span data-ttu-id="4d550-115">Bestimmen Sie den Speicherort der Eigenschaft in der Protokoll Instanz.</span><span class="sxs-lookup"><span data-stu-id="4d550-115">Determine the location of the property in the protocol instance.</span></span>
3.  <span data-ttu-id="4d550-116">Fügen Sie eine Eigenschaften Definition an den Speicherort der Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="4d550-116">Attach a property definition to the property location.</span></span>

<span data-ttu-id="4d550-117">Netzwerkmonitor implementiert eine [**propertyinst**](propertyinst.md) -Struktur, wenn der Parser die Eigenschafts Daten verwendet, die in der Erfassung vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="4d550-117">Network Monitor implements a [**PROPERTYINST**](propertyinst.md) structure when the parser uses the property data as it exists in the capture.</span></span> <span data-ttu-id="4d550-118">Netzwerkmonitor implementiert eine [**propertyinstex**](propertyinstex.md) -Struktur, wenn der Parser die Eigenschafts Daten in der Erfassung ändern muss.</span><span class="sxs-lookup"><span data-stu-id="4d550-118">Network Monitor implements a [**PROPERTYINSTEX**](propertyinstex.md) structure when the parser must modify the property data in the capture.</span></span>

 

 



