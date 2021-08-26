---
title: LSKeyPack-Struktur
description: Enthält Informationen zu einem bestimmten Remotedesktopdienste-Schlüsselpaket.
ms.assetid: c26d27ee-7dd3-49f0-a79c-752d23693a2a
ms.tgt_platform: multiple
keywords:
- LSKeyPack-Remotedesktopdienste
- LPLSKeyPack-Strukturzeiger Remotedesktopdienste
topic_type:
- apiref
api_name:
- LSKeyPack
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3a8b2c7c8b6c42464e273008f9de2730b41ea64981e44583eb48f4125da3ba9b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989089"
---
# <a name="lskeypack-structure"></a>LSKeyPack-Struktur

Enthält Informationen zu einem bestimmten Remotedesktopdienste-Schlüsselpaket.

> [!Note]  
> Diese Struktur ist in einer Headerdatei nicht definiert. Um diese Struktur zu verwenden, müssen Sie sie selbst definieren, wie in diesem Thema gezeigt.

 

## <a name="syntax"></a>Syntax


```C++
typedef struct _LSKeyPack {
  DWORD dwVersion;
  UCHAR ucKeyPackType;
  TCHAR szCompanyName[256];
  TCHAR szKeyPackId[256];
  TCHAR szProductName[256];
  TCHAR szProductId[256];
  TCHAR szProductDesc[256];
  WORD  wMajorVersion;
  WORD  wMinorVersion;
  DWORD dwPlatformType;
  UCHAR ucLicenseType;
  DWORD dwLanguageId;
  UCHAR ucChannelOfPurchase;
  TCHAR szBeginSerialNumber[256];
  DWORD dwTotalLicenseInKeyPack;
  DWORD dwProductFlags;
  DWORD dwKeyPackId;
  UCHAR ucKeyPackStatus;
  DWORD dwActivateDate;
  DWORD dwExpirationDate;
  DWORD dwNumberOfLicenses;
} LSKeyPack, *LPLSKeyPack;
```



## <a name="members"></a>Member

<dl> <dt>

**dwVersion**
</dt> <dd>

Version des Schlüsselpakets.

</dd> <dt>

**ucKeyPackType**
</dt> <dd>

Typ des Schlüsselpakets.

</dd> <dt>

**szCompanyName**
</dt> <dd>

Name des Unternehmens, das das Schlüsselpaket ausgestellt hat.

</dd> <dt>

**szKeyPackId**
</dt> <dd>

ID des Schlüsselpakets.

</dd> <dt>

**szProductName**
</dt> <dd>

Name des Produkts, zu dem dieses Key Pack gehört.

</dd> <dt>

**szProductId**
</dt> <dd>

ID des Produkts, zu dem dieses Key Pack gehört.

</dd> <dt>

**szProductDesc**
</dt> <dd>

Beschreibung des Produkts, zu dem dieses Key Pack gehört.

</dd> <dt>

**wMajorVersion**
</dt> <dd>

Hauptversion des Produkts, zu dem dieses Key Pack gehört.

</dd> <dt>

**wMinorVersion**
</dt> <dd>

Nebenversion des Produkts, zu dem dieses Key Pack gehört.

</dd> <dt>

**dwPlatformType**
</dt> <dd>

Plattformtyp.

</dd> <dt>

**ucLicenseType**
</dt> <dd>

Typ der Lizenzen im Schlüsselpaket.

</dd> <dt>

**dwLanguageId**
</dt> <dd>

Sprach-ID.

</dd> <dt>

**ucChannelOfPurchase**
</dt> <dd>

Kaufkanal.

</dd> <dt>

**szBeginSerialNumber**
</dt> <dd>

Seriennummer für die erste Lizenz.

</dd> <dt>

**dwTotalLicenseInKeyPack**
</dt> <dd>

Gesamtanzahl der Lizenzen im Schlüsselpaket.

</dd> <dt>

**dwProductFlags**
</dt> <dd>

Flaggen.

</dd> <dt>

**dwKeyPackId**
</dt> <dd>

ID des Schlüsselpakets.

</dd> <dt>

**ucKeyPackStatus**
</dt> <dd>

Status des Schlüsselpakets.

</dd> <dt>

**dwActivateDate**
</dt> <dd>

Aktivierungsdatum für das Schlüsselpaket.

</dd> <dt>

**dwExpirationDate**
</dt> <dd>

Ablaufdatum für das Schlüsselpaket.

</dd> <dt>

**dwNumberOfLicenses**
</dt> <dd>

Anzahl der Lizenzen.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md)
</dt> <dt>

[**TLSKeyPackEnumNext**](tlskeypackenumnext.md)
</dt> <dt>

[**TLSKeyPackEnumEnd**](tlskeypackenumend.md)
</dt> </dl>

 

 





