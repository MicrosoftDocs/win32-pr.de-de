---
title: Getvirtualdesktopdetails-Methode der Win32_RDMSVirtualDesktop-Klasse
description: Ruft die zusätzlichen Informationen zum virtuellen Desktop ab.
ms.assetid: 487e3a02-4306-4639-a44e-5b9519163a67
ms.tgt_platform: multiple
keywords:
- Getvirtualdesktopdetails-Methode Remotedesktopdienste
- Getvirtualdesktopdetails-Methode Remotedesktopdienste, Win32_RDMSVirtualDesktop-Klasse
- Win32_RDMSVirtualDesktop-Klasse Remotedesktopdienste, getvirtualdesktopdetails-Methode
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
ms.openlocfilehash: f7382a7ea10b3e557cd7317bdf1ddb0c4bcea55d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477445"
---
# <a name="getvirtualdesktopdetails-method-of-the-win32_rdmsvirtualdesktop-class"></a>Getvirtualdesktopdetails-Methode der Win32 \_ -Klasse rdmsvirtualdesktop

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

*Ramsizzumb* \[ vorgenommen\]
</dt> <dd>

Empfängt die dem virtuellen Desktop zugewiesene RAM-Größe in Bytes.

</dd> <dt>

*Remotefxaktiviert* \[ vorgenommen\]
</dt> <dd>

Empfängt einen Wert, der angibt, ob remotefx auf dem virtuellen Desktop aktiviert ist. **True** , wenn remotefx aktiviert ist. andernfalls **false**.

</dd> <dt>

*OSVersion* \[ vorgenommen\]
</dt> <dd>

Empfängt die Betriebssystemversion des virtuellen Desktops.

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

[**Win32 \_ rdmsvirtualdesktop**](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





