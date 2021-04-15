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
# <a name="storage-interfaces"></a>Speicher Schnittstellen

Steuerungs Container müssen Steuerelemente unterstützen können, die [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)oder [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit)implementieren. Optional kann ein Container auch beliebige andere persistenzschnittstellen unterstützen, z. b. [**ipersistmemory**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)), [**IPersistPropertyBag**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768205(v=vs.85))und [**ipersistmoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)) für die Steuerelemente, die Unterstützung bieten.

Nachdem ein ActiveX-Steuerelement Container eine zu verwendende Speicherschnittstelle ausgewählt und initialisiert hat ([**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream), [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit)usw.), bleibt diese Speicherschnittstelle für die Lebensdauer des Steuer Elements die primäre Speicherschnittstelle, d. h., das Steuerelement bleibt im Besitz des Speichers. Dadurch wird verhindert, dass der Container in anderen Speicher Schnittstellen gespeichert wird.

ActiveX-Steuerelement Container müssen keinen Save as Text-Mechanismus unterstützen, sodass die Verwendung von [**IPersistPropertyBag**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768205(v=vs.85)) und der zugeordneten Container seitigen [**IPropertyBag**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)) -Schnittstelle optional ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Container](containers.md)
</dt> </dl>

 

 