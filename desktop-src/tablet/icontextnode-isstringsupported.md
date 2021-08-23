---
description: Gibt an, ob die erkannte Zeichenfolge dieses IContextNode aus dem Systemwörterbuch, Benutzerwörterbuch oder der Wortliste stammt.
ms.assetid: 9eaee549-ae78-4a67-a39e-2096c7d5d9cd
title: IContextNode::IsStringSupported-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.IsStringSupported
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2eef383f059897665c013e3575d452564295ccd9bd014ae8084fd1635892bd99
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119709110"
---
# <a name="icontextnodeisstringsupported-method"></a>IContextNode::IsStringSupported-Methode

Gibt an, ob die erkannte Zeichenfolge dieses [**IContextNode**](icontextnode.md) aus dem Systemwörterbuch, Benutzerwörterbuch oder der Wortliste stammt.

## <a name="syntax"></a>Syntax


```C++
HRESULT IsStringSupported(
  [out, retval] VARIANT_BOOL *pfIsSupported
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pfIsSupported* \[ out, retval\]
</dt> <dd>

**VARIANT \_ TRUE,** wenn der erkannte Zeichenfolgenwert dieses [**IContextNode**](icontextnode.md) vom [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) mit allen entsprechenden angewendeten Hinweisknoten unterstützt wird; andernfalls **VARIANT \_ FALSE**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen – Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> </dl>

 

 




