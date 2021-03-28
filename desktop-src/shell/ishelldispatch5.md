---
description: Erweitert das IShellDispatch4-Objekt.
title: IShellDispatch5-Objekt (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch5
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9170340a-0f11-4ec9-877d-fb7fef9888b2
ms.openlocfilehash: cbf3e960d7bfb9cd15411142cc036a21a9995ff9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977968"
---
# <a name="ishelldispatch5-object"></a>IShellDispatch5-Objekt

Erweitert das [**IShellDispatch4**](ishelldispatch4.md) -Objekt. Zusätzlich zu den Eigenschaften und Methoden, die von **IShellDispatch4** unterstützt werden, fügt **IShellDispatch5** eine Methode hinzu, die geöffnete Fenster in einem 3D-Stapel anzeigt.

> [!Note]  
> **IShellDispatch5** wird implementiert, und der Zugriff erfolgt über das [**Shellobjekt**](shell.md) .

 

## <a name="members"></a>Member

Das **IShellDispatch5** -Objekt verfügt über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Das **IShellDispatch5** -Objekt verfügt über diese Methoden.



| Methode                                                   | BESCHREIBUNG                                                                    |
|:---------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**Windowswitcher**](ishelldispatch5-windowswitcher.md) | Zeigt die geöffneten Fenster in einem 3D-Stapel an, den Sie durchlaufen können.<br/> |



 

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
</dt> <dt>

[**IShellDispatch3**](ishelldispatch3.md)
</dt> <dt>

[**IShellDispatch4**](ishelldispatch4.md)
</dt> </dl>

 

 
