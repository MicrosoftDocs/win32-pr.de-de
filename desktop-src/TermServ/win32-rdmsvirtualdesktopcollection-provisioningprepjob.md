---
title: ProvisioningPrepJob-Methode der Win32_RDMSVirtualDesktopCollection Klasse
description: Erstellt einen Bereitstellungsauftrag für virtuelle Desktops.
ms.assetid: 240D4BE6-95BD-4858-8F8F-A00C92042AEF
ms.tgt_platform: multiple
keywords:
- ProvisioningPrepJob-Remotedesktopdienste
- ProvisioningPrepJob-Methode Remotedesktopdienste , Win32_RDMSVirtualDesktopCollection Schnittstelle
- Win32_RDMSVirtualDesktopCollection schnittstelle Remotedesktopdienste , ProvisioningPrepJob-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningPrepJob
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2dab9dcbd606dd32857f0d2dc4b2de3d8516e2b2da10e804fa36254679c1d2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119422840"
---
# <a name="provisioningprepjob-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>ProvisioningPrepJob-Methode der Win32 \_ RDMSVirtualDesktopCollection-Klasse

Erstellt einen Bereitstellungsauftrag für virtuelle Desktops.

## <a name="syntax"></a>Syntax


```mof
uint32 ProvisioningPrepJob(
  [in]  string  CollectionAlias,
  [in]  string  VMHostName,
  [in]  string  VMName,
  [in]  string  ExportToLocation,
  [in]  boolean bSysPrep,
  [in]  string  MachineName,
  [in]  string  UserName,
  [in]  string  Password,
  [out] string  JobGuid
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*CollectionAlias* \[ In\]
</dt> <dd>

Der Alias der Auflistung, die den virtuellen Desktop hostet.

</dd> <dt>

*VMHostName* \[ In\]
</dt> <dd>

Der Hostname des virtuellen Computers.

</dd> <dt>

*VMName* \[ In\]
</dt> <dd>

Der Name des virtuellen Computers.

</dd> <dt>

*ExportToLocation* \[ In\]
</dt> <dd>

Der vollständige Pfad des Speicherorts zum Exportieren des Bereitstellungsauftrags.

</dd> <dt>

*bSysPrep* \[ In\]
</dt> <dd>

Gibt an, ob der Bereitstellungsauftrag eine Sysprep-Bereitstellung darstellt.

</dd> <dt>

*MachineName* \[ In\]
</dt> <dd>

Der Computername des Computers, der den virtuellen Computer hostet.

</dd> <dt>

*UserName* \[ In\]
</dt> <dd>

Der Benutzername des Administrators des virtuellen Computers.

</dd> <dt>

*Kennwort* \[ In\]
</dt> <dd>

Das Kennwort des Administrators des virtuellen Computers.

</dd> <dt>

*JobGuid* \[ out\]
</dt> <dd>

Die **GUID,** die den Bereitstellungsauftrag eindeutig identifiziert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                              |
| Namespace<br/>                | Root \\ cimv2 \\ rdms<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**Win32 \_ RDMSVirtualDesktopCollection**](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





