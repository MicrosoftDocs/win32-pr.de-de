---
title: WMDRM_LICENSE_FILTER-Struktur (Wmdrmsdk.h)
description: Die WMDRM \_ LICENSE \_ FILTER-Struktur definiert Filterparameter für die Verwendung beim Erstellen einer Lizenzenumeration.
ms.assetid: 43bbbfdc-1ec4-44a6-8245-96853bbeea86
keywords:
- WMDRM_LICENSE_FILTER Strukturfenster Medienformat
- Strukturfenster Medienformat
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
ms.openlocfilehash: 94dc65758c7c5a25d31dd9fdb2d0fcd5cfa65debfff3defab4b88280a5ff3b3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118698137"
---
# <a name="wmdrm_license_filter-structure"></a>WMDRM \_ LICENSE \_ FILTER-Struktur

Die **WMDRM \_ LICENSE \_ FILTER-Struktur** definiert Filterparameter für die Verwendung beim Erstellen einer Lizenzenumeration.

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

Gibt eine Mindestversionsnummer für die zurückgegebenen Lizenzen an.

</dd> <dt>

**bstrKID**
</dt> <dd>

Gibt eine Schlüssel-ID an, nach der Lizenzen gefiltert werden sollen. Nur Lizenzen mit der angegebenen Schlüssel-ID werden in die Enumeration einbezogen.

</dd> <dt>

**bstrRights**
</dt> <dd>

Gibt einen Satz von Rechten an, nach dem Lizenzen gefiltert werden sollen. Nur Lizenzen, die alle angegebenen Rechte bereitstellen, werden in die Enumeration einbezogen.

</dd> <dt>

**bstrAllowedSourceIDs**
</dt> <dd>

Gibt die Quellen von geschützten Inhalten an, die in die Lizenzsuche eingeschlossen werden sollen.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Struktur wird von der [**IWMDRMLicenseManagement::CreateLicenseEnumeration-Methode**](iwmdrmlicensemanagement-createlicenseenumeration.md) verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdrmsdk.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Strukturen**](drm-structures.md)
</dt> </dl>

 

 





