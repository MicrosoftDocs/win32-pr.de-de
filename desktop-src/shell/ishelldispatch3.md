---
description: Erweitert das IShellDispatch2-Objekt.
ms.assetid: 89d0aa4d-844d-497d-82bb-bcc2bcf9c78b
title: IShellDispatch3-Objekt (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch3
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 8f02095415ff2682e1f2a2eeb21c4afe0754b72251f6129856f1b6a415913cf4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118720916"
---
# <a name="ishelldispatch3-object"></a>IShellDispatch3-Objekt

Erweitert das [**IShellDispatch2-Objekt.**](ishelldispatch2-object.md) **IShellDispatch3** unterstützt zusätzlich zu den Eigenschaften und Methoden, die von **IShellDispatch2** unterstützt werden, eine neue Methode.

> [!Note]  
> **IShellDispatch3** wird implementiert, und der Zugriff erfolgt über das [**Shell-Objekt.**](shell.md)

 

## <a name="members"></a>Member

Das **IShellDispatch3-Objekt** verfügt über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Das **IShellDispatch3-Objekt** verfügt über diese Methoden.



| Methode                                             | BESCHREIBUNG                                                  |
|:---------------------------------------------------|:-------------------------------------------------------------|
| [**AddToRecent**](ishelldispatch3-addtorecent.md) | Fügt der Liste zuletzt verwendeter Dateien (MRU) eine Datei hinzu.<br/> |



 

## <a name="remarks"></a>Hinweise

Eine Erläuterung Windows Dienste finden Sie in der [Dokumentation zu Diensten.](../services/services.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 6.0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[**Shell-Objekt**](shell.md)
</dt> <dt>

[**IShellDispatch**](ishelldispatch.md)
</dt> <dt>

[**IShellDispatch2**](ishelldispatch2-object.md)
</dt> </dl>

 

 
