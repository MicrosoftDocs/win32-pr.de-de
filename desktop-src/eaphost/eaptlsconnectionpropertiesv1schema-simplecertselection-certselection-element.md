---
title: Simplecertselection (certselection)-Element
description: Erfahren Sie mehr über das simplecertselection (certselection)-Element. Dieses Element bestimmt, wie der Benutzer ein Zertifikat auswählt.
ms.assetid: 28454877-fd07-4b47-9544-f2b4e91c6651
keywords:
- Simplecertselection-Element EAPHost
topic_type:
- apiref
api_name:
- SimpleCertSelection
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 30af9872f7583232e91b037c5b8961e18c7ce863
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039619"
---
# <a name="simplecertselection-certselection-element"></a>Simplecertselection (certselection)-Element

Das **simplecertselection (certselection)** -Element bestimmt, wie der Benutzer ein Zertifikat auswählt.

``` syntax
<xs:element name="SimpleCertSelection"
    type="boolean"
 />
```

Das **simplecertselection** -Element wird durch den komplexen [**certselection**](eaptlsconnectionpropertiesv1schema-certselection-complextype.md) -Typ definiert.

## <a name="remarks"></a>Bemerkungen

**Simplecertselection** ist standardmäßig auf "true" fest. Wenn **simplecertselection** auf true festgelegt ist, führt EAP-TLS eine einfache Zertifikat Suche ohne Dropdown Listen für die Auswahl der Zertifikate durch. Wenn **simplecertselection** den Wert false hat, veranschaulicht EAP-TLS dem Benutzer das geeignete Zertifikat, das ausgewählt werden soll.

## <a name="requirements"></a>Anforderungen



| Role | Mindestens unterstütztes Betriebssystem |
|------|----------------------|
| Client<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Server<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Definitions Kontext des Elements im Schema**
</dt> <dt>

[**Certselection**](eaptlsconnectionpropertiesv1schema-certselection-complextype.md)
</dt> <dt>

**Mögliches unmittelbar übergeordnetes Element in der Schema Instanz**
</dt> <dt>

[**Certifikatestore ("kredentialssourceparameters")**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md)
</dt> <dt>


</dt> <dt>

[EAPHost und Legacy Schema](eaphost-schemas.md)
</dt> <dt>

[eaptlsconnectionpropertiesv1-Schema](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[eaptlsconnectionpropertiesv1-Schema Elemente](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





