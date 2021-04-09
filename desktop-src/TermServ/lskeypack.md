---
title: Lschräypack-Struktur
description: Enthält Informationen zu einem bestimmten Remotedesktopdienste Licensing Key Pack.
ms.assetid: c26d27ee-7dd3-49f0-a79c-752d23693a2a
ms.tgt_platform: multiple
keywords:
- Lschräypack-Struktur Remotedesktopdienste
- Lplschräypack-Struktur Zeiger Remotedesktopdienste
topic_type:
- apiref
api_name:
- LSKeyPack
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2b1ac1f51e66a0a3c15c33f2535bc02f1fd3528f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957059"
---
# <a name="lskeypack-structure"></a>Lschräypack-Struktur

Enthält Informationen zu einem bestimmten Remotedesktopdienste Licensing Key Pack.

> [!Note]  
> Diese Struktur ist nicht in einer Header Datei definiert. Um diese Struktur verwenden zu können, müssen Sie Sie selbst definieren, wie in diesem Thema gezeigt.

 

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

Version des Schlüssel Pakets.

</dd> <dt>

**uckeypacktype**
</dt> <dd>

Der Typ des Schlüssel Pakets.

</dd> <dt>

**szcompanyname**
</dt> <dd>

Name des Unternehmens, von dem das Schlüssel Paket ausgestellt wurde.

</dd> <dt>

**szkeypackid**
</dt> <dd>

ID des Schlüssel Pakets.

</dd> <dt>

**szproductname**
</dt> <dd>

Der Name des Produkts, zu dem dieses Schlüssel Paket gehört.

</dd> <dt>

**szproductid**
</dt> <dd>

ID des Produkts, zu dem dieses Schlüssel Paket gehört.

</dd> <dt>

**szproductde**
</dt> <dd>

Die Beschreibung des Produkts, zu dem dieses Schlüssel Paket gehört.

</dd> <dt>

**wmajorversion**
</dt> <dd>

Hauptversion des Produkts, zu dem dieses Schlüssel Paket gehört.

</dd> <dt>

**wminorversion**
</dt> <dd>

Neben Version des Produkts, zu dem dieses Schlüssel Paket gehört.

</dd> <dt>

**dwplatformtype**
</dt> <dd>

Plattformtyp.

</dd> <dt>

**uclicensertyp**
</dt> <dd>

Der Typ der Lizenzen im Schlüssel Paket.

</dd> <dt>

**dwLanguageId**
</dt> <dd>

Sprach-ID.

</dd> <dt>

**ucchannelofpurchase**
</dt> <dd>

Kanal des Kaufs.

</dd> <dt>

**szbeginserialnumber**
</dt> <dd>

Seriennummer für die erste Lizenz.

</dd> <dt>

**dwtotallicenseingekeypack**
</dt> <dd>

Die Gesamtanzahl der Lizenzen im Schlüssel Paket.

</dd> <dt>

**dwproductflags**
</dt> <dd>

Fahren.

</dd> <dt>

**dwkeypackid**
</dt> <dd>

ID des Schlüssel Pakets.

</dd> <dt>

**uckeypackstatus**
</dt> <dd>

Der Status des Schlüssel Pakets.

</dd> <dt>

**dwactivatedate**
</dt> <dd>

Aktivierungsdatum für das Schlüssel Paket.

</dd> <dt>

**dwexpirationdate**
</dt> <dd>

Das Ablaufdatum für das Schlüssel Paket.

</dd> <dt>

**dwnumoflicenses**
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

[**Tlskeypackenumbegin**](tlskeypackenumbegin.md)
</dt> <dt>

[**Tlskeypackenumnext**](tlskeypackenumnext.md)
</dt> <dt>

[**Tlskeypackenumend**](tlskeypackenumend.md)
</dt> </dl>

 

 





