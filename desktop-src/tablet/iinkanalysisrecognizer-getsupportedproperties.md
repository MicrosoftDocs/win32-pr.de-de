---
description: Ruft die global eindeutigen Bezeichner (GUIDs) für die Eigenschaften ab, die von diesem iinkanalysiserkenzer für Analyseergebnisse generiert werden können.
ms.assetid: 3a36bc6c-5067-4291-9119-bc6836d32c21
title: 'Iinkanalysiserkenzer:: GetSupportedProperties-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetSupportedProperties
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 5507e135241285b8f316d3ff3c2a4ef4d904296f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958972"
---
# <a name="iinkanalysisrecognizergetsupportedproperties-method"></a>Iinkanalysiserkenzer:: GetSupportedProperties-Methode

Ruft die global eindeutigen Bezeichner (GUIDs) für die Eigenschaften ab, die von diesem [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) für Analyseergebnisse generiert werden können.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSupportedProperties(
  [in, out] ULONG *pulPropertiesCount,
  [out]     GUID  **ppProperties
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pulpropertiescount* \[ in, out\]
</dt> <dd>

Die Anzahl der GUIDs in *ppproperties*.

</dd> <dt>

*ppproperties* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf die GUIDs von Eigenschaften, die von diesem [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) für Analyseergebnisse generiert werden können.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

> [!Caution]  
> Um einen Speicherplatz zu vermeiden, verwenden Sie " [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) ", um den Arbeitsspeicher von \* *ppproperties* freizugeben, wenn Sie die Informationen nicht mehr benötigen.

 

Eine Erkennung kann Zeilenmetriken, Zeilennummern, Vertrauens Ebenen usw. unterstützen. Eine umfassende Liste der Eigenschaften, die von einer Erkennung unterstützt werden können, finden Sie unter [erkentionproperty-Konstanten](recognitionproperty-constants.md).

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

[Erkentionproperty-Konstanten](recognitionproperty-constants.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

