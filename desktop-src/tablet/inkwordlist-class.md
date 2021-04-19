---
description: Stellt eine Liste von Wörtern dar, die verwendet werden können, um das Erkennungs Ergebnis zu verbessern.
ms.assetid: d189fd13-ec69-45dc-8be4-fea48f337636
title: Inkwordlist-Klasse (msink AUT. h)
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
ms.openlocfilehash: 7f3bbf077758bfd0449f5bca1ba3739342fa3658
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359522"
---
# <a name="inkwordlist-class"></a>Inkwordlist-Klasse

Stellt eine Liste von Wörtern dar, die verwendet werden können, um das Erkennungs Ergebnis zu verbessern.

**Inkwordlist** enthält diese Typen von Membern:

-   [Schnittstellen](#interfaces)
-   [Methoden](#methods)

### <a name="interfaces"></a>Schnittstellen

Diese Schnittstellen werden von der **inkwordlist** -Klasse definiert.



| Schnittstelle        | BESCHREIBUNG                                                           |
|:-----------------|:----------------------------------------------------------------------|
| **Iinkwordlist** | Dieses Objekt implementiert die **iinkwordlist** -com-Schnittstelle.<br/> |



 

### <a name="methods"></a>Methoden

Die **inkwordlist** -Klasse verfügt über diese Methoden.



| Methode                                       | BESCHREIBUNG                                                             |
|:---------------------------------------------|:------------------------------------------------------------------------|
| [**AddWord**](/windows/win32/api/msinkaut/nf-msinkaut-iinkwordlist-addword)       | Fügt der **inkwordlist** ein einzelnes Wort hinzu.<br/>                   |
| [**Merge**](/windows/win32/api/msinkaut/nf-msinkaut-iinkwordlist-merge)           | Führt eine weitere **inkwordlist** mit in diese **inkwordlist** zusammen.<br/> |
| [**Removeword**](/windows/win32/api/msinkaut/nf-msinkaut-iinkwordlist-removeword) | Entfernt ein einzelnes Wort aus einer " **inkwordlist**".<br/>                |



 

## <a name="remarks"></a>Bemerkungen

Dieses Objekt kann durch Aufrufen der [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) -Methode in C++ instanziiert werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                       |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WordList-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist)
</dt> <dt>

[Faktoid-Konstanten](factoid-constants.md)
</dt> <dt>

[**Inkrecognizercontext-Klasse**](inkrecognizercontext-class.md)
</dt> </dl>

 

