---
title: Provisioningprepjob-Methode der Win32_RDMSVirtualDesktopCollection-Klasse
description: Erstellt einen Bereitstellungs Auftrag für virtuelle Desktops.
ms.assetid: 240D4BE6-95BD-4858-8F8F-A00C92042AEF
ms.tgt_platform: multiple
keywords:
- Provisioningprepjob-Methode Remotedesktopdienste
- Provisioningprepjob-Methode Remotedesktopdienste, Win32_RDMSVirtualDesktopCollection-Schnittstelle
- Win32_RDMSVirtualDesktopCollection Interface Remotedesktopdienste, provisioningprepjob-Methode
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
ms.openlocfilehash: d9727dec0e31dd199f324ed01a4510041ba3558f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949793"
---
# <a name="provisioningprepjob-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Provisioningprepjob-Methode der Win32 \_ rdmsvirtualdesktopcollection-Klasse

Erstellt einen Bereitstellungs Auftrag für virtuelle Desktops.

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

*Collectionalias* \[ in\]
</dt> <dd>

Der Alias der Auflistung, die den virtuellen Desktop hostet.

</dd> <dt>

*Vmhostname* \[ in\]
</dt> <dd>

Der Hostname des virtuellen Computers.

</dd> <dt>

*VMName* \[ in\]
</dt> <dd>

Der Name des virtuellen Computers.

</dd> <dt>

*Exporttolokation* \[ in\]
</dt> <dd>

Der vollständige Pfad des Speicher Orts, an den der Bereitstellungs Auftrag exportiert werden soll.

</dd> <dt>

*bsystreup* \[ in\]
</dt> <dd>

Gibt an, ob der Bereitstellungs Auftrag eine System Vorbereitungs Bereitstellung darstellt.

</dd> <dt>

*MachineName* \[ in\]
</dt> <dd>

Der Computername des Computers, der die virtuelle Maschine hostet.

</dd> <dt>

*Benutzername* \[ in\]
</dt> <dd>

Der Benutzername des Administrators der virtuellen Maschine.

</dd> <dt>

*Kennwort* \[ in\]
</dt> <dd>

Das Kennwort des Administrators des virtuellen Computers.

</dd> <dt>

*Jobguid* \[ vorgenommen\]
</dt> <dd>

Die **GUID** , die den Bereitstellungs Auftrag eindeutig identifiziert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                              |
| Namespace<br/>                | Root \\ CIMV2 \\ RDMs<br/>                                                                |
| MOF<br/>                      | <dl> <dt>Rdmanagement. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ rdmsvirtualdesktopcollection**](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





