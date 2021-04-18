---
description: Gibt an, ob die angegebene erkannte Zeichenfolge aus dem System Wörterbuch, dem Benutzerwörterbuch oder der Wort Liste stammt.
ms.assetid: 1504e633-5917-4ac6-b043-95d4bc75b020
title: 'Icontextnode:: isdatasestringsupported-Methode (iacom. h)'
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
ms.openlocfilehash: 93dfcdc59851aad3b06fb1451178e97b36ee0a9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345078"
---
# <a name="icontextnodeisalternatestringsupported-method"></a>Icontextnode:: isalternative estringsupported-Methode

Gibt an, ob die angegebene erkannte Zeichenfolge aus dem System Wörterbuch, dem Benutzerwörterbuch oder der Wort Liste stammt. Alle einschränkenden Daten, wie z. b. wordlists, Führungslinien oder Faktoide, werden verwendet, um zu bestimmen, ob die Zeichenfolge unterstützt wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT IsAlternateStringSupported(
  [in]  BSTR         bstrAlternateString,
  [out] VARIANT_BOOL *pfIsSupported
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrauchanestring* \[ in\]
</dt> <dd>

Erkannte Zeichenfolge zur Überprüfung.

</dd> <dt>

*pfissupported* \[ vorgenommen\]
</dt> <dd>

**Variant \_ TRUE** , wenn die angegebene Zeichenfolge von [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) mit den angewendeten entsprechenden Hinweis Knoten unterstützt wird. **Variant \_ FALSE** , wenn nicht unterstützt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

## <a name="requirements"></a>Requirements (Anforderungen)



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

 

 




