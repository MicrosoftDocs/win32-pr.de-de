---
title: WMDMRIGHTS-Struktur
description: Die WMDMRIGHTS-Struktur beschreibt Inhaltsnutzungsrechte.
ms.assetid: 1be9167b-0d20-4a17-a42b-9696ada2b539
keywords:
- WMDMRIGHTS-Strukturfenster Media Geräte-Manager
- PWMDMRIGHTS-Strukturzeigerfenster Media Geräte-Manager
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
ms.openlocfilehash: 6b54713add3bef1c51d18fea3f66ac4b3e2e8ff1a066bcd83781f0f522d5a4be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118583983"
---
# <a name="wmdmrights-structure"></a>WMDMRIGHTS-Struktur

Die **WMDMRIGHTS-Struktur** beschreibt Inhaltsnutzungsrechte.

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

**cbSize**
</dt> <dd>

Größe der -Struktur in Bytes.

</dd> <dt>

**dwContentType**
</dt> <dd>

**DWORD,** das den Inhaltstyp enthält.

</dd> <dt>

**fuFlags**
</dt> <dd>

Bitfeld, das die für den Inhalt zu verwendenden Rechteoptionen an gibt.



| Wert                        | BESCHREIBUNG                                  |
|------------------------------|----------------------------------------------|
| WMDM \_ RIGHTS \_ PLAYBACKCOUNT  | Gibt an, wie oft die Datei abgespielt werden kann. |
| WMDM \_ RIGHTS \_ EXPIRATIONDATE | Ablaufdatum der Datei.                 |
| WMDM \_ RIGHTS \_ FREESERIALIDS  | Freier serieller Bezeichner der Datei.          |
| WMDM \_ RIGHTS \_ GROUPID Group  | Bezeichner der Datei.                      |
| WMDM \_ RIGHTS \_ NAMEDSERIALIDS | Benannter serieller Bezeichner der Datei.         |



 

</dd> <dt>

**fuRights**
</dt> <dd>

Bitfeld, das die Rechtebits für den Inhalt enthält.



| Wert                                     | BESCHREIBUNG                                   |
|-------------------------------------------|-----------------------------------------------|
| WMDM \_ RIGHTS PLAY AUF DEM \_ \_ \_ PC                | Inhalte können auf einem PC abgespielt werden. |
| WMDM \_ RIGHTS COPY TO NON \_ SDMI DEVICE (WMDM-RECHTEKOPIE AUF EIN \_ \_ \_ NICHT-SDMI-GERÄT) \_ | Inhalte können auf ein Nicht-SDMI-Gerät kopiert werden.   |
| WMDM \_ RIGHTS \_ COPY \_ TO \_ CD                | Inhalte können auf eine CD kopiert werden.                |
| WMDM \_ RIGHTS COPY TO \_ SDMI DEVICE (WMDM-RECHTEKOPIE AUF \_ \_ SDMI-GERÄT) \_      | Inhalte können auf ein SDMI-Gerät kopiert werden.      |



 

</dd> <dt>

**dwAppSec**
</dt> <dd>

Bytearray, das die Mindestsicherheitsstufe der Anwendung angibt.

</dd> <dt>

**dwPlaybackCount**
</dt> <dd>

**DWORD** mit der Anzahl der verbleibenden Male, die der Inhalt gerendert werden kann.

</dd> <dt>

**ExpirationDate**
</dt> <dd>

[**WMDMDATETIME-Struktur,**](wmdmdatetime.md) die das Ablaufdatum und die Uhrzeit für den Inhalt enthält. Wenn die Lizenz kein Ablaufdatum hat, wird **das wYear-Mitglied** auf 0xFFFF festgelegt, und alle anderen Mitglieder von **WMDMDATETIME** werden ignoriert.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wmdm.idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMDSPStorage::GetRights**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getrights)
</dt> <dt>

[**IWMDMStorage::GetRights**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getrights)
</dt> <dt>

[**WMDMDATETIME**](wmdmdatetime.md)
</dt> <dt>

[**Strukturen**](structures.md)
</dt> </dl>

 

 





