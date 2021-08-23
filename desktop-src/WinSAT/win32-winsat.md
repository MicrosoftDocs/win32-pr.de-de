---
title: Win32_WinSAT-Klasse
description: Definiert zusammenfassende Bewertungsinformationen für die letzte formale Bewertung.
ms.assetid: adf4de42-9dfd-46a7-ae75-3bbcfd15dd68
keywords:
- Win32_WinSAT WinSAT-Klasse
- Win32_WinSAT WinSAT-Klasse , beschrieben
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
ms.openlocfilehash: c0a9e863bd22cebc6609e32521b85de4bca29ae048d9673e3b09cfff2b95408f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119504530"
---
# <a name="win32_winsat-class"></a>Win32 \_ WinSAT-Klasse

\[**Win32 \_ WinSAT** kann geändert werden oder ist für Releases nach der Windows 8.1.\]

Definiert zusammenfassende Bewertungsinformationen für die letzte formale Bewertung.

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

Die **Win32 \_ WinSAT-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ WinSAT-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**CPUScore**
</dt> <dd> <dl> <dt>

Datentyp: **real32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Bewertung für die Prozessoren auf dem Computer.

</dd> <dt>

**D3DScore**
</dt> <dd> <dl> <dt>

Datentyp: **real32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Nach Windows 8.1 bewertet WinSAT nicht mehr die Funktionen für dreidimensionale Grafiken (Gaming) des Computers und die Fähigkeit des Grafiktreibers, Objekte zu rendern und Shader mithilfe dieser Bewertung auszuführen. Aus Kompatibilitäts-, WinSAT-Berichts-Sentinel-Werten für die Metriken und Bewertungen werden diese jedoch nicht in Echtzeit berechnet.

</dd> <dt>

**DiskScore**
</dt> <dd> <dl> <dt>

Datentyp: **real32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Bewertung für den sequenziellen Lesedurchsatz auf der primären Festplatte des Computers.

</dd> <dt>

**GraphicsScore**
</dt> <dd> <dl> <dt>

Datentyp: **real32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Bewertung für die Grafikfunktionen des Computers.

</dd> <dt>

**MemoryScore**
</dt> <dd> <dl> <dt>

Datentyp: **real32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Eine Bewertung für den Arbeitsspeicherdurchsatz und die Kapazität des Computers.

</dd> <dt>

**TimeTaken**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Schlüssel**
</dt> </dl>

Diese Eigenschaft muss in der WHERE-Klausel Ihrer WQL-Abfrage auf "MostRecentAssessment" festgelegt werden.

</dd> <dt>

**WinSATAssessmentState**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Status der Bewertung. Eine Beschreibung der möglichen Werte finden Sie in der [**WINSAT \_ ASSESSMENT \_ STATE-Enumeration.**](/windows/win32/api/winsatcominterfacei/ne-winsatcominterfacei-winsat_assessment_state)

<dl> <dt>

<span id="StateUnknown"></span><span id="stateunknown"></span><span id="STATEUNKNOWN"></span>**StateUnknown** (0)
</dt> <dt>

<span id="Valid"></span><span id="valid"></span><span id="VALID"></span>**Gültig** (1)
</dt> <dt>

<span id="IncoherentWithHardware"></span><span id="incoherentwithhardware"></span><span id="INCOHERENTWITHHARDWARE"></span>**IncoherentWithHardware** (2)
</dt> <dt>

<span id="NoAssessmentAvailable"></span><span id="noassessmentavailable"></span><span id="NOASSESSMENTAVAILABLE"></span>**NoAssessmentAvailable** (3)
</dt> <dt>

<span id="Invalid"></span><span id="invalid"></span><span id="INVALID"></span>**Ungültig** (4)
</dt> </dl>

</dd> <dt>

**WinSPRLevel**
</dt> <dd> <dl> <dt>

Datentyp: **real32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Basispunktzahl für den Computer. Weitere Informationen zum Bewertungswert finden Sie in der [**IProvideWinSATResultsInfo::SystemRating-Eigenschaft.**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatresultsinfo-get_systemrating)

</dd> </dl>

## <a name="remarks"></a>Hinweise

Informationen zu den Unterkomponentenbewertungen wie **MemoryScore** finden Sie in der [**IProvideWinSATAssessmentInfo::Score-Eigenschaft.**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatassessmentinfo-get_score)

## <a name="examples"></a>Beispiele

Ein Beispiel, das zeigt, wie WMI zum Abrufen von Daten aus dieser Klasse verwendet wird, finden Sie in der [**IProvideWinSATVisuals::get \_ Bitmap-Methode.**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatvisuals-get_bitmap)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                |
| Namespace<br/>                | Root\\CIMv2<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WinSAT.mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>WinSATAPI.dll</dt> </dl> |



 

 





