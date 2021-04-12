---
title: IDWriteTextLayout2-Schnittstelle
description: Stellt einen TextBlock dar, nachdem er vollständig analysiert und formatiert wurde. | IDWriteTextLayout2-Schnittstelle
ms.assetid: 034D795B-016A-401E-AD75-D5B0D1E87806
keywords:
- IDWriteTextLayout2 Interface Direct Write
- IDWriteTextLayout2 Interface Direct Write, beschrieben
topic_type:
- apiref
api_name:
- IDWriteTextLayout2
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80bb6037a598096109a9255abbb01ef289c5ef99
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353279"
---
# <a name="idwritetextlayout2-interface"></a>IDWriteTextLayout2-Schnittstelle

Stellt einen TextBlock dar, nachdem er vollständig analysiert und formatiert wurde.

## <a name="members"></a>Member

Die **IDWriteTextLayout2** -Schnittstelle erbt von [**IDWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1). **IDWriteTextLayout2** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IDWriteTextLayout2** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                                | BESCHREIBUNG                                                                                 |
|:--------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**Getfontfallback**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getfontfallback)                         | Das aktuelle Schriftart-Fall Back-Objekt wird angezeigt. <br/>                                           |
| [**Getlastlinewrapping**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getlastlinewrapping)                 | Gibt an, ob das letzte Wort in der letzten Zeile umschließt ist.<br/>                    |
| [**Getmetrics**](idwritetextlayout2-getmetrics.md)                                   | Ruft allgemeine Metriken für die formatierte Zeichenfolge ab. <br/>                             |
| [**Getopticalalignment**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getopticalalignment)                 | Gibt an, wie die Symbole am Rand ausgerichtet werden. <br/>                               |
| [**Getverticalglyphorientation**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-getverticalglyphorientation) | Hiermit wird die bevorzugte Ausrichtung von Symbolen bei Verwendung einer vertikalen Leserichtung erhalten.<br/> |
| [**Setfontfallback**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setfontfallback)                         | Anwenden eines benutzerdefinierten Schriftart Fallbacks auf das Layout.<br/>                                        |
| [**Setlastlinewrapping**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setlastlinewrapping)                 | Legen Sie fest, ob das letzte Wort in der letzten Zeile umschließt ist. <br/>                   |
| [**Setopticalalignment**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setopticalalignment)                 | Legen Sie fest, wie die Symbole an den Rändern am Rand ausgerichtet werden.<br/>                                |
| [**Setverticalglyphorientation**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextlayout2-setverticalglyphorientation) | Legen Sie die bevorzugte Ausrichtung der Symbole fest, wenn Sie eine vertikale Leserichtung verwenden.<br/> |



 

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

[**IDWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1)
</dt> </dl>

 

