---
title: IMsRdpClientShell2 msrdpworkspace (Eigenschaft)
description: Ruft einen Zeiger auf die imsrdpworkspace-Schnittstelle ab, die zum Verwalten von RemoteApp-und Desktopverbindung Anmelde Informationen und Verbindungen verwendet wird.
ms.assetid: 5d505ce0-18cf-4e38-b1b8-026303f7069b
ms.tgt_platform: multiple
keywords:
- Msrdpworkspace-Eigenschaft Remotedesktopdienste
- Msrdpworkspace-Eigenschaft Remotedesktopdienste, IMsRdpClientShell2-Schnittstelle
- IMsRdpClientShell2 Interface Remotedesktopdienste, msrdpworkspace (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientShell2.MsRdpWorkspace
- IMsRdpClientShell2.get_MsRdpWorkspace
api_location:
- MsRdpWebAccess.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91eadd3f1b422e3da96d5bcd3a5178a2a0b0eb52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742400"
---
# <a name="imsrdpclientshell2msrdpworkspace-property"></a>IMsRdpClientShell2:: msrdpworkspace (Eigenschaft)

Ruft einen Zeiger auf die [**imsrdpworkspace**](imsrdpworkspace.md) -Schnittstelle ab, die zum Verwalten von RemoteApp-und Desktopverbindung Anmelde Informationen und Verbindungen verwendet wird.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_MsRdpWorkspace(
  [out, retval] IMsRdpWorkspace **pVal
);
```



## <a name="property-value"></a>Eigenschaftswert

Die Adresse eines Zeigers auf die [**imsrdpworkspace**](imsrdpworkspace.md) -Schnittstelle.

## <a name="remarks"></a>Bemerkungen

Die [**imsrdpworkspace**](imsrdpworkspace.md) -Schnittstelle wird nicht als benutzerdefinierte Schnittstelle verfügbar gemacht. Der Zugriff ist nur über [IDispatch](/windows/desktop/com/exposing-methods-through-idispatch) -Methoden möglich.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7<br/>                                                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                             |
| DLL<br/>                      | <dl> <dt>MsRdpWebAccess.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IMsRdpClientShell2**](imsrdpclientshell2.md)
</dt> </dl>

 

