---
title: Enableuservhd-Methode der Win32_TSSessionDirectory-Klasse
description: Aktiviert eine Benutzerprofil-VHD auf einem RDSH-Server.
ms.assetid: bb39fa19-38eb-4caf-ae81-2bccd901ee2f
ms.tgt_platform: multiple
keywords:
- Enableuservhd-Methode Remotedesktopdienste
- Enableuservhd-Methode Remotedesktopdienste, Win32_TSSessionDirectory-Klasse
- Win32_TSSessionDirectory-Klasse Remotedesktopdienste, enableuservhd-Methode
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.EnableUserVhd
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 464e105d2f8f0c80126e6b9ca5e5a383b2d17628
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346770"
---
# <a name="enableuservhd-method-of-the-win32_tssessiondirectory-class"></a>Enableuservhd-Methode der Win32- \_ Klasse "tssessiondirectory"

Aktiviert eine Benutzerprofil-VHD auf einem RDSH-Server.

## <a name="syntax"></a>Syntax


```mof
uint32 EnableUserVhd(
  [in] string UvhdShareUrl,
  [in] string UvhdRoamingPolicyXml
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Uvhdshareurl* \[ in\]
</dt> <dd>

Der Speicherort der Freigabe, in der alle Benutzerprofil-VHDs gespeichert sind.

</dd> <dt>

*Uvhdroamingpolicyxml* \[ in\]
</dt> <dd>

Die roamingrichtlinie für die Benutzerprofil-VHD.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                          |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>Tscsgwmi. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ tssessiondirectory**](win32-tssessiondirectory.md)
</dt> </dl>

 

 





