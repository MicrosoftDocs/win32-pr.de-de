---
title: IDWriteTextLayout3-Schnittstelle
description: Stellt einen TextBlock dar, nachdem er vollständig analysiert und formatiert wurde. | IDWriteTextLayout3-Schnittstelle
ms.assetid: a7741740-9524-caf0-650b-56808abcf328
keywords:
- IDWriteTextLayout3 Interface Direct Write
- IDWriteTextLayout3 Interface Direct Write, beschrieben
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
ms.openlocfilehash: 78a7a9203245939e40b522e0ef5998be0764085a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106355146"
---
# <a name="idwritetextlayout3-interface"></a>IDWriteTextLayout3-Schnittstelle

Stellt einen TextBlock dar, nachdem er vollständig analysiert und formatiert wurde.

## <a name="members"></a>Member

Die **IDWriteTextLayout3** -Schnittstelle erbt von [**IDWriteTextLayout2**](idwritetextlayout2.md). **IDWriteTextLayout3** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IDWriteTextLayout3** -Schnittstelle verfügt über diese Methoden.



| Methode                                                          | BESCHREIBUNG                                                                                                                                                                                                                                                          |
|:----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetLineMetrics**](idwritetextlayout3-getlinemetrics.md)     | Ruft die Eigenschaften der einzelnen Zeilen ab.<br/>                                                                                                                                                                                                                        |
| [**GetLineSpacing**](idwritetextlayout3-getlinespacing.md)     | Ruft Informationen zum Zeilenabstand ab.<br/>                                                                                                                                                                                                                            |
| [**Invalidatelayout**](idwritetextlayout3-invalidatelayout.md) | Macht das Layout ungültig und erzwingt, dass das Layout neu gemessen wird, bevor die Metriken oder Zeichnungsfunktionen aufgerufen werden. Dies ist hilfreich, wenn sich die Position einer Schriftart ändert und das Layout neu gezeichnet werden soll, oder wenn die Größe eines Clients idschreiteinlineobject-Änderungen implementiert hat. <br/> |
| [**SetLineSpacing**](idwritetextlayout3-setlinespacing.md)     | Zeilenabstand festlegen.<br/>                                                                                                                                                                                                                                         |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1 \[ Desktop-Apps \| UWP-apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]<br/>                          |
| Unterstützte Mindestversion (Telefon)<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]<br/> |
| Bibliothek<br/>                  | <dl> <dt>Dwrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IDWriteTextLayout2**](idwritetextlayout2.md)
</dt> </dl>

 

 





