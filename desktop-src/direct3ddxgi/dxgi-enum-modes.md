---
description: Optionen für das Auflisten der Anzeigemodi.
ms.assetid: 7e0f5629-f8e2-478b-b8eb-00780a3dcf1f
title: DXGI_ENUM_MODES (dxgi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 056ad959f0b86fb6f357d690f2daab908275e038
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353714"
---
# <a name="dxgi_enum_modes"></a>DXGI- \_ Enum- \_ Modi

Optionen für das Auflisten der Anzeigemodi.



| Konstante/Wert                                                                                                                                                                                                                                                                  | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                     |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DXGI_ENUM_MODES_INTERLACED"></span><span id="dxgi_enum_modes_interlaced"></span><dl> <dt>**DXGI \_ Enum \_ - \_ Modi**</dt> mit Zeilen Sprung <dt>1UL</dt> </dl>                 | Zeilen Sprung Modi einschließen.<br/>                                                                                                                                                                                                                                                                                                            |
| <span id="DXGI_ENUM_MODES_SCALING"></span><span id="dxgi_enum_modes_scaling"></span><dl> <dt>**DXGI \_ Enum- \_ Modi \_ skalieren**</dt> von <dt>2ul</dt> </dl>                          | Schließt den Modus für die gestreckte Skalierung ein<br/>                                                                                                                                                                                                                                                                                                     |
| <span id="DXGI_ENUM_MODES_STEREO"></span><span id="dxgi_enum_modes_stereo"></span><dl> <dt>**DXGI \_ Enum- \_ Modi \_ Stereo**</dt> <dt>4ul</dt> </dl>                             | Fügen Sie Stereo Modi ein.<br/> **Direct3D 11:** Dieser Enumerationswert wird ab Windows 8 unterstützt.<br/>                                                                                                                                                                                                                       |
| <span id="DXGI_ENUM_MODES_DISABLED_STEREO"></span><span id="dxgi_enum_modes_disabled_stereo"></span><dl> <dt>**DXGI \_ Enum- \_ Modi \_ deaktiviert \_ Stereo**</dt> <dt>8ul</dt> </dl> | Fügen Sie Stereo Modi ein, die ausgeblendet sind, da der Benutzer Stereo deaktiviert hat. System Steuerungsanwendungen können diese Option verwenden, um Stereo Funktionen anzuzeigen, die als Teil einer Benutzeroberfläche deaktiviert wurden, die Stereo aktiviert und deaktiviert.<br/> **Direct3D 11:** Dieser Enumerationswert wird ab Windows 8 unterstützt.<br/> |



## <a name="remarks"></a>Bemerkungen

Diese Flagoptionen werden in [**idxgioutput:: getdisplaymodelist**](/windows/desktop/api/DXGI/nf-dxgi-idxgioutput-getdisplaymodelist) zum Auflisten der Anzeigemodi verwendet.

Diese Flagoptionen werden auch in [**IDXGIOutput1:: GetDisplayModeList1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-getdisplaymodelist1) zum Auflisten der Anzeigemodi verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>DXGI. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DXGI-Konstanten](d3d10-graphics-reference-dxgi-constants.md)
</dt> </dl>

 

 




