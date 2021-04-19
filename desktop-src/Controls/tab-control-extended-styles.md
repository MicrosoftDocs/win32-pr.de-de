---
title: Erweiterte Stile des Register Steuer Elements (kommstrg. h)
description: Das Registerkarten-Steuerelement unterstützt jetzt erweiterte Stile. Diese Stile werden mithilfe der \_ Nachrichten TCM GetExtendedStyle und TCM- \_ textendedstyle manipuliert und sollten nicht mit erweiterten Fenster Stilen verwechselt werden, die an "kreatewindowex" übergeben werden.
ms.assetid: 24294037-598c-4fcd-8a7c-8647ccfb1d81
topic_type:
- apiref
api_name:
- TCS_EX_FLATSEPARATORS
- TCS_EX_REGISTERDROP
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c4e16b40a394bc9b808386d3cbdc3abf9b3d928
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360416"
---
# <a name="tab-control-extended-styles"></a>Erweiterte Stile des Register Steuer Elements

Das Registerkarten-Steuerelement unterstützt jetzt erweiterte Stile. Diese Stile werden mithilfe der Nachrichten [**TCM \_ GetExtendedStyle**](tcm-getextendedstyle.md) und [**TCM- \_ textendedstyle**](tcm-setextendedstyle.md) manipuliert und sollten nicht mit erweiterten Fenster Stilen verwechselt werden, die an " [**kreatewindowex**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)" übergeben werden.



| Konstante                                                                                                                                                                               | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TCS_EX_FLATSEPARATORS"></span><span id="tcs_ex_flatseparators"></span><dl> <dt>**TCS \_ Ex- \_ flatseparatoren**</dt> </dl> | [Version 4,71](common-control-versions.md). Das Registerkarten-Steuerelement zeichnet Trennzeichen zwischen den Registerkarten Elementen. Dieser erweiterte Stil wirkt sich nur auf Registerkarten Steuerelemente aus, die über die [**TCS- \_ Schalt**](tab-control-styles.md) Flächen und die [**TCS- \_ FlatButtons**](tab-control-styles.md) Standardmäßig wird durch das Erstellen des Registerkarten-Steuer Elements mit dem **TCS- \_ FlatButtons** -Stil dieser erweiterte Stil festgelegt. Wenn Sie keine Trennzeichen benötigen, sollten Sie diese erweiterte Formatvorlage nach dem Erstellen des Steuer Elements entfernen.<br/> |
| <span id="TCS_EX_REGISTERDROP"></span><span id="tcs_ex_registerdrop"></span><dl> <dt>**TCS \_ Ex \_ registerdrop**</dt> </dl>       | [Version 4,71](common-control-versions.md). Das Registerkarten-Steuerelement generiert [TCN \_ GetObject](tcn-getobject.md) -Benachrichtigungs Codes, um ein Ablage Zielobjekt anzufordern, wenn ein Objekt über die Registerkarten Elemente im Steuerelement gezogen wird. Die Anwendung muss vor dem Festlegen dieses Stils [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) oder [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) aufruft. <br/>                                                                                                                                               |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Kommstrg. h</dt> </dl> |



 

