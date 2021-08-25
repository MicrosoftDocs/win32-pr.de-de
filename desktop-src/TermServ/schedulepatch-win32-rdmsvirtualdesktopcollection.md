---
title: SchedulePatch-Methode der Win32_RDMSVirtualDesktopCollection-Klasse
description: Plant einen Auftrag zur Bereitstellung von Softwareupdates, mit dem Softwareupdates auf den virtuellen Computern in einer Sammlung virtueller Desktops installiert werden.
ms.assetid: 780d5709-9e7d-41d9-a4d0-b5d021615655
ms.tgt_platform: multiple
keywords:
- SchedulePatch-Methode Remotedesktopdienste
- SchedulePatch-Methode Remotedesktopdienste , Win32_RDMSVirtualDesktopCollection-Klasse
- Win32_RDMSVirtualDesktopCollection Klasse Remotedesktopdienste , SchedulePatch-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.SchedulePatch
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb29eb42f0f1d13ff1bf234c6fb41b8f414317a4b723af9a6d215cf25fa2ec95
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865510"
---
# <a name="schedulepatch-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>SchedulePatch-Methode der Win32 \_ RDMSVirtualDesktopCollection-Klasse

Plant einen Auftrag zur Bereitstellung von Softwareupdates, mit dem Softwareupdates auf den virtuellen Computern in einer Sammlung virtueller Desktops installiert werden.

## <a name="syntax"></a>Syntax


```mof
uint32 SchedulePatch(
  [in] DATETIME StartTime,
  [in] DATETIME ForceLogOffTime,
  [in] string   JobInputXml
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*StartTime* \[ In\]
</dt> <dd>

> [!Note]  
> Benutzer der virtuellen Computer werden vom System erst zu dem im *ForceLogOffTime-Parameter* angegebenen Zeitpunkt abgemeldet.

 

Das Datum und die Uhrzeit der Installation der Updates.

</dd> <dt>

*ForceLogOffTime* \[ In\]
</dt> <dd>

Das Datum und die Uhrzeit, zu der das System Benutzer der virtuellen Computer abmeldet.

</dd> <dt>

*JobInputXml* \[ In\]
</dt> <dd>

Eine XML-formatierte Zeichenfolge, die die Informationen zum Softwareupdateauftrag enthält.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ RDMSVirtualDesktopCollection**](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





