---
title: IDWriteColorGlyphRunEnumerator-Schnittstelle
description: Mit dieser Schnittstelle kann die Anwendung die Farbglyphenläufe aufzählen.
ms.assetid: 649AD648-32BB-4BF4-A82F-075E93505E33
keywords:
- IDWriteColorGlyphRunEnumerator-Schnittstelle – Direkter Schreibzugriff
- IDWriteColorGlyphRunEnumerator-Schnittstelle Direct Write , beschrieben
topic_type:
- apiref
api_name:
- IDWriteColorGlyphRunEnumerator
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fa665f7000ffaada5bc14f97671fb6e52266c712ef6081b956184653d1f1c95
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119536140"
---
# <a name="idwritecolorglyphrunenumerator-interface"></a>IDWriteColorGlyphRunEnumerator-Schnittstelle

Mit dieser Schnittstelle kann die Anwendung die Farbglyphenläufe aufzählen. Der Enumerator enumeriert die Ebenen in einer Back-to-Front-Reihenfolge für die entsprechende Schichtung.

## <a name="members"></a>Member

Die **IDWriteColorGlyphRunEnumerator-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IDWriteColorGlyphRunEnumerator** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IDWriteColorGlyphRunEnumerator-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                | Beschreibung                                                 |
|:----------------------------------------------------------------------|:------------------------------------------------------------|
| [**GetCurrentRun**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritecolorglyphrunenumerator-getcurrentrun) | Gibt die aktuelle Glyphen-Ausführung des Enumerators zurück.<br/> |
| [**MoveNext**](idwritecolorglyphrunenumerator-movenext.md)           | Wechseln Sie zur nächsten Glyphen-Ausführung im Enumerator.<br/>    |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8.1 Desktop-Apps \| UWP-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 \[R2-Desktop-Apps \| UWP-Apps\]<br/>                          |
| Unterstützte Mindestversion (Telefon)<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 und Windows Runtime-Apps\]<br/> |
| Bibliothek<br/>                  | <dl> <dt>Dwrite.lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



 

