---
title: Queryofflineinformation-Methode der Win32_TSVm-Klasse
description: Ruft die Eigenschaften des aktuellen virtuellen Desktop Servers (VDS) ab, jedoch nur, wenn der Server offline ist.
ms.assetid: f6ce74cb-a4a4-4e05-a0a7-bac0b7f52c45
ms.tgt_platform: multiple
keywords:
- Queryofflineinformation-Methode Remotedesktopdienste
- Queryofflineinformation-Methode Remotedesktopdienste, Win32_TSVm-Klasse
- Win32_TSVm-Klasse Remotedesktopdienste, queryofflineinformation-Methode
topic_type:
- apiref
api_name:
- Win32_TSVm.QueryOfflineInformation
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4750ebdb82b08ae1ed0350e1ac448d9aca4003b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859030"
---
# <a name="queryofflineinformation-method-of-the-win32_tsvm-class"></a>Queryofflineinformation-Methode der Win32- \_ Klasse "ZVM"

Ruft die Eigenschaften des aktuellen virtuellen Desktop Servers (VDS) ab, jedoch nur, wenn der Server offline ist.

## <a name="syntax"></a>Syntax


```mof
uint32 QueryOfflineInformation(
  [out] string  Build,
  [out] string  CurrentVersion,
  [out] string  InstallationType,
  [out] string  EditionId,
  [out] string  SysPrepImageState,
  [out] string  SysPrepMode,
  [out] sint32  ProcArch,
  [out] boolean fIsVmbusCapable,
  [out] boolean fIsRdvIcInstalled
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Build* \[ vorgenommen\]
</dt> <dd>

Bei erfolgreicher Ausführung wird die Buildversion der VDS zurückgegeben.

</dd> <dt>

*CurrentVersion* \[ vorgenommen\]
</dt> <dd>

Bei erfolgreicher Ausführung wird die aktuelle Version der VDS zurückgegeben.

</dd> <dt>

*Installationstyp* \[ vorgenommen\]
</dt> <dd>

Bei erfolgreicher Ausführung wird der Installationstyp der VDS zurückgegeben.

</dd> <dt>

*EditionID* \[ vorgenommen\]
</dt> <dd>

Bei erfolgreicher Ausführung wird die Editions-ID der VDS zurückgegeben.

</dd> <dt>

*Sygeopimagestate* \[ vorgenommen\]
</dt> <dd>

Bei Erfolg wird der Status des System prep-Images der VDS zurückgegeben.

</dd> <dt>

*Systreupmode* \[ vorgenommen\]
</dt> <dd>

Bei erfolgreicher Ausführung wird der System Vorbereitungsmodus der VDS zurückgegeben.

</dd> <dt>

*Procarch* \[ vorgenommen\]
</dt> <dd>

Bei erfolgreicher Ausführung wird ein Wert zurückgegeben, der die Prozessorarchitektur angibt.

<dt>

0
</dt> <dd>

x86

</dd> <dt>

1
</dt> <dd>

amd64

</dd> </dl> </dd> <dt>

*fisvmbuscapable* \[ vorgenommen\]
</dt> <dd>

gibt bei Erfolg an, ob das System VMBus-fähig ist.

</dd> <dt>

*fisrdvicinstallierte* \[ vorgenommen\]
</dt> <dd>

Bei erfolgreicher Ausführung wird angegeben, ob rdvic installiert ist.

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

 

 





