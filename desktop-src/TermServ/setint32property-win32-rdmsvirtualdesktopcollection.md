---
title: SetInt32Property-Methode der Win32_RDMSVirtualDesktopCollection-Klasse
description: Aktualisiert eine ganzzahlige Eigenschaft einer Sammlung virtueller Desktops.
ms.assetid: 2ea27385-5100-4e88-ad11-df5e439d0815
ms.tgt_platform: multiple
keywords:
- SetInt32Property-Methode Remotedesktopdienste
- SetInt32Property-Methode Remotedesktopdienste, Win32_RDMSVirtualDesktopCollection-Klasse
- Win32_RDMSVirtualDesktopCollection-Klasse Remotedesktopdienste, SetInt32Property-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.SetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33c2a93a52ce79bc185cd37dd9ac93e5b420b5d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105843"
---
# <a name="setint32property-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>SetInt32Property-Methode der Win32 \_ rdmsvirtualdesktopcollection-Klasse

Aktualisiert eine ganzzahlige Eigenschaft einer Sammlung virtueller Desktops.

## <a name="syntax"></a>Syntax


```mof
uint32 SetInt32Property(
  [in] string Key,
  [in] sint32 Value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Schlüssel* \[ in\]
</dt> <dd>

Ein Schlüssel, der die zu Aktualisier enswerte Eigenschaft identifiziert.

</dd> <dt>

*Wert* \[ in\]
</dt> <dd>

Der neue Eigenschaftswert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                              |
| Namespace<br/>                | Root \\ CIMv2 \\ RDMs<br/>                                                                |
| MOF<br/>                      | <dl> <dt>Rdmanagement. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ rdmsvirtualdesktopcollection**](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





