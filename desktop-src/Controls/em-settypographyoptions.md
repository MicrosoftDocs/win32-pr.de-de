---
title: EM_SETTYPOGRAPHYOPTIONS Meldung (RichEdit. h)
description: Legt den aktuellen Zustand der Typografieoptionen eines Rich-Edit-Steuer Elements fest.
ms.assetid: 000e72a6-3f8c-4735-8190-3ac06a2206ac
keywords:
- Windows-Steuerelemente für EM_SETTYPOGRAPHYOPTIONS Meldung
topic_type:
- apiref
api_name:
- EM_SETTYPOGRAPHYOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0528e19aacec394c5af6250536fdc4f693e60ece
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956633"
---
# <a name="em_settypographyoptions-message"></a>EM \_ settypographyoptions-Meldung

Legt den aktuellen Zustand der Typografieoptionen eines Rich-Edit-Steuer Elements fest.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Gibt einen oder beide der folgenden Werte an.



| Wert                                                                                                                                                                                    | Bedeutung                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="TO_ADVANCEDTYPOGRAPHY_"></span><span id="to_advancedtypography_"></span><dl> <dt>**An \_ Advancedtypografie**</dt> </dl> | Erweiterte Zeilenumbruch und Zeilen Formatierung sind aktiviert. <br/>                    |
| <span id="TO_SIMPLELINEBREAK"></span><span id="to_simplelinebreak"></span><dl> <dt>**an \_ simplelinebreak**</dt> </dl>             | Schnelleres Zeilenumbruch bei einfachem Text ( **erfordert \_ advancedtypografie**). <br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Eine Maske, die aus einem oder mehreren der Flags in *wParam* besteht. Nur die Flags, die in dieser Maske festgelegt sind, werden festgelegt oder gelöscht. Dadurch kann ein einzelnes Flag festgelegt oder gelöscht werden, ohne die aktuellen flagzustände zu lesen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn *wParam* gültig ist, andernfalls **false**.

## <a name="remarks"></a>Bemerkungen

Der erweiterte Zeilenumbruch wird automatisch durch das Rich Edit-Steuerelement aktiviert, z. b. für die Behandlung komplexer Skripts wie Arabisch und Hebräisch und für Mathematik. Es ist auch für begründete Absätze, Bindestriche und andere typografische Features erforderlich.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Verteilbare Komponente<br/>          | Rich Edit 3,0<br/>                                                              |
| Header<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EM \_ gettypographyoptions**](em-gettypographyoptions.md)
</dt> </dl>

 

 





