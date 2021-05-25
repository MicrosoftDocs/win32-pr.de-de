---
description: Enthält Informationen zum Identifizieren des Adapters.
ms.assetid: d0d59df9-c512-4d69-b0a0-7d87d7a380f6
title: D3DADAPTER_IDENTIFIER9-Struktur (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DADAPTER_IDENTIFIER9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: db4b25cb44b3b43b3b9754f241e2c505bdfedbc7
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343395"
---
# <a name="d3dadapter_identifier9-structure"></a>D3DADAPTER \_ IDENTIFIER9-Struktur

Enthält Informationen zum Identifizieren des Adapters.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DADAPTER_IDENTIFIER9 {
  char          Driver[MAX_DEVICE_IDENTIFIER_STRING];
  char          Description[MAX_DEVICE_IDENTIFIER_STRING];
  char          DeviceName[32];
  LARGE_INTEGER DriverVersion;
  DWORD         DriverVersionLowPart;
  DWORD         DriverVersionHighPart;
  DWORD         VendorId;
  DWORD         DeviceId;
  DWORD         SubSysId;
  DWORD         Revision;
  GUID          DeviceIdentifier;
  DWORD         WHQLLevel;
} D3DADAPTER_IDENTIFIER9, *LPD3DADAPTER_IDENTIFIER9;
```



## <a name="members"></a>Member

<dl> <dt>

**Treiber**
</dt> <dd>

Typ: **char**

</dd> <dd>

Wird für die Darstellung für den Benutzer verwendet. Dies sollte nicht verwendet werden, um bestimmte Treiber zu identifizieren, da viele verschiedene Zeichenfolgen dem gleichen Gerät und Treiber von verschiedenen Anbietern zugeordnet sein können.

</dd> <dt>

**Beschreibung**
</dt> <dd>

Typ: **char**

</dd> <dd>

Wird für die Darstellung für den Benutzer verwendet.

</dd> <dt>

**Devicename**
</dt> <dd>

Typ: **char**

</dd> <dd>

Gerätename für GDI.

</dd> <dt>

**DriverVersion**
</dt> <dd>

Typ: **[ **LARGE \_ INTEGER**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**

</dd> <dd>

Identifizieren Sie die Version des Direct3D-Treibers. Es ist zulässig, vergleicht den 64-Bit-Ganzzahlwert mit Vorzeichen kleiner als und größer als zu vergleichen. Seien Sie jedoch vorsichtig, wenn Sie dieses Element verwenden, um problematische Treiber zu identifizieren. Stattdessen sollten Sie DeviceIdentifier verwenden. Siehe Hinweise.

</dd> <dt>

**DriverVersionLowPart**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Identifizieren Sie die Version des Direct3D-Treibers. Es ist gesetzlich, < und > ganzzahligen 64-Bit-Wert mit Vorzeichen zu vergleichen. Seien Sie jedoch vorsichtig, wenn Sie dieses Element verwenden, um problematische Treiber zu identifizieren. Verwenden Sie stattdessen DeviceIdentifier. Siehe Hinweise.

</dd> <dt>

**DriverVersionHighPart**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Identifizieren Sie die Version des Direct3D-Treibers. Es ist gesetzlich, < und > ganzzahligen 64-Bit-Wert mit Vorzeichen zu vergleichen. Seien Sie jedoch vorsichtig, wenn Sie dieses Element verwenden, um problematische Treiber zu identifizieren. Verwenden Sie stattdessen DeviceIdentifier. Siehe Hinweise.

</dd> <dt>

**Vendorid**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Kann verwendet werden, um einen bestimmten Chipsatz zu identifizieren. Fragen Sie diesen Member ab, um den Hersteller zu identifizieren. Der Wert kann 0 (null) sein, wenn er unbekannt ist.

</dd> <dt>

**DeviceId**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Kann verwendet werden, um einen bestimmten Chipsatz zu identifizieren. Fragen Sie diesen Member ab, um den Typ des Chipsets zu identifizieren. Der Wert kann 0 (null) sein, wenn er unbekannt ist.

</dd> <dt>

**SubSysId**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Kann verwendet werden, um einen bestimmten Chipsatz zu identifizieren. Fragen Sie dieses Element ab, um das Subsystem zu identifizieren, in der Regel das jeweilige Board. Der Wert kann 0 (null) sein, wenn er unbekannt ist.

</dd> <dt>

**Revision**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Kann verwendet werden, um einen bestimmten Chipsatz zu identifizieren. Fragen Sie diesen Member ab, um die Revisionsebene des Chipsatzes zu identifizieren. Der Wert kann 0 (null) sein, wenn er unbekannt ist.

</dd> <dt>

**DeviceIdentifier**
</dt> <dd>

Typ: **[ **GUID**](guid.md)**

</dd> <dd>

Kann abgefragt werden, um Änderungen im Treiber- und Chipsatz zu überprüfen. Diese GUID ist ein eindeutiger Bezeichner für das Treiber- und Chipsatzpaar. Fragen Sie diesen Member ab, um Änderungen am Treiber- und Chipsatz nachzuverfolgen, um ein neues Profil für das Grafiksubsystem zu generieren. DeviceIdentifier kann auch verwendet werden, um bestimmte problematische Treiber zu identifizieren.

</dd> <dt>

**WHQLLevel**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Wird verwendet, um die Windows Hardware Quality Labs -Überprüfungsebene (WHQL) für dieses Treiber- und Gerätepaar zu bestimmen. Das DWORD ist eine gepackte Datumsstruktur, die das Datum der Veröffentlichung des letzten vom Treiber bestandenen WHQL-Tests definiert. Es ist zulässig, < und > Vorgänge für diesen Wert auszuführen. Im Folgenden wird das Datumsformat veranschaulicht.



| Bits  |  BESCHREIBUNG                                             |
|-------|-----------------------------------------------|
| 31-16 | Das Jahr, eine Dezimalzahl von 1999 nach oben. |
| 15-8  | Der Monat, eine Dezimalzahl von 1 bis 12.     |
| 7-0   | Der Tag, eine Dezimalzahl von 1 bis 31.       |



 

Die folgenden Werte werden ebenfalls verwendet.



| Wert    |  BESCHREIBUNG                                                     |
|-----|-------------------------------------------------------|
| 0   | Nicht zertifiziert.                                        |
| 1   | WHQL überprüft, aber es sind keine Datumsinformationen verfügbar. |



 

Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:

Für Direct3D9Ex unter Windows Vista, Windows Server 2008, Windows 7 und Windows Server 2008 R2 (oder mehr aktuelles Betriebssystem) gibt [**IDirect3D9::GetAdapterIdentifier**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapteridentifier) 1 für die WHQL-Ebene zurück, ohne den Status des Treibers zu überprüfen.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Das folgende Pseudocodebeispiel veranschaulicht das Versionsformat, das in den Membern DriverVersion, DriverVersionLowPart und DriverVersionHighPart codiert ist.


```
Product = HIWORD(DriverVersion.HighPart)
Version = LOWORD(DriverVersion.HighPart)
SubVersion = HIWORD(DriverVersion.LowPart)
Build = LOWORD(DriverVersion.LowPart)
```



Weitere Informationen zum HIWORD-Makro, zum LOWORD-Makro und zur LARGE INTEGER-Struktur finden Sie im \_ Plattform-SDK.

MAX \_ DEVICE IDENTIFIER STRING ist eine Konstante mit der folgenden \_ \_ Definition.


```
#define MAX_DEVICE_IDENTIFIER_STRING        512
```



Die Member VendorId, DeviceId, SubSysId und Revision können zusammen verwendet werden, um bestimmte Chipsätze zu identifizieren. Verwenden Sie diese Member jedoch mit Vorsicht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
