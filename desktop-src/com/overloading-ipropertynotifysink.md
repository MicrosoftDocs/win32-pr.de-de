---
title: Überladen von IPropertyNotifySink
description: Überladen von IPropertyNotifySink
ms.assetid: c6d52da0-7b7e-4ca8-b903-310bf988d2f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4faca0027144498138e1a60bf3df9a29b618aeb7eb09198ff97a3dd7616be67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118310023"
---
# <a name="overloading-ipropertynotifysink"></a>Überladen von IPropertyNotifySink

Viele ActiveX-Steuerelementcontainer implementieren ein fensterloses Durchsuchen von Eigenschaften. Wenn die Eigenschaften eines Steuerelements über die Eigenschaftenseiten des Steuerelements geändert werden, können die Eigenschaften des Steuerelements nicht mehr mit der Containeransicht dieser Eigenschaften synchronisiert werden (das Steuerelement ist natürlich immer richtig). Um sicherzustellen, dass er immer über die aktuellen Werte für die Eigenschaften eines Steuerelements verfügt, kann ein ActiveX-Steuerelementcontainer die [**IPropertyNotifySink-Schnittstelle**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) (Datenbindung) überladen und sie auch verwenden, um benachrichtigt zu werden, dass sich eine Steuerelementeigenschaft geändert hat. Diese Technik ist optional und nicht erforderlich, um ActiveX- oder ActiveX zu steuern.

Beachten Sie, dass ein Steuerelement [**OnRequestEdit nur für die**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit) Datenbindung verwenden sollte. Es ist kostenlos, [**OnChanged für**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onchanged) einen oder beide Zwecke zu verwenden.

 

 




