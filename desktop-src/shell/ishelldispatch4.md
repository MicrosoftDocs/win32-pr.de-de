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
ms.openlocfilehash: daec9c922a0bac05154c1108f236ddf336a2e380
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843061"
---
# <a name="ishelldispatch4-object"></a>IShellDispatch4-Objekt

Erweitert das [**IShellDispatch3-Objekt.**](ishelldispatch3.md) Zusätzlich zu den Eigenschaften und Methoden, die von **IShellDispatch3** unterstützt werden, unterstützt **IShellDispatch4** vier zusätzliche Methoden.

> [!Note]  
> **IShellDispatch4 wird** implementiert und über das [**Shell-Objekt aufgerufen.**](shell.md)

 

## <a name="members"></a>Member

Das **IShellDispatch4-Objekt** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Das **IShellDispatch4-Objekt** verfügt über diese Methoden.



| Methode                                                     | BESCHREIBUNG                                                         |
|:-----------------------------------------------------------|:--------------------------------------------------------------------|
| [**ExplorerPolicy**](ishelldispatch4-explorerpolicy.md)   | Ruft den Wert für eine angegebene Internet Explorer ab.<br/> |
| [**Getsetting**](ishelldispatch4-getsetting.md)           | Ruft eine globale Shelleinstellung ab.<br/>                        |
| [**ToggleDesktop**](ishelldispatch4-toggledesktop.md)     | Zeigt den Desktop an oder blendet den Desktop aus.<br/>                           |
| [**WindowsSecurity**](ishelldispatch4-windowssecurity.md) | Zeigt das **Windows-Sicherheit** An.<br/>            |



 

## <a name="remarks"></a>Hinweise

Eine Erörterung der Windows-Dienste finden Sie in der [Dokumentation zu Diensten.](../services/services.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ XP-Desktop-Apps\]<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/>                                                          |
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

 

 
