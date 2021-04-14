---
title: Sohattributevalue-Union (napprotocol. h)
description: Definiert den Inhalt des Typmembers in einer sohattribute-Struktur.
ms.assetid: 53b30455-33a5-4cf5-8d4e-f0fa8e4e1a12
keywords:
- Sohattributevalue Union NAP
topic_type:
- apiref
api_name:
- SoHAttributeValue
api_location:
- NapProtocol.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36660e4e360ff0df31bb3a76d06c50e5d366c894
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478441"
---
# <a name="sohattributevalue-union"></a>Sohattributevalue-Union

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **sohattributevalue** -Union definiert den Inhalt des **Typmembers** in einer [**sohattribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) -Struktur. Die Struktur der **sohattributevalue** -Union wird durch den [**sohattributetype**](sohattributetype-enum.md) bestimmt, der im **Typmember** der [**sohattribute**](/windows/win32/api/naptypes/ns-naptypes-sohattribute) -Struktur angegeben ist.

## <a name="syntax"></a>Syntax


```C++
typedef union tagSoHAttributeValue {
  SystemHealthEntityId     idVal;
  struct tagIpv4Addresses {
    UINT16      count;
    Ipv4Address *addresses;
  } v4AddressesVal;
  struct tagIpv6Addresses {
    UINT16      count;
    Ipv6Address *addresses;
  } v6AddressesVal;
  ResultCodes              codesVal;
  FILETIME                 dateTimeVal;
  struct tagVendorSpecific {
    UINT32 vendorId;
    UINT16 size;
    BYTE   *vendorSpecificData;
  } vendorSpecificVal;
  UINT8                    uint8Val;
  struct tagOctetString {
    UINT16 size;
    BYTE   *data;
  } octetStringVal;
} SoHAttributeValue;
```



## <a name="members"></a>Member

<dl> <dt>

**idval**
</dt> <dd>

**Case (sohattributetypesystemhealthid)**

Eine eindeutige [systemhealthentityid](nap-datatypes.md) , die die ID des Systemintegritäts-Agents (SHA) oder der System Integritätsprüfung (SHV) enthält, von der dieses [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) -Paket erstellt wurde.

</dd> <dt>

**v4AddressesVal**
</dt> <dd>

**Case (sohAttributeTypeIpv4FixupServers)**

Die IPv4-Adressen der fixupserver, die vom NAP-System verwendet werden.

<dl> <dt>

**count**
</dt> <dd>

Die Anzahl der IPv4-Adressen im **Adress** Element im Bereich von 1 bis [**maxIpv4CountPerSoHAttribute**](nap-type-constants.md).

</dd> <dt>

**addresses**
</dt> <dd>

Ein Array von [**Ipv4Address**](/windows/win32/api/naptypes/ns-naptypes-ipv4address) -Strukturen, die die IPv4-Adressen enthalten.

</dd> </dl> </dd> <dt>

**v6AddressesVal**
</dt> <dd>

**Case (sohAttributeTypeIpv6FixupServers)**

Die IPv6-Adressen der fixupserver, die vom NAP-System verwendet werden.

<dl> <dt>

**count**
</dt> <dd>

Die Anzahl der IPv4-Adressen im **Adress** Element im Bereich von 1 bis [**maxIpv6CountPerSoHAttribute**](nap-type-constants.md).

</dd> <dt>

**addresses**
</dt> <dd>

Ein Array von [**Ipv6Address**](/windows/win32/api/naptypes/ns-naptypes-ipv6address) -Strukturen, die die IPv4-Adressen enthalten.

</dd> </dl> </dd> <dt>

**codesval**
</dt> <dd>

**Case (sohattributetypecomplianceresultcodes, sohattributetypeerrorcodes)**

Eine [**ResultCodes**](/windows/win32/api/naptypes/ns-naptypes-resultcodes) -Struktur, die entweder die von der Anwendung definierten Kompatibilitäts Ergebnis Codes der Client-oder [**NAP-Fehler Konstanten**](nap-error-constants.md)enthält. Ein [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) -Paket muss dieses TLV oder **sohattributetypefailurecategory** TLV enthalten.

</dd> <dt>

**datetimeval**
</dt> <dd>

**Case (sohattributetypetimeoflatstupdate, sohattributetypesohgenerationtime)**

Eine [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) -Struktur, die die Uhrzeit des letzten [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) -Updates oder der **SoH** -Generierungs Zeit enthält.

</dd> <dt>

**vendorspecificval**
</dt> <dd>

**Case (sohattributetypevendorspecific)**

Anwendungsspezifische Daten, die vom Hersteller definiert werden.

<dl> <dt>

**vendorId**
</dt> <dd>

