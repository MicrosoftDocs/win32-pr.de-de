---
title: Treemightbecyclic
description: Treemightbecyclic
ms.assetid: 9A997949-A1A2-448C-9739-BE176621F1B4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9647f4429ba17226f342a8dceb3c51b033d08b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315279"
---
# <a name="treemightbecyclic"></a><span data-ttu-id="b6eab-103">Treemightbecyclic</span><span class="sxs-lookup"><span data-stu-id="b6eab-103">TreeMightBeCyclic</span></span>

## <a name="text"></a><span data-ttu-id="b6eab-104">Text</span><span class="sxs-lookup"><span data-stu-id="b6eab-104">Text</span></span>

<span data-ttu-id="b6eab-105">Struktur ist {0} Tiefe Ebenen.</span><span class="sxs-lookup"><span data-stu-id="b6eab-105">Tree is {0} levels deep.</span></span> <span data-ttu-id="b6eab-106">Dies weist möglicherweise darauf hin, dass die Barrierefreiheits Struktur zyklisch ist und daher scheinbar unendlich wäre.</span><span class="sxs-lookup"><span data-stu-id="b6eab-106">This might indicate that the accessibility tree is cyclic, and thus it would appear to be infinite.</span></span>

## <a name="type"></a><span data-ttu-id="b6eab-107">type</span><span class="sxs-lookup"><span data-stu-id="b6eab-107">Type</span></span>

<span data-ttu-id="b6eab-108">Fehler</span><span class="sxs-lookup"><span data-stu-id="b6eab-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="b6eab-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b6eab-109">Description</span></span>

<span data-ttu-id="b6eab-110">Die Elementstruktur ist zyklisch, und die Struktur Tiefe kann unendlich sein.</span><span class="sxs-lookup"><span data-stu-id="b6eab-110">The element tree is cyclic and the tree depth might be infinite.</span></span>

<span data-ttu-id="b6eab-111">Dieses Problem bewirkt, dass Personen, die sich auf einen Bildschirm-Reader und eine Tastatur für die Navigation verlassen, keine offensichtlichen Beschränkungen für die Durchquerung der Elemente in der Zielanwendung auftreten.</span><span class="sxs-lookup"><span data-stu-id="b6eab-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because there will be no apparent limit to the traversal of elements in the target application.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="b6eab-112">Mögliche Ursachen</span><span class="sxs-lookup"><span data-stu-id="b6eab-112">Possible causes</span></span>

<span data-ttu-id="b6eab-113">Mehrere Elemente oder ihre übergeordneten Elemente sind benutzerdefinierte Steuerelemente, die die Tabstopps nicht ordnungsgemäß implementieren.</span><span class="sxs-lookup"><span data-stu-id="b6eab-113">Multiple elements, or their parents, are custom controls that do not implement tabbing correctly.</span></span> <span data-ttu-id="b6eab-114">Beispielsweise wird die Eigenschaft MSAA [State](state-property.md) nicht ordnungsgemäß aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="b6eab-114">For example, the MSAA [State](state-property.md) property is not updated correctly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b6eab-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b6eab-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6eab-116">Richtlinien zur Gestaltung einer tastaturgesteuerten Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="b6eab-116">Guidelines for Keyboard User Interface Design</span></span>](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> <dt>

[<span data-ttu-id="b6eab-117">Windows-Benutzeroberflächen-Interaktions Richtlinien-Tastatur</span><span class="sxs-lookup"><span data-stu-id="b6eab-117">Windows User Experience Interaction Guidelines - Keyboard</span></span>](https://msdn.microsoft.com/library/bb545460.aspx#guidelines)
</dt> </dl>

 

 