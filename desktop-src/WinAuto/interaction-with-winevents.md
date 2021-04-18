---
title: Interaktion mit WinEvents
description: Die Lauf Zeit der dynamischen Anmerkung sendet keine WinEvents. Es liegt in der Verantwortung des Annotator, bei Bedarf geeignete Ereignisse zu senden. Wenn Sie WinEvents senden müssen, stellen Sie sicher, dass diese nach der Anmerkung gesendet werden.
ms.assetid: 657a540b-8838-4d2e-ade6-c4fa1ad08e21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2aedd09a22371f91a92eca891c77f6c424583b5
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "106339256"
---
# <a name="interaction-with-winevents"></a>Interaktion mit WinEvents

Die Lauf Zeit der dynamischen Anmerkung sendet keine [WinEvents](winevents-infrastructure.md). Es liegt in der Verantwortung des Annotator, bei Bedarf geeignete Ereignisse zu senden. Wenn Sie WinEvents senden müssen, stellen Sie sicher, dass diese nach der Anmerkung gesendet werden.

Wenn Sie z. b. [**IAccPropServices:: SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) verwenden, um die [**Name**](name-property.md) -Eigenschaft eines Elements festzulegen, senden Sie ein [**Ereignis \_ Objekt \_ NameChange**](event-constants.md) -Ereignis für dieses Objekt, nachdem **SetPropValue** zurückgegeben wurde.

Wenn Sie jedoch [**IAccPropServices:: SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) verwenden, um die ValueMap für einen Schieberegler festzulegen, sind keine Ereignisse erforderlich, da durch das Festlegen von ValueMap der Wert des Schiebereglers nicht geändert wird.

 

 




