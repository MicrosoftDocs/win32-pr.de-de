---
title: Speicher Schnittstellen
description: Speicher Schnittstellen
ms.assetid: bce0fd46-eeba-4a14-be1f-63d16885c28d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab06d8d0920ca7b29619df2173aaa0897c6eef6e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104517150"
---
# <a name="storage-interfaces"></a><span data-ttu-id="e72d1-103">Speicher Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="e72d1-103">Storage Interfaces</span></span>

<span data-ttu-id="e72d1-104">Steuerungs Container müssen Steuerelemente unterstützen können, die [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)oder [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit)implementieren.</span><span class="sxs-lookup"><span data-stu-id="e72d1-104">Control containers must be able to support controls that implement [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream), or [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit).</span></span> <span data-ttu-id="e72d1-105">Optional kann ein Container auch beliebige andere persistenzschnittstellen unterstützen, z. b. [**ipersistmemory**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)), [**IPersistPropertyBag**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768205(v=vs.85))und [**ipersistmoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)) für die Steuerelemente, die Unterstützung bieten.</span><span class="sxs-lookup"><span data-stu-id="e72d1-105">Optionally, a container can support any other persistence interfaces such as [**IPersistMemory**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)), [**IPersistPropertyBag**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768205(v=vs.85)), and [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)) for those controls that provide support.</span></span>

<span data-ttu-id="e72d1-106">Nachdem ein ActiveX-Steuerelement Container eine zu verwendende Speicherschnittstelle ausgewählt und initialisiert hat ([**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream), [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit)usw.), bleibt diese Speicherschnittstelle für die Lebensdauer des Steuer Elements die primäre Speicherschnittstelle, d. h., das Steuerelement bleibt im Besitz des Speichers.</span><span class="sxs-lookup"><span data-stu-id="e72d1-106">Once an ActiveX control container has chosen and initialized a storage interface to use ([**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream), [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), etc), that storage interface will remain the primary storage interface for the lifetime of the control, i.e. the control will remain in possession of the storage.</span></span> <span data-ttu-id="e72d1-107">Dadurch wird verhindert, dass der Container in anderen Speicher Schnittstellen gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="e72d1-107">This does not preclude the container from saving to other storage interfaces.</span></span>

<span data-ttu-id="e72d1-108">ActiveX-Steuerelement Container müssen keinen Save as Text-Mechanismus unterstützen, sodass die Verwendung von [**IPersistPropertyBag**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768205(v=vs.85)) und der zugeordneten Container seitigen [**IPropertyBag**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)) -Schnittstelle optional ist.</span><span class="sxs-lookup"><span data-stu-id="e72d1-108">ActiveX control containers do not need to support a save as text mechanism, thus using [**IPersistPropertyBag**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768205(v=vs.85)) and the associated container-side interface [**IPropertyBag**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)) are optional.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e72d1-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e72d1-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e72d1-110">Container</span><span class="sxs-lookup"><span data-stu-id="e72d1-110">Containers</span></span>](containers.md)
</dt> </dl>

 

 