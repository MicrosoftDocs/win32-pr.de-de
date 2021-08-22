---
title: MPVERSION_INFO -Struktur (MpClient.h)
description: Versionsinformationen für die Komponenten des Schadsoftwareschutz-Managers.
ms.assetid: C18EE6FE-57E1-4814-85CA-19C3ACE275D2
keywords:
- MPVERSION_INFO struktur Legacy-Windows-Umgebungsfeatures
- PMPVERSION_INFO Strukturzeiger Legacy-Windows-Umgebungsfeatures
topic_type:
- apiref
api_name:
- MPVERSION_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50a89b03b8b310416f9b0b496c055f732f4e83859bb7eba50b7891abebc27d26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608700"
---
# <a name="mpversion_info-structure"></a>MPVERSION \_ INFO-Struktur

Versionsinformationen für die Komponenten des Schadsoftwareschutz-Managers.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagMPVERSION_INFO {
  MPCOMPONENT_VERSION Product;
  MPCOMPONENT_VERSION Service;
  MPCOMPONENT_VERSION FileSystemFilter;
  MPCOMPONENT_VERSION Engine;
  MPCOMPONENT_VERSION ASSignature;
  MPCOMPONENT_VERSION AVSignature;
  MPCOMPONENT_VERSION NISEngine;
  MPCOMPONENT_VERSION NISSignature;
  MPCOMPONENT_VERSION Reserved[4];
} MPVERSION_INFO, *PMPVERSION_INFO;
```



## <a name="members"></a>Member

<dl> <dt>

**Produkt**
</dt> <dd>

Typ: **[ **MPCOMPONENT-VERSION \_**](mpcomponent-version.md)**

</dd> <dd>

Die Produktversion.

</dd> <dt>

**Service**
</dt> <dd>

Typ: **[ **MPCOMPONENT-VERSION \_**](mpcomponent-version.md)**

</dd> <dd>

Dienstkomponentenversion.

</dd> <dt>

**FileSystemFilter**
</dt> <dd>

Typ: **[ **MPCOMPONENT-VERSION \_**](mpcomponent-version.md)**

</dd> <dd>

Version der Dateisystemfilterkomponente.

</dd> <dt>

**Engine**
</dt> <dd>

Typ: **[ **MPCOMPONENT-VERSION \_**](mpcomponent-version.md)**

</dd> <dd>

Engine-Komponentenversion.

</dd> <dt>

**ASSignature**
</dt> <dd>

Typ: **[ **MPCOMPONENT-VERSION \_**](mpcomponent-version.md)**

</dd> <dd>

Version der Antispyware-Signaturkomponente.

</dd> <dt>

**AVSignature**
</dt> <dd>

Typ: **[ **MPCOMPONENT-VERSION \_**](mpcomponent-version.md)**

</dd> <dd>

Version der Antivirensignaturkomponente.

</dd> <dt>

**NISEngine**
</dt> <dd>

Typ: **[ **MPCOMPONENT-VERSION \_**](mpcomponent-version.md)**

</dd> <dd>

VERSION der NIS-Engine.

</dd> <dt>

**NISSignature**
</dt> <dd>

Typ: **[ **MPCOMPONENT-VERSION \_**](mpcomponent-version.md)**

</dd> <dd>

Version der NIS-Signatursignaturkomponente.

</dd> <dt>

**Reserved**
</dt> <dd>

Typ: **[**MPCOMPONENT \_ VERSION**](mpcomponent-version.md) \[ 4\]**

</dd> <dd>

Reservierte Felder.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MPCOMPONENT-VERSION \_**](mpcomponent-version.md)
</dt> </dl>

 

 





