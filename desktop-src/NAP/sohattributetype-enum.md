---
title: Sohattributetype-Enumeration (napprotocol. h)
description: Gibt den Typ des Attributs an, das im TLV-Objekt (Attribute Type-Length-Value) gespeichert ist.
ms.assetid: ba725bf1-1d0a-4489-b912-3e761557d772
keywords:
- Sohattributetype-Enumeration NAP
topic_type:
- apiref
api_name:
- SoHAttributeType
api_location:
- NapProtocol.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db164bbedf2267aaa5941a21a56ccfd53e1e1646
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340988"
---
# <a name="sohattributetype-enumeration"></a>Sohattributetype-Enumeration

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **sohattributetype** -Enumeration gibt den Typ des Attributs an, das im TLV-Objekt (Attribut Type-Length-Value) gespeichert ist.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagSoHAttributeType { 
  sohAttributeTypeSystemHealthId          = 2,
  sohAttributeTypeIpv4FixupServers        = 3,
  sohAttributeTypeComplianceResultCodes   = 4,
  sohAttributeTypeTimeOfLastUpdate        = 5,
  sohAttributeTypeClientId                = 6,
  sohAttributeTypeVendorSpecific          = 7,
  sohAttributeTypeHealthClass             = 8,
  sohAttributeTypeSoftwareVersion         = 9,
  sohAttributeTypeProductName             = 10,
  sohAttributeTypeHealthClassStatus       = 11,
  sohAttributeTypeSoHGenerationTime       = 12,
  sohAttributeTypeErrorCodes              = 13,
  sohAttributeTypeFailureCategory         = 14,
  sohAttributeTypeIpv6FixupServers        = 15,
  sohAttributeTypeExtendedIsolationState  = 16
} SoHAttributeType;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="sohAttributeTypeSystemHealthId"></span><span id="sohattributetypesystemhealthid"></span><span id="SOHATTRIBUTETYPESYSTEMHEALTHID"></span>**sohattributetypesystemhealthid**
</dt> <dd>

Gibt den Typ der Systemintegritäts-ID an.

</dd> <dt>

<span id="sohAttributeTypeIpv4FixupServers"></span><span id="sohattributetypeipv4fixupservers"></span><span id="SOHATTRIBUTETYPEIPV4FIXUPSERVERS"></span>**sohAttributeTypeIpv4FixupServers**
</dt> <dd>

Gibt den Typ des IPv4-fixupserverattributs an.

</dd> <dt>

<span id="sohAttributeTypeComplianceResultCodes"></span><span id="sohattributetypecomplianceresultcodes"></span><span id="SOHATTRIBUTETYPECOMPLIANCERESULTCODES"></span>**sohattributetypecomplianceresultcodes**
</dt> <dd>

Gibt den Attributtyp des Konformitäts Ergebnis Codes an.

</dd> <dt>

<span id="sohAttributeTypeTimeOfLastUpdate"></span><span id="sohattributetypetimeoflastupdate"></span><span id="SOHATTRIBUTETYPETIMEOFLASTUPDATE"></span>**sohattributetypetimeoflatstupdate**
</dt> <dd>

Gibt die Uhrzeit des letzten Update Attribut Typs an.

</dd> <dt>

<span id="sohAttributeTypeClientId"></span><span id="sohattributetypeclientid"></span><span id="SOHATTRIBUTETYPECLIENTID"></span>**sohattributetypeclientid**
</dt> <dd>

Gibt den Typ der Client-ID-Attribute an.

</dd> <dt>

<span id="sohAttributeTypeVendorSpecific"></span><span id="sohattributetypevendorspecific"></span><span id="SOHATTRIBUTETYPEVENDORSPECIFIC"></span>**sohattributetypevendorspecific**
</dt> <dd>

Gibt den herstellerspezifischen Attributtyp an.

</dd> <dt>

