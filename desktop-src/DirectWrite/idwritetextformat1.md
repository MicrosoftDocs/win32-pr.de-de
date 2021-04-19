---
title: IDWriteTextFormat1-Schnittstelle
description: Beschreibt die Schriftart-und Absatz Eigenschaften, die zum Formatieren von Text verwendet werden, und beschreibt Gebiets Schema Informationen. | IDWriteTextFormat1-Schnittstelle
ms.assetid: 15295A17-E542-4071-AE38-02014A1235D5
keywords:
- IDWriteTextFormat1 Interface Direct Write
- IDWriteTextFormat1 Interface Direct Write, beschrieben
topic_type:
- apiref
api_name:
- IDWriteTextFormat1
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 796c5f845b5ed0d0522039865f2acb023fc2ab0c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106373437"
---
# <a name="idwritetextformat1-interface"></a>IDWriteTextFormat1-Schnittstelle

Beschreibt die Schriftart-und Absatz Eigenschaften, die zum Formatieren von Text verwendet werden, und beschreibt Gebiets Schema Informationen. Diese Schnittstelle verfügt über dieselben Methoden wie [**idschreitetextformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) und bietet Ihnen die Möglichkeit, eine explizite Ausrichtung anzuwenden.

## <a name="members"></a>Member

Die **IDWriteTextFormat1** -Schnittstelle erbt von [**idschreitetextformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat). **IDWriteTextFormat1** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IDWriteTextFormat1** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                | BESCHREIBUNG                                                                                                             |
|:--------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**Getfontfallback**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-getfontfallback)                         | Ruft den aktuellen Fallback ab. Wenn seit dem Erstellen des Layouts nichts festgelegt wurde, wird es auf nullptr festgelegt.<br/>               |
| [**Getlastlinewrapping**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-getlastlinewrapping)                 | Ruft den Wrapping Modus der letzten Zeile ab.<br/>                                                                     |
| [**Getopticalalignment**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-getopticalalignment)                 | Ruft die optische Rand Ausrichtung für das Textformat ab.<br/>                                                       |
| [**Getverticalglyphorientation**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-getverticalglyphorientation) | Hiermit wird die bevorzugte Ausrichtung von Symbolen bei Verwendung einer vertikalen Leserichtung erhalten.<br/>                             |
| [**Setfontfallback**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-setfontfallback)                         | Wendet den benutzerdefinierten Schriftart Fall Back auf das Layout an. Wenn kein Wert festgelegt ist, wird die standardmäßige System Fall Back Liste verwendet. <br/> |
| [**Setlastlinewrapping**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-setlastlinewrapping)                   | Legt den Wrapping Modus der letzten Zeile fest.<br/>                                                                     |
| [**Setopticalalignment**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-setopticalalignment)                 | Legt die optische Rand Ausrichtung für das Textformat fest.<br/>                                                       |
| [**Setverticalglyphorientation**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-setverticalglyphorientation) | Legt die Ausrichtung eines Text Formats fest.<br/>                                                                       |



 

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

[**Idschreitetextformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)
</dt> </dl>

 

