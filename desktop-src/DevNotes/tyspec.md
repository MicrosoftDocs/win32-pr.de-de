---
description: Definiert Möglichkeiten zum Zuordnen zu einer Klassen-ID.
ms.assetid: 1af170e3-1edd-411f-acba-d4b244107996
title: TYSPEC-Enumeration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TYSPEC
api_type:
- IDLDef
api_location:
- Wtypes.idl
ms.openlocfilehash: 15e7ecdc06495c0fa68b2949ae159bbc76b8cababd2b8703d3ebbdebb874399b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075754"
---
# <a name="tyspec-enumeration"></a>TYSPEC-Enumeration

Definiert Möglichkeiten zum Zuordnen zu einer Klassen-ID.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagTYSPEC { 
  TYSPEC_CLSID,
  TYSPEC_FILEEXT,
  TYSPEC_MIMETYPE,
  TYSPEC_FILENAME,
  TYSPEC_PROGID,
  TYSPEC_PACKAGENAME,
  TYSPEC_OBJECTID
} TYSPEC;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="TYSPEC_CLSID"></span><span id="tyspec_clsid"></span>**TYSPEC \_ CLSID**
</dt> <dd>

EINE CLSID.

</dd> <dt>

<span id="TYSPEC_FILEEXT"></span><span id="tyspec_fileext"></span>**TYSPEC \_ FILEEXT**
</dt> <dd>

Eine Dateinamenerweiterung. Dieser Wert wird derzeit nicht unterstützt.

</dd> <dt>

<span id="TYSPEC_MIMETYPE"></span><span id="tyspec_mimetype"></span>**TYSPEC \_ MIMETYPE**
</dt> <dd>

Ein MIME-Typ. Dieser Wert wird derzeit nicht unterstützt.

</dd> <dt>

<span id="TYSPEC_FILENAME"></span><span id="tyspec_filename"></span>**TYSPEC \_ FILENAME**
</dt> <dd>

Ein Dateiname. Dieser Wert wird derzeit nicht unterstützt.

</dd> <dt>

<span id="TYSPEC_PROGID"></span><span id="tyspec_progid"></span>**TYSPEC \_ PROGID**
</dt> <dd>

EINE PROGID. Dieser Wert wird derzeit nicht unterstützt.

</dd> <dt>

<span id="TYSPEC_PACKAGENAME"></span><span id="tyspec_packagename"></span>**TYSPEC \_ PACKAGENAME**
</dt> <dd>

Ein Paketname. Dieser Wert wird derzeit nicht unterstützt.

</dd> <dt>

<span id="TYSPEC_OBJECTID"></span><span id="tyspec_objectid"></span>**TYSPEC \_ OBJECTID**
</dt> <dd>

Eine Objekt-ID. Dieser Wert wird derzeit nicht unterstützt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **uCLSSPEC-Union** ist wie folgt definiert:

``` syntax
typedef union switch(DWORD tyspec) {
    case TYSPEC_CLSID:
        CLSID clsid;
    case TYSPEC_FILEEXT:
        LPOLESTR pFileExt;
    case TYSPEC_MIMETYPE:
        LPOLESTR pMimeType;
    case TYSPEC_PROGID:
        LPOLESTR pProgId;
    case TYSPEC_FILENAME:
        LPOLESTR pFileName;
    case TYSPEC_PACKAGENAME:
        struct {
        LPOLESTR pPackageName;
        GUID PolicyId;
        } ByName;
    case TYSPEC_OBJECTID:
        struct {
        GUID ObjectId;
        GUID PolicyId;
        } ByObjectId;
} uCLSSPEC;
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|---------------------------------------------------------------------------------------|
| Idl<br/> | <dl> <dt>Wtypes.idl</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CoInstallieren**](/windows/win32/api/objbase/nf-objbase-coinstall)
</dt> </dl>

 

 
