---
description: Ein URI, der den Dienst Bezeichner darstellt.
ms.assetid: ef676f02-56a7-4b3a-9ca3-e7fa3c494ec7
title: Serviceid-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 305e97250b0b33d276dced4b5d454aec9298387c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351094"
---
# <a name="serviceid-element"></a>Serviceid-Element

Ein URI, der den Dienst Bezeichner darstellt.

## <a name="usage"></a>Verbrauch

``` syntax
<ServiceID/>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                          |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Host**](host.md)<br/>     | Definiert die **serviceid** -und [**types**](types.md) -Elemente für den Dienst Host. Wenn Sie nicht explizit bereitgestellt werden, stellt WSDAPI keine Standarddaten als Antwort auf Metadatenanforderungen bereit.<br/> <br/>                                                                                                                     |
| [**gehostet**](hosted.md)<br/> | Definiert die **serviceid** -und [**types**](types.md) -Elemente für die Dienste, die von diesem Dienst Host bereitgestellt werden. Jeder von diesem Dienst Host bereitgestellte Dienst sollte über eigene [**gehostete**](hosted.md) Element Informationen verfügen, um sicherzustellen, dass der Dienst in Antworten auf Metadatenanforderungen ordnungsgemäß veröffentlicht wird.<br/> <br/> |



## <a name="element-information"></a>Elementinformationen



|                                     |               |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




