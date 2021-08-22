---
description: Gibt an, ob die angegebene erkannte Zeichenfolge aus dem Systemverzeichnis, Benutzerwörterbuch oder der Wortliste stammt.
ms.assetid: 1504e633-5917-4ac6-b043-95d4bc75b020
title: IContextNode::IsAlternateStringSupported-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.IsAlternateStringSupported
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: cbf18c63ce81a439092ba3bdabfae38c5f52882ec5364ef5c8fbd67cab5d81a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119266300"
---
# <a name="icontextnodeisalternatestringsupported-method"></a>IContextNode::IsAlternateStringSupported-Methode

Gibt an, ob die angegebene erkannte Zeichenfolge aus dem Systemverzeichnis, Benutzerwörterbuch oder der Wortliste stammt. Alle einschränkenden Daten wie Wortlisten, Leitfäden oder Factoids in einem entsprechenden Hinweisknoten werden verwendet, um zu bestimmen, ob die Zeichenfolge unterstützt wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT IsAlternateStringSupported(
  [in]  BSTR         bstrAlternateString,
  [out] VARIANT_BOOL *pfIsSupported
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrAlternateString* \[ In\]
</dt> <dd>

Erkannte Zu überprüfende Zeichenfolge.

</dd> <dt>

*pfIsSupported* \[ out\]
</dt> <dd>

**VARIANT \_ TRUE,** wenn die angegebene Zeichenfolge vom [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) mit angewendeten entsprechenden Hinweisknoten unterstützt wird. **VARIANT \_ FALSE,** wenn nicht unterstützt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Bemerkungen

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> </dl>

 

 




