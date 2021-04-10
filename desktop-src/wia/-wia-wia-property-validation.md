---
description: 'Wenn eine Anwendung einen IPropertyStorage:: Write-Multiple-Vorgang für jede beschreibbare Windows-Abbild Erfassungs Eigenschaft (WIA) ausführt, führt der WIA-Treiber eine Validierung für den neuen Eigenschafts Wert aus.'
ms.assetid: 61ab2b8b-4c0a-40f4-87f0-2dd3ceea70ab
title: Überprüfung der WIA-Eigenschaft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a60d9e64122e19249c19bc47564631162d783920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214640"
---
# <a name="wia-property-validation"></a><span data-ttu-id="c2ef3-103">Überprüfung der WIA-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c2ef3-103">WIA Property Validation</span></span>

<span data-ttu-id="c2ef3-104">Wenn eine Anwendung einen [IPropertyStorage:: Write-Multiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) -Vorgang für jede beschreibbare Windows-Abbild Erfassungs Eigenschaft (WIA) ausführt, führt der WIA-Treiber eine Validierung für den neuen Eigenschafts Wert aus.</span><span class="sxs-lookup"><span data-stu-id="c2ef3-104">When an application performs an [IPropertyStorage::WriteMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) operation on any writeable Windows Image Acquisition (WIA) property, the WIA driver performs a validation on the new property value.</span></span> <span data-ttu-id="c2ef3-105">Das Schreiben einer Eigenschaft kann Nebenwirkungen aufweisen, die andere Eigenschaftswerte ändern.</span><span class="sxs-lookup"><span data-stu-id="c2ef3-105">Writing one property may have side affects that change other property values.</span></span> <span data-ttu-id="c2ef3-106">Die Anwendung muss alle Eigenschaftswerte nach einem Schreibvorgang lesen, um zu ermitteln, ob alle Eigenschaften auf die von der Anwendung gewünschten Werte festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="c2ef3-106">It is up to the application to read all property values after a write operation to determine that all properties are set to values the application desires.</span></span>

<span data-ttu-id="c2ef3-107">Mehrere Eigenschaften können gleichzeitig mit dem [IPropertyStorage:: schreitemultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) -Vorgang geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="c2ef3-107">Multiple properties can be written simultaneously using the [IPropertyStorage::WriteMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-writemultiple) operation.</span></span> <span data-ttu-id="c2ef3-108">Möglicherweise gibt es Fälle, in denen einige Eigenschafts Zuweisungen Konflikte verursachen.</span><span class="sxs-lookup"><span data-stu-id="c2ef3-108">There may be cases where some property assignments conflict.</span></span> <span data-ttu-id="c2ef3-109">In solchen Fällen ist die Priorität, die zum Auflösen von Konflikten verwendet wird, wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c2ef3-109">In such cases, the priority used to resolve conflicts is as follows:</span></span>

1.  <span data-ttu-id="c2ef3-110">\_ \_ cur- \_ Absicht der WIA-IPS</span><span class="sxs-lookup"><span data-stu-id="c2ef3-110">WIA\_IPS\_CUR\_INTENT</span></span>
2.  <span data-ttu-id="c2ef3-111">WIA \_ IPA- \_ DataType</span><span class="sxs-lookup"><span data-stu-id="c2ef3-111">WIA\_IPA\_DATATYPE</span></span>
3.  <span data-ttu-id="c2ef3-112">WIA \_ IPA- \_ Tiefe</span><span class="sxs-lookup"><span data-stu-id="c2ef3-112">WIA\_IPA\_DEPTH</span></span>
4.  <span data-ttu-id="c2ef3-113">WIA- \_ IPS- \_ xres</span><span class="sxs-lookup"><span data-stu-id="c2ef3-113">WIA\_IPS\_XRES</span></span>
5.  <span data-ttu-id="c2ef3-114">WIA- \_ IPS \_</span><span class="sxs-lookup"><span data-stu-id="c2ef3-114">WIA\_IPS\_YRES</span></span>
6.  <span data-ttu-id="c2ef3-115">WIA- \_ IPS- \_ xPos</span><span class="sxs-lookup"><span data-stu-id="c2ef3-115">WIA\_IPS\_XPOS</span></span>
7.  <span data-ttu-id="c2ef3-116">WIA- \_ IPS ( \_ yPos)</span><span class="sxs-lookup"><span data-stu-id="c2ef3-116">WIA\_IPS\_YPOS</span></span>
8.  <span data-ttu-id="c2ef3-117">WIA- \_ IPS- \_ XBlock</span><span class="sxs-lookup"><span data-stu-id="c2ef3-117">WIA\_IPS\_XEXTENT</span></span>
9.  <span data-ttu-id="c2ef3-118">WIA- \_ IPS \_ yblock</span><span class="sxs-lookup"><span data-stu-id="c2ef3-118">WIA\_IPS\_YEXTENT</span></span>

## <a name="related-topics"></a><span data-ttu-id="c2ef3-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c2ef3-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2ef3-120">**Iwiapropertystorage**</span><span class="sxs-lookup"><span data-stu-id="c2ef3-120">**IWiaPropertyStorage**</span></span>](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage)
</dt> </dl>

 

 
