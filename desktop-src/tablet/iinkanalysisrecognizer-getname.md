---
description: Ruft den Namen der Erkennung ab.
ms.assetid: bd97fead-1e80-49dc-ada0-38eb5dc015ae
title: IInkAnalysisRecognizer::GetName-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetName
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: df86f5526a6b28f8a7f383ddfb49ca999875b8aa08c66e07a9ac95c41acd13cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773620"
---
# <a name="iinkanalysisrecognizergetname-method"></a>IInkAnalysisRecognizer::GetName-Methode

Ruft den Namen der Erkennung ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetName(
  [out] BSTR *pbstrName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbstrName* \[ out\]
</dt> <dd>

Der Name der Erkennung.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Hinweise

> [!Caution]  
> Um einen Speicherverlust zu vermeiden, rufen Sie [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) für \* *pbstrName* auf, wenn Sie die Zeichenfolge nicht mehr verwenden müssen.

 

Der Name ist für die regionsneutrale Sprache lokalisiert, die von der Erkennung unterstützt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

