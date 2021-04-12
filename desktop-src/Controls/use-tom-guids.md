---
title: Verwenden von Tom-GUIDs
description: Tom-GUIDs (Text Object Model) werden in "Tom. h" in den-Anweisungen der Mittell- \_ Schnittstelle angegeben. Um die zugeordneten Schnittstellen zu verwenden, müssen Sie zuerst die-Schnittstelle mit der GUID deklarieren.
ms.assetid: 48FF98C9-D42E-4E7F-874F-8E56F730E24E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db9c937d8b3c3612a3a49f27f18ac7c392b7a596
ms.sourcegitcommit: f0ca63c18dc52c357d3398af7be766d2bdd40be7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2020
ms.locfileid: "104472452"
---
# <a name="how-to-use-tom-guids"></a><span data-ttu-id="86782-104">Verwenden von Tom-GUIDs</span><span class="sxs-lookup"><span data-stu-id="86782-104">How to Use TOM GUIDs</span></span>

<span data-ttu-id="86782-105">Tom-GUIDs (Text Object Model) werden in "Tom. h" in den-Anweisungen der Mittell- \_ Schnittstelle angegeben.</span><span class="sxs-lookup"><span data-stu-id="86782-105">Text Object Model (TOM) GUIDs are given in Tom.h inside the MIDL\_INTERFACE statements.</span></span> <span data-ttu-id="86782-106">Um die zugeordneten Schnittstellen zu verwenden, müssen Sie zuerst die-Schnittstelle mit der GUID deklarieren.</span><span class="sxs-lookup"><span data-stu-id="86782-106">To use the associated interfaces, you must first declare the interface by using the GUID.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="86782-107">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="86782-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="86782-108">Technologien</span><span class="sxs-lookup"><span data-stu-id="86782-108">Technologies</span></span>

-   [<span data-ttu-id="86782-109">Windows-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="86782-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="86782-110">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="86782-110">Prerequisites</span></span>

-   <span data-ttu-id="86782-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="86782-111">C/C++</span></span>
-   <span data-ttu-id="86782-112">Programmieren der Windows-Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="86782-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="86782-113">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="86782-113">Instructions</span></span>

### <a name="use-a-tom-guid"></a><span data-ttu-id="86782-114">Tom-GUID verwenden</span><span class="sxs-lookup"><span data-stu-id="86782-114">Use a TOM GUID</span></span>

<span data-ttu-id="86782-115">Der folgende Beispielcode zeigt, wie die [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument) -Schnittstelle verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="86782-115">The following example code demonstrates how to use the [**ITextDocument**](/windows/desktop/api/Tom/nn-tom-itextdocument) interface.</span></span>


```C++
#define DEFINE_GUIDXXX(name, l, w1, w2, b1, b2, b3, b4, b5, b6, b7, b8) \
        EXTERN_C const GUID CDECL name \
                = { l, w1, w2, { b1, b2,  b3,  b4,  b5,  b6,  b7,  b8 } }

DEFINE_GUIDXXX(IID_ITextDocument,0x8CC497C0,0xA1DF,0x11CE,0x80,0x98,
                0x00,0xAA,0x00,0x47,0xBE,0x5D);
```



## <a name="related-topics"></a><span data-ttu-id="86782-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="86782-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86782-117">Verwenden des Text Objektmodells</span><span class="sxs-lookup"><span data-stu-id="86782-117">Using The Text Object Model</span></span>](using-the-text-object-model.md)
</dt> <dt>

[<span data-ttu-id="86782-118">Verwenden von Rich Edit-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="86782-118">Using Rich Edit Controls</span></span>](using-rich-edit-controls.md)
</dt> <dt>

<span data-ttu-id="86782-119">[Demo zu allgemeinen Windows-Steuerelementen (cppwindowscommoncontrols)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span><span class="sxs-lookup"><span data-stu-id="86782-119">[Windows common controls demo (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)</span></span>
</dt> </dl>

 

 




