---
title: IConfigAsfWriter2 resetmultipassstate-Methode
description: Die resetmultipassstate-Methode setzt den Filter zurück, wenn ein Vorverarbeitungs-Codierungs Durchlauf abgebrochen wird, bevor er abgeschlossen wird.
ms.assetid: b6687af7-f3cd-4e92-9c76-dddff9063fa0
keywords:
- Resetmultipassstate-Methode, Windows Media-Format
- Resetmultipassstate-Methode, Windows Media-Format, IConfigAsfWriter2-Schnittstelle
- IConfigAsfWriter2-Schnittstelle Windows Media-Format, resetmultipassstate-Methode
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.ResetMultiPassState
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ed61e4f0517822a602f2bb88c944bba82fa1f943
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390805"
---
# <a name="iconfigasfwriter2resetmultipassstate-method"></a>IConfigAsfWriter2:: resetmultipassstate-Methode

Die **resetmultipassstate** -Methode setzt den Filter zurück, wenn ein Vorverarbeitungs-Codierungs Durchlauf abgebrochen wird, bevor er abgeschlossen wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT ResetMultiPassState();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                         | Beschreibung                                       |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                | Die Methode wurde erfolgreich ausgeführt.<br/>                  |
| <dl> <dt>**VFW \_ E \_ nicht \_ angehalten**</dt> </dl> | Der Filter befand sich nicht im beendeten Zustand.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode muss aufgerufen werden, um den internen Zustand des Filters zurückzusetzen, wenn ein Vorverarbeitungs-Codierungs Durchlauf abgebrochen wird, bevor der Filter ein Ereignis zum **abschließen des Vorgangs "EC \_ Preprocess \_** " empfangen hat. Es ist nicht erforderlich, diese Methode aufzurufen, wenn der Vorverarbeitungs-Codierungs Durchlauf ohne Fehler abgeschlossen wird.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IConfigAsfWriter2-Schnittstelle**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))
</dt> </dl>

 

