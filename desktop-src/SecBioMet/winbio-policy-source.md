---
title: WINBIO_POLICY_SOURCE-Enumeration (Winbio \_ types.h)
description: Listet die möglichen Quellen von Richtlinieninformationen für die Erkennung von Spoofing für biometrische Faktoren auf.
ms.assetid: 3DC3BB0B-1FD7-473C-8E0B-B7E0A4A44E9E
keywords:
- WINBIO_POLICY_SOURCE Enumeration Windows Biometric Framework-API
- PWINBIO_POLICY_SOURCE Enumerationszeiger Windows Biometrieframework-API
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
ms.openlocfilehash: 962d4bc3e8cffb778df56d78a9ddaf0641f57f8f96c8f7b024745a4b879f2f81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909933"
---
# <a name="winbio_policy_source-enumeration"></a>WINBIO \_ POLICY \_ SOURCE-Enumeration

Listet die möglichen Quellen von Richtlinieninformationen für die Erkennung von Spoofing für biometrische Faktoren auf.

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

<span id="WINBIO_POLICY_UNKNOWN"></span><span id="winbio_policy_unknown"></span>**\_WINBIO-RICHTLINIE \_ UNBEKANNT**
</dt> <dd>

Die Quelle der Richtlinie ist unbekannt.

</dd> <dt>

<span id="WINBIO_POLICY_DEFAULT"></span><span id="winbio_policy_default"></span>**\_WINBIO-RICHTLINIENSTANDARD \_**
</dt> <dd>

Die Richtlinie ist die Standardrichtlinie, die vom Windows Biometric Framework zur Verfügung steht.

</dd> <dt>

<span id="WINBIO_POLICY_LOCAL"></span><span id="winbio_policy_local"></span>**\_WINBIO-RICHTLINIE \_ LOKAL**
</dt> <dd>

Die Richtlinie, die der einzelne Benutzer mithilfe der **Einstellungen-App** für sein Konto festgelegt hat. Diese Richtlinie überschreibt die Standardrichtlinie.

</dd> <dt>

<span id="WINBIO_POLICY_ADMIN"></span><span id="winbio_policy_admin"></span>**\_WINBIO-RICHTLINIENADMINISTRATOR \_**
</dt> <dd>

Eine Gruppenrichtlinie, die der IT-Administrator für das Unternehmen festgelegt hat. Einzelne Benutzer können diese Richtlinie nicht überschreiben.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                                                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2016 Nur Desktop-Apps\]<br/>                                                                                                                     |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (winbio.h für Clientanwendungen oder Winbio \_ adapters.h für Adapter einschließen)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**WINBIO \_ ANTI \_ SPOOF \_ POLICY \_ ACTION**](winbio-anti-spoof-policy-action.md)
</dt> </dl>

 

 





