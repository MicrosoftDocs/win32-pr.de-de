---
description: Die Reset-Methode der CIM \_ TapeDrive-Klasse fordert das Zurücksetzen des logischen Geräts an.
ms.assetid: 48097e0d-7986-46b9-884d-7534f3848dd7
ms.tgt_platform: multiple
title: Reset-Methode der CIM_TapeDrive-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TapeDrive.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e5fd76d038e743ba5148f4c82555d50f0a5dde5d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861623"
---
# <a name="reset-method-of-the-cim_tapedrive-class"></a>Reset-Methode der CIM \_ TapeDrive-Klasse

Die **Reset** -Methode der CIM \_ TapeDrive-Klasse fordert das Zurücksetzen des logischen Geräts an. Diese Methode wird von [**CIM \_ LogicalDevice**](cim-logicaldevice.md)geerbt.

## <a name="syntax"></a>Syntax


```mof
uint32 Reset();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt 0 (null) zurück, wenn die Anforderung erfolgreich ausgeführt wurde, 1 (eins), wenn die Anforderung nicht unterstützt wird, und ein anderer Wert, wenn ein Fehler aufgetreten ist.

## <a name="remarks"></a>Bemerkungen

Diese Methode wird zurzeit nicht von WMI implementiert. Um diese Methode verwenden zu können, müssen Sie Sie in Ihrem eigenen Anbieter implementieren.

Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet. Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[CIM- \_ TapeDrive](reset-method-in-class-cim-tapedrive.md)
</dt> <dt>

[**CIM- \_ TapeDrive**](cim-tapedrive.md)
</dt> </dl>

 

 




