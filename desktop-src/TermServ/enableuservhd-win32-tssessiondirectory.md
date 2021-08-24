---
title: EnableUserVhd-Methode der Win32_TSSessionDirectory Klasse
description: Aktiviert eine Benutzerprofil-VHD auf einem RDSH-Server.
ms.assetid: bb39fa19-38eb-4caf-ae81-2bccd901ee2f
ms.tgt_platform: multiple
keywords:
- EnableUserVhd-Remotedesktopdienste
- EnableUserVhd-Methode Remotedesktopdienste , Win32_TSSessionDirectory-Klasse
- Win32_TSSessionDirectory klasse Remotedesktopdienste , EnableUserVhd-Methode
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
ms.openlocfilehash: 19e042b51c7060e4d4c2a8302a87b2d27ee2cf89608a9831cb3497fd0566689a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871740"
---
# <a name="enableuservhd-method-of-the-win32_tssessiondirectory-class"></a>EnableUserVhd-Methode der Win32 \_ TSSessionDirectory-Klasse

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

*UvhdShareUrl* \[ In\]
</dt> <dd>

Der Speicherort der Freigabe, an dem alle Benutzerprofil-VHDs gespeichert werden.

</dd> <dt>

*UvhdRoamingPolicyXml* \[ In\]
</dt> <dd>

Die Roamingrichtlinie für die Benutzerprofil-VHD.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                          |
| Namespace<br/>                | \\ \\ CiMv2-Stammterminaldienste<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md)
</dt> </dl>

 

 





