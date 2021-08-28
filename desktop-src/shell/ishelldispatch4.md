---
description: Erweitert das IShellDispatch3-Objekt.
title: IShellDispatch4-Objekt (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch4
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 4fe37e38-ee71-41f0-b620-35fdc18f9dbb
ms.openlocfilehash: 057ef4082bac8d04c006d951db7d2d251be2f8c62e88af65bc1a69678514af81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118969009"
---
# <a name="ishelldispatch4-object"></a>IShellDispatch4-Objekt

Erweitert das [**IShellDispatch3-Objekt.**](ishelldispatch3.md) Zusätzlich zu den Eigenschaften und Methoden, die von **IShellDispatch3** unterstützt werden, unterstützt **IShellDispatch4** vier zusätzliche Methoden.

> [!Note]  
> **IShellDispatch4** wird implementiert und über das [**Shell-Objekt**](shell.md) aufgerufen.

 

## <a name="members"></a>Member

Das **IShellDispatch4-Objekt** verfügt über folgende Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Das **IShellDispatch4-Objekt** verfügt über diese Methoden.



| Methode                                                     | BESCHREIBUNG                                                         |
|:-----------------------------------------------------------|:--------------------------------------------------------------------|
| [**ExplorerPolicy**](ishelldispatch4-explorerpolicy.md)   | Ruft den Wert für eine angegebene Internet Explorer Richtlinie ab.<br/> |
| [**Getsetting**](ishelldispatch4-getsetting.md)           | Ruft eine globale Shelleinstellung ab.<br/>                        |
| [**ToggleDesktop**](ishelldispatch4-toggledesktop.md)     | Zeigt den Desktop an oder blendet den Desktop aus.<br/>                           |
| [**WindowsSecurity**](ishelldispatch4-windowssecurity.md) | Zeigt das Dialogfeld **Windows-Sicherheit** an.<br/>            |



 

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[**Shell-Objekt**](shell.md)
</dt> <dt>

[**IShellDispatch**](ishelldispatch.md)
</dt> <dt>

[**IShellDispatch2**](ishelldispatch2-object.md)
</dt> <dt>

[**IShellDispatch3**](ishelldispatch3.md)
</dt> </dl>

 

 
