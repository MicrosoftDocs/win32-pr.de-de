---
title: IPropertyBag und IPersistPropertyBag
description: IPropertyBag und IPersistPropertyBag
ms.assetid: 128e847b-99f9-44a3-9176-56eb34f3dddc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de08d8af50ae9a0b91166a4f41c8a11d8c6eb69c4ffd77f93b2566c901342ac0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048088"
---
# <a name="ipropertybag-and-ipersistpropertybag"></a>IPropertyBag und IPersistPropertyBag

[**IPropertyBag**](/windows/win32/api/oaidl/nn-oaidl-ipropertybag) und [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag) optimieren die Save-as-Text-Mechanismen und werden daher für ActiveX Control-Container empfohlen, die einen Save-as-Text-Mechanismus implementieren. **IPropertyBag** wird von einem Container implementiert und entspricht in etwa [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream). **IPersistPropertyBag** wird von Steuerelementen implementiert und entspricht in etwa [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream).

 

 