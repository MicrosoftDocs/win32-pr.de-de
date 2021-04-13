---
title: Getpatchproperties-Methode der Win32_RDMSVirtualDesktopCollection-Klasse
description: Ruft die Eigenschaften eines Bereitstellungs Auftrags für Software Updates für die virtuellen Computer in einer Sammlung virtueller Desktops ab.
ms.assetid: 9f228d89-0613-49c7-8169-48491c3a2d9b
ms.tgt_platform: multiple
keywords:
- Getpatchproperties-Methode Remotedesktopdienste
- Getpatchproperties-Methode Remotedesktopdienste, Win32_RDMSVirtualDesktopCollection-Klasse
- Win32_RDMSVirtualDesktopCollection-Klasse Remotedesktopdienste, getpatchproperties-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.GetPatchProperties
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f0ca45c97512818aa5f8a9ea851d18fa5554c32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518185"
---
# <a name="getpatchproperties-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Getpatchproperties-Methode der Win32 \_ rdmsvirtualdesktopcollection-Klasse

Ruft die Eigenschaften eines Bereitstellungs Auftrags für Software Updates für die virtuellen Computer in einer Sammlung virtueller Desktops ab.

## <a name="syntax"></a>Syntax


```mof
uint32 GetPatchProperties(
  [out] DATETIME StartTime,
  [out] DATETIME ForceLogOffTime,
  [out] string   JobGuid,
  [out] uint32   State
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*StartTime* \[ vorgenommen\]
</dt> <dd>

Das Datum und die Uhrzeit der Installation der Updates.

</dd> <dt>

*Forcelogofftime* \[ vorgenommen\]
</dt> <dd>

Das Datum und die Uhrzeit, zu denen das Systembenutzer der virtuellen Maschinen abmeldet.

</dd> <dt>

*Jobguid* \[ vorgenommen\]
</dt> <dd>

Eine **GUID** , die den Bereitstellungs Auftrag eindeutig identifiziert.

</dd> <dt>

*Status* \[ vorgenommen\]
</dt> <dd>

Der Status des Bereitstellungs Auftrags.

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

 

 





