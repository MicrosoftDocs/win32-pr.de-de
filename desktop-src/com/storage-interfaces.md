---
title: Speicherschnittstellen
description: Speicherschnittstellen
ms.assetid: bce0fd46-eeba-4a14-be1f-63d16885c28d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97ad0cc646d45ca0b77a70ecaf47d28eadb4d136
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549265"
---
# <a name="storage-interfaces"></a><span data-ttu-id="28165-103">Speicherschnittstellen</span><span class="sxs-lookup"><span data-stu-id="28165-103">Storage Interfaces</span></span>

<span data-ttu-id="28165-104">Steuerelementcontainer müssen Steuerelemente unterstützen können, die [**IPersistStorage,**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage) [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)oder [**IPersistStreamInit implementieren.**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit)</span><span class="sxs-lookup"><span data-stu-id="28165-104">Control containers must be able to support controls that implement [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream), or [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit).</span></span> <span data-ttu-id="28165-105">Optional kann ein Container alle anderen Persistenzschnittstellen wie [**IPersistMemory,**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)) [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag)und [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)) für die Steuerelemente unterstützen, die Unterstützung bieten.</span><span class="sxs-lookup"><span data-stu-id="28165-105">Optionally, a container can support any other persistence interfaces such as [**IPersistMemory**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)), [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag), and [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)) for those controls that provide support.</span></span>

<span data-ttu-id="28165-106">Nachdem ein ActiveX-Steuerelementcontainer eine zu verwendende Speicherschnittstelle ausgewählt und initialisiert hat [**(IPersistStorage,**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage) [**IPersistStream,**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit)usw.), bleibt diese Speicherschnittstelle die primäre Speicherschnittstelle für die Lebensdauer des Steuerelements, d. h. das Steuerelement verbleibt im Besitz des Speichers.</span><span class="sxs-lookup"><span data-stu-id="28165-106">Once an ActiveX control container has chosen and initialized a storage interface to use ([**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream), [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), etc), that storage interface will remain the primary storage interface for the lifetime of the control, i.e. the control will remain in possession of the storage.</span></span> <span data-ttu-id="28165-107">Dies schließt nicht aus, dass der Container in anderen Speicherschnittstellen gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="28165-107">This does not preclude the container from saving to other storage interfaces.</span></span>

<span data-ttu-id="28165-108">ActiveX-Steuerelementcontainer müssen keinen Mechanismus zum Speichern als Text unterstützen, daher sind die Verwendung von [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag) und der zugehörigen containerseitigen [**Schnittstelle IPropertyBag**](/windows/win32/api/oaidl/nn-oaidl-ipropertybag) optional.</span><span class="sxs-lookup"><span data-stu-id="28165-108">ActiveX control containers do not need to support a save as text mechanism, thus using [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag) and the associated container-side interface [**IPropertyBag**](/windows/win32/api/oaidl/nn-oaidl-ipropertybag) are optional.</span></span>

## <a name="related-topics"></a><span data-ttu-id="28165-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="28165-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28165-110">Container</span><span class="sxs-lookup"><span data-stu-id="28165-110">Containers</span></span>](containers.md)
</dt> </dl>

 

 