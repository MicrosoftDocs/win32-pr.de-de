---
title: Synchronizepublishingdata-Methode der Win32_RDMSManagementData-Klasse
description: Synchronisiert den angegebenen Satz von Veröffentlichungsdaten für Remotedesktop Management Services (RDMs).
ms.assetid: 0476ce12-9b08-418c-83c2-208275574f5b
ms.tgt_platform: multiple
keywords:
- Synchronizepublishingdata-Methode Remotedesktopdienste
- Synchronizepublishingdata-Methode Remotedesktopdienste, Win32_RDMSManagementData-Klasse
- Win32_RDMSManagementData-Klasse Remotedesktopdienste, synchronizepublishingdata-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSManagementData.SynchronizePublishingData
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d389ad08d81f39cab45502a42f4ebd95e16f36c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391861"
---
# <a name="synchronizepublishingdata-method-of-the-win32_rdmsmanagementdata-class"></a>Synchronizepublishingdata-Methode der Win32 \_ rdmsmanagementdata-Klasse

Synchronisiert den angegebenen Satz von Veröffentlichungsdaten für Remotedesktop Management Services (RDMs).

## <a name="syntax"></a>Syntax


```mof
uint32 SynchronizePublishingData(
  [in] string Context
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Kontext* \[ in\]
</dt> <dd>

Die Kontextinformationen der zu synchronisierenden Veröffentlichungsdaten.

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

[**Win32 \_ rdmsmanagementdata**](win32-rdmsmanagementdata.md)
</dt> </dl>

 

 





