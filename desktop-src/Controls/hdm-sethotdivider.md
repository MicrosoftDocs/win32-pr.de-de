---
title: HDM_SETHOTDIVIDER Meldung (kommstrg. h)
description: Ändert die Farbe eines unter Teilers zwischen Header Elementen, um das Ziel eines externen Drag & Drop-Vorgangs anzugeben. Sie können diese Nachricht explizit senden oder das-Header-" \_ lthotdivider"-Makro verwenden.
ms.assetid: 56f6e5c6-1df3-4b4d-9ad8-97fb168c5462
keywords:
- Windows-Steuerelemente für HDM_SETHOTDIVIDER Meldung
topic_type:
- apiref
api_name:
- HDM_SETHOTDIVIDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feb894100878e9b3ee85e8e8367a4b81a022a0a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103551"
---
# <a name="hdm_sethotdivider-message"></a>HDM- \_ Nachricht

Ändert die Farbe eines unter Teilers zwischen Header Elementen, um das Ziel eines externen Drag & Drop-Vorgangs anzugeben. Sie können diese Nachricht explizit senden oder das- [**Header-" \_ lthotdivider**](/windows/desktop/api/Commctrl/nf-commctrl-header_sethotdivider) "-Makro verwenden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Der Typ des durch *LPARAM* dargestellten Werts. Die folgenden Werte sind möglich:



| Wert                                                                                                                                    | Bedeutung                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <dt>TRUE * * * *</dt> </dl>    | Gibt an, dass *LPARAM* die Client Koordinaten des Zeigers enthält.<br/> |
| <span id="FALSE"></span><span id="false"></span><dl> <dt>FALSE * * * *</dt> </dl> | Gibt an, dass *LPARAM* einen unter Teiler-Indexwert enthält.<br/>                 |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ein in *LPARAM* gehaltene Wert wird abhängig vom Wert von *wParam* interpretiert.

Wenn *wParam* den Wert **true** hat, stellt *LPARAM* die x-und y-Koordinaten des Zeigers dar. Die x-Koordinate ist das niedrige Wort, und die y-Koordinate befindet sich im hohen Wort. Wenn das Header Steuerelement die Nachricht empfängt, wird der entsprechende unter Teiler basierend auf den *LPARAM* -Koordinaten hervorgehoben.

Wenn *wParam* den Wert **false** hat, stellt *LPARAM* den ganzzahligen Index des unter Teilers dar, der hervorgehoben werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert zurück, der gleich dem Index des unter Teilers ist, den das Steuerelement hervorgehoben hat.

## <a name="remarks"></a>Bemerkungen

Diese Meldung erzeugt einen Effekt, den ein Header Steuerelement automatisch erzeugt, wenn es den [**HDS \_ DragDrop**](header-control-styles.md) -Stil aufweist. Die **HDM-Nachricht " \_ sthotdivider** " soll verwendet werden, wenn der Besitzer des Steuer Elements Drag & Drop-Vorgänge manuell behandelt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |



 

 





