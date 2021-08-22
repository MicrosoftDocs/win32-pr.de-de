---
title: IDWriteTextLayout3-Schnittstelle
description: Stellt einen Textblock dar, nachdem er vollständig analysiert und formatiert wurde. | IDWriteTextLayout3-Schnittstelle
ms.assetid: a7741740-9524-caf0-650b-56808abcf328
keywords:
- IDWriteTextLayout3-Schnittstelle – Direkter Schreibzugriff
- IDWriteTextLayout3-Schnittstelle Direct Write , beschrieben
topic_type:
- apiref
api_name:
- IDWriteTextLayout3
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f3a6d441c3f7d8ac9bf356bd835f800e026f8c6e27cb083a57ced571ba68fe8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070650"
---
# <a name="idwritetextlayout3-interface"></a>IDWriteTextLayout3-Schnittstelle

Stellt einen Textblock dar, nachdem er vollständig analysiert und formatiert wurde.

## <a name="members"></a>Member

Die **IDWriteTextLayout3-Schnittstelle** erbt von [**IDWriteTextLayout2.**](idwritetextlayout2.md) **IDWriteTextLayout3** verfügt auch über die folgenden Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IDWriteTextLayout3-Schnittstelle** verfügt über diese Methoden.



| Methode                                                          | Beschreibung                                                                                                                                                                                                                                                          |
|:----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetLineMetrics**](idwritetextlayout3-getlinemetrics.md)     | Ruft die Eigenschaften jeder Zeile ab.<br/>                                                                                                                                                                                                                        |
| [**GetLineSpacing**](idwritetextlayout3-getlinespacing.md)     | Ruft Zeilenabstandsinformationen ab.<br/>                                                                                                                                                                                                                            |
| [**InvalidateLayout**](idwritetextlayout3-invalidatelayout.md) | Erklärt das Layout für ungültig und erzwingt, dass das Layout vor dem Aufrufen der Metriken oder Zeichnungsfunktionen neu messen muss. Dies ist nützlich, wenn sich die Lokalität einer Schriftart ändert und das Layout neu gezeichnet werden soll, oder wenn sich die Größe eines von einem Client implementierten IDWriteInlineObject ändert. <br/> |
| [**SetLineSpacing**](idwritetextlayout3-setlinespacing.md)     | Legen Sie den Zeilenabstand fest.<br/>                                                                                                                                                                                                                                         |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Desktop-Apps \| UWP-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[R2-Desktop-Apps \| UWP-Apps\]<br/>                          |
| Unterstützte Mindestversion (Telefon)<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 und Windows Runtime-Apps\]<br/> |
| Bibliothek<br/>                  | <dl> <dt>Dwrite.lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IDWriteTextLayout2**](idwritetextlayout2.md)
</dt> </dl>

 

 





