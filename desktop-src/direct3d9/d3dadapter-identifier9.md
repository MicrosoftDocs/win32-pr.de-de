---
description: Enthält Informationen, die den Adapter identifizieren.
ms.assetid: d0d59df9-c512-4d69-b0a0-7d87d7a380f6
title: D3DADAPTER_IDENTIFIER9-Struktur (D3D9Types. h)
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
ms.openlocfilehash: 33aba75cafff5f9e69a74d5570f98455a9853289
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106350670"
---
# <a name="d3dadapter_identifier9-structure"></a>D3DADAPTER \_ IDENTIFIER9-Struktur

Enthält Informationen, die den Adapter identifizieren.

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

Wird für die Darstellung an den Benutzer verwendet. Dies sollte nicht verwendet werden, um bestimmte Treiber zu identifizieren, da viele verschiedene Zeichen folgen mit demselben Gerät und Treiber von unterschiedlichen Anbietern verknüpft werden können.

</dd> <dt>

**Beschreibung**
</dt> <dd>

Typ: **char**

</dd> <dd>

Wird für die Darstellung an den Benutzer verwendet.

</dd> <dt>

**DeviceName**
</dt> <dd>

Typ: **char**

</dd> <dd>

Der Gerätename für GDI.

</dd> <dt>

**DriverVersion**
</dt> <dd>

Typ: **[ **große \_ ganze Zahl**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**

</dd> <dd>

Identifizieren Sie die Version des Direct3D-Treibers. Es ist zulässig, kleiner als und größer als Vergleiche für den ganzzahligen Wert der 64-Bit-Ganzzahl mit Vorzeichen. Seien Sie jedoch vorsichtig, wenn Sie dieses Element verwenden, um problematische Treiber zu identifizieren. Stattdessen sollten Sie den Befehl "denviceidentifier" verwenden. Siehe Hinweise.

</dd> <dt>

**Driverversionlowpart**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Identifizieren Sie die Version des Direct3D-Treibers. Es ist zulässig, < und > Vergleiche für den Wert der 64-Bit-Ganzzahl mit Vorzeichen durchzuführen. Seien Sie jedoch vorsichtig, wenn Sie dieses Element verwenden, um problematische Treiber zu identifizieren. Stattdessen sollten Sie den Befehl "denviceidentifier" verwenden. Siehe Hinweise.

</dd> <dt>

**Driverversionhighpart**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Identifizieren Sie die Version des Direct3D-Treibers. Es ist zulässig, < und > Vergleiche für den Wert der 64-Bit-Ganzzahl mit Vorzeichen durchzuführen. Seien Sie jedoch vorsichtig, wenn Sie dieses Element verwenden, um problematische Treiber zu identifizieren. Stattdessen sollten Sie den Befehl "denviceidentifier" verwenden. Siehe Hinweise.

</dd> <dt>

**VendorID**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Kann verwendet werden, um einen bestimmten Chipsatz zu identifizieren. Fragen Sie diesen Member ab, um den Hersteller zu identifizieren. Der Wert kann NULL sein, wenn er unbekannt ist.

</dd> <dt>

**DeviceId**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Kann verwendet werden, um einen bestimmten Chipsatz zu identifizieren. Fragen Sie diesen Member ab, um den Typ der Chipmenge zu identifizieren. Der Wert kann NULL sein, wenn er unbekannt ist.

</dd> <dt>

**Subsysid**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Kann verwendet werden, um einen bestimmten Chipsatz zu identifizieren. Fragen Sie dieses Element ab, um das Subsystem, normalerweise das jeweilige Board, zu identifizieren. Der Wert kann NULL sein, wenn er unbekannt ist.

</dd> <dt>

**Novel**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Kann verwendet werden, um einen bestimmten Chipsatz zu identifizieren. Fragen Sie diesen Member ab, um die Revisions Ebene des Chipsatzes zu identifizieren. Der Wert kann NULL sein, wenn er unbekannt ist.

</dd> <dt>

**Geräte Bezeichner**
</dt> <dd>

Typ: **[ **GUID**](guid.md)**

</dd> <dd>

Kann abgefragt werden, um die Änderungen im Treiber und Chip Satz zu überprüfen. Diese GUID ist ein eindeutiger Bezeichner für das Treiber-und Chip Satz Paar. Fragen Sie dieses Element ab, um Änderungen am Treiber und Chip Satz zu verfolgen, um ein neues Profil für das Grafik Subsystem zu generieren. Der Geräte Bezeichner kann auch verwendet werden, um bestimmte problematische Treiber zu identifizieren.

</dd> <dt>

**Whqllevel**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Dient zum Bestimmen der Windows Hardware Quality Labs (WHQL)-Validierungs Ebene für dieses Treiber-und Geräte Paar. Das DWORD ist eine gepackte Datums Struktur, die das Datum der Freigabe des neuesten, vom Treiber übergebenen WHQL-Tests definiert. Es ist zulässig, <-und > Vorgänge für diesen Wert auszuführen. Im folgenden wird das Datumsformat veranschaulicht.



|       |                                               |
|-------|-----------------------------------------------|
| Bits  |                                               |
| 31-16 | Das Jahr, eine Dezimalzahl von 1999 aufwärts. |
| 15-8  | Der Monat, eine Dezimalzahl zwischen 1 und 12.     |
| 7-0   | Der Tag, eine Dezimalzahl zwischen 1 und 31.       |



 

Die folgenden Werte werden ebenfalls verwendet.



|     |                                                       |
|-----|-------------------------------------------------------|
| 0   | Nicht zertifiziert.                                        |
| 1   | WHQL wurde überprüft, aber es sind keine Datumsinformationen verfügbar. |



 

Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:

Für Direct3D9Ex, die unter Windows Vista, Windows Server 2008, Windows 7 und Windows Server 2008 R2 (oder höher) ausgeführt werden, gibt [**IDirect3D9:: getadapteridentifier**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapteridentifier) 1 für die WHQL-Ebene zurück, ohne den Status des Treibers zu überprüfen.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Im folgenden Pseudo Codebeispiel wird das Versions Format veranschaulicht, das in den Membern "DriverVersion", "driverversionlowpart" und "driverversionhighpart" codiert ist.


```
Product = HIWORD(DriverVersion.HighPart)
Version = LOWORD(DriverVersion.HighPart)
SubVersion = HIWORD(DriverVersion.LowPart)
Build = LOWORD(DriverVersion.LowPart)
```



Weitere Informationen über das HIWORD-Makro, das LoWord-Makro und die große ganzzahlige Struktur finden Sie im Platform SDK \_ .

\_ \_ \_ Die Zeichenfolge für die maximale Gerätekennung ist eine Konstante mit der folgenden Definition.


```
#define MAX_DEVICE_IDENTIFIER_STRING        512
```



Die Elemente VendorID, de viceid, subsysid und Revision können zusammen verwendet werden, um bestimmte Chip Sätze zu identifizieren. Verwenden Sie diese Member jedoch mit Bedacht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
