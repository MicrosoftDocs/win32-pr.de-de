---
title: WINBIO_POLICY_SOURCE-Enumeration (winbio \_ types. h)
description: Listet die möglichen Quellen der Richtlinien Informationen für die Erkennung von Spoofing für biometrische Faktoren auf.
ms.assetid: 3DC3BB0B-1FD7-473C-8E0B-B7E0A4A44E9E
keywords:
- WINBIO_POLICY_SOURCE Enumeration Windows-Biometrieframework-API
- PWINBIO_POLICY_SOURCE enumerationszeiger Windows-Biometrieframework-API
topic_type:
- apiref
api_name:
- WINBIO_POLICY_SOURCE
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 866d1d82d939f143c4385caa5d94c68ffe3758f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341267"
---
# <a name="winbio_policy_source-enumeration"></a>Quellenumeration der winbio- \_ Richtlinie \_

Listet die möglichen Quellen der Richtlinien Informationen für die Erkennung von Spoofing für biometrische Faktoren auf.

## <a name="syntax"></a>Syntax


```C++
typedef enum _WINBIO_POLICY_SOURCE { 
  WINBIO_POLICY_UNKNOWN  = 0x00000000,
  WINBIO_POLICY_DEFAULT  = 0x00000001,
  WINBIO_POLICY_LOCAL    = 0x00000002,
  WINBIO_POLICY_ADMIN    = 0x00000003
} WINBIO_POLICY_SOURCE, *PWINBIO_POLICY_SOURCE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="WINBIO_POLICY_UNKNOWN"></span><span id="winbio_policy_unknown"></span>**winbio- \_ Richtlinie \_ unbekannt**
</dt> <dd>

Die Quelle der Richtlinie ist unbekannt.

</dd> <dt>

<span id="WINBIO_POLICY_DEFAULT"></span><span id="winbio_policy_default"></span>**Standard für winbio- \_ Richtlinie \_**
</dt> <dd>

Die Richtlinie ist die Standard Richtlinie, die die Windows-Biometrieframework bereitstellt.

</dd> <dt>

<span id="WINBIO_POLICY_LOCAL"></span><span id="winbio_policy_local"></span>**lokale winbio- \_ Richtlinie \_**
</dt> <dd>

Die Richtlinie, die der jeweilige Benutzer für sein Konto mithilfe der App " **Einstellungen** " festgelegt hat. Diese Richtlinie überschreibt die Standard Richtlinie.

</dd> <dt>

<span id="WINBIO_POLICY_ADMIN"></span><span id="winbio_policy_admin"></span>**Administrator der winbio- \_ Richtlinie \_**
</dt> <dd>

Eine Gruppenrichtlinie, die der IT-Administrator für das Unternehmen festgelegt hat. Einzelne Benutzer können diese Richtlinie nicht außer Kraft setzen.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                                                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2016 \[ -Desktop-Apps\]<br/>                                                                                                                     |
| Header<br/>                   | <dl> <dt>Winbio \_ types. h (Include winbio. h für Client Anwendungen oder winbio \_ Adapters. h für Adapter)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Aktion für winbio- \_ \_ antispoof- \_ Richtlinie \_**](winbio-anti-spoof-policy-action.md)
</dt> </dl>

 

 





