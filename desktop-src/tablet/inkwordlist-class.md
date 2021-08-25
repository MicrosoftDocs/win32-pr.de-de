---
description: Stellt eine Liste von Wörtern dar, die verwendet werden können, um das Erkennungsergebnis zu verbessern.
ms.assetid: d189fd13-ec69-45dc-8be4-fea48f337636
title: InkWordList-Klasse (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkWordList
- InkWordList.IInkWordList
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: fe46cf8f1befaf2717cfcf0a8e131113ed4552843bd3b6572364c27f3418ab34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119938670"
---
# <a name="inkwordlist-class"></a>InkWordList-Klasse

Stellt eine Liste von Wörtern dar, die verwendet werden können, um das Erkennungsergebnis zu verbessern.

**InkWordList** verfügt über die folgenden Membertypen:

-   [Schnittstellen](#interfaces)
-   [Methoden](#methods)

### <a name="interfaces"></a>Schnittstellen

Die **InkWordList-Klasse** definiert diese Schnittstellen.



| Schnittstelle        | BESCHREIBUNG                                                           |
|:-----------------|:----------------------------------------------------------------------|
| **IInkWordList** | Dieses Objekt implementiert die **IInkWordList-COM-Schnittstelle.**<br/> |



 

### <a name="methods"></a>Methoden

Die **InkWordList-Klasse** verfügt über diese Methoden.



| Methode                                       | BESCHREIBUNG                                                             |
|:---------------------------------------------|:------------------------------------------------------------------------|
| [**AddWord**](/windows/win32/api/msinkaut/nf-msinkaut-iinkwordlist-addword)       | Fügt der **InkWordList ein einzelnes Wort hinzu.**<br/>                   |
| [**Zusammenführen**](/windows/win32/api/msinkaut/nf-msinkaut-iinkwordlist-merge)           | Führt eine weitere **InkWordList mit** dieser **InkWordList zusammen.**<br/> |
| [**RemoveWord**](/windows/win32/api/msinkaut/nf-msinkaut-iinkwordlist-removeword) | Entfernt ein einzelnes Wort aus einem **InkWordList-.**<br/>                |



 

## <a name="remarks"></a>Hinweise

Dieses Objekt kann durch Aufrufen der [**CoCreateInstance-Methode**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) in C++ instanziiert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msinkaut.h (erfordert auch Msinkaut \_ i.c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WordList-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist)
</dt> <dt>

[Factoid-Konstanten](factoid-constants.md)
</dt> <dt>

[**InkRecognizerContext-Klasse**](inkrecognizercontext-class.md)
</dt> </dl>

 

