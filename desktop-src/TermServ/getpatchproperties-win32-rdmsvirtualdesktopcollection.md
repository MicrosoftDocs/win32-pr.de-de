---
title: GetPatchProperties-Methode der Win32_RDMSVirtualDesktopCollection-Klasse
description: Ruft die Eigenschaften eines Softwareupdatebereitstellungsauftrags für die virtuellen Computer in einer Sammlung virtueller Desktops ab.
ms.assetid: 9f228d89-0613-49c7-8169-48491c3a2d9b
ms.tgt_platform: multiple
keywords:
- GetPatchProperties-Remotedesktopdienste
- GetPatchProperties-Methode Remotedesktopdienste , Win32_RDMSVirtualDesktopCollection-Klasse
- Win32_RDMSVirtualDesktopCollection klasse Remotedesktopdienste , GetPatchProperties-Methode
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
ms.openlocfilehash: 969a73e372dee430b280d4d16c267c6d8b75dda236c3ae7362d2392cb1bf8bf3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099510"
---
# <a name="getpatchproperties-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>GetPatchProperties-Methode der Win32 \_ RDMSVirtualDesktopCollection-Klasse

Ruft die Eigenschaften eines Softwareupdatebereitstellungsauftrags für die virtuellen Computer in einer Sammlung virtueller Desktops ab.

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

*StartTime* \[ out\]
</dt> <dd>

Das Datum und die Uhrzeit der Installation der Updates.

</dd> <dt>

*ForceLogOffTime* \[ out\]
</dt> <dd>

Das Datum und die Uhrzeit, zu der das System Benutzer der virtuellen Computer abmelden soll.

</dd> <dt>

*JobGuid* \[ out\]
</dt> <dd>

Eine **GUID,** die den Bereitstellungsauftrag eindeutig identifiziert.

</dd> <dt>

*Status* \[ out\]
</dt> <dd>

Der Status des Bereitstellungsauftrags.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                   |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                              |
| Namespace<br/>                | \\Stamm-CIMv2-Rdms \\<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ RDMSVirtualDesktopCollection**](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





