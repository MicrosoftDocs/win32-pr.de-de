---
title: Der ACF-Header
description: Der ACF-Header enthält plattformspezifische Attribute, die auf die gesamte Schnittstelle angewendet werden. Attribute, die auf einzelne Typen und Funktionen im ACF-Text angewendet werden, überschreiben die Attribute im ACF-Header. Im ACF-Header sind keine Attribute erforderlich.
ms.assetid: c09ec0f2-2302-450a-b74b-c9008beca325
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64e958044f043db8828f0fdda192918c632c321b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039269"
---
# <a name="the-acf-header"></a><span data-ttu-id="58f44-105">Der ACF-Header</span><span class="sxs-lookup"><span data-stu-id="58f44-105">The ACF Header</span></span>

<span data-ttu-id="58f44-106">Der ACF-Header enthält plattformspezifische Attribute, die auf die gesamte Schnittstelle angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="58f44-106">The ACF header contains platform-specific attributes that apply to the interface as a whole.</span></span> <span data-ttu-id="58f44-107">Attribute, die auf einzelne Typen und Funktionen im ACF-Text angewendet werden, überschreiben die Attribute im ACF-Header.</span><span class="sxs-lookup"><span data-stu-id="58f44-107">Attributes applied to individual types and functions in the ACF body override the attributes in the ACF header.</span></span> <span data-ttu-id="58f44-108">Im ACF-Header sind keine Attribute erforderlich.</span><span class="sxs-lookup"><span data-stu-id="58f44-108">No attributes are required in the ACF header.</span></span>

<span data-ttu-id="58f44-109">Der ACF-Header kann eines der folgenden Attribute enthalten: **\[** [**Automatisches \_ handle**](/windows/desktop/Midl/auto-handle) **\]** , **\[** [**implizites \_**](/windows/desktop/Midl/implicit-handle)Handle **\]** oder [**explizites \_ handle**](/windows/desktop/Midl/explicit-handle) **\]** .</span><span class="sxs-lookup"><span data-stu-id="58f44-109">The ACF header can include one of the following attributes: **\[**[**auto\_handle**](/windows/desktop/Midl/auto-handle)**\]**, **\[**[**implicit\_handle**](/windows/desktop/Midl/implicit-handle)**\]**, or [**explicit\_handle**](/windows/desktop/Midl/explicit-handle)**\]**.</span></span> <span data-ttu-id="58f44-110">Wenn ein **\[ Automatisches \_ handle \]** oder **\[ implizites \_ handle \]** verwendet wird, gibt es den Typ des Bindungs Handles an, der für die Bindung verwendet wird, wenn eine Remote Funktion keinen expliziten Bindungs handle-Parameter hat.</span><span class="sxs-lookup"><span data-stu-id="58f44-110">If **\[auto\_handle\]** or **\[implicit\_handle\]** is used, it specifies the type of binding handle that will be used for binding when a remote function does not have an explicit binding-handle parameter.</span></span> <span data-ttu-id="58f44-111">Wenn die ACF nicht vorhanden ist oder kein automatisches, implizites oder explizites Bindungs Handle angibt, verwendet die Mittel l das **\[ automatische \_ handle \]** für die implizite Bindung.</span><span class="sxs-lookup"><span data-stu-id="58f44-111">When the ACF is not present or does not specify an automatic, implicit, or explicit binding handle, MIDL uses **\[auto\_handle\]** for implicit binding.</span></span>

<span data-ttu-id="58f44-112">Entweder **\[** kann [**Code**](/windows/desktop/Midl/code) **\]** oder **\[** [**NoCode**](/windows/desktop/Midl/nocode) **\]** im Schnittstellen Header angezeigt werden, aber der von Ihnen gewählte kann nur ein Mal angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="58f44-112">Either **\[**[**code**](/windows/desktop/Midl/code)**\]** or **\[**[**nocode**](/windows/desktop/Midl/nocode)**\]** can appear in the interface header, but the one you choose can appear only once.</span></span> <span data-ttu-id="58f44-113">Wenn keines der Attribute vorhanden ist, verwendet der Compiler **\[ Code \]** als Standardwert.</span><span class="sxs-lookup"><span data-stu-id="58f44-113">When neither attribute is present, the compiler uses **\[code\]** as a default.</span></span>

<span data-ttu-id="58f44-114">Weitere Informationen finden Sie unter [ACF-Attribute](/windows/desktop/Midl/acf-attributes).</span><span class="sxs-lookup"><span data-stu-id="58f44-114">For more information, see [ACF Attributes](/windows/desktop/Midl/acf-attributes).</span></span>

 

 