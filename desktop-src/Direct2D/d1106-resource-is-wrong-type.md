---
title: D1106 Ressource ist falsch.
ms.assetid: 79a618cb-1d05-4895-b801-7663890b456a
description: Die angegebene Ressource weist nicht den erwarteten Typ auf.
keywords:
- D1106 Ressource hat den falschen Typ Direct2D
topic_type:
- apiref
api_name:
- D1106 Resource Is Wrong Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 5c38ef36319b8021de918a798c94a3be0683a7b7
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/27/2021
ms.locfileid: "106372019"
---
# <a name="d1106-resource-is-wrong-type"></a><span data-ttu-id="037de-104">D1106: Ressource ist falsch.</span><span class="sxs-lookup"><span data-stu-id="037de-104">D1106: Resource Is Wrong Type</span></span>

<span data-ttu-id="037de-105">Die angegebene Ressourcen \[ *Ressource* weist \] nicht den erwarteten Typ auf.</span><span class="sxs-lookup"><span data-stu-id="037de-105">The given resource \[*resource*\] is not of an expected type.</span></span>

## <a name="placeholders"></a><span data-ttu-id="037de-106">Platzhalter</span><span class="sxs-lookup"><span data-stu-id="037de-106">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="037de-107"><span id="resource"></span><span id="RESOURCE"></span>*Ressource*</span><span class="sxs-lookup"><span data-stu-id="037de-107"><span id="resource"></span><span id="RESOURCE"></span>*resource*</span></span>
</dt> <dd>

<span data-ttu-id="037de-108">Die Adresse der Ressource.</span><span class="sxs-lookup"><span data-stu-id="037de-108">The address of the resource.</span></span>

</dd> </dl> 




 

## <a name="possible-causes"></a><span data-ttu-id="037de-109">Mögliche Ursachen</span><span class="sxs-lookup"><span data-stu-id="037de-109">Possible Causes</span></span>

<span data-ttu-id="037de-110">Eine Schnittstelle wurde nicht ordnungsgemäß umgewandelt und als Parameter für eine Methode oder Funktion verwendet.</span><span class="sxs-lookup"><span data-stu-id="037de-110">An interface was improperly cast and used as a parameter for a method or function.</span></span>

## <a name="examples"></a><span data-ttu-id="037de-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="037de-111">Examples</span></span>

<span data-ttu-id="037de-112">Im folgenden Beispiel wird ein [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) -Wert weitergeleitet, wenn ein [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) erwartet wird.</span><span class="sxs-lookup"><span data-stu-id="037de-112">The following example passes an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) when an [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) is expected.</span></span>


```C++
        m_pRenderTarget->FillGeometry(
            (ID2D1Geometry*)m_pYellowGreenBrush,
            m_pYellowGreenBrush
            );
```



<span data-ttu-id="037de-113">Dieses Beispiel erzeugt die folgende Debugmeldung:</span><span class="sxs-lookup"><span data-stu-id="037de-113">This example produces the following debug message:</span></span>

``` syntax
DEBUG ERROR - The given resource[003A2C98] is not of an expected type
```

## <a name="fixes"></a><span data-ttu-id="037de-114">Fehlerbehebungen</span><span class="sxs-lookup"><span data-stu-id="037de-114">Fixes</span></span>

<span data-ttu-id="037de-115">Verwenden Sie den Typ, der von der Methode benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="037de-115">Use the type required by the method.</span></span>

 

 
