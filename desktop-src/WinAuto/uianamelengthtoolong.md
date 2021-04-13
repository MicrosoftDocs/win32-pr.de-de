---
title: Uianamelengthtoolong
description: Uianamelengthtoolong
ms.assetid: 01AF3F1E-9A3F-48B4-8219-6E80BAFC82EE
keywords:
- AutomationElement. NameProperty des UIA_NamePropertyId Bezeichners
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ab786b7167dab4a25384ce3abe2509babcf1f82
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388652"
---
# <a name="uianamelengthtoolong"></a><span data-ttu-id="4b3ab-104">Uianamelengthtoolong</span><span class="sxs-lookup"><span data-stu-id="4b3ab-104">UiaNameLengthTooLong</span></span>

## <a name="text"></a><span data-ttu-id="4b3ab-105">Text</span><span class="sxs-lookup"><span data-stu-id="4b3ab-105">Text</span></span>

<span data-ttu-id="4b3ab-106">Der Element Name darf keine Zeichenfolge zurückgeben, die länger als Zeichen ist. {0}</span><span class="sxs-lookup"><span data-stu-id="4b3ab-106">Element's name should not return a string longer than {0} character</span></span>

## <a name="type"></a><span data-ttu-id="4b3ab-107">type</span><span class="sxs-lookup"><span data-stu-id="4b3ab-107">Type</span></span>

<span data-ttu-id="4b3ab-108">Fehler</span><span class="sxs-lookup"><span data-stu-id="4b3ab-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="4b3ab-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4b3ab-109">Description</span></span>

<span data-ttu-id="4b3ab-110">Der Name eines Elements enthält zu viele Zeichen.</span><span class="sxs-lookup"><span data-stu-id="4b3ab-110">The name of an element contains too many characters.</span></span> <span data-ttu-id="4b3ab-111">Beispielsweise gibt die [**iuiautomationelement:: currentname**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) -Methode, die verwendet wird, um den UIA-Namen eines Elements abzurufen, eine Zeichenfolge zurück, die den Grenzwert überschreitet.</span><span class="sxs-lookup"><span data-stu-id="4b3ab-111">For example, the [**IUIAutomationElement::CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) method used to retrieve the UIA name of an element returns a string greater than the limit.</span></span>

<span data-ttu-id="4b3ab-112">Dieses Problem bewirkt, dass Personen, die sich auf einen Bildschirm-Reader und eine Tastatur für die Navigation verlassen, Probleme verursachen, da ein Element möglicherweise einen nicht Aussage fähigen, nicht intuitiven Namen hat.</span><span class="sxs-lookup"><span data-stu-id="4b3ab-112">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because an element might have an unpronounceable, non-intuitive name.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="4b3ab-113">Mögliche Ursachen</span><span class="sxs-lookup"><span data-stu-id="4b3ab-113">Possible causes</span></span>

<span data-ttu-id="4b3ab-114">Dem Element oder seinem übergeordneten Element ist ein falsch zugewiesener Name oder eine Bezeichnung zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="4b3ab-114">The element or its parent has an incorrectly assigned name or label.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4b3ab-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4b3ab-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b3ab-116">**UIA- \_ namepropertyid**</span><span class="sxs-lookup"><span data-stu-id="4b3ab-116">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)
</dt> <dt>

[<span data-ttu-id="4b3ab-117">**Iuiautomationelement:: currentname**</span><span class="sxs-lookup"><span data-stu-id="4b3ab-117">**IUIAutomationElement::CurrentName**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 




