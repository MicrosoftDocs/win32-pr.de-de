---
description: Ruft die Funktionen des Erkennungs Moduls ab.
ms.assetid: 9014bd9b-54fb-4735-9eb8-56a6188a5fc0
title: 'Iinkanalysiserkenzer:: getfunktionalitäten-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetCapabilities
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 07b66ffbed6f3e57edb8a6bfad36959fabbc047c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129477"
---
# <a name="iinkanalysisrecognizergetcapabilities-method"></a>Iinkanalysiserkenzer:: getfunktionalitäten-Methode

Ruft die Funktionen des Erkennungs Moduls ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetCapabilities(
  [out] InkAnalysisRecognizerCapabilities *pCapabilities
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pfunktionen* \[ vorgenommen\]
</dt> <dd>

Eine bitweise Kombination von [**Erkennungsfunktionen**](recognizercapabilities.md) -Werten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Dieser Wert ist für jede [ **iinkanalysiserkenzer** konstant.](iinkanalysisrecognizer.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Iacom. h (erfordert auch iacom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iinkanalysiserkenzer**](iinkanalysisrecognizer.md)
</dt> <dt>

[**Erkennungsfunktionen**](recognizercapabilities.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




