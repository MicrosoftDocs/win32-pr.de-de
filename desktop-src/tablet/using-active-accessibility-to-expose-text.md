---
description: Übersicht über die Verwendung von aktivem Barrierefreiheit zum verfügbar machen von Text.
ms.assetid: c04ade90-5f17-4e16-b82b-c99230000954
title: Verwenden von Active Accessibility zur Offenlegung von Text
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52d475a8c576e109f47be7b5a3d61cddf543038d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343668"
---
# <a name="using-active-accessibility-to-expose-text"></a><span data-ttu-id="40f07-103">Verwenden von Active Accessibility zur Offenlegung von Text</span><span class="sxs-lookup"><span data-stu-id="40f07-103">Using Active Accessibility to Expose Text</span></span>

<span data-ttu-id="40f07-104">Anwendungen können mit Microsoft Active Accessibility Text verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="40f07-104">Applications can use Microsoft Active Accessibility to expose text.</span></span> <span data-ttu-id="40f07-105">Die [**IAccessible**](/windows/win32/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle, die in früheren Versionen von Active Accessibility definiert ist, ist jedoch nicht für das verfügbar machen großer Mengen an Rich-Text optimiert.</span><span class="sxs-lookup"><span data-stu-id="40f07-105">However, the [**IAccessible**](/windows/win32/api/oleacc/nn-oleacc-iaccessible) interface defined by earlier versions of Active Accessibility is not optimized for exposing large amounts of rich text.</span></span> <span data-ttu-id="40f07-106">Spätere Versionen definieren Schnittstellen, die für die Bereitstellung großer Mengen von Text-und Textattributen optimiert sind.</span><span class="sxs-lookup"><span data-stu-id="40f07-106">Later versions define interfaces that are optimized for exposing large amounts of text and textual attributes.</span></span>

<span data-ttu-id="40f07-107">Um große Mengen an Text verfügbar zu machen, erstellen Sie separate Component Object Model (com)-Objekte, die [**IAccessible**](/windows/win32/api/oleacc/nn-oleacc-iaccessible)-und untergeordnete Elemente unterstützen, um die einzelnen Textelemente darzustellen.</span><span class="sxs-lookup"><span data-stu-id="40f07-107">To expose large amounts text, create separate Component Object Model (COM) objects that support [**IAccessible**](/windows/win32/api/oleacc/nn-oleacc-iaccessible), or child elements, to represent each run of text.</span></span> <span data-ttu-id="40f07-108">Ein Run ist eine Zeile oder ein Teil einer Zeile, die dieselbe Formatierung hat.</span><span class="sxs-lookup"><span data-stu-id="40f07-108">A run is a line, or portion of a line, that shares the same formatting.</span></span>

<span data-ttu-id="40f07-109">Active Accessibility macht nur den Text und seinen Speicherort verfügbar, verfügt aber über keinen Mechanismus, um die Formatierung des Texts verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="40f07-109">Active Accessibility exposes only the text and its location, but has no mechanism for exposing the formatting of the text.</span></span> <span data-ttu-id="40f07-110">Trotz dieser Einschränkungen verwenden einige Programme Active Accessibility, um Text verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="40f07-110">Despite these limitations, some programs use Active Accessibility to expose text.</span></span> <span data-ttu-id="40f07-111">Beispielsweise verwenden Microsoft Internet Explorer und Microsoft Visual Studio Active Accessibility, um große Mengen von Text verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="40f07-111">For example, Microsoft Internet Explorer and Microsoft Visual Studio both use Active Accessibility to expose large amounts of text.</span></span>

<span data-ttu-id="40f07-112">Weitere Informationen zum verfügbar machen von Text mithilfe Active Accessibility finden Sie unter [Barrierefreiheit](../accessibility/accessibility.md).</span><span class="sxs-lookup"><span data-stu-id="40f07-112">For more information about exposing text by using Active Accessibility, see [Accessibility](../accessibility/accessibility.md).</span></span>

 

 
