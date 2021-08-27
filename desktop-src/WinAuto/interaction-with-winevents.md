---
title: Interaktion mit WinEvents
description: Die Dynamische Anmerkungs-Laufzeit sendet keine WinEvents. Es liegt in der Verantwortung des Anmerkungserzählers, bei Bedarf geeignete Ereignisse zu senden. Wenn Sie WinEvents senden müssen, stellen Sie sicher, dass Sie sie senden, nachdem die Anmerkung erfolgt ist.
ms.assetid: 657a540b-8838-4d2e-ade6-c4fa1ad08e21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df1789a152ab37161e1f217639e4ad40d597b0689529da3a5f65bf669b986e14
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098460"
---
# <a name="interaction-with-winevents"></a>Interaktion mit WinEvents

Die Laufzeit der dynamischen Anmerkung sendet [keine WinEvents.](winevents-infrastructure.md) Es liegt in der Verantwortung des Anmerkungserzählers, bei Bedarf geeignete Ereignisse zu senden. Wenn Sie WinEvents senden müssen, stellen Sie sicher, dass Sie sie senden, nachdem die Anmerkung erfolgt ist.

Wenn Sie beispielsweise [**IAccPropServices::SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) zum Festlegen der [**Name-Eigenschaft**](name-property.md) eines Elements verwenden, senden Sie ein [**EVENT OBJECT \_ \_ NAMECHANGE-Ereignis**](event-constants.md) für dieses Objekt, nachdem **SetPropValue** zurückgegeben wurde.

Wenn Sie jedoch [**IAccPropServices::SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) zum Festlegen der ValueMap für einen Schieberegler verwenden, sind keine Ereignisse erforderlich, da das Festlegen der ValueMap den Wert des Schiebereglers nicht ändert.

 

 




