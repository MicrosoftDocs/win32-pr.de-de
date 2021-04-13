---
title: Tastatur Behandlung für Steuerelemente
description: Ein-Steuerelement reagiert auf Tastaturbeschleuniger, sodass der Endbenutzer Aktionen initiieren kann, die vom Steuerelement ausgeführt werden.
ms.assetid: 59aca5cb-f109-49ee-897d-43610501f7f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbe03058fdb0192a0f8f7b13032612288045775b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311400"
---
# <a name="keyboard-handling-for-controls"></a><span data-ttu-id="cac3c-103">Tastatur Behandlung für Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="cac3c-103">Keyboard Handling for Controls</span></span>

<span data-ttu-id="cac3c-104">Ein-Steuerelement reagiert auf Tastaturbeschleuniger, sodass der Endbenutzer Aktionen initiieren kann, die vom Steuerelement ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="cac3c-104">A control responds to keyboard accelerators so the end-user can initiate actions performed by the control.</span></span> <span data-ttu-id="cac3c-105">Der Container verwaltet die Tastatur Aktivität für alle eingebetteten Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="cac3c-105">The container manages keyboard activity for all its embedded controls.</span></span> <span data-ttu-id="cac3c-106">Mit Verbund Dokumenten gelten die Tastaturbeschleuniger nur für das derzeit aktive Objekt.</span><span class="sxs-lookup"><span data-stu-id="cac3c-106">With compound documents, keyboard accelerators apply only to the currently active object.</span></span> <span data-ttu-id="cac3c-107">Mit-Steuerelementen wurde ein Mechanismus hinzugefügt, sodass ein Steuerelement auf seine Tastatur-mnetmonics reagieren kann, auch wenn es zurzeit nicht auf der Benutzeroberfläche aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="cac3c-107">With controls, a mechanism has been added so that a control can respond to its keyboard mnemonics even if it is not currently UI-active.</span></span>

<span data-ttu-id="cac3c-108">Die [**IOleControl:: GetControlInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo) -und [**IOleControl:: onmnetmonic**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic) -Methoden und die [**iolecontrolsite:: oncontrolinfochanged**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-oncontrolinfochanged) -Methode behandeln die Tastatur-mnetmonics eines Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="cac3c-108">The [**IOleControl::GetControlInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo) and [**IOleControl::OnMnemonic**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic) methods and the [**IOleControlSite::OnControlInfoChanged**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-oncontrolinfochanged) method handle a control's keyboard mnemonics.</span></span> <span data-ttu-id="cac3c-109">Eine [**controlInfo**](/windows/win32/api/ocidl/ns-ocidl-controlinfo) -Struktur beschreibt die mnetmonischen Accelerators eines Steuer Elements, und die zurückgegebenen Flags über die **GetControlInfo** -Methode beschreiben das Verhalten der Steuerelemente mit der EINGABETASTE und der ESC-Taste.</span><span class="sxs-lookup"><span data-stu-id="cac3c-109">A [**CONTROLINFO**](/windows/win32/api/ocidl/ns-ocidl-controlinfo) structure describes a control's mnemonic accelerators, and the flags passed back with it through the **GetControlInfo** method describe the controls behavior with the Enter and Esc keys.</span></span> <span data-ttu-id="cac3c-110">Wenn ein Steuerelement seine mnetmonics ändert, ruft es **oncontrolinfochanged** auf, damit der Container die Struktur bei Bedarf erneut laden kann.</span><span class="sxs-lookup"><span data-stu-id="cac3c-110">When a control changes its mnemonics, it calls **OnControlInfoChanged** so the container can reload the structure if necessary.</span></span>

<span data-ttu-id="cac3c-111">Wenn ein Steuerelement aktiv ist, ist es auch das Steuerelement mit dem Fokus.</span><span class="sxs-lookup"><span data-stu-id="cac3c-111">When a control is UI active, it is also the control with the focus.</span></span> <span data-ttu-id="cac3c-112">Beim Aktivieren und Deaktivieren von Steuerelementen zwischen den direkten aktiven und den aktiven UI-Zuständen Ruft das Steuerelement [**iolecontrolsite:: onfocus**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-onfocus) auf, um den Container über solche Änderungen zu informieren.</span><span class="sxs-lookup"><span data-stu-id="cac3c-112">As controls are activated and deactivated between the in-place active and the UI active states, the control calls [**IOleControlSite::OnFocus**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-onfocus) to tell the container of such changes.</span></span>

<span data-ttu-id="cac3c-113">Wenn ein Steuerelement aktiv ist, hat es außerdem die Möglichkeit, beliebige Tastatureingaben zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="cac3c-113">In addition, when a control is UI active, it will have first chance to process any keystrokes.</span></span> <span data-ttu-id="cac3c-114">Um einem Container die Möglichkeit zu geben, die Tastatureingabe vor dem Steuerelement zu verarbeiten, ruft das Steuerelement [**iolecontrolsite:: TranslateAccelerator**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-translateaccelerator)auf.</span><span class="sxs-lookup"><span data-stu-id="cac3c-114">To give a container the opportunity to process the keystroke before the control, the control calls [**IOleControlSite::TranslateAccelerator**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-translateaccelerator).</span></span> <span data-ttu-id="cac3c-115">Wenn der Container die Tastatureingabe nicht behandelt, wird er vom-Steuerelement verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="cac3c-115">If the container does not handle the keystroke, the control then processes it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cac3c-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cac3c-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cac3c-117">ActiveX-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="cac3c-117">ActiveX Controls</span></span>](activex-controls.md)
</dt> </dl>

 

 




