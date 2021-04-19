---
description: Definiert Methoden für die Zuordnung zu einer Klassen-ID.
ms.assetid: 1af170e3-1edd-411f-acba-d4b244107996
title: Tyspec-Enumeration
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
ms.openlocfilehash: b4c8cf38a8f99458e76cabc726aa39ad01a71ebc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370512"
---
# <a name="tyspec-enumeration"></a>Tyspec-Enumeration

Definiert Methoden für die Zuordnung zu einer Klassen-ID.

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

<span id="TYSPEC_CLSID"></span><span id="tyspec_clsid"></span>**tyspec- \_ CLSID**
</dt> <dd>

eine CLSID.

</dd> <dt>

<span id="TYSPEC_FILEEXT"></span><span id="tyspec_fileext"></span>**tyspec- \_ fileext**
</dt> <dd>

Eine Dateinamenerweiterung. Dieser Wert wird derzeit nicht unterstützt.

</dd> <dt>

<span id="TYSPEC_MIMETYPE"></span><span id="tyspec_mimetype"></span>**tyspec- \_ MimeType**
</dt> <dd>

Ein MIME-Typ. Dieser Wert wird derzeit nicht unterstützt.

</dd> <dt>

<span id="TYSPEC_FILENAME"></span><span id="tyspec_filename"></span>**tyspec \_ Dateiname**
</dt> <dd>

Ein Dateiname. Dieser Wert wird derzeit nicht unterstützt.

</dd> <dt>

<span id="TYSPEC_PROGID"></span><span id="tyspec_progid"></span>**tyspec- \_ ProgID**
</dt> <dd>

eine ProgID. Dieser Wert wird derzeit nicht unterstützt.

</dd> <dt>

<span id="TYSPEC_PACKAGENAME"></span><span id="tyspec_packagename"></span>**tyspec \_ PackageName**
</dt> <dd>

Ein Paketname. Dieser Wert wird derzeit nicht unterstützt.

</dd> <dt>

<span id="TYSPEC_OBJECTID"></span><span id="tyspec_objectid"></span>**tyspec \_ objectID**
</dt> <dd>

Eine Objekt-ID. Dieser Wert wird derzeit nicht unterstützt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **uclsspec** -Union ist wie folgt definiert:

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
| IDL<br/> | <dl> <dt>Wtypes. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Coinstall**](/windows/win32/api/objbase/nf-objbase-coinstall)
</dt> </dl>

 

 
