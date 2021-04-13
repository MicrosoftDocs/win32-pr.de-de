---
title: MPVERSION_INFO Struktur (mpclient. h)
description: Versionsinformationen für die Komponenten von Malware Protection Manager.
ms.assetid: C18EE6FE-57E1-4814-85CA-19C3ACE275D2
keywords:
- MPVERSION_INFO Struktur Funktionen der Legacy-Windows-Umgebung
- PMPVERSION_INFO Struktur Zeiger Legacy-Windows-Umgebungs Features
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
ms.openlocfilehash: f30153c427b880600a3d8aeb3c411a8679cd64b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341047"
---
# <a name="mpversion_info-structure"></a>Mpversion- \_ Informationsstruktur

Versionsinformationen für die Komponenten von Malware Protection Manager.

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

Typ: **[ **mpcomponent- \_ Version**](mpcomponent-version.md)**

</dd> <dd>

Die Produktversion.

</dd> <dt>

**Service**
</dt> <dd>

Typ: **[ **mpcomponent- \_ Version**](mpcomponent-version.md)**

</dd> <dd>

Die Dienst Komponenten Version.

</dd> <dt>

**File System Filter**
</dt> <dd>

Typ: **[ **mpcomponent- \_ Version**](mpcomponent-version.md)**

</dd> <dd>

Version der Dateisystem Filter-Komponente.

</dd> <dt>

**Engine**
</dt> <dd>

Typ: **[ **mpcomponent- \_ Version**](mpcomponent-version.md)**

</dd> <dd>

Engine-Komponenten Version.

</dd> <dt>

**Assignature**
</dt> <dd>

Typ: **[ **mpcomponent- \_ Version**](mpcomponent-version.md)**

</dd> <dd>

Version der AntiSpyware-Signatur Komponente.

</dd> <dt>

**Avsignature**
</dt> <dd>

Typ: **[ **mpcomponent- \_ Version**](mpcomponent-version.md)**

</dd> <dd>

Version der Antivirus-Signatur Komponente.

</dd> <dt>

**Nisengine**
</dt> <dd>

Typ: **[ **mpcomponent- \_ Version**](mpcomponent-version.md)**

</dd> <dd>

Die NIS-Engine-Version.

</dd> <dt>

**Nissignature**
</dt> <dd>

Typ: **[ **mpcomponent- \_ Version**](mpcomponent-version.md)**

</dd> <dd>

Die Komponenten Version der NIS-Signatur Signatur.

</dd> <dt>

**Reserved**
</dt> <dd>

Typ: **[**mpcomponent \_ Version**](mpcomponent-version.md) \[ 4\]**

</dd> <dd>

Reservierte Felder.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Mpclient. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**mpcomponent- \_ Version**](mpcomponent-version.md)
</dt> </dl>

 

 





