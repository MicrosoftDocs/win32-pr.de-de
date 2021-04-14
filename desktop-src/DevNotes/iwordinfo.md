---
description: Die iwordinfo-Schnittstelle ist eine Japanisch-spezifische Sprachressourcen Komponente. Das-Objekt analysiert Text und identifiziert einzelne Wörter, wobei entweder die Wörter in der Zeichenfolge zurückgegeben werden oder die Wörterbuch Formen (root) der Wörter im Text der Zeichenfolge zurückgegeben werden.
ms.assetid: 760d9c78-d564-40a2-b2e4-d538c32361ed
title: Iwordinfo-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordInfo
- IWordInfo.BreakText
api_type:
- COM
api_location:
- Msir3jp.dll
ms.openlocfilehash: 9d685f2aa1b4ba4d31f221812c12729e4e689360
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104522976"
---
# <a name="iwordinfo-interface"></a>Iwordinfo-Schnittstelle

\[Diese Schnittstelle ist veraltet und wird unter Windows Vista nicht unterstützt.\]

Die **iwordinfo** -Schnittstelle ist eine Japanisch-spezifische Sprachressourcen Komponente. Das-Objekt analysiert Text und identifiziert einzelne Wörter, wobei entweder die Wörter in der Zeichenfolge zurückgegeben werden oder die Wörterbuch Formen (root) der Wörter im Text der Zeichenfolge zurückgegeben werden.

## <a name="members"></a>Member

Die **iwordinfo** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iwordinfo** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iwordinfo** -Schnittstelle verfügt über diese Methoden.



| Methode        | BESCHREIBUNG                                                                                                                                 |
|:--------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| **Halte Text** | Analysiert Text, um die Wörter zu identifizieren, und stellt die Ergebnisse für das [wordsink](/previous-versions//ms691570(v=vs.85)) -Objekt bereit.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Schnittstelle wird verwendet, um japanische Wort Umbrüche oder Wörterbuch Formulare für den zu analysierenden Text abzurufen. Die Wörterbuch Form eines Worts ist die unflexions Form des Worts.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                   |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                  |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                         |
| DLL<br/>                      | <dl> <dt>Msir3jp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WordInfo**](wordinfo-coclass.md)
</dt> <dt>

[Wordsink](/previous-versions//ms691570(v=vs.85))
</dt> </dl>

 

 
