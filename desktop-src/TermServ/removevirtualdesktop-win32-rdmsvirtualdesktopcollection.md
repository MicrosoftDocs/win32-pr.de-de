---
title: RemoveVirtualDesktop-Methode der Win32_RDMSVirtualDesktopCollection Klasse
description: Entfernt einen virtuellen Desktop aus der Sammlung virtueller Desktops.
ms.assetid: 287ebbb2-86db-4b4a-8dbb-ac5472789e72
ms.tgt_platform: multiple
keywords:
- RemoveVirtualDesktop-Remotedesktopdienste
- RemoveVirtualDesktop-Methode Remotedesktopdienste , Win32_RDMSVirtualDesktopCollection-Klasse
- Win32_RDMSVirtualDesktopCollection klasse Remotedesktopdienste , RemoveVirtualDesktop-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.RemoveVirtualDesktop
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3deefa38d7c7fcfc3f7942eb809b2ca14e96ea14ee4f2e014cdf3e0069a6ab9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009180"
---
# <a name="removevirtualdesktop-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>RemoveVirtualDesktop-Methode der Win32 \_ RDMSVirtualDesktopCollection-Klasse

Entfernt einen virtuellen Desktop aus der Sammlung virtueller Desktops.

## <a name="syntax"></a>Syntax


```mof
uint32 RemoveVirtualDesktop(
  [in] string VMName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*VMName* \[ In\]
</dt> <dd>

Der Name des virtuellen Computers, der den virtuellen Desktop hostet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                              |
| Namespace<br/>                | \\Stamm-CIMv2-Rdms \\<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ RDMSVirtualDesktopCollection**](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





