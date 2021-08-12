---
description: Die IWiaPropertyStorage-Schnittstelle stellt Methoden zum Lesen und Schreiben von WIA-Eigenschaften (Windows Image Acquisition) bereit. Zu den Elementeigenschaften gehören Gerätebefehle, Informationen zum Elementformat und Geräteinformationen.
ms.assetid: 268d2298-bc9c-479b-b078-a8180cd38bc3
title: Lesen und Festlegen von WIA-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 607e319723023a00c4159687c3dff13fedab8275a0522fdb2254b36b8e62edb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118439874"
---
# <a name="reading-and-setting-wia-properties"></a>Lesen und Festlegen von WIA-Eigenschaften

Die [**IWiaPropertyStorage-Schnittstelle**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) stellt Methoden zum Lesen und Schreiben der Eigenschaften eines WIA-Elements (Windows Image Acquisition) bereit. Zu den Elementeigenschaften gehören Gerätebefehle, Informationen zum Elementformat und Geräteinformationen.

Eine Anwendung kann einen Zeiger auf eine [**IWiaPropertyStorage-Schnittstelle**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) eines Elements abrufen, indem sie entweder die Geräteinformationen oder Ereignisinformationen des Elements aufzählt, indem sie [**IWiaItem::EnumDeviceCapabilities**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumdevicecapabilities) oder [**IWiaItem::EnumRegisterEventInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumregistereventinfo) aufruft oder die [**IWiaItem-Schnittstelle**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) des Elements abfragt. (Rufen Sie in WIA 2.0 [**IWiaItem2::EnumDeviceCapabilities**](-wia-iwiaitem2-enumdevicecapabilities.md) oder [**IWiaItem2::EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) auf, oder fragen Sie die [**IWiaItem2-Schnittstelle**](-wia-iwiaitem2.md) des Elements ab.)

[**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) erbt von [IPropertyStorage,](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) und die geerbten Methoden werden wie im Referenzabschnitt von Structured Storage im Windows Software Development Kit (SDK) beschrieben implementiert.

> [!Note]
>
> WIA-Anwendungen sollten immer Bilddatenheader lesen, um genaue Bildinformationen zu erhalten. Der WIA-Treiber kann die WIA-Eigenschaften und Imagedatenheader während der Datenübertragung ändern.
>
> Wenn kein Bilddatenheader mit dem angegebenen Format bereitgestellt wird, sollte die WIA-Anwendung die WIA-Eigenschaften als Informationsquelle für die Datenübertragung verwenden. Die WIA-Anwendung sollte die erforderlichen WIA-Eigenschaften nach Abschluss der Überprüfung oder Erfassung erneut durchlesen, um die aktualisierten Einstellungen zu erhalten.

 

In den folgenden Abschnitten werden die verschiedenen WIA-Eigenschaften beschrieben:

-   [WIA-Eigenschaftenüberprüfung](-wia-wia-property-validation.md)
-   [Geräteinformationseigenschaften](-wia-device-information-properties-wia-dip-xxxx.md)
-   [Geräteeigenschaften](-wia-device-properties.md)
-   [Elementeigenschaften](-wia-item-properties.md)
-   [Zusätzliche WIA-Eigenschaften](-wia-additional-wia-properties.md)
-   [Definieren benutzerdefinierter Eigenschaften](-wia-defining-custom-properties.md)
-   [Verwenden benutzerdefinierter Eigenschaften](-wia-using-custom-properties.md)
-   [Scan Profile Schema](-wia-scan-profile-schema.md)

 

 
