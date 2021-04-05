---
description: Ruft den Strich Bezeichner für den Strich ab, auf den durch einen Indexwert im icontextnode-Objekt verwiesen wird.
ms.assetid: faac142e-cac1-45f9-9b40-76c50ac7006b
title: 'Icontextnode:: getstrokeid-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokeId
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: b193b3719ac6b67284e3ff8c4297455888f6c9cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751841"
---
# <a name="icontextnodegetstrokeid-method"></a>Icontextnode:: getstrokeid-Methode

Ruft den Strich Bezeichner für den Strich ab, auf den durch einen Indexwert im [**icontextnode**](icontextnode.md) -Objekt verwiesen wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetStrokeId(
  [in]  ULONG ulIndex,
  [out] LONG  *plStrokeId
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ulindex* \[ in\]
</dt> <dd>

Der Index des Strichs, der zurückgegeben werden soll.

</dd> <dt>

*plstrokeid* \[ vorgenommen\]
</dt> <dd>

Der Strich Bezeichner für den Strich, auf den vom *ulindex* -Parameter innerhalb des aktuellen [**icontextnode**](icontextnode.md) -Objekts verwiesen wird.

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
</dt> <dt>

[**Icontextnode:: GetStrokeIds**](icontextnode-getstrokeids.md)
</dt> <dt>

[**Icontextnode:: getstrokecount**](icontextnode-getstrokecount.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




