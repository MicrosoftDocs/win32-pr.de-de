---
title: IPropertyBag und IPersistPropertyBag
description: IPropertyBag und IPersistPropertyBag
ms.assetid: 128e847b-99f9-44a3-9176-56eb34f3dddc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5a012fb2c202d93bcf4f4c8fa477133e841740b
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549065"
---
# <a name="ipropertybag-and-ipersistpropertybag"></a>IPropertyBag und IPersistPropertyBag

[**IPropertyBag**](/windows/win32/api/oaidl/nn-oaidl-ipropertybag) und [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag) optimieren die Save-as-Text-Mechanismen und werden daher für ActiveX Control-Container empfohlen, die einen Save-as-Text-Mechanismus implementieren. **IPropertyBag** wird von einem Container implementiert und entspricht in etwa [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream). **IPersistPropertyBag** wird von Steuerelementen implementiert und entspricht in etwa [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream).

 

 