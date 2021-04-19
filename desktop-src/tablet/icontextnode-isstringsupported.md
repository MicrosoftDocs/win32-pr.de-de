---
description: Gibt an, ob die erkannte Zeichenfolge dieses icontextnode aus dem System Wörterbuch, dem Benutzerwörterbuch oder der Wort Liste stammt.
ms.assetid: 9eaee549-ae78-4a67-a39e-2096c7d5d9cd
title: 'Icontextnode:: IsStringSupported-Methode (iacom. h)'
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
ms.openlocfilehash: 853b244cdd6f9e61d4474876190daeccaa2c8779
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357352"
---
# <a name="icontextnodeisstringsupported-method"></a>Icontextnode:: IsStringSupported-Methode

Gibt an, ob die erkannte Zeichenfolge dieses [**icontextnode**](icontextnode.md) aus dem System Wörterbuch, dem Benutzerwörterbuch oder der Wort Liste stammt.

## <a name="syntax"></a>Syntax


```C++
HRESULT IsStringSupported(
  [out, retval] VARIANT_BOOL *pfIsSupported
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pfissupported* \[ Out, retval\]
</dt> <dd>

**Variant \_ TRUE** , wenn der erkannte Zeichen folgen Wert dieses [**icontextnode**](icontextnode.md) von [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) unterstützt wird, wenn alle entsprechenden Hinweis Knoten angewendet werden. Andernfalls ist der Wert **\_ false**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

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
</dt> </dl>

 

 




