---
title: Wmdmrights-Struktur
description: Die wmdmrights-Struktur beschreibt Inhalts Nutzungsrechte.
ms.assetid: 1be9167b-0d20-4a17-a42b-9696ada2b539
keywords:
- Wmdmrights-Struktur Windows Media Device Manager
- Pwmdmrights-Struktur Zeiger Windows Media-Device Manager
topic_type:
- apiref
api_name:
- WMDMRIGHTS
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff8bc3bcd61efc64d32daa3179b77a9aaa518d4f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106350784"
---
# <a name="wmdmrights-structure"></a>Wmdmrights-Struktur

Die **wmdmrights** -Struktur beschreibt Inhalts Nutzungsrechte.

## <a name="syntax"></a>Syntax


```C++
typedef struct __WMDMRIGHTS {
  UINT         cbSize;
  DWORD        dwContentType;
  DWORD        fuFlags;
  DWORD        fuRights;
  DWORD        dwAppSec;
  DWORD        dwPlaybackCount;
  WMDMDATETIME ExpirationDate;
} WMDMRIGHTS, *PWMDMRIGHTS;
```



## <a name="members"></a>Member

<dl> <dt>

**CBSIZE**
</dt> <dd>

Größe der Struktur in Bytes.

</dd> <dt>

**dwcontenttype**
</dt> <dd>

**DWORD** , das den Inhaltstyp enthält.

</dd> <dt>

**fuflags**
</dt> <dd>

Bitfeld, das die Rechte Optionen angibt, die für den Inhalt verwendet werden.



| Wert                        | BESCHREIBUNG                                  |
|------------------------------|----------------------------------------------|
| playbackcount für WMDM- \_ Rechte \_  | Gibt an, wie oft die Datei wiedergegeben werden kann. |
| WMDM- \_ Rechte \_ ExpirationDate | Ablaufdatum der Datei.                 |
| WMDM- \_ Rechte \_ freeserialids  | Der freie serielle Bezeichner der Datei.          |
| Gruppen für WMDM- \_ Rechte \_ Gruppen  | Der Bezeichner der Datei.                      |
| WMDM- \_ Rechte \_ namedserialids | Der benannte serielle Bezeichner der Datei.         |



 

</dd> <dt>

**furights**
</dt> <dd>

Bitfeld, das die Rechte Bits für den Inhalt enthält.



| Wert                                     | BESCHREIBUNG                                   |
|-------------------------------------------|-----------------------------------------------|
| WMDM- \_ Rechte \_ spielen auf dem \_ \_ PC                | Inhalt kann auf einem PC wiedergegeben werden. |
| WMDM- \_ Rechte \_ Kopie \_ auf nicht- \_ \_ SDMI- \_ Gerät kopieren | Der Inhalt kann auf ein nicht-SDMI-Gerät kopiert werden.   |
| WMDM \_ - \_ Rechte \_ in \_ CD kopieren                | Der Inhalt kann auf eine CD kopiert werden.                |
| WMDM- \_ Rechte \_ Kopie \_ auf \_ SDMI- \_ Gerät kopieren      | Der Inhalt kann auf ein SDMI-Gerät kopiert werden.      |



 

</dd> <dt>

**dwappsec**
</dt> <dd>

Bytearray, das die minimale Ebene der Anwendungssicherheit angibt.

</dd> <dt>

**dwplaybackcount**
</dt> <dd>

**DWORD** , das die Anzahl der verbleibenden Zeiten enthält, zu denen der Inhalt gerendert werden kann.

</dd> <dt>

**ExpirationDate**
</dt> <dd>

Die [**wmdmdatetime**](wmdmdatetime.md) -Struktur, die das Ablaufdatum und die Ablaufzeit für den Inhalt enthält. Wenn die Lizenz kein Ablaufdatum hat, wird das **wYear** -Element auf 0xFFFF festgelegt, und alle anderen Member von **wmdmdatetime** werden ignoriert.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imdspstorage:: GetRights**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getrights)
</dt> <dt>

[**Iwmdmstorage:: GetRights**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getrights)
</dt> <dt>

[**Wmdmdatetime**](wmdmdatetime.md)
</dt> <dt>

[**Strukturen**](structures.md)
</dt> </dl>

 

 





