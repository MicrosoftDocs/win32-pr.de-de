---
title: Idschreitecolorglyphrunenumerator-Schnittstelle
description: Diese Schnittstelle ermöglicht es der Anwendung, die farbglyphe aufzählen.
ms.assetid: 649AD648-32BB-4BF4-A82F-075E93505E33
keywords:
- Idwrite-colorglyphrunenumerator-Schnittstelle direkt schreiben
- Direkter Schreibvorgang für idschreitecolorglyphrunenumerator-Schnittstelle, beschrieben
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
ms.openlocfilehash: e41831610f3ef564db55241267b75820cb9d87af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742240"
---
# <a name="idwritecolorglyphrunenumerator-interface"></a>Idschreitecolorglyphrunenumerator-Schnittstelle

Diese Schnittstelle ermöglicht es der Anwendung, die farbglyphe aufzählen. Der Enumerator listet die Ebenen in einer zurück zur Vorderseite auf, um eine geeignete Schicht zu haben.

## <a name="members"></a>Member

Die **idschreitecolorglyphrunenumerator** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Idwrite tecolorglyphrunenumerator** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **idschreitecolorglyphrunenumerator** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                | BESCHREIBUNG                                                 |
|:----------------------------------------------------------------------|:------------------------------------------------------------|
| [**Getcurrentrun**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritecolorglyphrunenumerator-getcurrentrun) | Gibt die aktuelle Glyphe des Enumerators zurück.<br/> |
| [**MoveNext**](idwritecolorglyphrunenumerator-movenext.md)           | Wechselt zum nächsten Symbol, das im Enumerator ausgeführt wird.<br/>    |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1 \[ Desktop-Apps \| UWP-apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]<br/>                          |
| Unterstützte Mindestversion (Telefon)<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]<br/> |
| Bibliothek<br/>                  | <dl> <dt>Dwrite. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



 

