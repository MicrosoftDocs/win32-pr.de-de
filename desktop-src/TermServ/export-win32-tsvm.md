---
title: Exportmethode der Win32_TSVm-Klasse
description: Ruft die Sitzungsüberwachungsinformationen des virtuellen Computers ab.
ms.assetid: 7996651c-aa7c-4fde-84a6-928b27c8c5b8
ms.tgt_platform: multiple
keywords:
- Exportmethode Remotedesktopdienste
- Exportmethode Remotedesktopdienste , Win32_TSVm-Klasse
- Win32_TSVm-Klasse Remotedesktopdienste , Export-Methode
topic_type:
- apiref
api_name:
- Win32_TSVm.Export
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f3a9fd517fe27db86b02680d1a2c7ad0c6663a985d0fddaccb5351bb799ba1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118855788"
---
# <a name="export-method-of-the-win32_tsvm-class"></a>Exportmethode der Win32 \_ TSVm-Klasse

Ruft die Sitzungsüberwachungsinformationen des virtuellen Computers ab.

## <a name="syntax"></a>Syntax


```mof
uint32 Export(
  [in]  string ExportFolderPath,
  [out] string ExportJobObjectPath
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ExportFolderPath* \[ In\]
</dt> <dd>

Pfad zum Exportort des virtuellen Computers.

</dd> <dt>

*ExportJobObjectPath* \[ out\]
</dt> <dd>

Bei erfolg gibt den HyperV ConcreteJob-Objektpfad zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls einen WMI-Fehlercode. Eine Liste dieser Werte finden [Sie unter Remotedesktopdienste WMI-Anbieterfehlercodes.](terminal-services-wmi-provider-error-codes.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                             |
| Namespace<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                   |
| MOF<br/>                      | <dl> <dt>TSVmHost.mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32 \_ TSVm**](win32-tsvm.md)
</dt> </dl>

 

 





