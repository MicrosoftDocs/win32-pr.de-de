---
description: Ruft den Bereich des Dokuments ab, der den Änderungen entspricht, die in der Kontext Knoten Struktur des iinkanalyzer-Objekts als Ergebnis einer frei Hand Analyse vorgenommen wurden.
ms.assetid: 25d511fb-ba2d-4c46-8a8c-8bb4187c9a5c
title: 'Ianalysisstatus:: getappliedchangesregion-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisStatus.GetAppliedChangesRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 08f6690091207b648c39cded161de64585e44b41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526546"
---
# <a name="ianalysisstatusgetappliedchangesregion-method"></a>Ianalysisstatus:: getappliedchangesregion-Methode

Ruft den Bereich des Dokuments ab, der den Änderungen entspricht, die in der Kontext Knoten Struktur des [**iinkanalyzer**](iinkanalyzer.md) -Objekts als Ergebnis einer frei Hand Analyse vorgenommen wurden.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetAppliedChangesRegion(
  [out] IAnalysisRegion **pAppliedChangesRegion
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pappliedchangesregion* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf den [**ianalysisregion**](ianalysisregion.md) des Dokuments, in dem Änderungen vorgenommen wurden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

> [!Caution]  
> Um einen Speicherplatz zu vermeiden, rufen Sie [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf \* *pappliedchangesregion* auf, wenn Sie den Analysebereich nicht mehr verwenden müssen.

 

Diese Methode wird am häufigsten verwendet, wenn die Anwendung Informationen zu Debuggingzwecken empfängt und den Bereich für ungültig erklären muss, in dem Änderungen auftreten können, damit die Debuginformationen gezeichnet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Iacom. h (erfordert auch iacom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ianalysisstatus**](ianalysisstatus.md)
</dt> <dt>

[**Ianalysisregion**](ianalysisregion.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

