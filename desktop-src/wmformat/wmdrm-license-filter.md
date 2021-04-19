---
title: WMDRM_LICENSE_FILTER Struktur (wmdrmsdk. h)
description: Die WMDRM- \_ Lizenz \_ Filter Struktur definiert Filter Parameter, die beim Erstellen einer Lizenzierungs Enumeration verwendet werden.
ms.assetid: 43bbbfdc-1ec4-44a6-8245-96853bbeea86
keywords:
- WMDRM_LICENSE_FILTER Struktur-Windows Media-Format
- Struktur des Windows-Medien Formats
topic_type:
- apiref
api_name:
- WMDRM_LICENSE_FILTER
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9200bea0d74b7c9a84c5731072e2e65bca81b6cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356408"
---
# <a name="wmdrm_license_filter-structure"></a>WMDRM- \_ Lizenz \_ Filter Struktur

Die **WMDRM- \_ Lizenz \_ Filter** Struktur definiert Filter Parameter, die beim Erstellen einer Lizenzierungs Enumeration verwendet werden.

## <a name="syntax"></a>Syntax


```C++
typedef struct WMDRM_LICENSE_FILTER {
  DWORD dwVersion;
  BSTR  bstrKID;
  BSTR  bstrRights;
  BSTR  bstrAllowedSourceIDs;
} ;
```



## <a name="members"></a>Member

<dl> <dt>

**dwVersion**
</dt> <dd>

Gibt eine minimale Versionsnummer für die zurückgegebenen Lizenzen an.

</dd> <dt>

**bstrinkid**
</dt> <dd>

Gibt eine Schlüssel-ID zum Filtern von Lizenzen an. Nur Lizenzen mit der angegebenen Schlüssel-ID werden in die-Enumeration eingeschlossen.

</dd> <dt>

**bstraurights**
</dt> <dd>

Gibt einen Satz von Rechten zum Filtern von Lizenzen an. Nur Lizenzen, die alle angegebenen Rechte bereitstellen, sind in der-Enumeration enthalten.

</dd> <dt>

**bstrauzuweisung-sourceids**
</dt> <dd>

Gibt die Quellen geschützter Inhalte an, die in der Lizenz Suche enthalten sein sollen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Struktur wird von der [**iwmdrmlicenaberation**](iwmdrmlicensemanagement-createlicenseenumeration.md) -Methode verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Strukturen**](drm-structures.md)
</dt> </dl>

 

 





