---
title: Storage Schnittstellen
description: Storage Schnittstellen
ms.assetid: bce0fd46-eeba-4a14-be1f-63d16885c28d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81c378b37c020f15e0fe497249b2834faffefc232bc184564f80fdb247550033
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129702"
---
# <a name="storage-interfaces"></a>Storage Schnittstellen

Steuerelementcontainer müssen Steuerelemente unterstützen können, die [**IPersistStorage,**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage) [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)oder [**IPersistStreamInit implementieren.**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit) Optional kann ein Container alle anderen Persistenzschnittstellen wie [**IPersistMemory,**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)) [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag)und [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)) für die Steuerelemente unterstützen, die Unterstützung bieten.

Nachdem ein ActiveX-Steuerelementcontainer eine zu verwendende Speicherschnittstelle ausgewählt und initialisiert hat [**(IPersistStorage,**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage) [**IPersistStream,**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit)usw.), bleibt diese Speicherschnittstelle die primäre Speicherschnittstelle für die Lebensdauer des Steuerelements, d. h. das Steuerelement verbleibt im Besitz des Speichers. Dies schließt nicht aus, dass der Container in anderen Speicherschnittstellen gespeichert wird.

ActiveX-Steuerelementcontainer müssen keinen Save-as-Text-Mechanismus unterstützen, daher sind die Verwendung von [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag) und der zugehörigen containerseitigen [**Schnittstelle IPropertyBag**](/windows/win32/api/oaidl/nn-oaidl-ipropertybag) optional.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Container](containers.md)
</dt> </dl>

 

 