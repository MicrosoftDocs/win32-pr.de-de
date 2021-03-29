---
description: Erweitert das IShellDispatch2-Objekt.
ms.assetid: 89d0aa4d-844d-497d-82bb-bcc2bcf9c78b
title: IShellDispatch3-Objekt (Shldisp. h)
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
ms.openlocfilehash: 501b1396bd08ad8fd06f25da9b7030d4ce28d1e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978008"
---
# <a name="ishelldispatch3-object"></a>IShellDispatch3-Objekt

Erweitert das [**IShellDispatch2**](ishelldispatch2-object.md) -Objekt. **IShellDispatch3** unterstützt eine neue Methode zusätzlich zu den Eigenschaften und Methoden, die von **IShellDispatch2** unterstützt werden.

> [!Note]  
> **IShellDispatch3** wird implementiert, und der Zugriff erfolgt über das [**Shellobjekt**](shell.md) .

 

## <a name="members"></a>Member

Das **IShellDispatch3** -Objekt verfügt über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Das **IShellDispatch3** -Objekt verfügt über diese Methoden.



| Methode                                             | BESCHREIBUNG                                                  |
|:---------------------------------------------------|:-------------------------------------------------------------|
| [**Addtor**](ishelldispatch3-addtorecent.md) | Fügt der Liste der zuletzt verwendeten (MRU) eine Datei hinzu.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Eine Erläuterung der Windows-Dienste finden Sie in der Dokumentation zu [Diensten](../services/services.md) .

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 6,0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[**Shellobjekt**](shell.md)
</dt> <dt>

[**Ishelldispatch**](ishelldispatch.md)
</dt> <dt>

[**IShellDispatch2**](ishelldispatch2-object.md)
</dt> </dl>

 

 
