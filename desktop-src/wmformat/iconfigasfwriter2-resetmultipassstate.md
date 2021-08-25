---
title: IConfigAsfWriter2 ResetMultiPassState-Methode
description: Die ResetMultiPassState-Methode setzt den Filter zurück, wenn ein Vorverarbeitungscodierungspass abgebrochen wird, bevor er abgeschlossen wird.
ms.assetid: b6687af7-f3cd-4e92-9c76-dddff9063fa0
keywords:
- ResetMultiPassState-Methode windows Media Format
- ResetMultiPassState-Methode windows Media Format, IConfigAsfWriter2-Schnittstelle
- IConfigAsfWriter2-Schnittstelle windows Media Format , ResetMultiPassState-Methode
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.ResetMultiPassState
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1f10563ed716b6b33258fe57ff8129bff78b401170db1512566015d0b05d54dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839870"
---
# <a name="iconfigasfwriter2resetmultipassstate-method"></a>IConfigAsfWriter2::ResetMultiPassState-Methode

Die **ResetMultiPassState-Methode** setzt den Filter zurück, wenn ein Vorverarbeitungscodierungspass abgebrochen wird, bevor er abgeschlossen wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT ResetMultiPassState();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                         | Beschreibung                                       |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                | Die Methode wurde erfolgreich ausgeführt.<br/>                  |
| <dl> <dt>**VFW \_ E \_ NICHT \_ BEENDET**</dt> </dl> | Der Filter wurde nicht beendet.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode muss aufgerufen werden, um den internen Zustand des Filters zurückzusetzen, wenn ein Vorverarbeitungscodierungspass abgebrochen wird, bevor der Filter ein **EC \_ PREPROCESS \_ COMPLETE-Ereignis empfangen** hat. Es ist nicht erforderlich, diese Methode auf aufruft, wenn der Vorverarbeitungscodierungspass ohne Fehler abgeschlossen wird.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IConfigAsfWriter2-Schnittstelle**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))
</dt> </dl>

 

