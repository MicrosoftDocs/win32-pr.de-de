---
title: Win32_WinSAT-Klasse
description: Definiert Übersichts Bewertungsinformationen für die aktuellste formale Bewertung.
ms.assetid: adf4de42-9dfd-46a7-ae75-3bbcfd15dd68
keywords:
- Win32_WinSAT Klasse WinSAT
- Win32_WinSAT Klasse WinSAT, beschrieben
topic_type:
- apiref
api_name:
- Win32_WinSAT
- Win32_WinSAT.TimeTaken
- Win32_WinSAT.WinSPRLevel
- Win32_WinSAT.WinSATAssessmentState
- Win32_WinSAT.MemoryScore
- Win32_WinSAT.CPUScore
- Win32_WinSAT.DiskScore
- Win32_WinSAT.D3DScore
- Win32_WinSAT.GraphicsScore
api_location:
- WinSATAPI.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 829e5e1b3658771728aab9ef30634d90a8bc6450
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344109"
---
# <a name="win32_winsat-class"></a>Win32- \_ WinSAT-Klasse

\[**Win32 \_ WinSAT** kann nach Windows 8.1 geändert werden oder für Releases nicht verfügbar sein.\]

Definiert Übersichts Bewertungsinformationen für die aktuellste formale Bewertung.

Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.

## <a name="syntax"></a>Syntax

``` syntax
class Win32_WinSAT
{
  string TimeTaken = "MostRecentAssessment";
  real32 WinSPRLevel;
  uint32 WinSATAssessmentState;
  real32 MemoryScore;
  real32 CPUScore;
  real32 DiskScore;
  real32 D3DScore;
  real32 GraphicsScore;
};
```

## <a name="members"></a>Member

Die **Win32- \_ WinSAT** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32- \_ WinSAT** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Cpuscore**
</dt> <dd> <dl> <dt>

Datentyp: **real32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Bewertung der Prozessoren auf dem Computer.

</dd> <dt>

**D3DScore**
</dt> <dd> <dl> <dt>

Datentyp: **real32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Nach Windows 8.1 bewertet WinSAT nicht mehr die dreidimensionalen Grafikfunktionen (Gaming) des Computers, und die Fähigkeit des Grafik Treibers, Objekte zu rendern und mithilfe dieser Bewertung Shader auszuführen. Aus Kompatibilitätsgründen werden WinSAT-Werte für die Metriken und Ergebnisse in WinSAT-Berichten angezeigt. Diese werden jedoch nicht in Echtzeit berechnet.

</dd> <dt>

**Diskscore**
</dt> <dd> <dl> <dt>

Datentyp: **real32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Ergebnis für den sequenziellen Lesedurchsatz auf der primären Festplatte auf dem Computer.

</dd> <dt>

**Graphicsscore**
</dt> <dd> <dl> <dt>

Datentyp: **real32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Bewertung für die Grafikfunktionen des Computers.

</dd> <dt>

**Memoryscore**
</dt> <dd> <dl> <dt>

Datentyp: **real32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Ergebnis für den Arbeitsspeicher Durchsatz und die Kapazität des Computers.

</dd> <dt>

**TimeTaken**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Diese Eigenschaft muss in der WHERE-Klausel der WQL-Abfrage auf "mustrecentassessment" festgelegt werden.

</dd> <dt>

**Winsatbewermentstate**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Status der Bewertung. Eine Beschreibung der möglichen Werte finden Sie in der [**WinSAT- \_ Bewertungs \_ Zustands**](/windows/win32/api/winsatcominterfacei/ne-winsatcominterfacei-winsat_assessment_state) Enumeration.

<dl> <dt>

<span id="StateUnknown"></span><span id="stateunknown"></span><span id="STATEUNKNOWN"></span>**Stateunknown** (0)
</dt> <dt>

<span id="Valid"></span><span id="valid"></span><span id="VALID"></span>**Gültig** (1)
</dt> <dt>

<span id="IncoherentWithHardware"></span><span id="incoherentwithhardware"></span><span id="INCOHERENTWITHHARDWARE"></span>**Incoherent entwithhardware** (2)
</dt> <dt>

<span id="NoAssessmentAvailable"></span><span id="noassessmentavailable"></span><span id="NOASSESSMENTAVAILABLE"></span>**Nogutamentavailable** (3)
</dt> <dt>

<span id="Invalid"></span><span id="invalid"></span><span id="INVALID"></span>**Ungültig** (4)
</dt> </dl>

</dd> <dt>

**Winsprlevel**
</dt> <dd> <dl> <dt>

Datentyp: **real32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Basisbewertung für den Computer. Ausführliche Informationen zum Wert "Score" finden Sie in der [**iprovidebug**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatresultsinfo-get_systemrating) -Eigenschaft.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Informationen zu den unter Komponenten Bewertungen, wie z. b. **memoryscore**, finden Sie in der [**iprovidewinsatprocessmentinfo:: Score**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatassessmentinfo-get_score) -Eigenschaft.

## <a name="examples"></a>Beispiele

Ein Beispiel für die Verwendung von WMI zum Abrufen von Daten aus dieser Klasse finden Sie in der [**iprovidewinsatvisuals:: get- \_ Bitmap**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatvisuals-get_bitmap) -Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                |
| Namespace<br/>                | Root\\CIMv2<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WinSAT. MOF</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>WinSATAPI.dll</dt> </dl> |



 

 





