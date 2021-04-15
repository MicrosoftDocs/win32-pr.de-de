---
description: Ruft Analyse Informationen aus dem InkDivider-Objekt ab.
ms.assetid: 1b073da4-80f4-48f4-8ff6-b21793c173a8
title: Calldivide-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CallDivide
api_type:
- LibDef
api_location:
- InkDiv.dll
- InkDiv.dll.dll
ms.openlocfilehash: 0084811ee471bee8fe67653dace49fa83642a7fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524403"
---
# <a name="calldivide-function"></a>Calldivide-Funktion

Ruft Analyse Informationen aus dem [**InkDivider**](inkdivider-class.md) -Objekt ab.

Diese Funktion ist nicht für die Verwendung durch den Anwendungscode vorgesehen.

## <a name="syntax"></a>Syntax


```C++
HRESULT WINAPI CallDivide(
  _In_  INT_PTR hDivider,
  _In_  int     *pWordSize,
  _In_  int     *pLineSize,
  _In_  int     *pParagraphSize,
  _In_  int     *pDrawingSize,
  _Out_ int     *pWordCount,
  _Out_ int     *pLineCount,
  _Out_ int     *pParagraphCount
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hdivider* \[ in\]
</dt> <dd>

Ein Handle für das [**InkDivider**](inkdivider-class.md) -Objekt.

</dd> <dt>

*pwordsize* \[ in\]
</dt> <dd>

Die Größe des vom [**InkDivider**](inkdivider-class.md) -Objekt zurückgegebenen Worts.

</dd> <dt>

*plinesize* \[ in\]
</dt> <dd>

Die Größe der Zeile, die vom [**InkDivider**](inkdivider-class.md) -Objekt zurückgegeben wird.

</dd> <dt>

*pparagphsize* \[ in\]
</dt> <dd>

Die Größe des vom [**InkDivider**](inkdivider-class.md) -Objekt zurückgegebenen Absatzes.

</dd> <dt>

*pdrawingsize* \[ in\]
</dt> <dd>

Die Größe der Zeichnung, die vom [**InkDivider**](inkdivider-class.md) -Objekt zurückgegeben wird.

</dd> <dt>

*pwordcount* \[ vorgenommen\]
</dt> <dd>

Die Anzahl der von der Ink-Analyse zurückgegebenen Wörter.

</dd> <dt>

*plinecount* \[ vorgenommen\]
</dt> <dd>

Die Anzahl der Zeilen, die von der Ink-Analyse zurückgegeben werden

</dd> <dt>

*pparagphcount* \[ vorgenommen\]
</dt> <dd>

Die Anzahl von Absätzen, die von der Ink-Analyse zurückgegeben werden

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion kann einen dieser Werte zurückgeben.



| Rückgabecode                                                                                  | Beschreibung                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Die Funktion, die unterstützt wird.<br/>              |
| <dl> <dt>**E \_ invalidArg**</dt> </dl> | Mindestens ein Parameter ist ungültig.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                         |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                             |
| Bibliothek<br/>                  | <dl> <dt>InkDiv.dll</dt> </dl> |



 

 




