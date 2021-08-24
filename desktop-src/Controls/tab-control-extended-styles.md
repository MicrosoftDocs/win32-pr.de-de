---
title: Erweiterte Stile des Registerkarten-Steuerelements (CommCtrl.h)
description: Das Registerkarten-Steuerelement unterstützt jetzt erweiterte Stile. Diese Stile werden mithilfe der \_ TCM-Meldungen GETEXTENDEDSTYLE und TCM SETEXTENDEDSTYLE bearbeitet und sollten nicht mit erweiterten Fensterstilen verwechselt werden, die an \_ CreateWindowEx übergeben werden.
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
ms.openlocfilehash: bd057a1ced7c2f594b9e4a7a2c67abe963caa270e770eebecd2f36b50f309aef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119769920"
---
# <a name="tab-control-extended-styles"></a>Erweiterte Stile des Registerkarten-Steuerelements

Das Registerkarten-Steuerelement unterstützt jetzt erweiterte Stile. Diese Stile werden mithilfe der [**\_ TCM-Meldungen GETEXTENDEDSTYLE**](tcm-getextendedstyle.md) und [**TCM \_ SETEXTENDEDSTYLE**](tcm-setextendedstyle.md) bearbeitet und sollten nicht mit erweiterten Fensterstilen verwechselt werden, die an [**CreateWindowEx übergeben werden.**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)



| Konstante                                                                                                                                                                               | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TCS_EX_FLATSEPARATORS"></span><span id="tcs_ex_flatseparators"></span><dl> <dt>**TCS \_ EX \_ FLATSEPARATORS**</dt> </dl> | [Version 4.71](common-control-versions.md). Das Registerkarten-Steuerelement zeichnen Trennzeichen zwischen den Registerkartenelementen. Dieser erweiterte Stil wirkt sich nur auf Registerkartensteuerelemente aus, die [**die STILE TCS \_ BUTTONS**](tab-control-styles.md) und [**TCS \_ FLATBUTTONS**](tab-control-styles.md) haben. Durch das Erstellen des Registerkarten-Steuerelements mit dem **TCS \_ FLATBUTTONS-Stil** wird dieser erweiterte Stil standardmäßig festgelegt. Wenn Sie keine Trennzeichen benötigen, sollten Sie diesen erweiterten Stil nach dem Erstellen des Steuerelements entfernen.<br/> |
| <span id="TCS_EX_REGISTERDROP"></span><span id="tcs_ex_registerdrop"></span><dl> <dt>**TCS \_ EX \_ REGISTERDROP**</dt> </dl>       | [Version 4.71](common-control-versions.md). Das Registerkarten-Steuerelement generiert [TCN GETOBJECT-Benachrichtigungscodes, \_ ](tcn-getobject.md) um ein Abbruchzielobjekt an fordern, wenn ein Objekt über die Registerkartenelemente im Steuerelement gezogen wird. Die Anwendung muss Vor dem [**Festlegen dieses Stils CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) oder [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) aufrufen. <br/>                                                                                                                                               |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

