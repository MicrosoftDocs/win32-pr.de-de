---
title: SetStringProperty-Methode der Win32_RDMSVirtualDesktopCollection-Klasse (Certenroll.h)
description: Aktualisiert eine Zeichenfolgeneigenschaft einer Sammlung virtueller Desktops.
ms.assetid: d76d5f77-3b51-41b9-8ec5-a737ddc0a9d3
ms.tgt_platform: multiple
keywords:
- SetStringProperty-Methode Remotedesktopdienste
- SetStringProperty-Methode Remotedesktopdienste , Win32_RDMSVirtualDesktopCollection-Klasse
- Win32_RDMSVirtualDesktopCollection-Klasse Remotedesktopdienste , SetStringProperty-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.SetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fa0f8302ca2b4c843e552bed8de9145d74c6492626694bb9da0b127d0a07d2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118349354"
---
# <a name="setstringproperty-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>SetStringProperty-Methode der Win32 \_ RDMSVirtualDesktopCollection-Klasse

Aktualisiert eine Zeichenfolgeneigenschaft einer Sammlung virtueller Desktops.

## <a name="syntax"></a>Syntax


```mof
uint32 SetStringProperty(
  [in] string Key,
  [in] string Value
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Schlüssel* \[ In\]
</dt> <dd>

Ein Schlüssel, der die zu aktualisierende Eigenschaft identifiziert.

</dd> <dt>

*Wert* \[ In\]
</dt> <dd>

Der neue Eigenschaftswert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls einen WMI-Fehlercode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                              |
| Namespace<br/>                | \\Stamm-CIMv2 \\ rdms<br/>                                                                |
| Header<br/>                   | <dl> <dt>Certenroll.h</dt> </dl>     |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ RDMSVirtualDesktopCollection**](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





