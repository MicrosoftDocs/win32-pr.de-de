---
title: Provisioningjobcancel-Methode der Win32_RDMSVirtualDesktopCollection-Klasse
description: Bricht einen Bereitstellungs Auftrag für virtuelle Desktops ab.
ms.assetid: 933ea0f3-b916-4e70-89de-597f9eb23976
ms.tgt_platform: multiple
keywords:
- Provisioningjobcancel-Methode Remotedesktopdienste
- Provisioningjobcancel-Methode Remotedesktopdienste, Win32_RDMSVirtualDesktopCollection-Klasse
- Win32_RDMSVirtualDesktopCollection-Klasse Remotedesktopdienste, provisioningjobcancel-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningJobCancel
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8f414bcdc264d682817898bae98fcf60a716452
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341808"
---
# <a name="provisioningjobcancel-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Provisioningjobcancel-Methode der Win32 \_ rdmsvirtualdesktopcollection-Klasse

Bricht einen Bereitstellungs Auftrag für virtuelle Desktops ab.

## <a name="syntax"></a>Syntax


```mof
uint32 ProvisioningJobCancel(
  [in] string JobGuid
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Jobguid* \[ in\]
</dt> <dd>

Die **GUID** , die den Abbruch des Bereitstellungs Auftrags eindeutig identifiziert.

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

[**Win32 \_ rdmsvirtualdesktopcollection**](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





