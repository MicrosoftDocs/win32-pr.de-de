---
title: Erweiterte Stile des Register Steuer Elements (kommstrg. h)
description: Das Registerkarten-Steuerelement unterstützt jetzt erweiterte Stile. Diese Stile werden mithilfe der \_ Nachrichten TCM GetExtendedStyle und TCM- \_ textendedstyle manipuliert und sollten nicht mit erweiterten Fenster Stilen verwechselt werden, die an "kreatewindowex" übergeben werden.
ms.assetid: 24294037-598c-4fcd-8a7c-8647ccfb1d81
topic_type:
- apiref
api_name:
- TCS_EX_FLATSEPARATORS
- TCS_EX_REGISTERDROP
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c4e16b40a394bc9b808386d3cbdc3abf9b3d928
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360416"
---
# <a name="tab-control-extended-styles"></a><span data-ttu-id="8625f-104">Erweiterte Stile des Register Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="8625f-104">Tab Control Extended Styles</span></span>

<span data-ttu-id="8625f-105">Das Registerkarten-Steuerelement unterstützt jetzt erweiterte Stile.</span><span class="sxs-lookup"><span data-stu-id="8625f-105">The tab control now supports extended styles.</span></span> <span data-ttu-id="8625f-106">Diese Stile werden mithilfe der Nachrichten [**TCM \_ GetExtendedStyle**](tcm-getextendedstyle.md) und [**TCM- \_ textendedstyle**](tcm-setextendedstyle.md) manipuliert und sollten nicht mit erweiterten Fenster Stilen verwechselt werden, die an " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)" übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="8625f-106">These styles are manipulated using the [**TCM\_GETEXTENDEDSTYLE**](tcm-getextendedstyle.md) and [**TCM\_SETEXTENDEDSTYLE**](tcm-setextendedstyle.md) messages and should not be confused with extended window styles that are passed to [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).</span></span>



| <span data-ttu-id="8625f-107">Konstante</span><span class="sxs-lookup"><span data-stu-id="8625f-107">Constant</span></span>                                                                                                                                                                               | <span data-ttu-id="8625f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8625f-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TCS_EX_FLATSEPARATORS"></span><span id="tcs_ex_flatseparators"></span><dl> <span data-ttu-id="8625f-109"><dt>**TCS \_ Ex- \_ flatseparatoren**</dt></span><span class="sxs-lookup"><span data-stu-id="8625f-109"><dt>**TCS\_EX\_FLATSEPARATORS**</dt></span></span> </dl> | <span data-ttu-id="8625f-110">[Version 4,71](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="8625f-110">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="8625f-111">Das Registerkarten-Steuerelement zeichnet Trennzeichen zwischen den Registerkarten Elementen.</span><span class="sxs-lookup"><span data-stu-id="8625f-111">The tab control will draw separators between the tab items.</span></span> <span data-ttu-id="8625f-112">Dieser erweiterte Stil wirkt sich nur auf Registerkarten Steuerelemente aus, die über die [**TCS- \_ Schalt**](tab-control-styles.md) Flächen und die [**TCS- \_ FlatButtons**](tab-control-styles.md)</span><span class="sxs-lookup"><span data-stu-id="8625f-112">This extended style only affects tab controls that have the [**TCS\_BUTTONS**](tab-control-styles.md) and [**TCS\_FLATBUTTONS**](tab-control-styles.md) styles.</span></span> <span data-ttu-id="8625f-113">Standardmäßig wird durch das Erstellen des Registerkarten-Steuer Elements mit dem **TCS- \_ FlatButtons** -Stil dieser erweiterte Stil festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8625f-113">By default, creating the tab control with the **TCS\_FLATBUTTONS** style sets this extended style.</span></span> <span data-ttu-id="8625f-114">Wenn Sie keine Trennzeichen benötigen, sollten Sie diese erweiterte Formatvorlage nach dem Erstellen des Steuer Elements entfernen.</span><span class="sxs-lookup"><span data-stu-id="8625f-114">If you do not require separators, you should remove this extended style after creating the control.</span></span><br/> |
| <span id="TCS_EX_REGISTERDROP"></span><span id="tcs_ex_registerdrop"></span><dl> <span data-ttu-id="8625f-115"><dt>**TCS \_ Ex \_ registerdrop**</dt></span><span class="sxs-lookup"><span data-stu-id="8625f-115"><dt>**TCS\_EX\_REGISTERDROP**</dt></span></span> </dl>       | <span data-ttu-id="8625f-116">[Version 4,71](common-control-versions.md).</span><span class="sxs-lookup"><span data-stu-id="8625f-116">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="8625f-117">Das Registerkarten-Steuerelement generiert [TCN \_ GetObject](tcn-getobject.md) -Benachrichtigungs Codes, um ein Ablage Zielobjekt anzufordern, wenn ein Objekt über die Registerkarten Elemente im Steuerelement gezogen wird.</span><span class="sxs-lookup"><span data-stu-id="8625f-117">The tab control generates [TCN\_GETOBJECT](tcn-getobject.md) notification codes to request a drop target object when an object is dragged over the tab items in the control.</span></span> <span data-ttu-id="8625f-118">Die Anwendung muss vor dem Festlegen dieses Stils [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) oder [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) aufruft.</span><span class="sxs-lookup"><span data-stu-id="8625f-118">The application must call [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) or [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) before setting this style.</span></span> <br/>                                                                                                                                               |



## <a name="requirements"></a><span data-ttu-id="8625f-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8625f-119">Requirements</span></span>



| <span data-ttu-id="8625f-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8625f-120">Requirement</span></span> | <span data-ttu-id="8625f-121">Wert</span><span class="sxs-lookup"><span data-stu-id="8625f-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8625f-122">Header</span><span class="sxs-lookup"><span data-stu-id="8625f-122">Header</span></span><br/> | <dl> <span data-ttu-id="8625f-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="8625f-123"><dt>CommCtrl.h</dt></span></span> </dl> |



 

