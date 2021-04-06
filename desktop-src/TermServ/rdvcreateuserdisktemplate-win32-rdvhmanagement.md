---
title: Rdvkreateuserdisktemplate-Methode der Win32_RdvhManagement-Klasse
description: Erstellt eine Vorlage für einen Benutzer Datenträger mit der angegebenen maximalen Größe an der angegebenen Position.
ms.assetid: b8ca8b8c-58fd-44fc-9a88-5d7d41ef96a2
ms.tgt_platform: multiple
keywords:
- Rdvkreateuserdisktemplate-Methode Remotedesktopdienste
- Rdvkreateuserdisktemplate-Methode Remotedesktopdienste, Win32_RdvhManagement-Klasse
- Win32_RdvhManagement-Klasse Remotedesktopdienste, rdvkreateuserdisktemplate-Methode
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvCreateUserDiskTemplate
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cdc7fec869fa4ffde9ac0a5a724f73b04b84351
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743288"
---
# <a name="rdvcreateuserdisktemplate-method-of-the-win32_rdvhmanagement-class"></a>Rdvkreateuserdisktemplate-Methode der Win32 \_ rdvhmanagement-Klasse

Erstellt eine Vorlage für einen Benutzer Datenträger mit der angegebenen maximalen Größe an der angegebenen Position.

## <a name="syntax"></a>Syntax


```mof
uint32 RdvCreateUserDiskTemplate(
  [in] string UserDisksStorageUrl,
  [in] uint32 UserDiskMaxSizeInGB
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Userdisksstorageurl* \[ in\]
</dt> <dd>

Speicherort des Benutzer Festplatten Speichers.

</dd> <dt>

*Userdiskmaxsizzugb* \[ in\]
</dt> <dd>

Maximale Größe des Benutzer Datenträgers in GB.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben. Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .

## <a name="remarks"></a>Bemerkungen

Alle Benutzer Datenträger, die mit dieser Vorlage erstellt werden, haben dieselbe maximale Größe wie die Vorlage.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                             |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                   |
| MOF<br/>                      | <dl> <dt>"Zvmhost. mof"</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ rdvhmanagement**](win32-rdvhmanagement.md)
</dt> </dl>

 

 





