---
title: Schedulepatch-Methode der Win32_RDMSVirtualDesktopCollection-Klasse
description: Plant einen Bereitstellungs Auftrag für Software Updates, mit dem Software Updates auf den virtuellen Computern in einer Sammlung virtueller Desktops installiert werden.
ms.assetid: 780d5709-9e7d-41d9-a4d0-b5d021615655
ms.tgt_platform: multiple
keywords:
- Schedulepatch-Methode Remotedesktopdienste
- Schedulepatch-Methode Remotedesktopdienste, Win32_RDMSVirtualDesktopCollection-Klasse
- Win32_RDMSVirtualDesktopCollection-Klasse Remotedesktopdienste, schedulepatch-Methode
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
ms.openlocfilehash: 7d9585e3d13ea1f02115506741c153d62c33fcc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476422"
---
# <a name="schedulepatch-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Schedulepatch-Methode der Win32 \_ rdmsvirtualdesktopcollection-Klasse

Plant einen Bereitstellungs Auftrag für Software Updates, mit dem Software Updates auf den virtuellen Computern in einer Sammlung virtueller Desktops installiert werden.

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

*StartTime* \[ in\]
</dt> <dd>

> [!Note]  
> Das System meldet die Benutzer der virtuellen Computer erst dann ab, wenn die im *forcelogofftime* -Parameter angegebene Zeit verwendet wird.

 

Das Datum und die Uhrzeit der Installation der Updates.

</dd> <dt>

*Forcelogofftime* \[ in\]
</dt> <dd>

Das Datum und die Uhrzeit, zu denen das Systembenutzer der virtuellen Maschinen abmeldet.

</dd> <dt>

*Jobinputxml* \[ in\]
</dt> <dd>

Eine XML-formatierte Zeichenfolge, die die Informationen zum Software Update Auftrag enthält.

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

 

 





