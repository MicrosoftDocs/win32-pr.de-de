---
description: Ein URI, der den Dienstbezeichner darstellt.
ms.assetid: ef676f02-56a7-4b3a-9ca3-e7fa3c494ec7
title: ServiceID-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0dc6ac1da57109f4f5671caf16a49b3a6174e7bfb63335d5ba15a548d7135990
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756740"
---
# <a name="serviceid-element"></a>ServiceID-Element

Ein URI, der den Dienstbezeichner darstellt.

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
| [**Host**](host.md)<br/>     | Definiert die **ServiceID-** und [**Types-Elemente**](types.md) für den Diensthost. Wenn dies nicht explizit erfolgt, stellt WSDAPI keine Standarddaten als Reaktion auf Metadatenanforderungen bereit.<br/> <br/>                                                                                                                     |
| [**Gehostet**](hosted.md)<br/> | Definiert die **ServiceID-** und [**Types-Elemente**](types.md) für die dienste, die von diesem Diensthost bereitgestellt werden. Jeder von diesem Diensthost bereitgestellte [](hosted.md) Dienst sollte über eigene gehostete Elementinformationen verfügen, um sicherzustellen, dass der Dienst ordnungsgemäß in Antworten auf Metadatenanforderungen veröffentlicht wird.<br/> <br/> |



## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




