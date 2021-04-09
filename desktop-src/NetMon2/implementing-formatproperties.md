---
description: Netzwerkmonitor Ruft die formatproperties-Funktion auf, um die Daten zu formatieren, die im Detailbereich der Netzwerkmonitor Benutzeroberfläche angezeigt werden.
ms.assetid: d0a58e1d-c867-4277-916e-f408627b5269
title: Implementieren von formatproperties
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 660b581bf29fd8e5d40af65f5ff90e1e9223ad2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128913"
---
# <a name="implementing-formatproperties"></a><span data-ttu-id="507fc-103">Implementieren von formatproperties</span><span class="sxs-lookup"><span data-stu-id="507fc-103">Implementing FormatProperties</span></span>

<span data-ttu-id="507fc-104">Netzwerkmonitor Ruft die [**formatproperties**](formatproperties.md) -Funktion auf, um die Daten zu formatieren, die im Detailbereich der Netzwerkmonitor Benutzeroberfläche angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="507fc-104">Network Monitor calls the [**FormatProperties**](formatproperties.md) function to format the data that is displayed in the details pane of the Network Monitor UI.</span></span> <span data-ttu-id="507fc-105">Normalerweise wird **formatproperties** aufgerufen, um die Zusammenfassungs Zeile für ein Protokoll zu formatieren, und dann alle Eigenschaften Instanzen des Protokolls innerhalb eines Frames zu formatieren.</span><span class="sxs-lookup"><span data-stu-id="507fc-105">Typically, **FormatProperties** is called to format the summary line for a protocol, and then to format all the property instances of the protocol within a frame.</span></span> <span data-ttu-id="507fc-106">Netzwerkmonitor gibt jedoch nicht an, wie oft **formatproperties** für einen bestimmten Parser aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="507fc-106">However, Network Monitor does not identify the number of times that **FormatProperties** is called for a specific parser.</span></span>

<span data-ttu-id="507fc-107">Beim Aufrufen von [**formatproperties**](formatproperties.md)stellt Netzwerkmonitor eine [**propertyinst**](propertyinst.md) -Struktur für jede angezeigte Eigenschaft bereit.</span><span class="sxs-lookup"><span data-stu-id="507fc-107">When calling [**FormatProperties**](formatproperties.md), Network Monitor provides a [**PROPERTYINST**](propertyinst.md) structure for each property that it displays.</span></span> <span data-ttu-id="507fc-108">Die **propertyinst** -Struktur stellt Informationen zu den anzuzeigenden Daten bereit, einschließlich eines Zeigers auf die [**PropertyInfo**](propertyinfo.md) -Struktur, die die Funktion angibt, die zum Formatieren der angezeigten Dateneigenschaft verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="507fc-108">The **PROPERTYINST** structure provides information about the data to be displayed, including a pointer to the [**PROPERTYINFO**](propertyinfo.md) structure that specifies the function to use to format the displayed data property.</span></span>

> [!Note]  
> <span data-ttu-id="507fc-109">Eine [**PropertyInfo**](propertyinfo.md) -Struktur wird angegeben, wenn der- [*Eigenschaften Datenbank*](p.md) des Parsers eine Eigenschaft hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="507fc-109">A [**PROPERTYINFO**](propertyinfo.md) structure is specified when adding a property to the [*property database*](p.md) of the parser.</span></span>

 

<span data-ttu-id="507fc-110">Netzwerkmonitor identifiziert die Formatierungsfunktion, die für jede Eigenschaften Instanz aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="507fc-110">Network Monitor identifies the format function to call for each property instance.</span></span> <span data-ttu-id="507fc-111">Der **InstanceData** -Member der [**PropertyInfo**](propertyinfo.md) -Struktur kann Folgendes angeben:</span><span class="sxs-lookup"><span data-stu-id="507fc-111">The **InstanceData** member of the [**PROPERTYINFO**](propertyinfo.md) structure can specify the following:</span></span>

-   <span data-ttu-id="507fc-112">Die [**formatpropertyinstance**](formatpropertyinstance.md) -Funktion, um den von Netzwerkmonitor bereitgestellten [*generischen Formatierer*](g.md) zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="507fc-112">The [**FormatPropertyInstance**](formatpropertyinstance.md) function to use the [*generic formatter*](g.md) that Network Monitor provides.</span></span>

    <span data-ttu-id="507fc-113">– oder –</span><span class="sxs-lookup"><span data-stu-id="507fc-113">– or –</span></span>

-   <span data-ttu-id="507fc-114">Der Name einer benutzerdefinierten Format Funktion, die der Parser bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="507fc-114">The name of a custom format function that the parser provides.</span></span>

<span data-ttu-id="507fc-115">Die [**formatpropertyinstance**](formatpropertyinstance.md) und die benutzerdefinierten Formatfunktionen geben die formatierten Daten zurück, die im Detailbereich der Netzwerkmonitor-Benutzeroberfläche angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="507fc-115">The [**FormatPropertyInstance**](formatpropertyinstance.md) and the custom format functions return the formatted data that is displayed in the details pane of the Network Monitor UI.</span></span>

<span data-ttu-id="507fc-116">In der folgenden Abbildung wird gezeigt, wie Netzwerkmonitor die Funktion identifiziert, die für jede Eigenschaften Instanz aufgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="507fc-116">The following illustration shows how Network Monitor identifies the function to call for each property instance.</span></span>

![Identifizieren der aufzurufenden Funktion durch den Netzwerkmonitor](images/formatprop1.png)

<span data-ttu-id="507fc-118">Im folgenden Verfahren werden die erforderlichen Schritte zum Implementieren von [**formatproperties**](formatproperties.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="507fc-118">The following procedure identifies the steps necessary to implement [**FormatProperties**](formatproperties.md).</span></span>

<span data-ttu-id="507fc-119">**So implementieren Sie Format Properties**</span><span class="sxs-lookup"><span data-stu-id="507fc-119">**To implement FormatProperties**</span></span>

-   <span data-ttu-id="507fc-120">Rufen Sie mithilfe einer Schleifen Struktur die Format-Funktion für jede [**propertyinst**](propertyinst.md) -Struktur auf, die dem Parser im *lppropinst* -Parameter der [**formatproperties**](formatproperties.md) -Funktion übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="507fc-120">Using a loop structure, call the format function for each [**PROPERTYINST**](propertyinst.md) structure that is passed to the parser in the *lpPropInst* parameter of the [**FormatProperties**](formatproperties.md) function.</span></span>

<span data-ttu-id="507fc-121">Im folgenden finden Sie eine grundlegende Implementierung von [**formatproperties**](formatproperties.md).</span><span class="sxs-lookup"><span data-stu-id="507fc-121">The following is a basic implementation of [**FormatProperties**](formatproperties.md).</span></span>

``` syntax
#include <windows.h>

DWORD BHAPI MyProtocolFormatProperties( HFRAME hFrame,
                                        LPBYTE         pMacFrame,
                                        LPBYTE         pBLRPLATEFrame,
                                        DWORD          nPropertyInsts
                                        LPPROPERTYINST  p)
  {
    while( nPropertyInsts-- > 0)
      {
         ( (FORMAT) p->lpPropertyInfo->InstanceData) ) (p);
         p++;
      }
  return BHERR_SUCCESS;
  }
```

 

 