<span id="sohAttributeTypeHealthClass"></span><span id="sohattributetypehealthclass"></span><span id="SOHATTRIBUTETYPEHEALTHCLASS"></span>**sohattributetypehealthclass**
</dt> <dd>

Gibt den Typ der Integritäts Klassenattribute an.

</dd> <dt>

<span id="sohAttributeTypeSoftwareVersion"></span><span id="sohattributetypesoftwareversion"></span><span id="SOHATTRIBUTETYPESOFTWAREVERSION"></span>**sohattributetypesoftwareversion**
</dt> <dd>

Gibt den Typ der Software Versions Attribute an.

</dd> <dt>

<span id="sohAttributeTypeProductName"></span><span id="sohattributetypeproductname"></span><span id="SOHATTRIBUTETYPEPRODUCTNAME"></span>**sohattributetypeproductname**
</dt> <dd>

Gibt den Attributtyp des Produkt namens an.

</dd> <dt>

<span id="sohAttributeTypeHealthClassStatus"></span><span id="sohattributetypehealthclassstatus"></span><span id="SOHATTRIBUTETYPEHEALTHCLASSSTATUS"></span>**sohattributetypehealthclassstatus**
</dt> <dd>

Gibt den Attributtyp der Integritäts Klassen Status an.

</dd> <dt>

<span id="sohAttributeTypeSoHGenerationTime"></span><span id="sohattributetypesohgenerationtime"></span><span id="SOHATTRIBUTETYPESOHGENERATIONTIME"></span>**sohattributetypesohgenerationtime**
</dt> <dd>

Gibt die Generierungs Zeit des Statement of Health-Attribut Typs an.

</dd> <dt>

<span id="sohAttributeTypeErrorCodes"></span><span id="sohattributetypeerrorcodes"></span><span id="SOHATTRIBUTETYPEERRORCODES"></span>**sohattributetypeerrorcodes**
</dt> <dd>

Gibt den Typ des Fehlercode Attributs an.

</dd> <dt>

<span id="sohAttributeTypeFailureCategory"></span><span id="sohattributetypefailurecategory"></span><span id="SOHATTRIBUTETYPEFAILURECATEGORY"></span>**sohattributetypefailurecategory**
</dt> <dd>

Gibt den Attributtyp der Fehler Kategorie an.

</dd> <dt>

<span id="sohAttributeTypeIpv6FixupServers"></span><span id="sohattributetypeipv6fixupservers"></span><span id="SOHATTRIBUTETYPEIPV6FIXUPSERVERS"></span>**sohAttributeTypeIpv6FixupServers**
</dt> <dd>

Gibt den Typ des IPv6-fixupserverattributs an.

</dd> <dt>

<span id="sohAttributeTypeExtendedIsolationState"></span><span id="sohattributetypeextendedisolationstate"></span><span id="SOHATTRIBUTETYPEEXTENDEDISOLATIONSTATE"></span>**sohattributetypeextendedisolationstate**
</dt> <dd>

Gibt den Typ des erweiterten Isolations Zustands Attributs an.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die [**sohattributevalue**](sohattributevalue-union.md) -Struktur definiert die Attributwerte, die den einzelnen Attributtypen entsprechen.

Diese Attributtypen werden vom NAP-System verwendet:

-   sohattributetypesystemhealthid
-   sohAttributeTypeIpv4FixupServers
-   sohAttributeTypeIpv6FixupServers
-   sohattributetypecomplianceresultcodes
-   sohattributetypefailurecategory

Die übrigen Typen sind nur für die Verwendung durch SHAs und SHVs vorgesehen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Napprotocol. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Napprotocol. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Sohattributevalue**](sohattributevalue-union.md)
</dt> <dt>

[**Sohattribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute)
</dt> <dt>

[**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh)
</dt> <dt>

[**Inapsohconstructor**](inapsohconstructor.md)
</dt> <dt>

[**Inapsohprocessor**](inapsohprocessor.md)
</dt> </dl>

 

 