Ein 4-Byte-Bezeichner, der die SHA/SHV-paar-ID definiert. Die ersten 3 Bytes sind der durch IETF zugewiesene SMI-Code des Anbieters, und das letzte Byte identifiziert die Komponente selbst. Verwenden Sie bei der Implementierung eines SHA-oder SHV-Dienstanbieters nicht die ID-Werte, die internen Microsoft-System Integritäts Komponenten von [**NAP-Anbieter Konstanten**](nap-vendor-constants.md)

</dd> <dt>

**size**
</dt> <dd>

Die Größe (in Bytes) der Herstellerdaten im Bereich von 0 bis ([**maxsohattributesize**](nap-type-constants.md) -4).

</dd> <dt>

**vendorSpecificData**
</dt> <dd>

Ein Zeiger auf die herstellerspezifischen Daten in der Netzwerk-Byte Reihenfolge.

</dd> </dl> </dd> <dt>

**uint8Val**
</dt> <dd>

**Case (sohattributetypehealthclass, sohattributetypefailurecategory, sohattributetypeextendedisolationstate)**

Die Integritäts Klasse, Fehler Kategorie oder der erweiterte Isolations Status einer NAP-Komponente als [**healthclassvalue**](healthclassvalue-enum.md) -Wert oder [**failurecategory**](/windows/win32/api/naptypes/ne-naptypes-failurecategory) -Wert oder in einer [**isolationinfoex**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) -Struktur.

</dd> <dt>

**octetstringval**
</dt> <dd>

**default**

Die folgenden Attributwerte sind Oktett-Zeichen folgen:

-   sohattributetypesoftwareversion
-   sohattributetypeclientid
-   sohattributetypeproductname
-   sohattributetypehealthclassstatus

Für die Vorwärtskompatibilität werden alle nicht erkannten Attribute als Oktett-Zeichen folgen zurückgegeben. die **Daten** müssen in der Reihenfolge der Netzwerk Bytes vorliegen.

<dl> <dt>

**size**
</dt> <dd>

Die Größe (in Bytes) der **Daten** im Bereich von 0 bis [**maxsohattributesize**](nap-type-constants.md).

</dd> <dt>

**data**
</dt> <dd>

Ein Zeiger auf den Oktett-Zeichen folgen Wert.

</dd> </dl> </dd> </dl>

## <a name="actual-data-layout"></a>Tatsächliches Datenlayout

Aufgrund der Art der SDK-Veröffentlichungs Umgebung werden Unions nicht eindeutig in Syntax Blöcken dargestellt. Dies ist die tatsächliche Syntax aus der Header Datei "napprotocol. h".


```C++
#include <windows.h>

typedef [switch_type(SoHAttributeType)] 
   union tagSoHAttributeValue
   {
      [case(sohAttributeTypeSystemHealthId)]
         SystemHealthEntityId idVal;
   
      [case(sohAttributeTypeIpv4FixupServers)]
         struct tagIpv4Addresses
         {
            [range(1, maxIpv4CountPerSoHAttribute)] 
               UINT16 count;
            [size_is(count)] Ipv4Address* addresses;
         } v4AddressesVal;

      [case(sohAttributeTypeIpv6FixupServers)]
         struct tagIpv6Addresses
         {
            [range(1, maxIpv6CountPerSoHAttribute)]
               UINT16 count;
            [size_is(count)] Ipv6Address* addresses;
         } v6AddressesVal;

      [case(sohAttributeTypeComplianceResultCodes, 
            sohAttributeTypeErrorCodes)]
         ResultCodes codesVal;

      [case(sohAttributeTypeTimeOfLastUpdate, 
            sohAttributeTypeSoHGenerationTime)]
         FILETIME dateTimeVal;

      [case(sohAttributeTypeVendorSpecific)]
         struct tagVendorSpecific
         {
            UINT32 vendorId;
            [range(0, maxSoHAttributeSize - 4)] 
               UINT16 size;
            [size_is(size)] BYTE* vendorSpecificData;
         } vendorSpecificVal;

      [case(sohAttributeTypeHealthClass, 
            sohAttributeTypeFailureCategory,
            sohAttributeTypeExtendedIsolationState)]
         UINT8 uint8Val;

      [default]
         struct tagOctetString
         {
            [range(0, maxSoHAttributeSize)] UINT16 size;
            [size_is(size)] BYTE* data;
         } octetStringVal;

   } SoHAttributeValue;
};
```



## <a name="remarks"></a>Bemerkungen

Diese Attributtypen werden vom NAP-System verwendet:

-   sohattributetypesystemhealthid
-   sohAttributeTypeIpv4FixupServers
-   sohAttributeTypeIpv6FixupServers
-   sohattributetypecomplianceresultcodes
-   sohattributetypefailurecategory

Der Rest der [**sohattributetypes**](sohattributetype-enum.md) ist ausschließlich als ausführliche Anleitung für die Verwendung durch SHAs und SHVs gedacht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Napprotocol. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Napprotocol. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[NAP-Referenz](nap-reference.md)
</dt> <dt>

[NAP-Strukturen](nap-structures.md)
</dt> </dl>

 

