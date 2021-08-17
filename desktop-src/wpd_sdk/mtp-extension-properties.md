---
description: MTP-Erweiterungseigenschaften
ms.assetid: 58fc8741-261a-4e63-9fd3-8f0ca05866ad
title: MTP-Erweiterungseigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0468d249b469c4e768962ab6a920935e7a64b51d8e035af111e8274f7f0b9af6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118193946"
---
# <a name="mtp-extension-properties"></a>MTP-Erweiterungseigenschaften

Eigenschaften beschreiben Objekte, Eigenschaften, Ressourcen und Geräte.

## <a name="vendor-extended-object-properties"></a>Eigenschaften von vendor-extended-Objekten

Wenn ein Gerätehersteller eine vom Hersteller erweiterte Eigenschaft für ein Geräteobjekt erstellt, kombiniert er die **WPD \_ PROPERTIES \_ MTP \_ VENDOR EXTENDED \_ \_ OBJECT \_ PROPS** GUID mit dem Eigenschaftencode des Objekts, um eine **PROPERTYKEY-Struktur** zu erstellen.

Wenn der Eigenschaftencode des Objekts beispielsweise 0xD801 ist, würde **der resultierende PROPERTYKEY** wie im folgenden Beispiel gezeigt sein:


```C++
{4D545058-4FCE-4578-95C8-8698A9BC0F49}\D801
```



## <a name="vendor-extended-device-properties"></a>Eigenschaften von vom Hersteller erweiterten Geräten

Wenn ein Gerätehersteller eine vom Hersteller erweiterte Eigenschaft für ein Gerät erstellt, kombiniert er die **WPD \_ PROPERTIES \_ MTP \_ VENDOR EXTENDED \_ \_ DEVICE \_ PROPS** GUID mit dem Eigenschaftencode des Objekts, um eine **PROPERTYKEY-Struktur** zu erstellen.

Wenn der Eigenschaftencode des Objekts z. B. 0xD001 ist, würde die resultierende **PROPERTYKEY-Eigenschaft** wie im folgenden Beispiel gezeigt sein:


```C++
{4D545058-8900-40b3-8F1D-DC246E1E8370}\D001
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Unterstützen von MTP-Erweiterungen](supporting-mtp-extensions.md)
</dt> </dl>

 

 



