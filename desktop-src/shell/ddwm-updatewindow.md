---
description: Weist ein Fenster zum Löschen von Bildern an, das mithilfe neuer dropdescription-Informationen aktualisiert werden soll.
title: DDWM_UPDATEWINDOW Meldung
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3b74f2e1-8121-4b7c-8d7a-b449cda529da
api_name:
- DDWM_UPDATEWINDOW
api_type:
- NA
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2bff0e007c735fcf202aaf16cf304eb4ff5358f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977312"
---
# <a name="ddwm_updatewindow-message"></a><span data-ttu-id="a5624-103">Ddwm- \_ UpdateWindow-Meldung</span><span class="sxs-lookup"><span data-stu-id="a5624-103">DDWM\_UPDATEWINDOW message</span></span>

<span data-ttu-id="a5624-104">Weist ein Fenster zum Löschen von Bildern an, das mithilfe neuer [**dropdescription**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription) -Informationen aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a5624-104">Instructs a drop image window to update using new [**DROPDESCRIPTION**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription) information.</span></span>

## <a name="parameters"></a><span data-ttu-id="a5624-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5624-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5624-106">*wParam* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a5624-106">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5624-107">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="a5624-107">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="a5624-108">*LPARAM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a5624-108">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5624-109">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="a5624-109">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a5624-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a5624-110">Remarks</span></span>

<span data-ttu-id="a5624-111">Ddwm \_ UpdateWindow ist als WM- \_ Benutzer + 3 definiert.</span><span class="sxs-lookup"><span data-stu-id="a5624-111">DDWM\_UPDATEWINDOW is defined as WM\_USER+3.</span></span>

<span data-ttu-id="a5624-112">Wenn sich der Zustand eines Drop-Vorgangs ändert – z. b. als Reaktion auf einen modifiziererschlüssel – gibt [**IDropTarget::D ragover**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) einen neuen [**DropEffect**](../com/dropeffect-constants.md) -Wert zurück (dieser **DropEffect** -Wert kann auch über [**IDropSource:: GiveFeedback**](/windows/win32/api/oleidl/nf-oleidl-idropsource-givefeedback)empfangen werden).</span><span class="sxs-lookup"><span data-stu-id="a5624-112">When the state of a drop operation changes—such as in response to a modifier key—[**IDropTarget::DragOver**](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) returns a new [**DROPEFFECT**](../com/dropeffect-constants.md) value (this **DROPEFFECT** value can also be received through [**IDropSource::GiveFeedback**](/windows/win32/api/oleidl/nf-oleidl-idropsource-givefeedback)).</span></span> <span data-ttu-id="a5624-113">In der Antwort aktualisiert die Anwendung die [**dropdescription**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription) -Struktur des Ablage Ziels mit einem neuen [**dropimagetype**](/windows/desktop/api/shlobj_core/ne-shlobj_core-dropimagetype) -Wert, der die Dekoration angibt, die auf die Visualisierung des Zieh Fensters angewendet werden soll. beispielsweise ein Hinweis darauf, dass die Datei kopiert wird, anstatt verschoben zu werden, oder dass das Objekt an diesem Speicherort nicht gelöscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="a5624-113">In response, the application updates the drop target's [**DROPDESCRIPTION**](/windows/desktop/api/shlobj_core/ns-shlobj_core-dropdescription) structure with a new [**DROPIMAGETYPE**](/windows/desktop/api/shlobj_core/ne-shlobj_core-dropimagetype) value that indicates the decoration to be applied to the drag window's visual; for instance, an indication that the file is being copied rather than moved or that the object cannot be dropped to that location.</span></span> <span data-ttu-id="a5624-114">Die visuellen Elemente werden jedoch erst aktualisiert, wenn das Objekt eine **ddwm \_ UpdateWindow** -Meldung empfängt.</span><span class="sxs-lookup"><span data-stu-id="a5624-114">However, the visuals are not updated until the object receives a **DDWM\_UPDATEWINDOW** message.</span></span>

<span data-ttu-id="a5624-115">Das [dragwindow](clipboard.md) -Zwischenablage Format gibt das **HWND** des Empfänger Zieh Fensters an den Absender der **ddwm \_ UpdateWindow** -Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="a5624-115">The [DragWindow](clipboard.md) clipboard format provides the **HWND** of the recipient drag window to the sender of the **DDWM\_UPDATEWINDOW** message.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5624-116">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="a5624-116">Requirements</span></span>



| <span data-ttu-id="a5624-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a5624-117">Requirement</span></span> | <span data-ttu-id="a5624-118">Wert</span><span class="sxs-lookup"><span data-stu-id="a5624-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a5624-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a5624-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a5624-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a5624-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a5624-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a5624-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a5624-122">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a5624-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 
