---
title: IDWriteFont2-Schnittstelle
description: Stellt eine physische Schriftart in einer Schriftart Auflistung dar.
ms.assetid: 4E3069AE-5882-4A26-A36D-BE7D7EE1B0C3
keywords:
- IDWriteFont2 Interface Direct Write
- IDWriteFont2 Interface Direct Write, beschrieben
topic_type:
- apiref
api_name:
- IDWriteFont2
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f82a47e56915747b0e118a6f63484b9dd3dcdbd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340838"
---
# <a name="idwritefont2-interface"></a>IDWriteFont2-Schnittstelle

Stellt eine physische Schriftart in einer Schriftart Auflistung dar.

Diese Schnittstelle bietet die Möglichkeit, zu überprüfen, ob möglicherweise ein farbrenderingpfad erforderlich ist.

## <a name="members"></a>Member

Die **IDWriteFont2** -Schnittstelle erbt von [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1). **IDWriteFont2** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IDWriteFont2** -Schnittstelle verfügt über diese Methoden.



| Methode                                          | BESCHREIBUNG                                                                        |
|:------------------------------------------------|:-----------------------------------------------------------------------------------|
| [**Iscolorfont**](idwritefont2-iscolorfont.md) | Ermöglicht die Ermittlung, ob ein farbrenderingpfad möglicherweise erforderlich ist.<br/> |



 

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

[**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1)
</dt> </dl>

 

