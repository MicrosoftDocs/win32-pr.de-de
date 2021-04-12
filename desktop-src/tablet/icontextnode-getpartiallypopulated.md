---
description: Ruft den Wert ab, der angibt, ob ein icontextnode-Objekt teilweise aufgefüllt oder vollständig ausgefüllt ist.
ms.assetid: 13ac3fb2-7baa-48d7-bf8e-f36b4031fbc4
title: 'Icontextnode:: getpartiallygefüllte-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetPartiallyPopulated
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4b05cb8aae681a7302ae7da40a7412cf828fc159
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129501"
---
# <a name="icontextnodegetpartiallypopulated-method"></a>Icontextnode:: getpartiallygefüllte-Methode

Ruft den Wert ab, der angibt, ob ein [**icontextnode**](icontextnode.md) -Objekt teilweise aufgefüllt oder vollständig ausgefüllt ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetPartiallyPopulated(
  [out] VARIANT_BOOL *pfPartiallyPopulated
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pfpartiallyausgefüllt* \[ vorgenommen\]
</dt> <dd>

**Variant \_ TRUE** , wenn dieses [**icontextnode**](icontextnode.md) -Objekt keine kompletten Daten enthält. Andernfalls ist der Wert **\_ false**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Methode, wenn Ihre Anwendung ihre eigene Datenstruktur verwaltet, die mit der von [**iinkanalyzer**](iinkanalyzer.md)synchronisiert wird. Weitere Informationen finden Sie unter [Daten Proxy mit Ink-Analyse](data-proxy-with-ink-analysis.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Iacom. h (erfordert auch iacom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Icontextnode**](icontextnode.md)
</dt> <dt>

[**Icontextnode:: setpartiallyaufgefüllt**](icontextnode-setpartiallypopulated.md)
</dt> <dt>

[**Icontextnode:: kreatepartiallypopulatedsubnode**](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[**\_Ianalysisproxyevents::P opulatecontextnode**](-ianalysisproxyevents-populatecontextnode.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




