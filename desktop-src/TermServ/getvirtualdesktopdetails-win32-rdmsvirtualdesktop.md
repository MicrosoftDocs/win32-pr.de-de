---
title: GetVirtualDesktopDetails-Methode der Win32_RDMSVirtualDesktop-Klasse
description: Ruft die zusätzlichen Informationen zum virtuellen Desktop ab.
ms.assetid: 487e3a02-4306-4639-a44e-5b9519163a67
ms.tgt_platform: multiple
keywords:
- GetVirtualDesktopDetails-Methode Remotedesktopdienste
- GetVirtualDesktopDetails-Methode Remotedesktopdienste , Win32_RDMSVirtualDesktop-Klasse
- Win32_RDMSVirtualDesktop-Klasse Remotedesktopdienste , GetVirtualDesktopDetails-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.GetVirtualDesktopDetails
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6ca1b552147623822ae007ca17abf8e4eaebfb149f5e80ac4760719f1ef7168
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059488"
---
# <a name="getvirtualdesktopdetails-method-of-the-win32_rdmsvirtualdesktop-class"></a>GetVirtualDesktopDetails-Methode der Win32 \_ RDMSVirtualDesktop-Klasse

Ruft die zusätzlichen Informationen zum virtuellen Desktop ab.

## <a name="syntax"></a>Syntax


```mof
uint32 GetVirtualDesktopDetails(
  [out] uint32  RAMSizeInMB,
  [out] boolean RemoteFXEnabled,
  [out] string  OSVersion
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*RAMSizeInMB* \[ out\]
</dt> <dd>

Empfängt die dem virtuellen Desktop zugewiesene RAM-Menge in Bytes.

</dd> <dt>

*RemoteFXEnabled* \[ out\]
</dt> <dd>

Empfängt einen Wert, der angibt, ob RemoteFX auf dem virtuellen Desktop aktiviert ist. **TRUE,** wenn RemoteFX aktiviert ist; Andernfalls **FALSE**.

</dd> <dt>

*OSVersion* \[ out\]
</dt> <dd>

Empfängt die Betriebssystemversion des virtuellen Desktops.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls einen WMI-Fehlercode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                              |
| Namespace<br/>                | \\Stamm-CIMv2 \\ rdms<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ RDMSVirtualDesktop**](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





