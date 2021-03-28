---
description: Erweitert das IShellDispatch3-Objekt.
title: IShellDispatch4-Objekt (Shldisp. h)
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
ms.openlocfilehash: 0bdada12a48f9c48749b614e6b45ff5427e62b4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527323"
---
# <a name="ishelldispatch4-object"></a>IShellDispatch4-Objekt

Erweitert das [**IShellDispatch3**](ishelldispatch3.md) -Objekt. Zusätzlich zu den Eigenschaften und Methoden, die von **IShellDispatch3** unterstützt werden, unterstützt **IShellDispatch4** vier zusätzliche Methoden.

> [!Note]  
> **IShellDispatch4** wird implementiert, und der Zugriff erfolgt über das [**Shellobjekt**](shell.md) .

 

## <a name="members"></a>Member

Das **IShellDispatch4** -Objekt verfügt über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Das **IShellDispatch4** -Objekt verfügt über diese Methoden.



| Methode                                                     | BESCHREIBUNG                                                         |
|:-----------------------------------------------------------|:--------------------------------------------------------------------|
| [**Explorerpolicy**](ishelldispatch4-explorerpolicy.md)   | Ruft den Wert für eine angegebene Internet Explorer-Richtlinie ab.<br/> |
| [**GetSetting**](ishelldispatch4-getsetting.md)           | Ruft eine globale shelleinstellung ab.<br/>                        |
| [**ToggleDesktop**](ishelldispatch4-toggledesktop.md)     | Zeigt den Desktop an oder blendet ihn aus.<br/>                           |
| [**WindowsSecurity**](ishelldispatch4-windowssecurity.md) | Zeigt das Dialogfeld **Windows-Sicherheit** an.<br/>            |



 

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
</dt> <dt>

[**IShellDispatch3**](ishelldispatch3.md)
</dt> </dl>

 

 
