---
description: Definiert einen 802,11-PHY-und Medientyp.
ms.assetid: f3804e57-c633-4288-9749-2b267b1353ae
title: DOT11_PHY_TYPE-Enumeration (Windot11. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_PHY_TYPE
api_type:
- HeaderDef
api_location:
- windot11.h
ms.openlocfilehash: 4e8fc4a1154b9f95fad5024607435861b9e98ae1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866036"
---
# <a name="dot11_phy_type-enumeration"></a>DOT11 \_ PHY- \_ Typenumeration

Die **DOT11 \_ PHY- \_ Typenumeration** definiert einen 802,11-PHY-und Medientyp.

## <a name="syntax"></a>Syntax


```C++
typedef enum _DOT11_PHY_TYPE { 
  dot11_phy_type_unknown     = 0,
  dot11_phy_type_any         = 0,
  dot11_phy_type_fhss        = 1,
  dot11_phy_type_dsss        = 2,
  dot11_phy_type_irbaseband  = 3,
  dot11_phy_type_ofdm        = 4,
  dot11_phy_type_hrdsss      = 5,
  dot11_phy_type_erp         = 6,
  dot11_phy_type_ht          = 7,
  dot11_phy_type_vht         = 8,
  dot11_phy_type_IHV_start   = 0x80000000,
  dot11_phy_type_IHV_end     = 0xffffffff
} DOT11_PHY_TYPE, *PDOT11_PHY_TYPE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="dot11_phy_type_unknown"></span><span id="DOT11_PHY_TYPE_UNKNOWN"></span>**Dot11 \_ PHY- \_ Typ \_ unbekannt**
</dt> <dd>

Gibt einen unbekannten oder nicht initialisierten phiertyp an.

</dd> <dt>

<span id="dot11_phy_type_any"></span><span id="DOT11_PHY_TYPE_ANY"></span>**Dot11 \_ PHY \_ Typ \_ beliebig**
</dt> <dd>

Gibt einen beliebigen PHY-Typ an.

</dd> <dt>

<span id="dot11_phy_type_fhss"></span><span id="DOT11_PHY_TYPE_FHSS"></span>**Dot11- \_ PHY- \_ Typ ( \_ SSS)**
</dt> <dd>

Gibt eine "Frequency-Spring"-e/a-Rate (SHSS) an. Für Bluetooth-Geräte können Sie den Einsatz von SSS oder eine Anpassung von SHSS verwenden.

</dd> <dt>

<span id="dot11_phy_type_dsss"></span><span id="DOT11_PHY_TYPE_DSSS"></span>**Dot11 \_ PHY- \_ Typ \_ DSSS**
</dt> <dd>

Gibt einen DSSS (Direct Sequence Spread)-PHY-Typ an.

</dd> <dt>

<span id="dot11_phy_type_irbaseband"></span><span id="DOT11_PHY_TYPE_IRBASEBAND"></span>**Dot11 \_ PHY- \_ Typ " \_ unbaseband"**
</dt> <dd>

Gibt einen Infrarot-Baseband-phikentyp (IR) an.

</dd> <dt>

<span id="dot11_phy_type_ofdm"></span><span id="DOT11_PHY_TYPE_OFDM"></span>**Dot11 \_ PHY \_ Typ von \_ DM**
</dt> <dd>

Gibt einen Multiplexing (OFDM)-PHY-Typ der orthogonalen Frequenz Division an. 802.11 a-Geräte können OFDM verwenden.

</dd> <dt>

<span id="dot11_phy_type_hrdsss"></span><span id="DOT11_PHY_TYPE_HRDSSS"></span>**Dot11 \_ PHY \_ Type \_ hrdsss**
</dt> <dd>

Gibt einen höchst wertigen DSSS (hrdsss)-PHY-Typ an.

</dd> <dt>

<span id="dot11_phy_type_erp"></span><span id="DOT11_PHY_TYPE_ERP"></span>**Dot11 \_ PHY- \_ Typ \_ ERP**
</dt> <dd>

Gibt den Typ des erweiterten Raten-PHY (ERP) an. 802.11 g-Geräte können ERP verwenden.

</dd> <dt>

<span id="dot11_phy_type_ht"></span><span id="DOT11_PHY_TYPE_HT"></span>**Dot11 \_ PHY \_ Typ \_ HT**
</dt> <dd>

Gibt den 802.11 n-PHY-Typ an.

</dd> <dt>

<span id="dot11_phy_type_vht"></span><span id="DOT11_PHY_TYPE_VHT"></span>**Dot11 \_ PHY \_ Typ \_ VHT**
</dt> <dd>

Gibt den 802.11-AC-phikentyp an. Dies ist der in IEEE 802.11 AC angegebene extrem hohe Durchsatz-PHY-Typ.

Dieser Wert wird auf Windows 8.1, Windows Server 2012 R2 und höher unterstützt.

</dd> <dt>

<span id="dot11_phy_type_IHV_start"></span><span id="dot11_phy_type_ihv_start"></span><span id="DOT11_PHY_TYPE_IHV_START"></span>**Dot11 \_ PHY \_ Type \_ IHV \_ Start**
</dt> <dd>

Gibt den Anfang des Bereichs an, der zum Definieren von PHY-Typen verwendet wird, die von einem unabhängigen Hardwarehersteller (IHV) entwickelt wurden.

</dd> <dt>

<span id="dot11_phy_type_IHV_end"></span><span id="dot11_phy_type_ihv_end"></span><span id="DOT11_PHY_TYPE_IHV_END"></span>**Dot11 \_ PHY \_ Typ \_ IHV \_ Ende**
</dt> <dd>

Gibt den Anfang des Bereichs an, der zum Definieren von PHY-Typen verwendet wird, die von einem unabhängigen Hardwarehersteller (IHV) entwickelt wurden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Ein IHV kann einen Wert für seine proprietären PHY-Typen vom **Dot11 \_ PHY \_ Type \_ IHV \_ Start** through **Dot11 \_ PHY \_ Type \_ IHV \_ End** zuweisen. Der IHV muss eine eindeutige Zahl aus diesem Bereich für jeden seiner eigenen eigenen PHY-Typen zuweisen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista, Windows XP mit SP3 \[ Desktop-Apps\]<br/>                   |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                  |
| Verteilbare Komponente<br/>          | Drahtlose LAN-API für Windows XP mit SP2<br/>                                   |
| Header<br/>                   | <dl> <dt>Windot11. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WLAN-Zuordnungs \_ \_ Attribute**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_association_attributes)
</dt> <dt>

[**WLAN- \_ Schnittstellen \_ Funktion**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_interface_capability)
</dt> </dl>

 

 




