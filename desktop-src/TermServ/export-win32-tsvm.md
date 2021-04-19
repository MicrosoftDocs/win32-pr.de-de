---
title: Export-Methode der Win32_TSVm-Klasse
description: Ruft die Überwachungsinformationen für die Sitzung der virtuellen Maschine ab.
ms.assetid: 7996651c-aa7c-4fde-84a6-928b27c8c5b8
ms.tgt_platform: multiple
keywords:
- Export Methode Remotedesktopdienste
- Export Methode Remotedesktopdienste, Win32_TSVm Klasse
- Win32_TSVm-Klasse Remotedesktopdienste, Export-Methode
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
ms.openlocfilehash: c72d94b24af5563f9cdb668e269c260e8fe19049
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339544"
---
# <a name="export-method-of-the-win32_tsvm-class"></a>Export-Methode der Win32-Klasse "t- \_ VM"

Ruft die Überwachungsinformationen für die Sitzung der virtuellen Maschine ab.

## <a name="syntax"></a>Syntax


```mof
uint32 Export(
  [in]  string ExportFolderPath,
  [out] string ExportJobObjectPath
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Exportfolderpath* \[ in\]
</dt> <dd>

Der Pfad zum Speicherort der virtuellen Maschine.

</dd> <dt>

*Exportjobobjectpath* \[ vorgenommen\]
</dt> <dd>

Bei erfolgreicher Ausführung wird der HyperV-Objekt Pfad "concretejob" zurückgegeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben. Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .

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

[**Win32- \_ VM**](win32-tsvm.md)
</dt> </dl>

 

 





