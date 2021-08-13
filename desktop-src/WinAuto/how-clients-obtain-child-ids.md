---
title: Abrufen untergeordneter IDs durch Clients
description: Abrufen untergeordneter IDs durch Clients
ms.assetid: 8e5786fe-5123-4262-b0b8-5c9aff4787bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78a12dc3f40c2aaa776c1fa8e61713c52ffbdcde554c9f6a1cbca7093998780c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119388600"
---
# <a name="how-clients-obtain-child-ids"></a>Abrufen untergeordneter IDs durch Clients

Cliententwickler können die untergeordnete ID eines Objekts wie folgt abrufen:

-   Rufen Sie [**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren)auf. Diese Funktion ruft ein Array von [**VARIANT-Strukturen**](variant-structure.md) ab.
-   Fragen Sie das -Objekt ab, um festzustellen, ob es die [**IEnumVARIANT-Schnittstelle**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant) unterstützt. Falls vorhanden, verwenden Sie [**IEnumVARIANT::Next**](/previous-versions/windows/desktop/api/oaidl/nf-oaidl-ienumvariant-next) zum Abrufen untergeordneter IDs.
-   Sammeln Sie die untergeordneten IDs, indem Sie die [**IAccessible::accNavigate-Methode**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) des übergeordneten Objekts aufrufen.

> [!Note]  
> Es liegt in der Verantwortung des Clients, den für die [**VARIANT-Strukturen**](variant-structure.md) verwendeten Arbeitsspeicher freizugeben. Clients müssen auch [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) für jede [**zurückgegebene IDispatch-Schnittstelle**](idispatch-interface.md) aufrufen.

 

 

 