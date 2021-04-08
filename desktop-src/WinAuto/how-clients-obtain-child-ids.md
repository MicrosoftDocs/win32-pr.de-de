---
title: Abrufen von untergeordneten IDs durch Clients
description: Abrufen von untergeordneten IDs durch Clients
ms.assetid: 8e5786fe-5123-4262-b0b8-5c9aff4787bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18a67322a80a00c7cc65463ef50e5d1b470fc0b0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727721"
---
# <a name="how-clients-obtain-child-ids"></a>Abrufen von untergeordneten IDs durch Clients

Client Entwickler können die untergeordnete ID eines Objekts auf folgende Weise erhalten:

-   " [**Accessiblechildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren)" aufzurufen. Diese Funktion Ruft ein Array von [**Variant**](variant-structure.md) -Strukturen ab.
-   Fragen Sie das-Objekt ab, um festzustellen, ob es die [**IEnumVARIANT**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant) -Schnittstelle Wenn Sie vorhanden ist, verwenden Sie [**IEnumVARIANT:: Next**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-ienumvariant-next) Abruf untergeordneter IDs.
-   Erfassen Sie die untergeordneten IDs, indem Sie die [**IAccessible:: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) -Methode des übergeordneten Objekts aufrufen.

> [!Note]  
> Der Client ist dafür verantwortlich, den für die [**Variant**](variant-structure.md) -Strukturen genutzten Arbeitsspeicher freizugeben. Clients müssen auch [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) für jede zurückgegebene [**IDispatch**](idispatch-interface.md) -Schnittstelle abrufen.

 

 

 