---
title: Überladen von IPropertyNotifySink
description: Überladen von IPropertyNotifySink
ms.assetid: c6d52da0-7b7e-4ca8-b903-310bf988d2f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 037b27650ae68f355962454ae154d7c332c73518
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388640"
---
# <a name="overloading-ipropertynotifysink"></a>Überladen von IPropertyNotifySink

Viele ActiveX-Steuerelement Container implementieren ein nicht modalem Eigenschaften Browserfenster. Wenn die Eigenschaften eines Steuer Elements über die Eigenschaften Seiten des-Steuer Elements geändert werden, können die Eigenschaften des Steuer Elements nicht mehr mit der Ansicht des Containers synchronisiert werden (das Steuerelement ist natürlich immer richtig). Um sicherzustellen, dass Sie immer über die aktuellen Werte für die Eigenschaften eines Steuer Elements verfügt, kann ein ActiveX-Steuerelement Container die [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) -Schnittstelle (Datenbindung) überladen und damit darüber benachrichtigt werden, dass sich eine Steuerelement Eigenschaft geändert hat. Diese Technik ist optional und nicht erforderlich für ActiveX-Steuerelement Container oder ActiveX-Steuerelemente.

Beachten Sie, dass ein Steuerelement [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit) nur für die Datenbindung verwenden soll. Es ist kostenlos, [**OnChanged**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onchanged) für beide Zwecke zu verwenden.

 

 




