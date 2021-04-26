---
description: Ein URI, der den Dienstbezeichner darstellt.
ms.assetid: ef676f02-56a7-4b3a-9ca3-e7fa3c494ec7
title: ServiceID-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4c8b02fa8ecfa936aa658a1f18242e4f14eb0dd
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995107"
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
| [**Host**](host.md)<br/>     | Definiert die **Elemente ServiceID** und [**Types**](types.md) für den Diensthost. Wenn sie nicht explizit angegeben wird, stellt WSDAPI als Reaktion auf Metadatenanforderungen keine Standarddaten bereit.<br/> <br/>                                                                                                                     |
| [**Gehostet**](hosted.md)<br/> | Definiert die **Elemente ServiceID** und [**Types**](types.md) für die von diesem Diensthost bereitgestellten Dienste. Jeder von diesem Diensthost bereitgestellte Dienst sollte über eigene Informationen zu [**gehosteten**](hosted.md) Elementen verfügen, um sicherzustellen, dass der Dienst ordnungsgemäß als Antwort auf Metadatenanforderungen veröffentlicht wird.<br/> <br/> |



## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




