---
title: Healthclassvalue-Enumeration (napprotocol. h)
description: Gibt den Wert der Integritäts Klasse TLV an.
ms.assetid: af80c27a-a686-494b-8795-73eb366deaa0
keywords:
- Healthclassvalue-Enumeration NAP
topic_type:
- apiref
api_name:
- HealthClassValue
api_location:
- NapProtocol.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ade44b74d03a69d6ccf410a042adf3819b8cc782
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475069"
---
# <a name="healthclassvalue-enumeration"></a>Healthclassvalue-Enumeration

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Der " **healthclassvalue** "-Enumerationstyp gibt den Wert der Integritäts Klasse "TLV" an.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagHealthClassValue { 
  healthClassFirewall        = 0,
  healthClassPatchLevel      = 1,
  healthClassAntiVirus       = 2,
  healthClassCriticalUpdate  = 3,
  healthClassReserved        = 128
} HealthClassValue;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="healthClassFirewall"></span><span id="healthclassfirewall"></span><span id="HEALTHCLASSFIREWALL"></span>**healthclassfirewall**
</dt> <dd>

Die Integritäts Klasse TLV ist Firewall.

</dd> <dt>

<span id="healthClassPatchLevel"></span><span id="healthclasspatchlevel"></span><span id="HEALTHCLASSPATCHLEVEL"></span>**healthclasspatchlevel**
</dt> <dd>

Die Integritäts Klasse TLV ist die Patchebene.

</dd> <dt>

<span id="healthClassAntiVirus"></span><span id="healthclassantivirus"></span><span id="HEALTHCLASSANTIVIRUS"></span>**healthclassantivirus**
</dt> <dd>

Die Integritäts Klasse TLV ist Antivirus.

</dd> <dt>

<span id="healthClassCriticalUpdate"></span><span id="healthclasscriticalupdate"></span><span id="HEALTHCLASSCRITICALUPDATE"></span>**healthclasscriticalupdate**
</dt> <dd>

Die Integritäts Klasse TLV ist ein kritisches Update.

</dd> <dt>

<span id="healthClassReserved"></span><span id="healthclassreserved"></span><span id="HEALTHCLASSRESERVED"></span>**healthclassreserved**
</dt> <dd>

Nur für die Verwendung durch das System reserviert.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Napprotocol. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Napprotocol. idl</dt> </dl> |



 

 





